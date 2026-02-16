# AI Audit Appendix (Assignment 04)

## Tool(s) Used
- [Tool name + version] (e.g., ChatGPT, Claude, GitHub Copilot)
- If none, write: **"No AI tools were used for this assignment."**
GitHub Copilot 

## Task(s) Where AI Was Used
- [Specific task] (e.g., "Statsmodels OLS formula for ret ~ div12m_me")
To do the entire assignment 

## Prompt(s)
- [Exact prompt text]
summarize the key results 

## Output Summary
- [What the AI suggested or generated]
Key Results Summary:

1. Dividend Yield → Annual Returns

Slope: -0.069 (negative)
p-value: 0.035 → Significant at 5%
R²: 0.18% (very weak explanatory power)
Higher dividend yields are associated with slightly lower returns
2. Prime Rate → Annual Returns

Slope: -0.019 (negative)
p-value: <0.001 → Highly significant
R²: 1.64% (weak but strongest of the three)
Higher interest rates are associated with lower REIT returns
3. FFO/Assets → Annual Returns

Slope: +0.577 (positive)
p-value: 0.309 → Not significant
R²: 0.04% (essentially zero)
No statistically reliable relationship found
Takeaway: Only the prime rate shows meaningful predictive power for REIT returns. Rising interest rates hurt REITs, which aligns with theory (higher borrowing costs, competing fixed-income yields). The other predictors have minimal explanatory value despite dividend yield being marginally significant.

## Verification & Modifications (Disclose • Verify • Critique)
- **Verify:** How you checked the output (e.g., ran the script, spot-checked regression table)
I looked over all outputs and compared to the ones in the video. 
- **Critique:** What was wrong/incomplete and why
None 
- **Modify:** What you changed in your final work
Looked over everything and cleaned up 

## If No AI Tools Used
Write: "No AI tools were used for this assignment."
