# Leave-Management-System

# 📝 Leave Management System using PowerApps

A modern low-code application built using **Microsoft PowerApps** to streamline the employee leave request and approval process. This system enhances productivity by automating tasks, enabling efficient communication between employees, managers, and HR.

---

## 📌 Table of Contents

- [Features](#-features)
- [Technologies Used](#-technologies-used)
- [How It Works](#-how-it-works)
- [Power Automate Workflow](#-power-automate-workflow)
- [SharePoint List Schema](#-sharepoint-list-schema)
- [Screenshots](#-screenshots)
- [Future Enhancements](#-future-enhancements)
- [Author](#-author)
- [Disclaimer](#-disclaimer)

---

## ✅ Features

- 👤 **Employee Portal** – Apply for leave with type, date range, and reason.
- 🧑‍💼 **Manager View** – Approve or reject requests with comments.
- 🛠️ **Admin Dashboard** – Track leave balances and employee records.
- 🔄 **Real-Time Status** – Application status updates and history logs.
- 🔐 **Role-Based Access** – Permissions based on logged-in user roles.
- 📧 **Email Notifications** – Auto-triggered via Power Automate.
- 📅 **Calendar Integration** – Visualize team leaves on a calendar.
- 📊 **Report View** – Export leave data for HR analysis.

---

## 🧰 Technologies Used

| Tool/Platform        | Purpose                               |
|----------------------|----------------------------------------|
| PowerApps            | Frontend UI and logic                  |
| SharePoint List      | Backend data storage                   |
| Power Automate       | Automation of workflows & notifications |
| Microsoft 365        | User login and access management       |

---

## ⚙️ How It Works

1. **User Login**: Authenticated using Microsoft 365 login.
2. **Leave Request**:
   - Employee submits a leave request.
   - Manager receives a notification to approve/reject.
3. **Approval Workflow**:
   - Manager updates the status via PowerApps.
   - Email notification is sent to the employee via Power Automate.
4. **Tracking**:
   - All requests are logged and tracked in SharePoint.
   - Admin can view/download reports.

---

## 🔄 Power Automate Workflow

Power Automate is used to:

- ✅ Send email when a new leave request is submitted.
- 🔁 Notify the manager for approval.
- 📬 Inform the employee once leave is approved/rejected.

### Sample Flow Logic

1. **Trigger**: When a new item is created in SharePoint list.
2. **Condition**: Check if `Status = Pending`.
3. **Action**:
   - Send approval email to manager.
   - On approval/rejection, send status update to employee.

---

## 🗂️ SharePoint List Schema

| Column Name     | Type          | Description                        |
|------------------|---------------|------------------------------------|
| Title            | Text          | Leave Request Title (Auto/Manual)  |
| EmployeeName     | Person/Group  | Employee submitting the request    |
| LeaveType        | Choice        | Sick Leave / Casual / Earned       |
| StartDate        | DateTime      | Start date of leave                |
| EndDate          | DateTime      | End date of leave                  |
| Reason           | Multiple lines of text | Reason for leave          |
| Status           | Choice        | Pending / Approved / Rejected      |
| ManagerComment   | Single line of text | Manager's remarks            |
| SubmittedDate    | DateTime      | Auto-captured on submission        |

---


### 📝 Leave Application Form
![Leave Form](assets/leave-form.png)

### 📬 Manager Approval Screen
![Manager View](assets/manager-approval.png)

### 📊 Admin Dashboard with Status Tracking
![Admin Dashboard](assets/admin-dashboard.png)

---

## 🔮 Future Enhancements

- 📲 Mobile responsiveness with adaptive layout.
- 🧮 Automated leave balance calculator.
- 🔐 Multi-level approval chain.
- 📥 PDF export for leave history and monthly summaries.
- 📊 Power BI Integration for HR insights.

---

## 👨‍💻 Author

**Uday Kumar Botlagunta**  
🎓 B.Tech CSE | 💻 Developer  
📧 [23kq5a0501cse@gmail.com](mailto:23kq5a0501cse@gmail.com)  
🔗 [GitHub](https://github.com/uday0103) | [LinkedIn](https://www.linkedin.com/in/uday-kumar-0b5564348/)

---

## ⚠️ Disclaimer

This project is intended for **educational purposes only**. Please review and comply with your organization's IT and data governance policies before deployment in a production environment.

---

## 📂 Repository Structure (Optional)

```bash
Leave-Management-System/
├── README.md
├── assets/
│   ├── leave-form.png
│   ├── manager-approval.png
│   └── admin-dashboard.png
├── LeaveManagementApp.msapp
└── FlowExport.zip (Power Automate Export)
