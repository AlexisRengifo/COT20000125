# COT20000125

This repo is used to keep lab work for foundation of computing.

This repo contains lab 4 and lab 5 code.

Lab 4 - Sets with Python
COT2000 - Spring 2025
Introduction to Sets in Python
In Python, a set is an unordered collection of unique elements. Sets are defined using curly braces {} and can be used to perform various operations like union, intersection, and difference. Sets are useful for membership testing and eliminating duplicate entries. Here is an example of how to create and display a set:

my_set = {1, 2, 3, 4, 5, 6, 7}   # This creates a set with elements 1, 2, 3, 4, 5
print(my_set)              # Print the set to see its elements

Practice: Try adding more elements to the set and print it again
{1, 2, 3, 4, 5, 6, 7}

Membership Testing
Sets in Python are particularly useful for testing membership, i.e., checking whether an element is in a set. This operation is very efficient. Here is an example of how to test if specific elements are present in a set:

print(4 in my_set)  # Check if 4 is in the set (Should return True)
print(8 in my_set)
print(2 in my_set) # Check if 8 is in the set (Should return False)

# Practice: Try checking for other elements
True
False
True
Subset and Superset Operations
A set A is a subset of set B if all elements of A are also elements of B. Similarly, B is a superset of A. Python provides methods to check these relationships. Here is how you can check if one set is a subset or a superset of another:

subset = {1, 2}                      # Define a subset
print(subset.issubset(my_set))       # Check if subset is a subset of my_set (Should return True)
print(my_set.issuperset(subset))     # Check if my_set is a superset of subset (Should return True)

subset2 = {2, 3}
print(subset2.issubset(my_set))      
print(my_set.issuperset(subset2))

# Practice: Try defining other subsets and check the relationships
# Example: subset2 = {2, 3}
# Then check subset2.issubset(my_set) and my_set.issuperset(subset2)
True
True
True
True
Set Operations (Union, Intersection, Difference)
Python sets support various mathematical operations such as union, intersection, and difference. The union of two sets is a set containing all unique elements from both sets. The intersection is a set containing only elements that are in both sets. The difference is a set containing elements that are in one set but not in the other. Here is how you can perform these operations:

another_set = {4, 5, 6, 7, 8}                        # Define another set
union_set = my_set.union(another_set)                # Perform union operation
intersection_set = my_set.intersection(another_set)  # Perform intersection operation
difference_set = my_set.difference(another_set)      # Perform difference operation

print("Union:", union_set)                           # Print the union of my_set and another_set
print("Intersection:", intersection_set)             # Print the intersection of my_set and another_set
print("Difference:", difference_set)                 # Print the difference of my_set and another_set

set1 = {1, 2, 3}  # Example set1
set2 = {3, 4, 5}  # Example set2
union_set2 = set1.union(set2)
intersection_set2 = set1.intersection(set2)
difference_set2 = set1.difference(set2)

print("\nUnion of set1 and set2:", union_set2)
print("Intersection of set1 and set2:", intersection_set2)
print("Difference of set1 and set2:", difference_set2)

# Practice: Try creating your own sets and perform these operations
# Example: set1 = {1, 2, 3}
# Example: set2 = {3, 4, 5}
# Then find the union, intersection, and difference of set1 and set2
Union: {1, 2, 3, 4, 5, 6, 7, 8}
Intersection: {4, 5, 6, 7}
Difference: {1, 2, 3}

Union of set1 and set2: {1, 2, 3, 4, 5}
Intersection of set1 and set2: {3}
Difference of set1 and set2: {1, 2}
Ordered Pairs and Cartesian Products
An ordered pair is a pair of elements with the order of the elements being significant. The Cartesian product of two sets is the set of all possible ordered pairs where the first element is from the first set and the second element is from the second set. Here is an example:

A = {1, 2}  # Define the first set
B = {3, 4}  # Define the second set
cartesian_product = {(a, b) for a in A for b in B}  # Compute the Cartesian product
print("Cartesian Product: A x B =", cartesian_product)  # Print the Cartesian product

A = {1, 2, 3}  
B = {4, 5}      

cartesian_product2 = {(a, b) for a in A for b in B}

print("\nCartesian Product: A x B =", cartesian_product2)

# Practice: Try defining different sets and compute their Cartesian product
# Example: A = {1, 2, 3}
# Example: B = {4, 5}
# Then find the Cartesian product of A and B
Cartesian Product: A x B = {(2, 3), (2, 4), (1, 3), (1, 4)}

Cartesian Product: A x B = {(2, 4), (3, 4), (1, 5), (1, 4), (2, 5), (3, 5)}
Cartesian Plane
The Cartesian plane is a two-dimensional plane defined by an x-axis and a y-axis. Each point on the plane can be described by an ordered pair (x, y). Here is an example of how to plot points from the Cartesian product on a Cartesian plane using matplotlib:

import matplotlib.pyplot as plt

# Convert the Cartesian product to a list of points
points = list(cartesian_product)
x_coords = [x for x, y in points]  # Get x-coordinates
y_coords = [y for x, y in points]  # Get y-coordinates

# Plot the points on the Cartesian plane
plt.scatter(x_coords, y_coords)  # Plot the points
plt.title("Cartesian Plane")  # Set the title of the plot
plt.xlabel("X-axis")  # Set the label for the x-axis
plt.ylabel("Y-axis")  # Set the label for the y-axis
plt.grid(True)  # Enable grid
plt.show()  # Display the plot

points2 = list(cartesian_product2)
x_coords2 = [x for x, y in points2]  
y_coords2 = [y for x, y in points2]  

plt.scatter(x_coords2, y_coords2)  
plt.title("Cartesian Plane for A = {1, 2, 3} and B = {4, 5}")  
plt.xlabel("X-axis")  
plt.ylabel("Y-axis")  
plt.grid(True) 
plt.show()  

# Practice: Try plotting the Cartesian product of different sets
# Example: Use sets A and B from the previous example


Relations
A relation between two sets is a subset of the Cartesian product of those sets. It pairs elements from the first set with elements from the second set. Here is an example of a relation between two sets:

A = {1, 2}  # Define the first set
B = {3, 4}  # Define the second set

# Define a relation as a subset of the Cartesian product
R = {(1, 3), (2, 4)}
print("Relation R:", R)  # Print the relation

R2 = {(1, 4), (2, 3)}  
print("Relation R2:", R2)  # Print the new relation

# Practice: Try defining other relations and print them
# Example: R2 = {(1, 4), (2, 3)}
# Then print R2
Relation R: {(2, 4), (1, 3)}
Relation R2: {(2, 3), (1, 4)}
Functions (Mathematical Definition)
In mathematics, a function is a special type of relation where each element in the domain is associated with exactly one element in the codomain. Here is how you can define a function in Python and verify its properties:

def is_function(relation, domain):
    # Check if every element in the domain has exactly one pair in the relation
    domain_elements = [pair[0] for pair in relation]
    return all(domain_elements.count(e) == 1 for e in domain)

A = {1, 2}  # Define the domain
B = {3, 4}  # Define the codomain

# Define a function as a set of ordered pairs
f = {(1, 3), (2, 4)}

# Check if f is a function
print("f is a function:", is_function(f, A))

f2 = {(1, 3), (1, 4)}  
print("f2 is a function:", is_function(f2, A))

# Practice: Try defining other functions and check their properties
# Example: f2 = {(1, 3), (1, 4)}
# Then check is_function(f2, A)
f is a function: True
f2 is a function: False
