# Ghost Carbon: Claimed vs Measured Compute Carbon for Common ML Training Recipes

## Abstract
Relative "X% greener" claims hide absolute kgCO2e and grid intensity. We compare claimed greening percentages against bottom-up TDP×time×grid estimates across regions.

## Results (notebook run)
Ghost gap (claimed − estimated true greener %), by recipe/region:
```
                      recipe     region  train_kg  infer_1m_kg  total_kg  claim_greener_pct  true_greener_pct_vs_baseline  ghost_gap_pp
 efficient_cnn_claimed_40pct    iceland      0.04         0.01      0.04                 40                         37.86          2.14
 efficient_cnn_claimed_40pct    vietnam      0.59         0.09      0.69                 40                         37.86          2.14
 efficient_cnn_claimed_40pct coal_heavy      1.05         0.17      1.22                 40                         37.86          2.14
tiny_distilled_claimed_70pct    iceland      0.01         0.00      0.02                 70                         77.55         -7.55
tiny_distilled_claimed_70pct    vietnam      0.22         0.02      0.25                 70                         77.55         -7.55
tiny_distilled_claimed_70pct coal_heavy      0.40         0.04      0.44                 70                         77.55         -7.55
   llm_ft_lora_claimed_green    iceland      0.08         0.03      0.11                 35                        -63.27         98.27
   llm_ft_lora_claimed_green    vietnam      1.26         0.54      1.80                 35                        -63.27         98.27
   llm_ft_lora_claimed_green coal_heavy      2.24         0.96      3.20                 35                        -63.27         98.27
```

## Conclusion
Points below the claim diagonal overstate climate benefit. Report absolute CO2e and grid factor, not only relative %.

## Code
`notebook/ghost-carbon-ml-claims.ipynb` — independent repository.
