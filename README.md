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

<img width="1885" height="772" alt="image" src="https://github.com/user-attachments/assets/your-image-id-here" />  

---

## 🛠️ Project Implementation  

### 1️⃣ Creating Users  
Users represent individuals in the system. Two users were created:  
- **Katherine Pierce** – Member of the Certificates Group.  
- **Manne Niranjan** – Member of the Platform Group.  

<img width="1392" height="678" alt="user_record" src="https://github.com/user-attachments/assets/your-image-id-here" />  

---

### 2️⃣ Creating Groups  
Groups represent teams that handle tickets:  
- **Certificates Group** – Manages certificate-related issues.  
- **Platform Group** – Handles login issues, 404 errors, and expired accounts.  

<img width="1388" height="517" alt="group_record" src="https://github.com/user-attachments/assets/your-image-id-here" />  

---

### 3️⃣ Creating Roles  
Roles define permissions:  
- **Certificate_role** – Grants certificate issue handling access.  
- **Platform_role** – Grants platform issue handling access.  

<img width="1413" height="466" alt="role_record" src="https://github.com/user-attachments/assets/your-image-id-here" />  

---

### 4️⃣ Creating Table & Choices  
A custom table **Operations related** was created with fields:  
- Issue, Description, Assigned To, Status.  

Choices for the **Issue** field:  
- Unable to login to platform  
- 404 error  
- Regarding certificates  
- Regarding user expired  

<img width="1367" height="727" alt="columns" src="https://github.com/user-attachments/assets/your-image-id-here" />  

---

### 5️⃣ Assigning Users & Roles to Groups  
- **Certificates Group:** Katherine Pierce + Certificate_role  
- **Platform Group:** Manne Niranjan + Platform_role  

<img width="1327" height="757" alt="assign_cert" src="https://github.com/user-attachments/assets/your-image-id-here" />  

---

### 6️⃣ Assigning Roles to Table  
Both **Certificate_role** and **Platform_role** were assigned **Read/Write access** to the *Operations related* table.  

<img width="1372" height="482" alt="access_write" src="https://github.com/user-attachments/assets/your-image-id-here" />  

---

### 7️⃣ Creating ACLs  
Access Control Lists (ACLs) were defined for sensitive fields (Issue, Priority, Ticket Raised Date) to restrict access to authorized roles (admin).  

<img width="1390" height="480" alt="acl" src="https://github.com/user-attachments/assets/your-image-id-here" />  

---

### 8️⃣ Creating Flows for Ticket Assignment  
- **Flow 1:** Automatically assign *“Regarding Certificates”* tickets to the Certificates Group.  
- **Flow 2:** Automatically assign *Platform-related issues* (Login, 404 Error, User Expired) to the Platform Group.  

<img width="1887" height="832" alt="flow_designer" src="https://github.com/user-attachments/assets/your-image-id-here" />  

---

## 📷 Screenshots of Output  
- Tickets with “Regarding Certificates” → Auto-assigned to Certificates Group.  
- Tickets with “Unable to login”, “404 Error”, “User Expired” → Auto-assigned to Platform Group.  

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
