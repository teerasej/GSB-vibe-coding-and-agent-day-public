# Workshop IT Readiness Checklist

**Sessions:** Power Apps vibe experience (preview) and Microsoft Copilot Studio

> **Recommended setup:** Use one IT-managed **Trial** Power Platform environment in the **Asia** region, with **Dataverse** and a participant security group. Create it at least **7 days before training**.

## 1. Environment

> สามารถกำหนด environment แยกตามผู้เรียน (1 environment ต่อผู้เรียน) หรือใช้ environment เดียวกันสำหรับผู้เรียนหลายคนก็ได้ แต่ต้องมีการจัดการสิทธิ์และการเข้าถึงอย่างเหมาะสม

- [x] **สร้าง environment ใหม่**; หลีกเลี่ยง Default หรือ Production environment ถ้าทำได้ห
- [ ] ตั้งค่า environment ใหม่ดังนี้
  - **Type: Developer**
  - **Region: United States**
  - Name: [ตามที่องค์กรกำหนด] (เช่น `GSB Vibe Coding and Agent Day`)
  - Owner: [admin]
  **- Database: Yes**
  - Environment group: None
  - Managed: No
  - Get new features early: No


## 2. Accounts, licenses, and roles

- [ ] ยืนยันว่าผู้เข้าอบรมทุกคนมีบัญชีองค์กรที่ใช้งานได้ 
- [ ] สำหรับ Power Apps ให้กำหนดสิทธิการใช้งานที่มีอยู่และเข้าเงื่อนไข หรือ **Power Apps trial 30 วัน** หรือ **Microsoft Power Apps for Developer** หรือเทียบเท่า
- [ ] สำหรับ Copilot Studio ให้กำหนดสิทธิการใช้งานให้ผู้เข้าอบรมแต่ละคน ได้ license **Copilot Studio Viral trial** หรือเทียบเท่า
- [ ] เพิ่มผู้เข้าอบรมเข้าใน Security Group ของ environment และกำหนด role **Environment Maker**
- [ ] เนื่องจากแล็บมีการสร้างตาราง Dataverse ให้กำหนด role **System Customizer** เพิ่มเติม หรือ role แบบกำหนดเองที่ได้รับอนุมัติและมีสิทธิ์ที่จำเป็นต่อการใช้งาน table ใน Dataverse
- [ ] **ยืนยันว่าผู้เข้าอบรมสามารถมองเห็นและเลือก training environment ได้ในทั้งสองผลิตภัณฑ์**
- [ ] ให้ผู้สอนและเจ้าหน้าที่ IT support ที่ระบุชื่อไว้มีสิทธิ์เพียงพอสำหรับการช่วยเหลือและกู้คืนงานในแล็บ


## 3. การเปิดใช้งาน the Power Apps vibe experience

- [ ] ใน [Power Platform admin center > Tenant Setting](https://admin.powerplatform.microsoft.com/manage/tenantsettings) ให้เปิดใช้งาน **Copilot in Power Apps (preview)** ในระดับ tenant
- [ ] ยืนยันว่า training environment อยู่ใน region ที่รองรับ และไม่ใช่ Default environment
- [ ] ยืนยันว่าผู้เข้าอบรมสามารถเปิด [Power Apps vibe](https://vibe.preview.powerapps.com/) หรือ [Power Apps preview](https://make.preview.powerapps.com/) ได้
  - ภาพตัวอย่างถ้า environment ไม่รองรับ: 
  ![Power Apps vibe experience not available](https://raw.githubusercontent.com/teerasej/GSB-vibe-coding-and-agent-day-public/main/images/environment-not-support-vibe-coding.png)
  - ภาพตัวอย่างถ้า environment รองรับ: 
  ![Power Apps vibe experience available](https://raw.githubusercontent.com/teerasej/GSB-vibe-coding-and-agent-day-public/main/images/power-app-vibe-coding.png)


## 5. Network และเครื่องที่ใช้อบรม

ทดสอบตามรายการด้านล่าง**ด้วยบัญชีผู้เข้าอบรม** และอุปกรณ์บน internal network จริง

- [ ] ใช้เบราว์เซอร์ Microsoft Edge หรือ Google Chrome เวอร์ชันล่าสุด โดยอนุญาตป๊อปอัปและคุกกี้ที่จำเป็น
- [ ] ยืนยันการเข้าถึง outbound **HTTPS และ WSS** สำหรับการลงชื่อเข้าใช้ Microsoft และบริการ Power Platform
- [ ] ทดสอบการเข้าถึงผ่าน Wi-Fi, proxy, VPN, firewall, DNS, และ SSL inspection path เดียวกับที่ผู้เข้าอบรมจะใช้
- [ ] ยืนยันว่า portal เหล่านี้เปิดโดยไม่มีข้อผิดพลาด:
  - [ ] `https://login.microsoftonline.com`
  - [ ] `https://vibe.preview.powerapps.com`
  - [ ] `https://make.preview.powerapps.com`
  - [ ] `https://copilotstudio.microsoft.com`

## 6. การเข้าถึง exercise

ทดสอบตามรายการด้านล่าง**ด้วยบัญชีผู้เข้าอบรม** และอุปกรณ์บน internal network จริง

- [ ] ยืนยันว่านโยบายขององค์กรอนุญาตให้ผู้เข้าอบรมเข้าถึง public GitHub repository [ผ่าน link ที่กำหนดให้ในเอกสารนี้](https://github.com/teerasej/GSB-vibe-coding-and-agent-day-public/) 
- [ ] อนุญาต outbound HTTPS สำหรับ `github.com`, `raw.githubusercontent.com`, และ `codeload.github.com`
- [ ] เปิด [public workshop repository](https://github.com/teerasej/GSB-vibe-coding-and-agent-day-public)
- [ ] ดาวน์โหลด [repository ZIP](https://github.com/teerasej/GSB-vibe-coding-and-agent-day-public/archive/refs/heads/main.zip)

- [ ] ยืนยันว่าเบราว์เซอร์หรือการดาวน์โหลดไม่ถูกบล็อกโดย DNS, proxy, firewall, SSL inspection, content filtering, หรือ endpoint security policy

> **Reference:** [GitHub connectivity troubleshooting](https://docs.github.com/en/get-started/using-github/troubleshooting-connectivity-problems)


## Microsoft references

- [Power Apps vibe experience prerequisites](https://learn.microsoft.com/power-apps/vibe/overview#prerequisites)
- [Permissions to create and edit Dataverse tables](https://learn.microsoft.com/power-apps/maker/data-platform/create-edit-entities-portal#prerequisites)
- [Power Platform trial environments](https://learn.microsoft.com/power-platform/admin/trial-environments)
- [Copilot Studio trial access and limitations](https://learn.microsoft.com/microsoft-copilot-studio/requirements-licensing-subscriptions#sign-up-for-a-copilot-studio-trial)
- [Secure Copilot Studio projects](https://learn.microsoft.com/microsoft-copilot-studio/guidance/sec-gov-phase3)
- [Power Platform data policies](https://learn.microsoft.com/power-platform/admin/wp-data-loss-prevention)
- [Power Apps required network services](https://learn.microsoft.com/power-apps/limits-and-config#required-services)
