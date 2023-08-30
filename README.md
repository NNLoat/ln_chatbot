# ln_chatbot

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

   

10. 
