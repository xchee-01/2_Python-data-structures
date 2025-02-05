## Basic Level Questions

#### 1. What would be the output of the following code?
   
```
snp_data = ("rs789", "C", "T")
risk_allele = snp_data[2]
print(risk_allele)
```

   <details>
   <summary>Click to view answer</summary>
   T
   </details>

#### 2. How would you access the binding score in this tuple?
   
```
protein_binding = ("P53", "DNA_binding_domain", 0.92)
```

   <details>
   <summary>Click to view answer</summary>
   protein_binding[2]
   </details>

#### 3. How can you determine how many genetic variants are stored in this tuple?
   
```
variants = ("rs123", "rs456", "rs789", "rs012", "rs345")
```

   <details>
   <summary>Click to view answer</summary>
   len(variants) 
   </details>


## Intermediate Level Questions

#### 4. Given these two tuples of drug response data, create a new tuple that contains both patient responses. Have a look at the documentation [here](https://www.w3schools.com/python/gloss_python_join_tuple.asp)
   
```
patient1_response = ("Erlotinib", 0.8, "Positive")
patient2_response = ("Erlotinib", 0.4, "Negative")
```

   <details>
   <summary>Click to view answer</summary>

   ```
   combined_response = patient1_response + patient2_response
   ```

   </details>

#### 5. You have a tuple containing protein domain information, print the domain name and its start position (second and third elements).

```
domain_info = ("EGFR", "Kinase", 720, 1020)
```

   <details>
   <summary>Click to view answer</summary>

   ```
   print(domain_info[1], domain_info[2])
   ```

   </details>

#### 6. Given these variant tuples, create a new tuple containing only the variant IDs (first element of each tuple).

```
variant1 = ("rs123", "A", "G")
variant2 = ("rs456", "C", "T")
variant3 = ("rs789", "G", "A")
```

   <details>
   <summary>Click to view answer</summary>

   ```
   variant_ids = variant1[0], variant2[0], variant3[0]
   ```

   </details>

## Advanced Level Questions

#### 7. You are working on analyzing drug response data for a precision medicine study involving targeted cancer therapies. You have the following data stored in tuples:

```
# Each tuple contains: (drug_name, target_protein, IC50_value, response_category, mutation_status)
patient1_data = ("Osimertinib", "EGFR", 0.05, "Highly_Sensitive", "T790M")
patient2_data = ("Osimertinib", "EGFR", 1.52, "Resistant", "T790M")
patient3_data = ("Osimertinib", "EGFR", 0.08, "Highly_Sensitive", "L858R")
patient4_data = ("Osimertinib", "EGFR", 2.31, "Resistant", "Wild_Type")
```

**a. Extract and create a new tuple containing only the IC50 values (third element) from all patients.**
   
   <details>
   <summary>Click to view answer</summary>

   ```
   ic50_values = (patient1_data[2], patient2_data[2], patient3_data[2], patient4_data[2])
   print("IC50 values:", ic50_values)
   ```

   </details>

**b. Create a new tuple that pairs each mutation_status (last element) with its corresponding response_category (fourth element).**

   <details>
   <summary>Click to view answer</summary>

   ```
   mutation_response_pairs = (
   (patient1_data[4], patient1_data[3]),
   (patient2_data[4], patient2_data[3]),
   (patient3_data[4], patient3_data[3]),
   (patient4_data[4], patient4_data[3])
   )
   print("Mutation-Response pairs:", mutation_response_pairs)
   ```

   </details>

**c. Create a tuple containing data only from patients who are "Highly_Sensitive" (check fourth element) without using any functions.**
   
   <details>
   <summary>Click to view answer</summary>
       
   ```
   sensitive_patients = patient1_data + patient3_data
   print("Highly sensitive patient data:", sensitive_patients)
   ```
   
   </details>

**d. Create a tuple of tuples containing the drug_name (first element) and mutation_status (last element) for patients with IC50 values (third element) greater than 1.0.**

   <details>
   <summary>Click to view answer</summary>
       
   ```
   high_ic50_pairs = (
   (patient2_data[0], patient2_data[4]),  # IC50 = 1.52
   (patient4_data[0], patient4_data[4])   # IC50 = 2.31
   )
   print("High IC50 drug-mutation pairs:", high_ic50_pairs)
   ```
   
   </details>
