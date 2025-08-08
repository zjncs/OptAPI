[User: natural language] 
       ↓ (1)
   [API Gateway / FastAPI]
       ↓ (2) 　　　　　　 ┌────────────┐
[LLM Parsing Service] ───→│ JSON Schema │  (validation)
 (prompt → LLM)           └────────────┘
       ↓ (3)                     ↓ (4)
  [Model Store / Versioned JSON] ←───────┐
       ↓ (5)                             │
[Model Translator] (JSON → LP/LP-file / Pyomo) 
       ↓ (6)
[Solver Service] (CPLEX/Gurobi/GLPK) → [Solution]
       ↓ (7)
[Postprocessing] (metrics, duals, feasibility check)
       ↓ (8)
[LLM Explanation Service] ←── feed original model + solution
 (LLM returns natural-language explanation + "理解的目标/约束")
       ↓ (9)
[API Gateway returns] → JSON (solution) + NL explanation + editable model
       ↓ (10)
[Persistence: DB] (store problem JSON, solution, metadata)
       ↓ (11)
[Visualization / UI] (optional)
