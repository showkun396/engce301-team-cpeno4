# User Stories – ENGCE301 Lab Submission Portal

> หมายเหตุ:
> - ใช้สำหรับสร้าง Use Case Diagram / Use Case Scenario
> - ใช้เป็น base ในการออกแบบหน้า HTML/CSS (Week 3 LAB)

---

## กลุ่ม Student

### US-01 – View Event List
**As a** student  
**I want** Record of university activity participation data. 
**So that** I can see what activities I have already participated in.

**Acceptance Criteria (Checklist)**  
- [ ] เมื่อฉันเปิดหน้าหลักของระบบ จะเห็นรายการ History Event  
- [ ] ตารางแต่ละตารางจะบอกชื่อกิจกรรม และรายชั่วโมงที่ได้รับ 
- [ ] ท้ายตารางจะบอกชั่วโมงทั้งหมดที่ฉันมี

*(ใน LAB HTML, ส่วนนี้ map → Section “Upcoming Labs”)*

---

### US-02 – View index
**As a** student  
**I want** Want to know the number of activity hours, dating competition.  
**So that** I know of upcoming events.

**Acceptance Criteria (ตัวอย่าง Given–When–Then)**  
- **Given** ฉันอยู่ในหน้า index   
- **When** ฉันเห็น Event ทั้งหมดที่ถูกเสนอและ Event ที่อนุมัติ  
- **Then** ระบบแสดงหน้า Event ที่มี
  - ชื่อ Event, รายละเอียด, ชั่วโมงที่ได้รับ

*(ใน LAB HTML ระยะนี้ อาจใช้เป็น link หรือ section แสดงรายละเอียดแบบย่อ)*

---

### US-03 – Submit Event Access
**As a** student    
**I want** Log in Log in via your university account (SSO) to get started quickly and easily. 
**So that** I can log in quickly and safely to use.

**Acceptance Criteria (ย่อ)**  
- ก่อนใช้งานระบบต่องสมัครล็อคอินด้วยเมลมอ
- เมื่อเข้าได้สำเร็จระบบจะสำipเครื่องและประวัติต่างๆ
- สามารถเช็คการกระทำของแต่ละไอดีได้

*(ในวิชานี้อาจใช้เป็น mock UI เฉย ๆ ใน HTML/CSS – ยังไม่ต้องทำ backend)*

---

### US-04 – View My Event Status
**As a** student 
**I want** I want to see all the activities and hours I have participated in.
**So that** I can view my activity participation history.

**Acceptance Criteria**  
- หน้า “History” แสดงรายการเข้าร่วมกิจกรรม ทั้งหมด
- ท้ายตารางจะแสดงชั่วโมงการเข้าร่วมของแต่ละไอดี
*(ใน LAB HTML, ใช้ตารางหรือ card แสดงสถานะ → my-labs.html)*

---

### US-05 – Track activities
**As a** secretary 
**I want** I would like to access the Admin Dashboard to view overall statistics for the entire university.  
**So that** I can contact the president to see what educational activities he can participate in.

**Acceptance Criteria**  
- สามารถติดต่อประธานหรือแอดมินเพื่อดูประวัติกิจกรรมที่จัดขึ้นได้

---

## กลุ่ม Instructor / TA

### US-06 – Create New Event
**As a** university officials  
**I want** Learning creative and things and the number of students participating in the activities.  
**So that** I can organize activities for students to learn and create different things.

**Acceptance Criteria (ย่อ)**  
- มีปุ่ม Access Event ให้เสนอยื่นกรอกแบบฟอร์ม 
- เมื่อส่งสำเร็จ ระบบยืนยันว่ารับไฟล์แล้ว และบันทึกเวลาส่ง  
- รออาจารย์หรือประธานมากดอนุมัติกิจกรรมที่ยื่น  

*(ใน HTML prototype อาจเป็นเพียง section อธิบาย “Instructor View” หรือ mock form)*

### US-07 – Grade a Submission
**As a** niversity officials 
**I want** I want students to participate in monthly activities to clearly track their progress.
**So that** I know the activities being held and the hours being given.

**Acceptance Criteria**  
- หน้า “index” แสดงรายการ กิจกรรม ทั้งหมด
- แต่ละ กิจกรรม มีสถานะอย่างน้อย:  
  - “Not pass”, “pass” 
- ถ้ามีการอนุมัติแล้ว จะแสดงสถานนะ และ Feedback สั้น ๆ 

*(ใน HTML/CSS LAB อาจทำเป็น mock table/section หรือ modal แสดงตัวอย่างเท่านั้น)*

---

## 3) วิธีใช้ชุด SRS + User Stories นี้ใน LAB

1. **ทำ Use Case Diagram**  
   - จาก FR และ User Stories ด้านบน ให้ นศ. ระบุ Use Cases เช่น  
     - UC-01 View Event List  
     - UC-02 View index  
     - UC-03 Submit Event Access
     - UC-04 View My Event Status  
     - UC-05 Track activities  
     - UC-06 Create New Event  
   - วาด diagram (Student, Instructor, TA + System Boundary)

2. **เขียน Use Case Scenario** (อย่างน้อย 2–3 ตัว)  
   - แนะนำ:  
     - UC-01 View Event List (Student)  
     - UC-02 View index (Student)  
     - UC-04 View My Event Status (student)

     - UC-03 Submit Event Access (student)
     - UC-06 Create New Event (university officials)

3. **เชื่อมกับ LAB HTML/CSS (Week 3)**  
   - แปลง User Stories ที่เกี่ยวกับ Student เป็นหน้าเว็บ เช่น:
     - US-01 + US-02 + UC-04 → Section “Upcoming Event” และสถานะ Event บน `index.html`

     - US-03 + US-06 → หน้าเว็ปหลังจากกด ปุ่ม Access Event เพื่อเสนอยื่นกิจกรรมที่ตนเองอยากให้จัดขึ้น
     
   - ใช้ NFR (Usability / Layout) เป็น guideline ในการออกแบบ HTML/CSS