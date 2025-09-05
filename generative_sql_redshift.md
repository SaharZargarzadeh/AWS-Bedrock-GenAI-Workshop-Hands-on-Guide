# Lab 4: Natural Language to SQL with Amazon Q Generative SQL

##  Objective
Use **Amazon Q Generative SQL** in Redshift to convert plain-English questions into optimized SQL code, enabling business users and analysts to get insights without deep SQL knowledge.

---

##  Steps & AWS Documentation

### 1. Enable & Access Amazon Q Generative SQL
- In the **Redshift Query Editor v2**, click the Amazon Q icon to open the chat panel.  
- If it’s your first time, an administrator must enable Generative SQL:  
  - Permissions needed: `sqlworkbench:UpdateAccountQSqlSettings`  
  - Admins can turn it on via **Generative SQL settings** in the editor.  
  :contentReference[oaicite:0]{index=0}

### 2. Feature Overview & Benefits
- You ask questions like *"Show total sales by region last quarter"* in natural language.  
- Amazon Q analyzes the context—your metadata, schema, and query history—and returns a suggested SQL statement.  
- All of this happens within your current permission scope. Your data and queries remain private and are not used to train any foundational model.  
  :contentReference[oaicite:1]{index=1}

### 3. Feature Workflow
1. User types a question in plain English.
2. Query Editor passes metadata (schema, history, etc.) to Amazon Q.
3. The service generates SQL and returns it in the chat.
4. You can insert it into your notebook, run it, or ask follow-up prompts to refine it.  
   :contentReference[oaicite:2]{index=2}

### 4. Try with Sample Data & Iterative Refinement
- AWS provides TPC-DS or TICKIT sample datasets to test prompts quickly.  
- Example:  
  - User: *“How many venues are there?”*  
  - Generated SQL: `SELECT COUNT(*) AS num_venues FROM tickit.venue;`  
  - You can then ask: *“Group by state?”* to get refined results.  
  :contentReference[oaicite:3]{index=3}

### 5. Add Custom Context for Better Accuracy
- Provide a JSON custom context file to enhance SQL generation, including:
  - `TablesToInclude`, `TablesToExclude`
  - `ColumnAnnotations`, `TableAnnotations`
  - `CuratedQueries`, `CustomDocuments`, etc.  
- This is especially helpful when table names or abbreviations are obscure.  
  :contentReference[oaicite:4]{index=4}

### 6. Safety & Security
- Amazon Q detects statements that may modify data (DML/DDL) and prompts a warning for review.  
- Generated SQL respects your permissions, and CloudTrail logs can monitor usage.  
  :contentReference[oaicite:5]{index=5}

---

##  Outcomes
- Create SQL queries via conversational prompts without SQL syntax worry.
- Improve productivity and onboarding for analysts.
- Maintain enterprise-grade safety and auditability.

---

##  Additional Resources
- **Blog**: *Write queries faster with Amazon Q generative SQL for Amazon Redshift* — Nov 2024 overview and walkthrough. :contentReference[oaicite:6]{index=6}  
- **Security Deep Dive**: *Secure generative SQL with Amazon Q* — July 2025, focus on data privacy & encryption. :contentReference[oaicite:7]{index=7}  
- **Documentation**: *Interacting with Amazon Q generative SQL* in the Redshift User Guide — available regions, prompting tips, permissions. :contentReference[oaicite:8]{index=8}  
- **Tutorial**: *Using Amazon Q generative SQL with TICKIT sample data* — walkthrough of example prompts. :contentReference[oaicite:9]{index=9}  
- **Admin Guide**: *Update Generative SQL settings as an administrator* — enabling and governing access. :contentReference[oaicite:10]{index=10}
