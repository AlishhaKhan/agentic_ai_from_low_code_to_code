# Lab: Customer Support System Using All 5 Agentic Patterns

**Duration:** 60 minutes  
**Level:** Intermediate  
**Prerequisites:** Sessions 4 & 5 (Agent Builder, File Search, Connectors, MCP)

---

## Overview
In this lab, you’ll build a **customer support system** that integrates all **five agentic design patterns** to automate routing, reasoning, quality control, and human oversight.

### Patterns Used
1. **Multi-Agent Pattern** – Route issues to the right specialist  
2. **Tool Use Pattern** – Access documents and real-time data  
3. **Reflection Pattern** – Review and improve responses  
4. **Planning Pattern** – Handle complex, multi-step issues  
5. **Handoff/Delegation Pattern** – Delegate tasks between agents  

---

## System Design

### Architecture Summary
- **Router Agent** analyzes the customer’s issue → directs to Billing, Technical, or General Agent  
- **Specialist Agents** use:
  - *File Search* → retrieves knowledge base info  
  - *MCP Node* → fetches real-time account/shipping data  
- **Critic Agent** reviews responses for accuracy and tone  
- **Improver Agent** refines weak answers  
- **Delegation Logic** sends special cases to Legal or Data Analyst agents  
- **Human Approval Nodes** handle high-value refunds or complex issues  

---

## Implementation Steps (Summary)

### **Step 1: Multi-Agent Routing**
- Create a **Router Agent** to classify issues (billing / technical / general).  
- Use **If/Else nodes** to route the user input to the appropriate specialist agent.  

### **Step 2: Tool Use Pattern**
- Add **File Search** for internal documents.  
- Add **MCP Node** for real-time info (e.g., account data).  
- Update each specialist prompt to use both tools smartly.  

### **Step 3: Reflection Pattern**
- Create a **Critic Agent** to rate responses as `good` or `needs_work`.  
- Add **Improver Agent** for refining low-quality answers.  

### **Step 4: Handoff / Delegation Pattern**
- Allow agents to delegate:
  - Legal questions → **Legal Specialist**
  - Data insights → **Data Analyst**
- Return delegated results to the original agent.  

### **Step 5: Human Approval**
- Add approval for refunds over `$100`.  
- Escalate unresolved or complex issues to human supervisors.  

---

## Testing Scenarios
| **Pattern** | **Test Case** | **Expected Behavior** |
|--------------|----------------|------------------------|
| Tool Use | “What’s your return policy?” | Uses File Search |
| Multi-Agent | “I was charged twice.” | Routes to Billing |
| Reflection | “I want a refund.” | Critic → Improver |
| Delegation | “Is it legal to charge restocking fees?” | Sends to Legal |
| Human Approval | “Refund $500 order.” | Triggers approval |

---

## Lab Completion Checklist
- [x] Router correctly classifies issues  
- [x] Tool use (File Search, MCP Node) works  
- [x] Reflection (Critic + Improver) integrated  
- [x] Delegation logic functional  
- [x] Human approval triggers correctly  
- [x] All patterns operate seamlessly  

---

## Troubleshooting Tips
- Verify **Router outputs** match If/Else conditions exactly  
- Confirm **tool connections** are active  
- Ensure **Critic Agent outputs** “good” or “needs_work”  
- Test each pattern **individually** before combining  

---

## Outcome
By completing this lab, you’ll:
- Build a **multi-agent customer support system**
- Integrate **all five agentic patterns**
- Enable **real-time data retrieval, reflection, and human oversight**
- Prepare for **Session 7: Deploy and Monitor Your Agentic System**
