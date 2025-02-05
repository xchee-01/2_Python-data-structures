## 3.1. Basics of Dictionaries
Dictionaries are key-value pair data structures that allow us to store and retrieve related information efficiently.

```
# Basic dictionary structure
patient_profile = {
    "patient_id": "PM001",
    "gene_variants": ["BRCA1", "TP53"],
    "drug_response": "positive"
}
```

Here are some of the common operations.
1. Adding/updating values (continuing on the example above)
```
# Adding new key-value pair
patient_profile["metabolic_score"] = 85

# Updating existing value
patient_profile["drug_response"] = "partial_response"
```

2. Accessing values
```
# Direct access
variant = patient_profile["gene_variants"]

# Safe access with .get()
response = patient_profile.get("drug_response", "unknown")
```

3. Removing items
```
# Remove specific key-value pair
del patient_profile["metabolic_score"]

# Remove and return value
removed_value = patient_profile.pop("drug_response")
```

A nested dictionary is a dictionary that contains other dictionaries as values.
```
molecular_profile = {
    "genetic_markers": {
        "BRCA1": {"variant": "c.181T>G", "pathogenic": True},
        "TP53": {"variant": "c.524G>A", "pathogenic": False}
    },
    "expression_levels": {
        "EGFR": 245.6,
        "VEGF": 189.3
    }
}
```

You have a few ways of actually accessing a nested dictionary. 

1. Accessing direct nested values
```
# Get BRCA1 information
brca1_data = molecular_profile["genetic_markers"]["BRCA1"]  

# Get specific BRCA1 values
brca1_variant = molecular_profile["genetic_markers"]["BRCA1"]["variant"]  
brca1_pathogenic = molecular_profile["genetic_markers"]["BRCA1"]["pathogenic"]

# Get expression levels
egfr_level = molecular_profile["expression_levels"]["EGFR"]
```

2. Using get() method
You can read about the documentation for the method [here](https://www.w3schools.com/python/ref_dictionary_get.asp)
```
tp53_variant = molecular_profile.get("genetic_markers", {}).get("TP53", {}).get("variant")  
vegf_level = molecular_profile.get("expression_levels", {}).get("VEGF")  # Returns 189.3
```

3. Iterating through nested structures:
```
# Loop through genetic markers
for gene, data in molecular_profile["genetic_markers"].items():
    print(f"Gene: {gene}")
    print(f"Variant: {data['variant']}")
    print(f"Pathogenic: {data['pathogenic']}")

# Loop through expression levels
for gene, level in molecular_profile["expression_levels"].items():
    print(f"Gene: {gene}, Expression Level: {level}")
```

