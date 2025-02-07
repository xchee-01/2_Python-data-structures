## Basic Level Questions 

#### 1. A doctor has a list of patient IDs who need genetic testing. How would you add a new patient "PT004" to this list?

   ```
   patient_ids = ["PT001", "PT002", "PT003"]
   ```

   <details>
   <summary>Click to view answer</summary>
   patient_ids.append("PT004")
   </details>

#### 2. You have a list of biomarkers to test. The lab ran out of KRAS testing kits. How do you remove KRAS from the list?

   ```
   biomarkers = ["EGFR", "BRAF", "KRAS", "ALK"]
   ```
   
   <details>
   <summary>Click to view answer</summary>
   biomarkers.remove("KRAS")
   </details>

#### 3. You have a list of drug treatments. How would you access the third drug in the list?

   ```
   treatments = ["Erlotinib", "Gefitinib", "Osimertinib", "Afatinib"]
   ```

   <details>
   <summary>Click to view answer</summary>
   third_drug = treatments[2] # Remember, indexing starts at 0
   </details>
   
#### 4. You have a prioritized list of genes to sequence. How would you insert "PTEN" as the second gene in the list?

   ```
   genes = ["BRCA1", "BRCA2", "TP53"]
   ```

   <details>
   <summary>Click to view answer</summary>
   genes.insert(1, "PTEN")
   </details>

#### 5. Given the DNA sequence below, what will be the output of each slice operation?

   ```
   dna = ["A", "T", "C", "G", "A", "T", "G", "C", "A", "T"]
   1. print(dna[::2])   
   2. print(dna[1::2])  
   3. print(dna[::-2])  
   4. print(dna[2:8:2])  
   ```
   <details>
   <summary>Click to view answer</summary>

    1. ["A", "C", "A", "G", "A"]
    2. ["T", "G", "T", "C", "T"]
    3. ["T", "C", "G", "T", "A"]
    4. ["C", "A", "G"]

   </details>

#### 6. For this patient treatment timeline, write the slice operation to:
   ```
   timeline = ["Week1_Chemo", "Week2_Rest", "Week3_Chemo", "Week4_Rest", 
            "Week5_Chemo", "Week6_Rest", "Week7_Assessment"]

   1. Get only the chemotherapy weeks
   2. Get only the rest weeks
   3. Get the timeline in reverse order
   4. Get every second week starting from Week1_Chemo
   ```

   <details>
   <summary>Click to view answer</summary>
      
    1. chemo_weeks = timeline[:6:2]    
    2. rest_weeks = timeline[1:7:2]  
    3. reverse_timeline = timeline[::-1]
    4. alternate_weeks = timeline[::2]
       
   </details>

## Intermediate Level Questions

#### 7. You have a list of patient mutations. How would you find out how many mutations are in the list?

   ```
   mutations = ["MT001", "MT002", "MT003", "MT004", "MT005"]
   ```

   <details>
   <summary>Click to view answer</summary>
   mutation_count = len(mutations)
   </details>

#### 8. You have a list of cancer types. How would you find the position of "Colon" in the list?

   ```
   cancers = ["Lung", "Breast", "Colon", "Melanoma", "Pancreatic"]
   ```
   
   <details>
   <summary>Click to view answer</summary>
   colon_position = cancers.index("Colon")
   </details>

#### 9. For a gene panel test result, write the slice operation to:

   ```
   genes = ["BRCA1", "TP53", "BRCA2", "EGFR", "KRAS", "BRAF", "PTEN"]
   A) ["BRCA1", "BRCA2", "KRAS"]
   B) ["PTEN", "KRAS", "BRCA2", "BRCA1"]
   ```

   <details>
   <summary>Click to view answer</summary>
      
    1. result_a = genes[:5:2]
    2. result_b = genes[::-2]
       
   </details>

## Advanced Level Questions

#### 10. You are a bioinformatician working with genetic variants found in a patient's tumor sample. You need to write a Python program that helps analyze these variants.

**Given the following list of variant identifications (IDs) found in the tumor:**
**variants = ["BRAF-V600E", "EGFR-T790M", "KRAS-G12D", "EGFR-L858R", "BRAF-V600K"]**

**Tasks:**
**1. Create a new list containing only the EGFR variants**
**2. Add a newly discovered variant "EGFR-C797S" to your EGFR variants list**
**3. Sort the EGFR variants alphabetically. This was not taught explicitly here. See if you are able to try it out by reading the documentations [here](https://www.w3schools.com/python/ref_list_sort.asp)**
**4. Print how many EGFR variants were found in total**
**5. Position of "EGFR-L858R" is in your final list of EGFR variants**

**Write a Python program that accomplishes these tasks. Think about which list methods you'll need to use.**

<details>
<summary>Click for answer</summary>

```
 egfr_variants = ["EGFR-T790M", "EGFR-L858R"]
 egfr_variants.append("EGFR-C797S")
 egfr_variants.append("EGFR-C797S")
 total_egfr = len(egfr_variants)
 L858R_position = egfr_variants.index("EGFR-L858R")
```
 
</details>

#### 11. You're working at a cancer research center managing a clinical trial for a new targeted therapy. You need to write a program to manage patient enrollment and treatment responses using Python lists.

**Here is the data of the patients:**

```
patient_ids = ["PT101", "PT102", "PT103", "PT104", "PT105"]
responses = ["Partial Response", "Progressive Disease", "Complete Response", "Partial Response", "Stable Disease"]
mutations = ["EGFR+/KRAS-", "EGFR-/KRAS+", "EGFR+/KRAS-", "EGFR+/KRAS-", "EGFR-/KRAS-"]
```

**1. Two new patients (PT106 and PT107) join the trial. Add them to patient_ids.** 
   - **Their responses are "Complete Response" and "Progressive Disease".**
   - **Their mutation statuses are "EGFR+/KRAS-" and "EGFR-/KRAS+".**
   - **Print all the above to make sure your lists data are correct**
**2. Patient PT103 drops out of the trial. Remove all their information.**
**3. Find and print:**
   - **Total number of patients currently in trial**
   - **Index of the first "Complete Response" in responses list**
4. **Insert a new patient (PT108) at position 2 in all lists:**
   - **Response: "Stable Disease"**
   - **Mutation: "EGFR+/KRAS-"**

<details>
<summary>Click to view answer</summary>

1.
```
patient_ids.append("PT106")
patient_ids.append("PT107")
responses.append("Complete Response")
responses.append("Progressive Disease")
mutations.append("EGFR+/KRAS-")
mutations.append("EGFR-/KRAS+")

print("After adding new patients:")
print("Patient IDs:", patient_ids)
print("Responses:", responses)
print("Mutations:", mutations)
```
    
2. 
```
pt103_index = patient_ids.index("PT103")
patient_ids.remove("PT103")
responses.remove(responses[pt103_index])
mutations.remove(mutations[pt103_index])

print("After removing PT103:")
print("Patient IDs:", patient_ids)
print("Responses:", responses)
print("Mutations:", mutations)
print()
```
    
3.
```
total_patients = len(patient_ids)
first_complete_response = responses.index("Complete Response")

print("Total patients in trial:", total_patients)
print("Index of first Complete Response:", first_complete_response)
print()
```

4. 
```
patient_ids.insert(2, "PT108")
responses.insert(2, "Stable Disease")
mutations.insert(2, "EGFR+/KRAS-")

print("After inserting PT108 at position 2:")
print("Patient IDs:", patient_ids)
print("Responses:", responses)
print("Mutations:", mutations)
```

</details>
