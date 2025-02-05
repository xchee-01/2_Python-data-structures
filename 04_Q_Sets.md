## Intermediate questions

#### 1. Given these sets of patients with different genetic variants:

```
cohort_brca = {'P001', 'P002', 'P003', 'P004'}
cohort_tp53 = {'P003', 'P004', 'P005', 'P006'}
cohort_pten = {'P001', 'P004', 'P006'}
```

**i. How many unique patients are there in total?**

**ii. Which patients have both BRCA and TP53 variants?**

**iii. Which patients have PTEN variants but not BRCA variants?**



   <details>
   <summary>Click to view answer</summary>
     
   ```
    i. total_patients = cohort_brca | cohort_tp53 | cohort_pten
       print(len(total_patients))

    ii. brca_tp53_patients = cohort_brca & cohort_tp53
        print(brca_tp53_patients)

    iii. pten_not_brca = cohort_pten - cohort_brca
         print(pten_not_brca)
   ```

   </details>

#### 2. Given these sets of patient responses to different drugs:

```
   drug_a_responders = {'P001', 'P002', 'P003'}
   drug_b_responders = {'P002', 'P003', 'P004'}
   all_patients = {'P001', 'P002', 'P003', 'P004', 'P005'}
```

**i. Which patients responded to both drugs?**
   
**ii. Which patients didn't respond to either drug?**
   
**iii. Which patients responded to exactly one drug?**

   
   <details>
   <summary>Click to view answer</summary>
     
   ```
    i. dual_responders = drug_a_responders & drug_b_responders
       print(dual_responders)

    ii. non_responders = all_patients - (drug_a_responders | drug_b_responders)
        print(non_responders)

    iii. single_drug_responders = (drug_a_responders ^ drug_b_responders)
         print(single_drug_responders)
   ```

   </details>

