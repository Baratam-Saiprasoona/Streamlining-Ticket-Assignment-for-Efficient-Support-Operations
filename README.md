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

### 1️⃣ Creating Users  
Users represent individuals in the system. Two users were created:  
- **Katherine Pierce** – Member of the Certificates Group.  
- **Manne Niranjan** – Member of the Platform Group.  


---

### 2️⃣ Creating Groups  
Groups represent teams that handle tickets:  
- **Certificates Group** – Manages certificate-related issues.  
- **Platform Group** – Handles login issues, 404 errors, and expired accounts.  


---

### 3️⃣ Creating Roles  
Roles define permissions:  
- **Certificate_role** – Grants certificate issue handling access.  
- **Platform_role** – Grants platform issue handling access.  

---

### 4️⃣ Creating Table & Choices  
A custom table **Operations related** was created with fields:  
- Issue, Description, Assigned To, Status.  

Choices for the **Issue** field:  
- Unable to login to platform  
- 404 error  
- Regarding certificates  
- Regarding user expired  


---

### 5️⃣ Assigning Users & Roles to Groups  
- **Certificates Group:** Katherine Pierce + Certificate_role  
- **Platform Group:** Manne Niranjan + Platform_role  


---

### 6️⃣ Assigning Roles to Table  
Both **Certificate_role** and **Platform_role** were assigned **Read/Write access** to the *Operations related* table.  


---

### 7️⃣ Creating ACLs  
Access Control Lists (ACLs) were defined for sensitive fields (Issue, Priority, Ticket Raised Date) to restrict access to authorized roles (admin).  


---

### 8️⃣ Creating Flows for Ticket Assignment  
- **Flow 1:** Automatically assign *“Regarding Certificates”* tickets to the Certificates Group.  
- **Flow 2:** Automatically assign *Platform-related issues* (Login, 404 Error, User Expired) to the Platform Group.  


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
[Streamlining Ticket Assignment for Efficient Support Operations](https://github.com/Baratam-Saiprasoona/Streamlining-Ticket-Assignment-for-Efficient-Support-Operations)  
