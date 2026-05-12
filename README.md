# CADCAM_ADXL345

Print-in-place hinge assembly สำหรับยึด ADXL345 accelerometer ออกแบบให้พิมพ์ออกมาจากเครื่องเป็นชิ้นเดียวพร้อมใช้งานทันที โดยอาศัยกระบวนการ SLS (Selective Laser Sintering)

![Hinge assembly preview](Screenshot%202569-05-12%20at%2016.38.39.png)

## Concept

Hinge นี้ทำงานโดยใช้หลัก **interlocking knuckle geometry**

- ชิ้น **Base** มี knuckle สองตัวอยู่ด้านนอก
- ชิ้น **Lid** มี knuckle หนึ่งตัวสอดอยู่ตรงกลาง
- ทั้งสามตัวร้อยรวมกันด้วย **pin เดียว** ที่วิ่งผ่านตลอด

เนื่องจาก pin ถูก Base โอบล้อมทั้งสองด้าน จึงมีเพียง Lid เท่านั้นที่หมุนได้รอบ pin ส่วน Base และ pin อยู่นิ่ง

## Why SLS

สิ่งที่ทำให้ design นี้พิมพ์ได้เป็นชิ้นเดียวคือการออกแบบ **clearance gap** ระหว่าง knuckle ให้พอดีกับกระบวนการ SLS

- ผง Nylon ที่อยู่รอบชิ้นงานทำหน้าที่เป็น support ตามธรรมชาติ
- gap ที่ออกแบบไว้จะเต็มไปด้วยผงหลวมๆ หลังพิมพ์เสร็จ
- ทำ depowdering → ผงร่วงออก → hinge พร้อมใช้งานทันทีโดยไม่ต้องประกอบเพิ่ม

ข้อได้เปรียบเหนือ FDM: FDM ต้องการ gap ที่กว้างกว่ามากเพราะ layer bonding ทำให้ผนังบวมและติดกันง่าย

## Design for Assembly (DFA)

แม้ hinge จะประกอบด้วยสามส่วนที่เคลื่อนไหวต่อกัน แต่ผู้ใช้ได้รับชิ้นงานที่ functional ออกมาจาก printer โดยตรง — ไม่มีขั้นตอนประกอบ

## Files

| File | Description |
|------|-------------|
| [ADXL345.f3z](ADXL345.f3z) | Fusion 360 archive ของชิ้นงาน |
| [Screenshot 2569-05-12 at 16.38.39.png](Screenshot%202569-05-12%20at%2016.38.39.png) | Render preview |
| [brief.md](brief.md) | คำอธิบาย design rationale แบบเต็ม |
