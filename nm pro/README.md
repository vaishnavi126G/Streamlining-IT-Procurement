# Streamlining IT Procurement: Automating Standard Laptop Orders with Flow Designer

[![ServiceNow](https://img.shields.io/badge/ServiceNow-Flow%20Designer-81B5A1?style=for-the-badge&logo=servicenow&logoColor=white)](https://www.servicenow.com/)
[![Track](https://img.shields.io/badge/Track-AI%2FML%20%26%20ITSM%20Automation-blue?style=for-the-badge)](https://github.com/Ravi-teja-777/AI-ML-and-GEN-AI-Track-Project-Template)
[![Status](https://img.shields.io/badge/Project%20Status-Completed-success?style=for-the-badge)]()

---

## 📌 Project Overview

This repository contains the complete set of project deliverables and documentation for **"Streamlining IT Procurement: Automating Standard Laptop Orders with Flow Designer"**, developed under the **SmartBridge / SmartInternz** curriculum.

The project automates the end-to-end requisition, approval, and provisioning workflow for corporate laptop procurement using **ServiceNow Flow Designer**, eliminating manual handoffs and ensuring timely device configuration.

---

## 🎯 Problem Statement & Objectives

### Problem Statement
The current IT procurement process lacks efficiency and automation, resulting in delays and manual overhead, particularly in handling standard laptop orders. Requests for standard laptops often require configuration, but this step is prone to oversight or delay, leading to frustration among users and inefficient resource allocation within the IT department.

### User Story
> **As a member of the IT procurement team,** I want a streamlined process for ordering standard laptops so that tasks are automatically generated and assigned to the hardware team for configuration. This will ensure that laptops are promptly configured upon arrival, reducing user wait times and minimising manual intervention.

### Project Objectives
1. **Seamless User Experience:** Ensure prompt, transparent laptop procurement and timely hardware configuration.
2. **Eliminate Manual Intervention:** Replace manual email coordination with an automated ServiceNow Flow Designer trigger.
3. **Optimize Resource Allocation:** Automatically route configuration tasks (`sc_task`) to the dedicated **Hardware** assignment group.
4. **Boost Procurement Efficiency:** Accelerate request-to-delivery turnaround time while maintaining an end-to-end audit trail.

---

## 📂 Repository Structure

All deliverables have been prepared according to the required 8-phase submission template:

```
├── 1. Brainstorming & Ideation/
│   ├── Brainstorming & Idea Prioritization.pdf
│   ├── Define Problem Statements .pdf
│   └── Empathy Map.pdf
├── 2. Requirement Analysis/
│   ├── Customer Journey Map.pdf
│   ├── Data Flow Diagram.pdf
│   ├── Solution Requirements.pdf
│   └── Technology Stack.pdf
├── 3. Project Design Phase/
│   ├── Problem-Solution Fit.pdf
│   ├── Proposed Solution.pdf
│   └── Solution Architecture.pdf
├── 4. Project Planning Phase/
│   └── Project Planning.pdf
├── 5. Project Development Phase/
│   ├── Code-Layout, Readability and Reusability.pdf
│   ├── Coding & Solution.pdf
│   └── No. of Functional Features Included in the Solution.pdf
├── 6.Project Testing/
│   └── Performance Testing.pdf
├── 7.Project Documentation/
│   ├── Project Executable Files.pdf
│   ├── Sample Project Documentation.pdf
│   └── Project Documentation.pdf
├── 8.Project Demonstration/
│   ├── Communication.pdf
│   ├── Demonstration of Proposed Features.pdf
│   ├── Project Demo Planning.pdf
│   ├── Scalability & Future Plan.pdf
│   └── Team Involvement in Demonstration.pdf
└── README.md
```

---

## ⚙️ ServiceNow Flow Designer Implementation Guide

### 🔹 Milestone 1: Flow Creation
1. Open ServiceNow instance.
2. Navigate to **All >> search for Flow Designer** under *Process Automation*.
3. Click on **New** and select **Flow**.
4. In Flow Properties:
   - **Flow Name:** `Standard laptop task`
   - **Application:** `Global`
   - **Run As:** `System user`
5. Click **Submit**.
6. Click **Add a trigger**, search for **Service Catalog**, and select it. Click **Done**.
7. Under **Actions**, click **Add an action** and choose **Create Catalog Task**.
8. Configure action parameters:
   - **Action:** `Create Catalog Task`
   - **Request item:** Drag and drop `Trigger -> Requested Item Record`
   - **Table:** Auto-populates as `Catalog Task [sc_task]`
   - **Short description:** `Laptop need to Configured`
   - **Description:** `Laptop need to Configured`
   - **Assignment group:** `Hardware`
   - **Approval:** `Approved`
9. Click **Save** and **Activate** the flow.

---

### 🔹 Milestone 2: Flow Assignment to Catalog Item
1. In ServiceNow, navigate to **All >> Maintain Items**.
2. Search for the catalog item **Standard Laptop** (Lenovo Carbon x1) and open the record.
3. Switch to the **Process Engine** tab.
4. Remove legacy automations/workflows and set the **Flow** field to **`Standard Laptop task`**.
5. Save the record.

---

### 🔹 Milestone 3: Service Catalog Execution & Verification
1. Navigate to **Service Catalog >> Hardware >> Standard Laptop**.
2. Select hardware specifications (Intel Core i5 processor, 512GB SSD, Backlit keyboard) and optional software (Adobe Acrobat, Photoshop).
3. Click **Order Now** to submit the request.
4. View order status and open the generated Request Number (**`REQ0010001`**).
5. In the **Approvers** related list, right-click the record and click **Approve**.
6. Switch to the **Requested Item (`RITM0010001`)** record.
7. Scroll down to the **Catalog Tasks** section:
   - Verify the auto-generated task (**`SCTASK0010001`**).
   - Verify **Assignment group** is set to `Hardware`.
   - Verify **Short description** is set to `Laptop needs to Configured`.
   - Verify **State** is `Open` and **Priority** is `4 - Low`.

---

## 📊 Summary of Phase Deliverables

| Phase | Deliverable File | Key Focus Area | Marks |
|---|---|---|---|
| **Phase 1** | `Brainstorming & Idea Prioritization.pdf` | Idea listing, grouping, prioritization matrix | 3 Marks |
| **Phase 1** | `Define Problem Statements .pdf` | Customer problem statement (PS-1, PS-2, PS-3) | 3 Marks |
| **Phase 1** | `Empathy Map.pdf` | Persona Says, Thinks, Does, Feels analysis | 4 Marks |
| **Phase 2** | `Customer Journey Map.pdf` | Stage-by-stage actions, touchpoints, emotions | 2 Marks |
| **Phase 2** | `Data Flow Diagram.pdf` | Level 1 DFD, external entities, data stores | 2 Marks |
| **Phase 2** | `Solution Requirements.pdf` | Functional & Non-Functional specifications | 4 Marks |
| **Phase 2** | `Technology Stack.pdf` | ServiceNow Flow Designer, architecture tools | 2 Marks |
| **Phase 3** | `Problem-Solution Fit.pdf` | Problem-Solution Fit 10-box canvas | 5 Marks |
| **Phase 3** | `Proposed Solution.pdf` | Project proposal, scope, hardware/software specs | 5 Marks |
| **Phase 3** | `Solution Architecture.pdf` | Presentation, Application, and Data layer blueprint | 5 Marks |
| **Phase 4** | `Project Planning.pdf` | Agile product backlog, sprint schedule (4 sprints) | 5 Marks |
| **Phase 5** | `Code-Layout, Readability and Reusability.pdf` | Code layout checklist, modular components | 5 Marks |
| **Phase 5** | `Coding & Solution.pdf` | Solution summary, verification checklist | 5 Marks |
| **Phase 5** | `No. of Functional Features Included in the Solution.pdf` | Catalog of 8 features, implementation metrics | 5 Marks |
| **Phase 6** | `Performance Testing.pdf` | Benchmark results: <0.7ms latency, 0% error rate | 5 Marks |
| **Phase 7** | `Project Executable Files.pdf` | Submission checklist, run guide, directory tree | 3 Marks |
| **Phase 7** | `Sample Project Documentation.pdf` | 20+ page comprehensive project guide & report | 20 Marks |
| **Phase 8** | `Communication.pdf` | Standups, stakeholder reviews, challenge resolution | 1 Mark |
| **Phase 8** | `Demonstration of Proposed Features.pdf` | Proposed vs demonstrated feature tracking (100%) | 1 Mark |
| **Phase 8** | `Project Demo Planning.pdf` | Live presentation agenda and member assignments | 1 Mark |
| **Phase 8** | `Scalability & Future Plan.pdf` | Scalability roadmap (Phase 2, Phase 3, Phase 4) | 1 Mark |
| **Phase 8** | `Team Involvement in Demonstration.pdf` | Individual member roles, demo evaluation | 1 Mark |

---

## 🏆 Conclusion & Business Impact

By automating the standard laptop procurement process with **ServiceNow Flow Designer**, the solution delivers:
- **Zero Manual Overhead:** Tasks are created and dispatched automatically without email chains or manual ticket logging.
- **75%+ Lead Time Reduction:** Hardware technicians receive tasks immediately upon manager approval.
- **Accurate Resource Utilization:** Tasks are uniformly assigned to the **Hardware** group with standard configuration descriptions.
- **Predictable SLAs & Audit Compliance:** Transparent tracking across `sc_request`, `sc_req_item`, and `sc_task` records.
