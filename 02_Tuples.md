# 2. Tuples

## 2.1. Basics of tuples
Tuples are immutable sequences in Python that can store multiple items. In molecular precision medicine, tuples are particularly useful for representing fixed data structures. A key characteristic of tuples is its **immutability**; in other words, once created tuples **cannot be modified**

```
# Single element tuple (note the comma, comma tells Python that this a tuple)
single_snp = ("rs334",)

# You can put multiple elements
gene_location = ("BRCA1", 17, "q21.31")

# Nested tuples
protein_structure = (("Met", 1, "Start"), ("Gly", 2, "Alpha"), ("Ser", 3, "Beta"))
```

Once created, you would also need to learn to access the elements. 

```
gene_location = ("BRCA1", 17, "q21.31")
gene_name = gene_location[0]    
chromosome = gene_location[1]    
position = gene_location[2]      
```

There are two main tuple methods that you should learn: **count()** and **index()**

Let's see how to use the basic count() examples. 
```
amino_acids = ('A', 'C', 'G', 'A', 'T', 'A', 'C')
a_count = amino_acids.count('A')  
c_count = amino_acids.count('C')  
u_count = amino_acids.count('U')
```

And this is how you can use the index() method. 
```
dna_sequence = ('A', 'T', 'G', 'C', 'A', 'T')
first_a = dna_sequence.index('A')      
first_t = dna_sequence.index('T')      
dna_sequence.index('U')              # Would raise ValueError - not found
```

You may also use index() with start and end parameters. 
```
metabolizer_status = ('Poor', 'Normal', 'Poor', 'Rapid', 'Ultra', 'Poor')
second_poor = metabolizer_status.index('Poor', 1)     # Returns 2 (starts searching from index 1)
third_poor = metabolizer_status.index('Poor', 3)      # Returns 5 (starts searching from index 3)
```
