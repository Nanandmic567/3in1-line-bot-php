# Multifunction LINE Bot Webhook
ระบบแชทบอตที่ผสานการทำงานของ LINE Messaging API, Abdul Platform และ Dialogflow ไว้ใน Webhook ตัวเดียว...

<p> ขอขอบคุณแนวคิดต้นฉบับโดยอาจารย์กิตติ มดคำรามด้วยนะครับ (เข้าไปดูได้ครับผม เนื้อหาเยอะมาก) <br> https://medium.com/@modcumram/%E0%B8%81%E0%B8%B2%E0%B8%A3%E0%B8%9E%E0%B8%B1%E0%B8%92%E0%B8%99%E0%B8%B2%E0%B9%84%E0%B8%A5%E0%B8%99%E0%B9%8C%E0%B9%81%E0%B8%8A%E0%B8%95%E0%B8%9A%E0%B8%AD%E0%B8%95-line-message-api-abdul-dialogflow-mad-fcf570fdf954

ส่วน Source code ได้มาจากที่นี่ฮะ... (หรือดูจากที่ผม fork มาก็ได้ครับ) <br>
https://medium.com/@itchampclub/php-linebot-x-dialogflow-x-webhook-%E0%B8%97%E0%B8%B5%E0%B9%88%E0%B8%A3%E0%B8%B1%E0%B8%9A%E0%B8%AA%E0%B9%88%E0%B8%87-message-objects-%E0%B9%84%E0%B8%94%E0%B9%89%E0%B8%97%E0%B8%B8%E0%B8%81-type-c35490b5e9e0

<h2>Requirement (สิ่งที่ต้องมี)</h2>

- LINE Dev Account (ใช้บัญชี Line ของเราได้เลย)

- Dialogflow (ใช้ Google Account ของเรา)

- Abdul Platform (ล็อกอินด้วย Facebook)

- Heroku (หรือเครื่อง Server ทั่วไปก็ได้)

- OpenWeatherMap API (สำหรับสภาพอากาศ)

- โปรแกรม Git หรือ Google Cloud Shell

<b>(อย่าลืมว่าเราต้องมี Channel Access Token กับ Channel Secret ของ LINE ด้วยนะ สำคัญมาก)</b>

## วิธีทำ

1. Clone Repo นี้ด้วยคำสั่ง <tt>git clone</tt><br>
2. ปรับแก้โค้ดในไฟล์ bot.php ให้เป็นของเรา

<tt>$channelAccessToken = ‘line-channelAccessToken’;</tt>

<tt>$channelSecret = ‘line-channelSecret’;</tt>

<tt>$picurl = ‘https://your-app-name.herokuapp.com' . $fileFullSavePath;</tt> <-- ตรงนี้รวมถึง $vidurl และ $audurl ด้วย

<tt>$url = “https://bots.dialogflow.com/line/your-app-name/webhook";</tt> <-- Abdul ก็ต้องเปลี่ยนด้วยนะ

<tt>$uri = "https://api.openweathermap.org/data/2.5/weather?lat=" . $msg_latitude . "&lon=" . $msg_longitude . "&lang=th&units=metric&appid=YOUR_OPENWEATHERMAP_ID_HERE";</tt> <-- OWM API

(รายละเอียดทั้งหมด เร็วๆนี้ครับ)
