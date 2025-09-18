# 🚀 Streamlining Ticket Assignment for Efficient Support Operations  

## 📌 Project Overview  
At **ABC Corporation**, the growing number of support requests exposed the need for a **streamlined and automated ticket management system**. Manual assignment often led to **delays, misrouting, and uneven workloads** across support teams.  

This project leverages **ServiceNow** to deploy an **automated ticket assignment process**, ensuring tickets are routed to the right team without manual effort.  

---

## 🎯 Project Objectives  
- Automate ticket routing to ensure accurate and timely assignment.  
- Reduce delays in issue resolution by minimizing manual intervention.  
- Improve customer satisfaction with faster response times.  
- Optimize workload distribution across teams.  
- Enhance transparency with clear assignment logic, reporting, and monitoring.  

---

## ✨ Key Features  
- **Automated Routing** – Instantly assigns tickets to the right team/person.  
- **Dynamic Rules** – Configurable logic based on category or priority.  
- **Load Balancing** – Even distribution of workload across teams.  
- **Escalation Support** – Automatic escalation for SLA breaches.  
- **Notifications** – Real-time alerts for quicker responses.  
- **Analytics** – Detailed reports on ticket flow and team performance.  

---

## ⚙️ ServiceNow Developer Setup  
1. Create a free developer account at [ServiceNow Developer Portal](https://developer.servicenow.com/dev.do).  
2. Verify your email and log in.  
3. Request a **Personal Developer Instance (PDI)**.  
4. Use **Creator Studio/App Engine Studio** to build the application.  

<img width="968" height="478" alt="image" src="https://github.com/user-attachments/assets/54420330-ab7f-45f7-bdb6-583ec17139c2" />

---

## 🛠️ Project Implementation  
The project was implemented in ServiceNow with the following components:
### 1️⃣ Creating Users  
Users represent individuals in the system. Two users were created:  
- **Katherine Pierce** – Member of the Certificates Group.  
- **Manne Niranjan** – Member of the Platform Group.  

<img width="1437" height="601" alt="image" src="https://github.com/user-attachments/assets/810dedf1-3a3a-419d-92e1-f6afda1b8573" />

---

### 2️⃣ Creating Groups  
Groups represent teams that handle tickets:  
- **Certificates Group** – Manages certificate-related issues.  
- **Platform Group** – Handles login issues, 404 errors, and expired accounts.  

<img width="1435" height="609" alt="image" src="https://github.com/user-attachments/assets/c30db0fa-e90a-4b1d-bc1e-df222b1c11ad" />

---

### 3️⃣ Creating Roles  
Roles define permissions:  
- **Certificate_role** – Grants certificate issue handling access.  
- **Platform_role** – Grants platform issue handling access.  

<img width="1437" height="601" alt="image" src="https://github.com/user-attachments/assets/56f2114c-81e7-4ad9-bd7e-902100974cd3" />

---

### 4️⃣ Creating Table & Choices  
A custom table **Operations related** was created with fields:  
- Issue, Description, Assigned To, Status.
    
<img width="940" height="249" alt="image" src="https://github.com/user-attachments/assets/e2a1a850-8c07-41ab-93e3-543306656243" />

<img width="767" height="431" alt="image" src="https://github.com/user-attachments/assets/1c66b6c1-60d3-48c1-b2b1-ecea37f346a4" />

Choices for the **Issue** field:  
- Unable to login to platform  
- 404 error  
- Regarding certificates  
- Regarding user expired  

<img width="958" height="459" alt="image" src="https://github.com/user-attachments/assets/66ec7d4c-297d-4f37-b3b9-b37afc62a433" />

---

### 5️⃣ Assigning Users & Roles to Groups  
- **Certificates Group:** Katherine Pierce + Certificate_role
<img width="719" height="196" alt="image" src="https://github.com/user-attachments/assets/59013cea-428f-46b8-a0a9-e1a678120689" />
<img width="719" height="206" alt="image" src="https://github.com/user-attachments/assets/2b68395f-b05b-42ee-8126-7aa715554ccf" />

- **Platform Group:** Manne Niranjan + Platform_role  
<img width="719" height="205" alt="image" src="https://github.com/user-attachments/assets/729a7f28-086a-42af-9bc5-f8b5ee621cdb" />
<img width="719" height="206" alt="image" src="https://github.com/user-attachments/assets/0aaa25c2-bcdb-441e-803a-6730e6dcb8b5" />

---

### 6️⃣ Assigning Roles to Table  
Both **Certificate_role** and **Platform_role** were assigned **Read/Write access** to the *Operations related* table.  
<img width="718" height="244" alt="image" src="https://github.com/user-attachments/assets/e66c9dd1-711b-45e0-be29-5b8c8dd1c09d" />

---

### 7️⃣ Creating ACLs  
Access Control Lists (ACLs) were defined for sensitive fields (Issue, Priority, Ticket Raised Date) to restrict access to authorized roles (admin).  
<img width="1390" height="480" alt="image" src="https://github.com/user-attachments/assets/b00249dc-92c6-4561-826a-fc3ec372e4f5" />

---

### 8️⃣ Creating Flows for Ticket Assignment  
- **Flow 1:** Automatically assign *“Regarding Certificates”* tickets to the Certificates Group.  
- **Flow 2:** Automatically assign *Platform-related issues* (Login, 404 Error, User Expired) to the Platform Group.  
<img width="1918" height="843" alt="image" src="https://github.com/user-attachments/assets/656b8f1e-29fc-4afa-83ef-7aec49430f30" />

---

## ✅ Conclusion  
The **automated ticket assignment system** implemented in ServiceNow has transformed IT support operations at ABC Corporation by:  
- **Reducing delays** with automatic routing.  
- **Improving accuracy** by ensuring tickets reach the right team.  
- **Optimizing efficiency** through balanced workloads.  
- **Enhancing customer satisfaction** with faster resolution.  

This project demonstrates how **ServiceNow automation** streamlines IT Service Management (ITSM) by eliminating manual tasks and enabling teams to focus on resolving issues instead of managing ticket assignments.  

---

### 🔗 GitHub Link  
[Streamlining Ticket Assignment for Efficient Support Operations](https://github.com/Baratam-Saiprasoona/Streamlining-Ticket-Assignment-for-Efficient-Support-Operations.git)  
