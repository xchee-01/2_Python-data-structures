## Basic Level Question

#### 1. Create a dictionary mapping these specific cancer types to their associated mutations:
   
| Cancer | Mutations |
|--------|-----------|
| Lung Adenocarcinoma | EGFR L858R |
| Lung Adenocarcinoma | ALK fusion |
| Lung Adenocarcinoma | KRAS G12C |
| Triple Negative Breast Cancer | BRCA1 |
| Triple Negative Breast Cancer | TP53 R175H |
| Triple Negative Breast Cancer | PIK3CA H1047R |
| Melanoma | BRAF V600E |
| Melanoma | NRAS Q61K |
| Melanoma | NF1 loss |


   <details>
   <summary>Click to view answer</summary>
   
   ```
   cancer_mutations = {
   "Lung Adenocarcinoma": ["EGFR L858R", "ALK fusion", "KRAS G12C"],
   "Triple Negative Breast Cancer": ["BRCA1", "TP53 R175H", "PIK3CA H1047R"],
   "Melanoma": ["BRAF V600E", "NRAS Q61K", "NF1 loss"]
   }

   cancer_mutations["Colorectal Cancer"] = ["KRAS G12D", "BRAF V600E", "PIK3CA E545K"]
   ```

   </details>

## Intermediate Level Question

#### 2. Answer the following questions 
   
```
drug_response = {
  'Gefitinib': 'responsive',
  'Erlotinib': 'resistant',
  'Osimertinib': 'partially_responsive'
}
```

**i. How would you check if 'Afatinib' is in the dictionary?**

**ii. Add a new drug 'Lapatinib' with response 'unknown'**

**iii. How would you print all drug names that show 'resistant' response?**

   
   <details>
   <summary>Click to view answer</summary>
       
   i. is_afatinib_present = 'Afatinib' in drug_response  
   
   ii. drug_response['Lapatinib'] = 'unknown'
   
   iii. for drug, response in drug_response.items():
         if response == 'resistant':
            print(drug)
   
   </details>


#### 3. Answer the following questions
   
```
variant_frequency = {
  'rs123': 0.15,
  'rs456': 0.32,
  'rs789': 0.08,
  'rs012': 0.45
 }
```

**i. How would you find the variant with the highest frequency?**

**ii. Create a new dictionary containing only variants with frequency > 0.30**

**iii. Calculate the average frequency of all variants**

**iv. How would you sort variants by their frequency in descending order?**


   <details>
   <summary>Click to view answer</summary>

   ```
    i. Finding variant with highest frequency
    max_freq = 0
    max_variant = ''
    for variant, freq in variant_frequency.items():
        if freq > max_freq:
             max_freq = freq
            max_variant = variant

    ii. Variants with frequency > 0.30
    high_freq_variants = {}
    for variant, freq in variant_frequency.items():
        if freq > 0.30:
            high_freq_variants[variant] = freq

    iii. Average frequency
    total_freq = 0
    count = 0
    for freq in variant_frequency.values():
        total_freq += freq
        count += 1
    average_freq = total_freq / count

    iv. Sorting by frequency
    sorted_variants = {}
    freqs = list(variant_frequency.values())
    freqs.sort(reverse=True)
    for freq in freqs:
        for variant, var_freq in variant_frequency.items():
            if var_freq == freq and variant not in sorted_variants:
                sorted_variants[variant] = freq
   ```
   
   </details>


## Advanced Level Question

#### 4. You have a dictionary containing patient genetic test results for different genes and their variants:

```
genetic_variants = {
    'P101': {
        'BRCA1': 'wild_type',
        'BRCA2': 'mutant',
        'TP53': 'wild_type',
        'age': 45,
        'family_history': True
    },
    'P102': {
        'BRCA1': 'mutant',
        'BRCA2': 'wild_type',
        'TP53': 'mutant',
        'age': 35,
        'family_history': False
    },
    'P103': {
        'BRCA1': 'wild_type',
        'BRCA2': 'wild_type',
        'TP53': 'mutant',
        'age': 55,
        'family_history': True
    },
    'P104': {
        'BRCA1': 'mutant',
        'BRCA2': 'mutant',
        'TP53': 'wild_type',
        'age': 40,
        'family_history': True
    }
}
```

**Create a new dictionary containing only patients who are**
   - **Under 50 years old AND**
   - **Have at least one mutation in either BRCA1 or BRCA2**


   <details>
   <summary>Click to view answer</summary>

   ```
        selected_patients = {}
    
        for patient_id in genetic_variants:
            patient = genetic_variants[patient_id]
    
            # Check age condition
            age_condition = patient['age'] < 50
    
            # Check BRCA mutation condition
            brca_condition = (patient['BRCA1'] == 'mutant' or patient['BRCA2'] == 'mutant')
    
            # If both conditions are met, add to selected patients
            if age_condition and brca_condition:
                selected_patients[patient_id] = patient
   ```

   </details>

