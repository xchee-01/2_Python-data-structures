# **1. Lists**

## **1.1. Basics of lists**

A list in Python is a versatile data structure that lets you store multiple items in a single variable. Think of it like a container that can hold different types of items in a specific order. 

```
# Example: Patient treatment response data
patient_responses = ["Complete Response", "Partial Response", "Stable Disease", "Progressive Disease"]

# Common operations
patient_responses.append("Not Evaluable")  # Add new response
patient_responses.remove("Not Evaluable")  # Remove response
response_count = len(patient_responses)    # Length of list
is_responding = "Complete Response" in patient_responses  # Check membership
patient_responses[0] #Indexing
patient_responses[2] #Indexing
index_of_stable_disease = patient_responses.index("Stable Disease")
patient_responses.insert(2, "Fully recovered")
```

> [!NOTE]  
> Remember that in Python, indexing starts from 0. 

## **1.2. Slicing**

Now that you know how basic list function works, let's explore list slicing with examples relevant to genomics and precision medicine. Splciing is a way to extract parts of sequences like lists, strings or tuples. 

```
dna_sequence = ["A", "T", "G", "C", "G", "A", "T", "T", "C", "G"]

first_three = dna_sequence[0:3]    # ["A", "T", "G"]
first_three = dna_sequence[:3]     # Same result
last_three = dna_sequence[-3:]     # ["T", "C", "G"]
```

We could also do something called "stepping" through the list. The step value in Python slicing determines how many items you "jump" or "skip" as you move through the sequence. 

```
treatment_timeline = [
    "Chemotherapy",
    "Immunotherapy",
    "Targeted_Therapy",
    "Combination_Therapy",
    "Maintenance_Therapy",
    "Follow_up",
    "Monitoring"
]

# 1. Stepping through list
alternate_months = treatment_timeline[::2]

# 2. Negative stepping (reverse order)
reverse_timeline = treatment_timeline[::-1]

# 3. Subsection with step 
mid_treatments = treatment_timeline[1:5:2]
```  

> [!NOTE]  
> Remember that end index is exclusive

> [!CAUTION]
> Modifying slices of mutable objects affects the original


Now, let's talk about **list comprehensions**. List comprehensions provide a concise way to create lists based on existing sequences or iterables. They combine a for loop and list creation into a single line of readable code.

The basic syntax is as follows:
```
new_list = [expression **for** item in iterable **if** condition]
```
at which: 
expression: What to put in the new list
item: The variable representing each element from the iterable
iterable: The sequence you're iterating over
if condition: Optional filter


For example,
1. If you want to do basic list creation, you could:
   
do it the traditional way:

```
squares = []
for x in range(5):
   squares.append(x**2)
```

or do it using list comprehension:

```
squares = [x**2 for x in range(5)]
```

2. For filtering with conditions
   
do it the traditional way:

```
even_numbers = []
for x in range(10):
   if x % 2 == 0：
      even_numbers.append(x)
```

or do it using list comprehension:

```
even_numbers = [x for x in range(10) if x % 2 == 0]
```

3. Strings operations
   
```
words = ["hello", "world", "python"]
#convert all to upper case
upper_words = [word.upper() for word in words]
```

4. Multiple operations
   
```
numbers = [1, 2, 3, 4]
manipulated = [x*2+1 for x in numbers]
```

