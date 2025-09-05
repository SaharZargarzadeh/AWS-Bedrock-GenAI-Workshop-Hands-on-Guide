# Lab 3: Bedrock Flows – Visual AI Pipelines  

## 🎯 Objective  
Use **Bedrock Flows** to visually design multi-step generative AI workflows that combine classification, routing, and knowledge bases.  

---

## 📝 What I Did  

### 1. Created a New Flow  
- Opened **Bedrock Flows** in the console.  
- Added a classification prompt using **Nova Pro**.  

---

### 2. Designed Conditional Routing  
- Classified incoming queries into three categories:  
  - **EDW (Redshift KB)**  
  - **VECTOR (OpenSearch KB)**  
  - **OTHER (general inquiries)**  
- Set conditional branches to route queries to the right KB.  

🔗 [Designing Flows in Bedrock](https://docs.aws.amazon.com/bedrock/latest/userguide/flows-design.html)  

---

### 3. Integrated Knowledge Bases  
- Linked both Redshift and Vector KBs.  
- Configured outputs for factual vs contextual answers.  

---

### 4. Tested & Validated  
- Sent customer-style queries and verified routing worked correctly.  
- Example: *“Why isn’t my charger working?”* → Routed to Vector KB (support docs).  

🔗 [Example Flows in Bedrock](https://docs.aws.amazon.com/bedrock/latest/userguide/flows-ex.html)  

---

## ✅ Why This Helps Us  
Flows turn **AI experiments into repeatable workflows**.  
- Easy to **visualize complex pipelines**.  
- Business analysts (not just developers) can design workflows.  
- Supports scaling to real enterprise customer service or analytics.  

---

## 📚 Resources  
- [Amazon Bedrock Flows](https://docs.aws.amazon.com/bedrock/latest/userguide/flows.html)  
- [Create Your First Flow](https://docs.aws.amazon.com/bedrock/latest/userguide/flows-get-started.html)  
- [Example Flows](https://docs.aws.amazon.com/bedrock/latest/userguide/flows-ex.html)  
