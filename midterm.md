> basically just everything put all together 🤷🏻‍♂️

## Week 2 Lecture

### Why do we need Software Testing?
- เพราะว่าเราต้องการ software ที่มี quality to deliver to the customer
	- **Functional Testing**
		- quality according to the requirement of the customer <- requirement
		- software works as expected (not including in the requirement) <- system
	 - **Non-Functional Testing**
		- -ity eg. Availability, Integratbility, ...

### Qualitied Software
- Reliability : ความน่าเชื่อถือ
- Efficiency : ประสิทธิภาพ (การใช้ทรัพยากรคุ้มค่า)
- Maintainability : ความสามารในการดูแลรักษา
- Compatibility : ความสามารถเข้ากันได้กับสิ่งอื่นหรือเวอร์ชั่นอื่น
- Usability : สามารถใช้ได้ง่ายเข้าใจได้ง่าย
- Performance : ความสามารถในการตอบสนองผู้ใช้ (เร็ว, เยอะ)

### Bug (Terms)
- **Defect**: ปัญหาที่พบในการทดสอบระบบ
- **Error**: กิจกรรมที่ทำให้เกิดผลลัพธ์ที่ผิด
- **Bug**: สิ่งที่ทำให้เกิดขึ้นของ error ขณะซอฟต์แวร์ที่ทำงาน
- **Fault**: สถานะของซอฟต์แวร์ที่เกิด error ขึ้น
- **Failure**: ความผิดพลาดจากการทำงานของซอฟต์แวร์
- "A person makes an **error** that creates a **fault** in the software that can cause a **failure** in operation."

### Defect Types
- **Requirement**
	- from changing the business requirement without noticing the team that are responsible
- **Coding**
	- from coding that is un-tested from the Developer
- **Graphic Design** 
	- from in-compatible design with the browser or when the Dev put the design to code and the outcome is wrong
- **Data Test**
	- from the test data ไม่มีใน environment หรือระบบอาจะไม่รองรับ data
- **Other**
	- system limitation, etc.

### Defect Severity
> probably in the exams
- **Critical** ☢️ 
	- defect ที่ไม่สามารถทดสอบโปรแกรมในส่วนของ function ต่อได้เลย
	- Show-stopper
 - **High** 🔥
	- defect ที่เกิดจากการใส่ข้อมูลที่ถูก้อง แต่ระบบแสดงผลผิด eg. error
	- still has a work-around
- **Medium** 😰
	- ระบบจะแสดงผลถูกต้องเมื่อใส่ข้อมูลถูกต้อง แต่เมื่อใส่ข้อมูลไม่ถูกต้อง ระบบจะแสดงผลผิดพลาด เช่น Field ที่มีการ validate ผล เมื่อใส่ค่าว่าง, อักขระพิเศษ และ script ที่มีผลต่อการแสดงผลของระบบๆ จะแสดงผลผิดพลาด
- **Low** 😎
	- defect ที่เกิดจากการแสดงผลข้อความ หรือเรื่องของการ design ซึ่ง defect เหล่านี้จะไม่มีผลกระทบกับการทำงานของระบบ

### Software Testing
- คือการทดสอบความสมบูรณ์ของโปรแกรม รวมทั้งความน่าเชื่อถือและความถูกต้องของผลลัพธ์จากโปรแกรมที่พัฒนาขึ้น
- ตรวจสอบประสิทธิภาพการทำงาน และเป็นผลสัมพันธ์กับคุณภาพของซอฟต์แวร์ด้วย
- จัดทำขึ้นเพื่อประเมินและปรับปรุงคุณภาพของซอฟต์แวร์
- ส่วนใหญ่ทำโดย Testers แต่ก็สามารถทำได้โดย Developers
- นิสัยที่ดีของ software tester : ช่างจินตนาการ, ช่างสงสัย
- มีแบบแผนการปฏิบัติ

### Testing Process
![](https://media.discordapp.net/attachments/1014398974649708624/1064743879385030819/image.png) 

### Black Box Testing
![](https://media.discordapp.net/attachments/1014398974649708624/1064747194961379328/image.png)

### White Box Testing
![](https://media.discordapp.net/attachments/1014398974649708624/1064750868496392292/image.png?width=1264&height=685)

### Software Testing
![](https://media.discordapp.net/attachments/1014398974649708624/1064751107198435460/image.png)

### Unit Test
- เป็น White Box Testing

![](https://media.discordapp.net/attachments/1014398974649708624/1064751289667440670/image.png?width=1219&height=685)

### Integration Test
- เพื่อให้เห็นว่าระบบย่อยทั้งหมดทำงานร่วมกันได้
- ทดสอบการทำงานของ classes, modules, หรือ subsystems ต่างๆ
- ถ้ามี API หรือ Database ก็ต้องทดสอบร่วมด้วย

### System Test
- ทดสอบการเชื่อมต่อระหว่างระบบของซอฟต์แวร์ที่พัฒนาขึ้น
- เช่น ทดสอบการโอนเงิน กับระบบธนาคาร, กับระบบบัญชีผู้ใช้
	- alpha testing : จำลองการทำงานระบบให้เหมือนจริงในฝั่ง dev
	- beta testing (pilot testing) : ทดสอบกับระบบจริงๆ ด้วย real environment ก่อนส่งมอบ

### Acceptance Test
- ทดสอบระบบจาก Requirement หรือ User Story ของลูกค้า
- ระบบต้องใช้งานได้จริงและสมบูรณ์ตาม Business Logic ที่ต้องลงไว้
- ลูกค้า, คนที่ให้ requirement มีส่วนร่วมในการเขียน test cast และทดสอบ
- ทดสอบทุก Roles ของ user
- Environment (HW, SW, Infra) ต้องเหมือนจริงมากที่สุด
- eg. ผู้ดูแลระบบสามารถนำข้อมูลสินค้าเข้าในระบบ และเมื่อนำสินค้าเข้าสู่ระบบแล้ว ผู้ใช้จะสามารถเห็นข้อมูลของสินค้านั้นได้ และสามารถค้นหาได้

### Performance Testing
- **Load testing**: ทดสอบซอฟต์แวร์ ระบบจะมีความเร็วมากน้อยแค่ไหน ภายใต้สภาวะและขนาดภาระที่คาดว่าจะเกิดขึ้นจริง เช่น หากมีผู้ใช้งานเข้ามาใช้ระบบพร้อมกัน 100 คน ระบบจะตอบสนองเร็วหรือช้าแค่ไหน (concurrent user)
- **Stress testing**: การทดสอบระบบที่นอกเหนือจากการทำงานปกติ เพื่อทดสอบความเสถียร ในความพร้อมและการจัดการข้อผิดพลาด เมื่อระบบมีการทำงาน
- **Spike testing**: การทดสอบระบบเมื่อมีการเพิ่มจำนวนผู้ใช้งานอย่างรวดเร็ว
- **Soak testing / Endurance testing**: ทดสอบว่าระบบยังทำงานได้ดีหรือไม่ เมื่อมีการใช้เวลานาน throughput and/or response time ยังดีเหมือนกับตอนเริ่มต้นหรือไม่
- **Capacity testing**: การทดสอบเพื่อหาว่า จะมีผู้ใช้งานกี่คนที่ระบบรองรับได้
- **Recovery testing**: การทดสอบระบบว่าระบบสามารถฟื้นตัวจากการล่มได้เร็วหรือดีแค่ไหน
- **Smoke testing**: การเริ่มต้นทดสอบระบบในการทดสอบประสิทธิภาพ เพื่อดูว่าระบบทำงานได้ปกติในสภาวะปกติ
- **Volume testing**: การทดสอบโดยการใช้จำนวนข้อมูล เพื่อแสดงให้เห็นว่า จำนวนข้อมูลเท่าไหร่ที่ระบบไม่สามารถรองรับได้
- **Network Sensitivity testing**: ทดสอบขีดจำกัดของ WAN และการทำงานของ network
- **Scalability testing**: ทดสอบเพื่อวัดความสามารถในการประยุกต์ใช้เมื่อนำไปใช้กับระบบที่ใหญ่ขึ้น

#### Load Test Report
![](https://media.discordapp.net/attachments/1014398974649708624/1064758138374463538/image.png?width=1166&height=685)

### Test-Driven Development
![](https://media.discordapp.net/attachments/1014398974649708624/1064758352225259590/image.png?width=1256&height=685)

### Testing Document
![](https://media.discordapp.net/attachments/1014398974649708624/1083027020046413875/image.png)
#### Test case Description
- test items
- input specifications
- output specifications
- environmental needs
- special procedural requirements/rules
- intercase dependencies

#### Defect Log
- **Description**
	- test item id
	- test environment description
- **Activity and event entries**
	- date and time
	- author
	- test procedure
	- staff
	- pass/fail
	- error msg generated
	- environment info
	- anomalous events

#### Defect Tracking
![](https://media.discordapp.net/attachments/1014398974649708624/1064761654853783673/image.png?width=1198&height=685)

#### Defect Status Flow
![](https://media.discordapp.net/attachments/1014398974649708624/1064761802900111431/image.png?width=1058&height=685)

### Summary
- **Test Techniques**
	- Black box testing
	- White box testing
- **Test Types**
	- unit testing
	- integration testing
	- system testing
	- acceptance testing
	- performance testing
	- test-first development

## Week 3 Lecture

## Software Quality Assurance
- ทดสอบและหาจุดบกพร่อง

#### QA (Quality Assurance)
- ตรวจสอบ find bug, defect or issue 

#### Tester
- เน้นที่การป้องกันการเกิด bug, defect or issue and find the best strategy to test the system

![](https://media.discordapp.net/attachments/1014398974649708624/1067266777156964372/image.png)

### Software Crisis
- เมื่อมีความต้องการอยากได้ software มากๆ แต่ไม่สนใจ quality ของ software ทำให้เกิด Quality Assurance

![](https://media.discordapp.net/attachments/1014398974649708624/1067268750769934336/1b8YM5srFHh705lpqvVgG3A.png)
- Unit Tests: เทสในฟังก์ชั่นของตัวเอง -> faster (least expensive)
- Integration Tests: นำหลายอย่างมาเทสการใช้ร่วมกัน
- UI Test: will based on the first two test

### QA is important as same as Developer
- system crash
- rate limit
- micro-service
- integration problems

#### Role Of Testers
- manual tester
- automation tester
- penetration tester

## Basic Software Testing's Slide

### what is software testing?
- is a process of *verifying* and *validation* that a software application or program
	- meets the business and techinal requirements that guided its design and development and
	- works as expected
- software testing also identifies important **defects, flaws, or erros** in the application code that must be **fixed**

### what do we test?
- **core functionality, common usage situations**
- testing provides **an opportunity to validate and verify things like the assumptions** that went into the requirements

### who's involved in testing?
- requirement analyts - inpections, peer reviews
- developers - code inspection, unit testing
- testers - system & integration testing
- trainers - training materials production
- users - user acceptance testing
- project manager - scheduling, resourcing, risks, issues, defect status
- "everybody is responsible for quality" - NASA

### testing principles
- all tests should be **traceable to customer** requirements
- tests should be **planed long before** testing begins
- testing should being "in the small" and progress toward testing "in the large"
- exhaustive testing is not possible

### types of testing
- unit testing
- integration testing
- functional and system testing
- acceptance testing
- regression testing
- beta testing

### summary
![](https://media.discordapp.net/attachments/1014398974649708624/1083031358642868254/image.png?width=1287&height=702)

### black box testing
- methodologies
	- boundary testing
	- equivalence classes
	- decision tables
	- state transitional diagrams

### still more whole bunch of shit that taught in software development process