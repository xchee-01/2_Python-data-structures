# 4. Sets

# 4.1. Basics of Sets

Sets are a fundamental data structure in programming that offer several key advantages. Their most distinctive feature is maintaining unique elements, automatically eliminating duplicates, which makes them perfect for scenarios where you need to track distinct items. They support powerful mathematical operations like unions, intersections, and differences, making them invaluable for comparing collections of data.

You can create sets as follows
```
# Creating a set of gene variants found in a patient
patient_variants = {'BRCA1', 'TP53', 'KRAS'}

# Converting a list of drug responses to a set (removes duplicates)
drug_responses = set(['responsive', 'resistant', 'partial', 'resistant'])
```

And you can add or remove elements from sets
```
# Adding a newly discovered variant
patient_variants.add('EGFR')

# Removing a variant after validation shows it was a false positive
patient_variants.remove('KRAS')
```

You can even do mathematical operations using sets
```
# Set A: Drugs that target EGFR
egfr_drugs = {'erlotinib', 'gefitinib', 'osimertinib'}

# Set B: Drugs that target VEGF
vegf_drugs = {'bevacizumab', 'ramucirumab', 'osimertinib'}

# Union (all drugs)
all_targeted_drugs = egfr_drugs | vegf_drugs

# Intersection (drugs targeting both pathways)
dual_action_drugs = egfr_drugs & vegf_drugs

# Difference (drugs unique to EGFR pathway)
egfr_specific = egfr_drugs - vegf_drugs
```

