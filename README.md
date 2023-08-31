# ln_chatbot
# Part 1 Setup

## การรัน project 
1. ไปที่ Firebase Console (https://console.firebase.google.com) แล้วกดสร้าง project ใหม่ ![image](https://github.com/NNLoat/ln_chatbot/assets/83104226/7838defd-d6b0-4b9e-afe9-379504a2db11)
2. ทำการติดตั้ง Node.js ให้เรียบร้อย
3. ติดตั้ง Firebase CLI ด้วยคำสั่ง ```npm install -g firebase-tools``` และ login ที่ firebase account ด้วย ```firebase login```
4. จากนั้นใช้คำสั่ง ```firebase init functions``` เลือก existing function แล้วเลือกฟังก์ชั่นที่พึ่งสร้างใน ข้อที่ 1,  เลือก Javascript, แล้วกดข้าม ES Lint, กด ```Y``` ตอน Install dependencies![image](https://github.com/NNLoat/ln_chatbot/assets/83104226/3c247f89-8c85-412e-8300-c38dcedddf8f)![image](https://github.com/NNLoat/ln_chatbot/assets/83104226/ffcaa9a5-41a8-48f3-9aea-066cc24781ea)![image](https://github.com/NNLoat/ln_chatbot/assets/83104226/cdbf24ba-8150-4958-856d-b0d241a8f16f)![image](https://github.com/NNLoat/ln_chatbot/assets/83104226/33df0954-5b80-4fca-9691-6535dc15302b)![image](https://github.com/NNLoat/ln_chatbot/assets/83104226/87c1f0e3-1812-44d8-9196-3d8d48da2be5)![image](https://github.com/NNLoat/ln_chatbot/assets/83104226/7f771402-c1b7-4704-ba73-38352b565a2c)
5. หากมีข้อสงสัยเพิ่มเติมสามารถ ดูวิธีการทำตั้งแต่ข้อ 1 ถึง 4 ได้ที่เว็บ (https://www.mikkipastel.com/how-to-do-line-chatbot-for-newly-developer-with-out-dialogflow/)
6. จากนั้น กด Extract zip ไฟล์ project ไปที่ root folder ของโปรเจคที่สร้างในข้อ 4 เลือก overwrite ถ้าเกิด prompt จาก system
7. ติดตั้ง dependencies โดย ```npm install```
8. double click ที่ ไฟล์ running.bat จะมีสองหน้าต่างขึ้นมา firebase console และ ngrok
   <br>หน้าต่าง ngrok
   ![image](https://github.com/NNLoat/ln_chatbot/assets/83104226/4115bebd-0c98-4ff9-a52d-c8b2fd8dc6c2)
   หน้าต่าง Firebase console
   ![image](https://github.com/NNLoat/ln_chatbot/assets/83104226/f06e3fae-11be-4167-9713-6f4f211387cb)
9. ให้ทำการ copy URL ของ ngrok แล้วตามด้วย ```/${ชื่อ project ที่สร้างใน firebase}/asia-southeast1/app/editURL``` เช่นในตัวอย่างหน้าตา ngrok![image](https://github.com/NNLoat/ln_chatbot/assets/83104226/015e3f30-89e5-4929-b31e-c2676899b2d1) <br>link ที่ต้องใช้ก็คือ ```https://1e4e-1-46-80-75.ngrok-free.app/test-bot-9e216/asia-southeast1/app/editURL``` นำ link นี้ไปใส่ที่ browser 
10.  เมื่อเข้าไปได้จะเจอกับหน้าเว็บ สำหรับ edit cloud function<br>![image](https://github.com/NNLoat/ln_chatbot/assets/83104226/2c8b4087-a647-4669-bb0d-d12c42aab4f6)
<br> แล้ว paste URL ของ ngrok ในช่อง "แก้ Public URL ของ server" จากนั้นคลิก Save
![image](https://github.com/NNLoat/ln_chatbot/assets/83104226/5f74d63d-c94b-4ae2-a224-2df5b2a5b77b) <br>
11.  copy channel token (long live access) จาก Line OA (developer.line.biz) มาวางในช่อง "แก้ line message token" แล้วกด save <br> line message token: ![image](https://github.com/NNLoat/ln_chatbot/assets/83104226/c8659a07-e31d-48a1-8e8f-3e874748d8d9) <br> ![image](https://github.com/NNLoat/ln_chatbot/assets/83104226/74ac362f-1cee-4492-abd0-1ce6f27fe662) 
12.  เข้า ไปที่เว็บ Line developer console --> settings --> message API --> Webhook URL แล้ว นำ link จาก ngrok ที่ตามด้วย ```/test-bot-9e216/asia-southeast1/lineBot``` ในตัวอย่างก็คือ ```https://1e4e-1-46-80-75.ngrok-free.app/test-bot-9e216/asia-southeast1/lineBot``` <br> ![image](https://github.com/NNLoat/ln_chatbot/assets/83104226/82272333-8de7-4277-bf8d-7bb1089854bc) จากนั้นกด update
13.  เป็นอันเสร็จสิ้น การ set up line chatbot ครั้งแรก

# การเปลี่ยนรอบคำถามที่ต้องเปลี่ยนทุกปี
หากผู้ใช้ต้องการเปลี่ยนคำตอบสำหรับชุดคำถามที่ต้องเปลี่ยนทุกปี สามารถทำได้โดยเข้าไปที่เว็บไซต์ ```${public URL}/${ชื่อ project ที่สร้างใน firebase}/asia-southeast1/app/edit```(ในตัวอย่างก็ ```https://1e4e-1-46-80-75.ngrok-free.app/test-bot-9e216/asia-southeast1/app/edit```)ซึ่งจะโชว์หน้าเว็บตามรูปภาพด้านล่าง ![image](https://github.com/NNLoat/ln_chatbot/assets/83104226/429ad222-923c-4cc8-94a5-f5d4381b465b) <br> หากต้องการที่จะแก้ไขชุดคำตอบ ให้แก้ไขข้อความใน textbox แล้ว กดปุ่ม "Save"![image](https://github.com/NNLoat/ln_chatbot/assets/83104226/978736cd-c0d3-496e-a06f-0168aafe68a2)

# การเปลี่ยนรอบคำถามตามเวลา (time-based response)
หากผู้ใช้ต้องการจะเปลี่ยนคำตอบสำหรับชุดคำถามที่ตอบตามเวลาที่ถูกถาม สามารถทำได้โดยเข้าไปที่เว็บไซต์ ```${public URL}/${ชื่อ project ที่สร้างใน firebase}/asia-southeast1/app/edit```(ในตัวอย่างก็ ```https://1e4e-1-46-80-75.ngrok-free.app/test-bot-9e216/asia-southeast1/app/edit```) เลื่อนหน้าเว็บให้ลงมาถึงด้านล่าง จะเจอกับหัวข้อ ```ลิสต์คำตอบ link สมัครสอบของ ICT แต่ละรอบ ใส่วันที่แบบ (YYYY-MM-DD+'Z')``` ![image](https://github.com/NNLoat/ln_chatbot/assets/83104226/52b4831f-b36e-4b75-93e9-79d191aff27c) เทมเพลตของ ชุดคำตอบจะเป็น ```ชื่อรอบ,คำตอบของรอบนั้นๆ,วันที่เริ่มปล่อยคำตอบรอบนี้,วันที่สิ้นสุดคำตอบรอบนี้```![image](https://github.com/NNLoat/ln_chatbot/assets/83104226/16894cfd-dd21-44f9-8932-153735787f70)



