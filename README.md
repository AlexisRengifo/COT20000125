# COT20000125

This repo is used to keep lab work for foundation of computing.

This repo contains lab 4 and lab 5 code.

{
 "cells": [
  {
   "cell_type": "markdown",
   "id": "207a3194-6f3e-45b8-8a7b-307e35c6026d",
   "metadata": {},
   "source": [
    "# Lab 4 - Sets with Python\n",
    "### COT2000 - Spring 2025"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "b4da7443-64e6-4938-aafe-27bc28e0dee6",
   "metadata": {},
   "source": [
    "### Introduction to Sets in Python\n",
    "\n",
    "In Python, a set is an unordered collection of unique elements. Sets are defined using curly braces `{}` and can be used to perform various operations like union, intersection, and difference. Sets are useful for membership testing and eliminating duplicate entries. Here is an example of how to create and display a set:\n"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 1,
   "id": "977bcc1d-deb9-4c4d-acaa-76a2b20e43d6",
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "{1, 2, 3, 4, 5, 6, 7}\n"
     ]
    }
   ],
   "source": [
    "my_set = {1, 2, 3, 4, 5, 6, 7}   # This creates a set with elements 1, 2, 3, 4, 5\n",
    "print(my_set)              # Print the set to see its elements\n",
    "\n",
    "# Practice: Try adding more elements to the set and print it again"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "f9308a5d-46ee-470c-90fc-b37cab49d974",
   "metadata": {},
   "source": [
    "### Membership Testing\n",
    "\n",
    "Sets in Python are particularly useful for testing membership, i.e., checking whether an element is in a set. This operation is very efficient. Here is an example of how to test if specific elements are present in a set:\n"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 3,
   "id": "5b487025-40a8-43cb-9269-3ef9fc9d0d71",
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "True\n",
      "False\n",
      "True\n"
     ]
    }
   ],
   "source": [
    "print(4 in my_set)  # Check if 4 is in the set (Should return True)\n",
    "print(8 in my_set)\n",
    "print(2 in my_set) # Check if 8 is in the set (Should return False)\n",
    "\n",
    "# Practice: Try checking for other elements"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "9bf2910a-6fe6-4cf5-ae4f-32a76107f597",
   "metadata": {},
   "source": [
    "### Subset and Superset Operations\n",
    "\n",
    "A set `A` is a subset of set `B` if all elements of `A` are also elements of `B`. Similarly, `B` is a superset of `A`. Python provides methods to check these relationships. Here is how you can check if one set is a subset or a superset of another:\n"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 7,
   "id": "102c23c0-5e09-4b2d-bf58-eaf7a105eaea",
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "True\n",
      "True\n",
      "True\n",
      "True\n"
     ]
    }
   ],
   "source": [
    "subset = {1, 2}                      # Define a subset\n",
    "print(subset.issubset(my_set))       # Check if subset is a subset of my_set (Should return True)\n",
    "print(my_set.issuperset(subset))     # Check if my_set is a superset of subset (Should return True)\n",
    "\n",
    "subset2 = {2, 3}\n",
    "print(subset2.issubset(my_set))      \n",
    "print(my_set.issuperset(subset2))\n",
    "\n",
    "# Practice: Try defining other subsets and check the relationships\n",
    "# Example: subset2 = {2, 3}\n",
    "# Then check subset2.issubset(my_set) and my_set.issuperset(subset2)"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "33dbb0a2-7186-4dcb-8898-ad6f2ddadfc4",
   "metadata": {},
   "source": [
    "### Set Operations (Union, Intersection, Difference)\n",
    "\n",
    "Python sets support various mathematical operations such as union, intersection, and difference. The union of two sets is a set containing all unique elements from both sets. The intersection is a set containing only elements that are in both sets. The difference is a set containing elements that are in one set but not in the other. Here is how you can perform these operations:\n"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 9,
   "id": "2449278b-300c-4b6b-8bd1-bbacde778c95",
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "Union: {1, 2, 3, 4, 5, 6, 7, 8}\n",
      "Intersection: {4, 5, 6, 7}\n",
      "Difference: {1, 2, 3}\n",
      "\n",
      "Union of set1 and set2: {1, 2, 3, 4, 5}\n",
      "Intersection of set1 and set2: {3}\n",
      "Difference of set1 and set2: {1, 2}\n"
     ]
    }
   ],
   "source": [
    "another_set = {4, 5, 6, 7, 8}                        # Define another set\n",
    "union_set = my_set.union(another_set)                # Perform union operation\n",
    "intersection_set = my_set.intersection(another_set)  # Perform intersection operation\n",
    "difference_set = my_set.difference(another_set)      # Perform difference operation\n",
    "\n",
    "print(\"Union:\", union_set)                           # Print the union of my_set and another_set\n",
    "print(\"Intersection:\", intersection_set)             # Print the intersection of my_set and another_set\n",
    "print(\"Difference:\", difference_set)                 # Print the difference of my_set and another_set\n",
    "\n",
    "set1 = {1, 2, 3}  # Example set1\n",
    "set2 = {3, 4, 5}  # Example set2\n",
    "union_set2 = set1.union(set2)\n",
    "intersection_set2 = set1.intersection(set2)\n",
    "difference_set2 = set1.difference(set2)\n",
    "\n",
    "print(\"\\nUnion of set1 and set2:\", union_set2)\n",
    "print(\"Intersection of set1 and set2:\", intersection_set2)\n",
    "print(\"Difference of set1 and set2:\", difference_set2)\n",
    "\n",
    "# Practice: Try creating your own sets and perform these operations\n",
    "# Example: set1 = {1, 2, 3}\n",
    "# Example: set2 = {3, 4, 5}\n",
    "# Then find the union, intersection, and difference of set1 and set2\n"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "7d44dcb4-588a-4a21-acd1-98559f2da152",
   "metadata": {},
   "source": [
    "### Ordered Pairs and Cartesian Products\n",
    "\n",
    "An ordered pair is a pair of elements with the order of the elements being significant. The Cartesian product of two sets is the set of all possible ordered pairs where the first element is from the first set and the second element is from the second set. Here is an example:\n"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 11,
   "id": "7ea7075f-4296-42ac-9977-62b0e273bae9",
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "Cartesian Product: A x B = {(2, 3), (2, 4), (1, 3), (1, 4)}\n",
      "\n",
      "Cartesian Product: A x B = {(2, 4), (3, 4), (1, 5), (1, 4), (2, 5), (3, 5)}\n"
     ]
    }
   ],
   "source": [
    "A = {1, 2}  # Define the first set\n",
    "B = {3, 4}  # Define the second set\n",
    "cartesian_product = {(a, b) for a in A for b in B}  # Compute the Cartesian product\n",
    "print(\"Cartesian Product: A x B =\", cartesian_product)  # Print the Cartesian product\n",
    "\n",
    "A = {1, 2, 3}  \n",
    "B = {4, 5}      \n",
    "\n",
    "cartesian_product2 = {(a, b) for a in A for b in B}\n",
    "\n",
    "print(\"\\nCartesian Product: A x B =\", cartesian_product2)\n",
    "\n",
    "# Practice: Try defining different sets and compute their Cartesian product\n",
    "# Example: A = {1, 2, 3}\n",
    "# Example: B = {4, 5}\n",
    "# Then find the Cartesian product of A and B"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "eba3addd-7148-4a1c-ab18-14c7a8e1d3bf",
   "metadata": {},
   "source": [
    "### Cartesian Plane\n",
    "\n",
    "The Cartesian plane is a two-dimensional plane defined by an x-axis and a y-axis. Each point on the plane can be described by an ordered pair `(x, y)`. Here is an example of how to plot points from the Cartesian product on a Cartesian plane using matplotlib:\n"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 13,
   "id": "d88345fd-afce-4591-83fb-5eed00cb569a",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "image/png": "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czVmzBgVFRWpXbt2GjdunMaPH3/e9T///POaOHGiRo8erWeeeUbNmjWTn5+fpk2bVm1waNq0qcPjs/ck/XQ/z2fOnDnq16+f/Pz81KxZs1pd+pswYYJeeeUV/eEPf1CfPn101VVXydfXVyNHjqx2uxeq8ejRo5Kke+6557zbPHHihBo2bFirfQJMRLgBDOLn56f+/ftr48aNOnz48AXfNr1582YdOXJE6enplWdrJOnkyZPVzv/xjcK10axZMzVt2vS8785q1KhR5Z979+6t3r17q7y8XFlZWXrppZf02GOPqUWLFrrvvvuqXf7NN99U3759lZyc7DBeWFjoVJ211a5dO0VGRjq1zNn7Y2bOnOkwfvz4cTVu3NjpGpo1ayZJeumll8777rEWLVo4vV7AJFyWAgwzefJkWZalhx9+WKWlpVWet9vteueddySdCys/fVfVwoULndpmYGBgtWch7rrrLn333XcqLy9XZGRklZ+f3kwrnQloP//5z/XKK69Iknbu3Hne7fr4+FSpfc+ePdq2bZtT9btTdTW+++67+uabby5qfb169VLjxo21b9++ansaGRl53jNlwJWCMzeAYaKiopScnKxHH31U3bp10yOPPKKbbrpJdrtdu3bt0quvvqrOnTsrPj5ePXv21FVXXaXRo0crMTFRAQEBWrZsmT755BOnttmlSxetW7dOycnJ6tatm3x9fRUZGan77rtPy5YtU1xcnMaPH6/u3bsrICBAhw8f1r/+9S8NGjRIv/zlL7VgwQJt3rxZAwcOVJs2bXT69GktXrxYkhQdHX3e7d5111165plnlJiYqD59+uizzz7Tn/70J7Vt21ZlZWWX1EdXueuuu7RkyRLdeOONioiI0Mcff6w///nPF/1hhMHBwXrppZc0bNgwnThxQvfcc4+aN2+ub7/9Vp988om+/fbbKmeygCsN4QYw0MMPP6zu3bvrhRde0Jw5c5SXl6eAgAB17NhRQ4YM0e9//3tJZ+7vePfddzVx4kQ98MADatiwoQYNGqRVq1bplltuqfX2xo8fr71792rKlCnKz8+XZVmyLEt+fn56++23NW/ePP3tb3/TrFmz5O/vr9DQUPXp00ddunSRdOaG4k2bNikxMVF5eXkKDg5W586d9fbbbys2Nva82506daqKi4uVkpKiuXPnKjw8XAsWLND69esrb1b2tnnz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AEYh3AAAAKMQbgAAgFEINwAAwCiEGwAAYBSnw01qaqo+/PDDysevvPKKunbtqiFDhuj77793aXEAAADOcjrcTJo0SQUFBZKk7OxsTZw4UXFxcTpw4IAmTJjg8gIBAACc4fR3Sx08eFDh4eGSpLVr1+quu+7SzJkztXPnTsXFxbm8QAAAAGc4feamXr16Ki4uliS9//77io2NlSQ1adKk8owOAACAtzh95ua2227ThAkT1KtXL+3YsUOrVq2SJP33v/9VaGioywsEAABwhtNnbl5++WX5+/trzZo1Sk5O1jXXXCNJ2rhxowYMGODyAgEAAJzh9JmbNm3a6J///GeV8RdeeMElBQEAAFyKWoWbgoIC2Wy2yj/X5Ow8AAAAb6hVuLnqqquUm5ur5s2bq3HjxvLx8akyx7Is+fj4qLy83OVFAgAA1Fatws3mzZvVpEmTyj9XF24AAADqglqFmz59+lT+uW/fvu6qBQAA4JI5/W6padOmVXvpKT8/X7/97W9dUhQAAMDFcjrcvPHGG+rVq5e+/PLLyrH09HR16dJFX331lStrAwAAcJrT4WbPnj267rrr1LVrV7322muaNGmSYmNj9eCDDzp8oSYAAIA3OP05NyEhIVq5cqWmTp2qUaNGyd/fXxs3blT//v3dUR8AAIBTnD5zI0kvvfSSXnjhBf32t79Vu3btNG7cOH3yySeurg0AAMBpToebO++8U9OnT9cbb7yhZcuWadeuXfrFL36hHj16aO7cue6oEQAAoNacDjdlZWXas2eP7rnnHklSgwYNlJycrDVr1vAVDAAAwOucvucmLS2t2vGBAwcqOzv7kgsCAAC4FBd1z835NGvWzJWrAwAAcJrTZ27Ky8v1wgsv6O9//7tycnJUWlrq8PyJEydcVhwAAICznD5zM336dD3//PO69957lZ+frwkTJuhXv/qVfH19lZSU5IYSAQAAas/pcLNs2TK99tpreuKJJ+Tv76/f/va3WrRokZ5++mlt377dHTUCAADUmtPhJi8vT126dJEkBQcHKz8/X5J011136d1333VtdQAAAE5yOtyEhoYqNzdXktS+fXtt2rRJkpSZmanAwEDXVgcAAOAkp8PNL3/5S33wwQeSpPHjx2vatGnq0KGDEhISNGLECJcXCAAA4Ayn3y01e/bsyj/fc889Cg0N1b///W+1b99ed999t0uL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wCiEGwBXpPT0dPn4+OjkyZPeLgWAixFuAHhVeXm5evbsqcGDBzuM5+fnKywsTH/84x/dst2ePXsqNzfX4QsqAZiBTygG4HWff/65unbtqldffVX333+/JCkhIUGffPKJMjMzVa9ePS9XCOBywpkbAF7XoUMHzZo1S2PHjtWRI0f01ltvaeXKlVq6dOl5g80f/vAHdezYUUFBQWrXrp2mTZsmu90u6cw3F0dHR2vAgAGV3/B88uRJtWnTRlOnTpVU9bLUoUOHFB8fr6uuukoNGzbUTTfdpA0bNrh/5wG4nP+FpwCA+40dO1br169XQkKCsrOz9fTTT6tr167nnd+oUSMtWbJErVu3VnZ2th5++GE1atRITz75pHx8fLR06VJ16dJF8+fP1/jx4zV69Gi1aNFCSUlJ1a5vzJgxKi0t1ZYtW9SwYUPt27dPwcHB7tlZAG7FZSkAdcZ//vMfderUSV26dNHOnTvl71/7///685//rFWrVikrK6tybPXq1Ro6dKgmTJigefPmadeuXerYsaOkM2dubr/9dn3//fdq3LixIiIiNHjwYCUmJrp8vwB4FpelANQZixcvVlBQkA4ePKjDhw9LkkaPHq3g4ODKn7PWrFmj2267TS1btlRwcLCmTZumnJwch/X9+te/1q9+9SvNmjVLzz33XGWwqc64ceM0Y8YM9erVS4mJidqzZ497dhKA2xFuANQJ27Zt0wsvvKC33npLUVFReuihh2RZlv70pz9p9+7dlT+StH37dt13332688479c9//lO7du3S1KlTVVpa6rDO4uJiffzxx/Lz89Pnn39e4/ZHjhypAwcOaOjQocrOzlZkZKReeukld+0uADci3ADwuh9++EHDhg3TqFGjFB0drUWLFikzM1MLFy5U8+bN1b59+8ofSfroo4907bXXaurUqYqMjFSHDh106NChKuudOHGifH19tXHjRs2fP1+bN2+usY6wsDCNHj1a69at08SJE/Xaa6+5ZX8BuBfhBoDXPfXUU6qoqNCcOXMkSW3atNFzzz2nSZMm6auvvqoyv3379srJydHKlSv15Zdfav78+Vq/fr3DnHfffVeLFy/WsmXLFBMTo6eeekrDhg3T999/X20Njz32mN577z0dPHhQO3fu1ObNm9WpUyeX7ysA9+OGYgBelZGRof79+ys9PV233Xabw3N33HGHysrK9P7778vHx8fhuSeffFKLFy9WSUmJBg4cqB49eigpKUknT57Ut99+qy5dumj8+PGaPHmyJKmsrEy9evXSddddp1WrVlW5oXjs2LHauHGjDh8+LJvNpgEDBuiFF15Q06ZNPdYLAK5BuAEAAEbhshQAADAK4QYAABiFcAMAAIxCuAEAAEYh3AAAAKMQbgAAgFEINwAAwCiEGwAAYBTCDQAAMArhBgAAGIVwAwAAjEK4AQAARvk/1mRlRnSap6EAAAAASUVORK5CYII=",
      "text/plain": [
       "<Figure size 640x480 with 1 Axes>"
      ]
     },
     "metadata": {},
     "output_type": "display_data"
    },
    {
     "data": {
      "image/png": "iVBORw0KGgoAAAANSUhEUgAAAjcAAAHFCAYAAAAOmtghAAAAOXRFWHRTb2Z0d2FyZQBNYXRwbG90bGliIHZlcnNpb24zLjkuMiwgaHR0cHM6Ly9tYXRwbG90bGliLm9yZy8hTgPZAAAACXBIWXMAAA9hAAAPYQGoP6dpAABD8klEQVR4nO3dd3xUVf7/8fekkJBGCb2DiBFpStQgKGAgICGioi6CVFFRVkCswCJBEZSVFQUXBGkqRSUUCyBxkaKAhh7EgsJSliAgkkCiYUjO7w+/mR9D6sCEmbm8no/HPGDOnHvv+czMSd65ZcZmjDECAACwCD9PDwAAAMCdCDcAAMBSCDcAAMBSCDcAAMBSCDcAAMBSCDcAAMBSCDcAAMBSCDcAAMBSCDcAAMBSCDc+ateuXerfv7/q16+v4OBghYWF6YYbbtDEiRN18uRJt25rwYIFmjx5slvXWRCbzabExMRS386F1q5dK5vN5rj5+/uratWquu+++/T99987+v33v/+VzWbT3LlzL/sYXbF9+3a1bdtW5cqVk81muyyvnSSdOHFCQUFBstls2rJly2XZZnFmzZql6667TmXLltXdd9/t9Nh3332nxx9/XK1atVJoaKhsNpvWrl17Sdtbs2aNBgwYoKioKIWGhqpmzZrq1q2btm7detHrzMzMVI8ePXTNNdcoPDxcoaGhuu666zRu3DhlZmbm6+/n56fy5cvr9ttv1w8//HAp5ZSqksz3vDl3/i0iIkLNmzfX5MmTlZOTc3kGW4jx48erYcOGCgoK0pNPPlloP2OMbrvtNtlsNv3973+/6O3NnTs33/ORdzt69Gi+voGBgapZs6aGDBni8efqcgvw9ADgupkzZ+rxxx/XNddco2eeeUaNGzeW3W7Xli1bNH36dG3atElLly512/YWLFig3bt3a9iwYW5bZ0E2bdqkWrVqleo2ijJ+/Hi1b99eZ8+e1ZYtW/Tiiy/qP//5j1JTU1WzZk2PjctVAwYMUGZmphYtWqQKFSqoXr16l2W77733ns6ePSvpr1ARHR19WbZbmJMnT2rQoEG6/vrrlZSUpIYNGzo9vmXLFi1btkzXX3+9YmNj9cknn1zyNqdNm6bffvtNQ4cOVePGjXX8+HFNmjRJMTEx+vzzz3X77be7vE673S5jjIYPH6769evLz89P69ev14svvqi1a9fqiy++cOr/1Vdfad++fRo8eLBGjBjh1p8FnvLEE0+oZ8+ekqRTp07p448/1pNPPqlDhw5p0qRJHhnTrl27NGrUKHXu3FnTpk1To0aNCu371ltv6eeff3bbtufMmaOoqCintsjISKf78fHxSk5OVlJSkqZMmaLY2Fh169bNbWPwegY+ZePGjcbf39907tzZ/Pnnn/kez87ONsuXL3fLtjIzM40xxsTHx5u6deu6ZZ3e6MsvvzSSzEcffeTUPmvWLCPJjBs3zhhjzP79+40kM2fOHA+MsuQCAgLMY4895rb1nT171tjt9mL7NWnSxFSpUsXceOONply5ciYrK8ttY7gYGzduNJLM7NmzC3w8JyfH8f+PPvrISDJffvnlJW3z119/zdd2+vRpU7VqVRMbG3tJ677Qs88+aySZX375pcDH7777btOoUSO3btOdJJkxY8YU2Sdvzv3zn//M99itt95qqlevXkqjK96CBQuMJLNmzZoi++3fv9+EhYWZJUuWGElm8ODBF73NOXPmGEkmJSWlxMukp6cbSWb8+PEXvV1fxGEpHzN+/HjZbDbNmDFDQUFB+R4vU6aM7rzzTsf9Dz74QHFxcapevbrKli2ra6+9Vs8//3y+3dn9+vVTWFiYUlNTFRcXp/DwcMXGxqpdu3b67LPPdODAAaddoHnOnj2rcePGKSoqSkFBQapcubL69++v48ePO61/zZo1ateunSIjI1W2bFnVqVNH3bt3V1ZWlqPPhbupjx8/rscff1yNGzdWWFiYqlSpottvv10bNmxwWnferuvXXntN//rXv1S/fn2FhYWpVatW2rx580U9z5IUExMjSTpw4EChfX7++Wf1799fV199tUJCQlSzZk0lJCQoNTXVqV/eoa+FCxdq1KhRqlGjhiIiItShQwf9+OOP+db7xRdfKDY2VhEREQoJCVHr1q31n//8p8jx5u2yPnfunKZNm5bvtdq9e7e6deumChUqKDg4WC1atNC8efMKHOd7772np556SjVr1lRQUFCxf3V+88032r17t3r37q2HH35Y6enpSkpKKnKZ0padnS1JCg8PL/BxPz/3//irUqVKvrawsDA1btxYhw4dcuu2KleuLEkKCCh4B3xERITjOSip5ORkdevWTbVq1VJwcLAaNmyoRx99VCdOnHDql5iYKJvNpu+++04PPPCAypUrp6pVq2rAgAFKT0936puRkaGHH35YkZGRCgsLU+fOnfXTTz+5NK6ClCtXToGBgZe8notV3PsrzyOPPKKOHTvmOyx6uUREREiSy+8FX0e48SE5OTlas2aNWrZsqdq1a5domb1796pLly6aNWuWVq1apWHDhunDDz9UQkJCvr5nz57VnXfeqdtvv13Lly/X2LFj9e9//1utW7dWtWrVtGnTJsdNknJzc9WtWze98sor6tmzpz777DO98sorSk5OVrt27fTHH39I+it8xMfHq0yZMpo9e7ZWrVqlV155RaGhoY7DGAXJO3dozJgx+uyzzzRnzhw1aNBA7dq1K/DciLfeekvJycmaPHmy5s+fr8zMTHXp0iXfD9uSyvuFnvdLpCBHjhxRZGSkXnnlFa1atUpvvfWWAgICdPPNNxcYWkaOHKkDBw7onXfe0YwZM7R3714lJCQ4HQ9///33FRcXp4iICM2bN08ffvihKlasqE6dOhUZcOLj4x2vzb333uv0Wv3444+65ZZb9N133+nNN9/UkiVL1LhxY/Xr108TJ07Mt64RI0bo4MGDmj59uj755JMCf2mfb9asWZL+OiTWo0cPhYSEONqKY4zRuXPnSnTzRenp6dq2bZuuu+66S1pP3vOUkZGhVatWadKkSXrggQdUp04dN41U+uWXX9SqVStNmzZNq1ev1gsvvKBvvvlGbdq0kd1uz9e/e/fuatSokZKSkvT8889rwYIFTueeGGN01113OcLy0qVLFRMTozvuuMOlceXm5jreA7/99pvj50jv3r2LXdaT76933nlH3377raZOnerW9Xbt2lX+/v6qWLGi7rnnHu3evdut67cEz+44giuOHj1qJJkePXpc1PK5ubnGbrebdevWGUlm586djsf69u1b6C78wg5LLVy40EgySUlJTu0pKSlGkvn3v/9tjDFm8eLFRpLZsWNHkeNTMbupz507Z+x2u4mNjTV33323oz1v13XTpk3NuXPnHO3ffvutkWQWLlxY5HbzDkt98MEHxm63m6ysLLN+/XrTsGFD4+/v73ieSnJY6ty5c+bs2bPm6quvNk8++WS+bXTp0sWp/4cffmgkmU2bNhlj/joUWLFiRZOQkODULycnxzRv3tzcdNNNRdZijClw13ePHj1MUFCQOXjwoFP7HXfcYUJCQsypU6ecxnnbbbcVu508mZmZJiIiwsTExDja+vbta2w2m/n555+LXT5vmyW57d+/v8TjSkpKMpLMypUri+3rrsNSBenVq5cJCAgwW7ZsuaT15M23vFv//v2LPFz42GOPmYiIiIveXt7PiwMHDhhJToe7x4wZYySZiRMnOi3z+OOPm+DgYJObm2uMMWblypVGknnjjTec+r388ssuHZYq6NavXz+n+V6YvEM5Jbm5YtKkSUaS+f777wt8/PDhw6ZcuXLm7bffdrQVNDddsXLlSjNq1CjzySefmHXr1pmpU6eaWrVqmdDQ0CJ/vpYtW9YMGTLkorfri9hzY3H79u1Tz549Va1aNfn7+yswMFBt27aVJKcrgfJ07969xOv+9NNPVb58eSUkJDj99dOiRQtVq1bNsXelRYsWKlOmjB555BHNmzdP+/btK/E2pk+frhtuuEHBwcEKCAhQYGCg/vOf/xQ49vj4ePn7+zvuN2vWTFLRh5XO97e//U2BgYEKCQnRbbfdppycHC1evNixnoKcO3dO48ePV+PGjVWmTBkFBASoTJky2rt3b4FjPP+QYUFj3Lhxo06ePKm+ffs6Pae5ubnq3LmzUlJSCrxCpjhr1qxRbGxsvj1+/fr1U1ZWlmMPTx5X3gcffvihMjIyNGDAAEfbgAEDZIzRnDlzil2+ZcuWSklJKdGtRo0axa4vJydHBw4c0L///W8FBwfrhhtuKHEt7jZ69GjNnz9fr7/+ulq2bHlJ6+rUqZNSUlK0Zs0avfzyy0pKSlL37t2Vm5tbYP+bb75ZGRkZeuONN3Tq1CkZY4rdxrFjxzRo0CDVrl3bMd/q1q0rqeCfFwW9n//8808dO3ZMkvTll19Kknr16uXUL+/k4JIaOnSo4z3w5Zdfavz48frwww/1wAMPFLtsQkJCid9fJWG32/XDDz9o3rx5qlq1qho0aFBgv0GDBql58+Z6+OGHXaq1KJ07d9a4cePUtWtX3XbbbRo8eLA2bNggm82mF154odDlbr75ZiUlJWnLli36888/3TYeb8bVUj6kUqVKCgkJ0f79+0vU/8yZM7r11lsVHByscePGqVGjRgoJCdGhQ4d0zz33OA4b5QkJCXEcny2JX3/9VadOnVKZMmUKfDzvOP1VV12lL774QhMnTtTgwYOVmZmpBg0aaMiQIRo6dGih6//Xv/6lp556SoMGDdJLL72kSpUqyd/fX6NHjy7wB+2FVwvknZN0YZ2FefXVV3X77bfL399flSpVKtGhv+HDh+utt97Sc889p7Zt26pChQry8/PTwIEDC9xucWP89ddfJf11WKkwJ0+eVGhoaIlqyvPbb7+pevXq+drzwsJvv/3m1F5Q38LMmjVLwcHB6ty5s06dOiXpr19y9erV09y5czV27Fin0HmhsLAwtWjRokTbKuz8kvPFxsZq3bp1Cg8P1+LFi4s9pFZaxo4dq3Hjxunll1++pMt/81SoUMFxBVr79u111VVXqUePHlq+fHmB53P07dtX3377rYYNG6Zhw4bp9ddfL/KKx9zcXMXFxenIkSMaPXq0mjZtqtDQUOXm5iomJuai3s+//fabAgIC8vWrVq2aS7XXqlXL6eq7du3ayWazacSIEfr888/VqVOnQpetWLGiypUr59L2inL11VfrwIEDqlq1qj755JMCf/4tXrxYq1at0ldffZXvsPjZs2d16tQphYaGuuWcoXr16qlNmzZFnl/47rvvKi4uTjfeeKMk6ffff1f58uUvedvejHDjQ/z9/RUbG6uVK1fq8OHDxV42vWbNGh05ckRr16517K2R5PgFdKHzTz4tiUqVKikyMlKrVq0q8PHzT7S79dZbdeuttyonJ0dbtmzRlClTNGzYMFWtWlU9evQocPn3339f7dq107Rp05zaT58+7dI4S6pBgwYuX778/vvvq0+fPho/frxT+4kTJy7qh0elSpUkSVOmTHGc0HyhqlWrurzeyMhIpaWl5Ws/cuSI03bzlPS98NNPP+mrr76SpELP/fj888/VpUuXQtexbt06tW/fvkTb279/f7GXtk+fPl3ff/+9Ro4cqUceeUR79+5VSEhIidbvLmPHjlViYqISExM1cuTIUtnGTTfdJEmFnpybnJysadOmacCAAXrwwQeLPedn9+7d2rlzp+bOnau+ffs62i/lEubIyEjHeTLnB5wLP5PlYuTt9dy5c2eR4WbevHnq379/idZZkr1by5Yt0549e/T000/rkUce0bZt2/LNl927d+vcuXMFzuGZM2dq5syZWrp0qe66664Sjask4y7qBPmRI0fq8OHDevvtt9W0adNiT4K2AsKNjxkxYoRWrFihhx9+WMuXL8/3V4PdbteqVauUkJDgmHAXXlX19ttvu7TNoKCgAv9q69q1qxYtWqScnBzdfPPNJVqXv7+/br75ZkVFRWn+/Pnatm1boeHGZrPlG/uuXbu0adOmEp9QXdoKGuNnn32m//3vf/k+V6UkWrdurfLly2vPnj1u+Ws/T2xsrJYuXaojR444Hdp59913FRISUmiQKk7eScMzZ87MV+8ff/yhbt26afbs2UWGm7zDUiVRksNSUVFRioqKUmZmpnr37q1NmzYpNja2ROt3h5deekmJiYn6xz/+oTFjxpTadvIO+RT2Pvv0008VHBys6dOnl2gPgbt+Xpyvffv2mjhxoubPn68hQ4Y42hcsWHDR68yzY8cOSQVfoXa+vMNS7tKiRQu1aNFC+/bt0+jRo7Vv3z5dddVVTn369eundu3a5Vu2ffv2uuuuuzR06FA1adLELePZv3+/vv76a3Xo0KHQPh9//LF69OihRx55xC3b9AWEGx+TdyXD448/rpYtW+qxxx7TddddJ7vdru3bt2vGjBlq0qSJEhISdMstt6hChQoaNGiQxowZo8DAQM2fP187d+50aZtNmzbVkiVLNG3aNLVs2VJ+fn6Kjo5Wjx49NH/+fHXp0kVDhw7VTTfdpMDAQB0+fFhffvmlunXrprvvvlvTp0/XmjVrFB8frzp16ujPP//U7NmzJanICdm1a1e99NJLGjNmjNq2basff/xRL774ourXr+81V8507dpVc+fOVVRUlJo1a6atW7fqn//850V/GGFYWJimTJmivn376uTJk7r33ntVpUoVHT9+XDt37tTx48fz7ckqiTFjxujTTz9V+/bt9cILL6hixYqaP3++PvvsM02cOPGidtufO3dO7777rq699loNHDiwwD4JCQn6+OOPdfz48UKvOgsPDy+VD/zL++DFwvZUZmVlacWKFZLk2KW/bt06nThxQqGhoU5X9PTr10/z5s0rds/RpEmT9MILL6hz586Kj4/Pd6jg/BA5d+5c9e/fX3PmzFG/fv0KXefbb7+tDRs2KC4uTrVr11ZmZqY2bNigKVOm6JZbbin0g9kyMjJUuXLlEh/6iIqK0lVXXaXnn39exhhVrFhRn3zyiZKTk0u0fEHi4uJ022236dlnn1VmZqaio6P19ddf67333nNpPQcPHnQ8l5mZmdq0aZMmTJigunXr6p577ily2cjIyHyHxdyhqPdXvXr1Cn2f1KxZM1/wadeundatW1fsnqMOHTrotttuU7NmzRQREaHU1FRNnDhRNptNL730UqHLZWRklOgP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+++/u3VwAAAArnI53DzzzDPKyMiQJKWmpuqpp55Sly5dtG/fPg0fPtztAwQAAHCFy98ttX//fjVu3FiSlJSUpK5du2r8+PHatm2bunTp4vYBAgAAuMLlPTdlypRRVlaWJOmLL75QXFycJKlixYqOPToAAACe4vKemzZt2mj48OFq3bq1vv32W33wwQeSpJ9++km1atVy+wABAABc4fKem6lTpyogIECLFy/WtGnTVLNmTUnSypUr1blzZ7cPEAAAwBUu77mpU6eOPv3003ztr7/+ulsGBAAAcClKFG4yMjIUERHh+H9R8voBAAB4QonCTYUKFZSWlqYqVaqofPnystls+foYY2Sz2ZSTk+P2QQIAAJRUicLNmjVrVLFiRcf/Cwo3AAAA3qBE4aZt27aO/7dr1660xgIAAHDJXL5aavTo0QUeekpPT9cDDzzglkEBAABcLJfDzbvvvqvWrVvrl19+cbStXbtWTZs21X//+193jg0AAMBlLoebXbt2qV69emrRooVmzpypZ555RnFxcerXr5/TF2oCAAB4gsufc1OuXDktWrRIo0aN0qOPPqqAgACtXLlSsbGxpTE+AAAAl7i850aSpkyZotdff10PPPCAGjRooCFDhmjnzp3uHhsAAIDLXA43d9xxh8aOHat3331X8+fP1/bt23XbbbcpJiZGEydOLI0xAgAAlJjL4ebcuXPatWuX7r33XklS2bJlNW3aNC1evJivYAAAAB7n8jk3ycnJBbbHx8crNTX1kgcEAABwKS7qnJvCVKpUyZ2rAwAAcJnLe25ycnL0+uuv68MPP9TBgwd19uxZp8dPnjzptsEBAAC4yuU9N2PHjtW//vUv3X///UpPT9fw4cN1zz33yM/PT4mJiaUwRAAAgJJzOdzMnz9fM2fO1NNPP62AgAA98MADeuedd/TCCy9o8+bNpTFGAACAEnM53Bw9elRNmzaVJIWFhSk9PV2S1LVrV3322WfuHR0AAICLXA43tWrVUlpamiSpYcOGWr16tSQpJSVFQUFB7h0dAACAi1wON3fffbf+85//SJKGDh2q0aNH6+qrr1afPn00YMAAtw8QAADAFS5fLfXKK684/n/vvfeqVq1a2rhxoxo2bKg777zTrYMDAABwlcvh5kIxMTGKiYlxx1gAAAAu2SV9iF9ERIT27dvnrrEAAABcshKHm8OHD+drM8a4dTAAAACXqsThpkmTJnrvvfdKcywAAACXrMThZvz48Ro8eLC6d++u3377TZL04IMPKiIiotQGBwAA4KoSh5vHH39cO3fu1O+//67rrrtOH3/8saZNm8aXZQIAAK/i0tVS9evX15o1azR16lR1795d1157rQICnFexbds2tw4QAADAFS5fCn7gwAElJSWpYsWK6tatW75wAwAA4EkuJZOZM2fqqaeeUocOHbR7925Vrly5tMYFAABwUUocbjp37qxvv/1WU6dOVZ8+fUpzTAAAABetxOEmJydHu3btUq1atUpzPAAAAJekxOEmOTm5NMcBAADgFpf09QsAAADehnADAAAshXADAAAshXADAAAshXADAAAshXADAAAshXADAAAshXADAAAsxWvCzYQJE2Sz2TRs2LAS9f/6668VEBCgFi1alOq4AACAb/GKcJOSkqIZM2aoWbNmJeqfnp6uPn36KDY2tpRHBgAAfI3Hw82ZM2fUq1cvzZw5UxUqVCjRMo8++qh69uypVq1alfLoAACAr/F4uBk8eLDi4+PVoUOHEvWfM2eOfvnlF40ZM6aURwYAAHxRib84szQsWrRI27ZtU0pKSon67927V88//7w2bNiggICSDT07O1vZ2dmO+xkZGZIku90uu93u+qCLkLc+d6/XW1i9Psn6NVKf77N6jdTn+0qrRlfWZzPGGLduvYQOHTqk6OhorV69Ws2bN5cktWvXTi1atNDkyZPz9c/JyVFMTIweeughDRo0SJKUmJioZcuWaceOHYVuJzExUWPHjs3XvmDBAoWEhLilFgAAULqysrLUs2dPpaenKyIiosi+Hgs3y5Yt09133y1/f39HW05Ojmw2m/z8/JSdne302KlTp1ShQgWnttzcXBlj5O/vr9WrV+v222/Pt52C9tzUrl1bJ06cKPbJcZXdbldycrI6duyowMBAt67bG1i9Psn6NVKf77N6jdTn+0qrxoyMDFWqVKlE4cZjh6ViY2OVmprq1Na/f39FRUXpueeecwoxkhQREZGv/7///W+tWbNGixcvVv369QvcTlBQkIKCgvK1BwYGltobqzTX7Q2sXp9k/Rqpz/dZvUbq833urtGVdXks3ISHh6tJkyZObaGhoYqMjHS0jxgxQv/73//07rvvys/PL1//KlWqKDg4OF87AAC4cnn8aqmipKWl6eDBg54eBgAA8CEevVrqQmvXrnW6P3fu3CL7JyYmKjExsdTGAwAAfI9X77kBAABwFeEGAABYCuEGAABYCuEGAABYCuEGAABYCuEGAABYCuEGAABYCuEGAABYCuEGAABYCuEGAABYCuEGAABYCuEGAABYCuEGAABYCuEGAABYCuEGAABYCuEGAABYCuEGAABYCuEGAABYCuEGAABYCuEGAABYCuEGAABYCuEGAABYCuEGAABYCuEGAABYCuEGAABYCuEGAABYCuEGAABYCuEGAABYCuEGAABYCuEGAABYCuEGAABYCuEGAABYCuEGAABYCuEGAABYCuEGAABYCuEGAABYCuEGAABYCuEGAABYCuEGAABYCuEGAABYCuEGAABYCuEGAABYCuEGAABYCuEGAABYCuEGAABYCuEGAABYCuEGAABYCuEGAABYCuEGAABYCuEGAABYCuEGAABYCuEGAABYCuEGAABYCuEGAABYCuEGAABYCuEGAABYiteEmwkTJshms2nYsGGF9lmyZIk6duyoypUrKyIiQq1atdLnn39++QYJAAC8nleEm5SUFM2YMUPNmjUrst/69evVsWNHrVixQlu3blX79u2VkJCg7du3X6aRAgAAbxfg6QGcOXNGvXr10syZMzVu3Lgi+06ePNnp/vjx47V8+XJ98sknuv7660txlAAAwFd4fM/N4MGDFR8frw4dOri8bG5urk6fPq2KFSuWwsgAAIAv8uiem0WLFmnbtm1KSUm5qOUnTZqkzMxM3X///YX2yc7OVnZ2tuN+RkaGJMlut8tut1/UdguTtz53r9dbWL0+yfo1Up/vs3qN1Of7SqtGV9ZnM8YYt269hA4dOqTo6GitXr1azZs3lyS1a9dOLVq0yHf4qSALFy7UwIEDtXz58iL3+iQmJmrs2LH52hcsWKCQkJCLHj8AALh8srKy1LNnT6WnpysiIqLIvh4LN8uWLdPdd98tf39/R1tOTo5sNpv8/PyUnZ3t9Nj5PvjgA/Xv318fffSR4uPji9xOQXtuateurRMnThT75LjKbrcrOTlZHTt2VGBgoFvX7Q2sXp9k/Rqpz/dZvUbq832lVWNGRoYqVapUonDjscNSsbGxSk1NdWrr37+/oqKi9NxzzxUabBYuXKgBAwZo4cKFxQYbSQoKClJQUFC+9sDAwFJ7Y5Xmur2B1euTrF8j9fk+q9dI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rVu31t69ez040pKrXr26ZsyYoaSkJC1ZskTXXHONYmNjtX79ekcfq7yGaWlpWrlypQYOHOjU7q2voTFGw4cPV5s2bdSkSZNC+/nqPCxpfRfypXlY0hp9dR5ezGvoC/MwNTVVYWFhCgoK0qBBg7R06VI1bty4wL7eNP+uuG8FL002m83pvvm/D38+v72gPhe2ebuFCxcqMTFRy5cvV5UqVRztMTExiomJcdxv3bq1brjhBk2ZMkVvvvmmJ4bqkmuuuUbXXHON436rVq106NAhvfbaa7rtttsc7VZ4DefOnavy5cvrrrvucmr31tfw73//u3bt2qWvvvqq2L6+OA9dqS+Pr83Dktboq/PwYl5DX5iH11xzjXbs2KFTp04pKSlJffv21bp16woNON4y/9hz4ybVqlXLlzyPHTumgIAARUZGFtnnwhTrzT744AM99NBD+vDDD9WhQ4ci+/r5+enGG2/0+F+MlyImJsZp/FZ4DY0xmj17tnr37q0yZcoU2dcbXsMnnnhCH3/8sb788kvVqlWryL6+OA9dqS+Pr83Di6nxfN4+Dy+mPl+Zh2XKlFHDhg0VHR2tCRMmqHnz5nrjjTcK7OtN849w4yatWrVScnKyU9vq1asVHR2twMDAIvvccsstl22cl2LhwoXq16+fFixYoPj4+GL7G2O0Y8cOVa9e/TKMrnRs377dafy+/hpKf13h8fPPP+uhhx4qtq8nX0NjjP7+979ryZIlWrNmjerXr1/sMr40Dy+mPsm35uHF1nghb52Hl1Kfr8zDgsaSnZ1d4GNeNf/cenqyhZw+fdps377dbN++3Ugy//rXv8z27dvNgQMHjDHGPP/886Z3796O/vv27TMhISHmySefNHv27DGzZs0ygYGBZvHixY4+X3/9tfH39zevvPKK+f77780rr7xiAgICzObNm72+vgULFpiAgADz1ltvmbS0NMft1KlTjj6JiYlm1apV5pdffjHbt283/fv3NwEBAeabb7657PUZ43qNr7/+ulm6dKn56aefzO7du83zzz9vJJmkpCRHH19+DfM8+OCD5uabby5wnd70Gj722GOmXLlyZu3atU7vuaysLEcfX56HF1Ofr83Di6nRl+bhxdSXxxfm4YgRI8z69evN/v37za5du8zIkSONn5+fWb16tTHGu+cf4aYQeZcjXnjr27evMcaYvn37mrZt2zots3btWnP99debMmXKmHr16plp06blW+9HH31krrnmGhMYGGiioqKcJuzl5Gp9bdu2LbK/McYMGzbM1KlTx5QpU8ZUrlzZxMXFmY0bN17ews7jao2vvvqqueqqq0xwcLCpUKGCadOmjfnss8/yrddXX0NjjDl16pQpW7asmTFjRoHr9KbXsKDaJJk5c+Y4+vjyPLyY+nxtHl5Mjb40Dy/2Peor83DAgAGmbt26jnHExsY6go0x3j3/bMb839k+AAAAFsA5NwAAwFIINwAAwFIINwAAwFIINwAAwFIINwAAwFIINwAAwFIINwAAwFIINwCuSGvXrpXNZtOpU6c8PRQAbka4AeBROTk5uuWWW9S9e3en9vT0dNWuXVv/+Mc/SmW7t9xyi9LS0lSuXLlSWT8Az+ETigF43N69e9WiRQvNmDFDvXr1kiT16dNHO3fuVEpKSrHfmgwA52PPDQCPu/rqqzVhwgQ98cQTOnLkiJYvX65FixZp3rx5hQab5557To0aNVJISIgaNGig0aNHy263S/rrm4s7dOigzp07K+/vt1OnTqlOnToaNWqUpPyHpQ4cOKCEhARVqFBBoaGhuu6667RixYrSLx6A2wV4egAAIElPPPGEli5dqj59+ig1NVUvvPCCWrRoUWj/8PBwzZ07VzVq1FBqaqoefvhhhYeH69lnn5XNZtO8efPUtGlTvfnmmxo6dKgGDRqkqlWrKjExscD1DR48WGfPntX69esVGhqqPXv2KCwsrHSKBVCqOCwFwGv88MMPuvbaa9W0aVNt27ZNAQEl//vrn//8pz744ANt2bLF0fbRRx+pd+/eGj58uN544w1t375djRo1kvTXnpv27dvr999/V/ny5dWsWTN1795dY8aMcXtdAC4vDksB8BqzZ89WSEiI9u/fr8OHD0uSBg0apLCwMMctz+LFi9WmTRtVq1ZNYWFhGj16tA4ePOi0vvvuu0/33HOPJkyYoEmTJjmCTUGGDBmicePGqXXr1hozZox27dpVOkUCKHWEGwBeYdOmTXr99de1fPlytWrVSg899JCMMXrxxRe1Y8cOx02SNm/erB49euiOO+7Qp59+qu3bt2vUqFE6e/as0zqzsrK0detW+fv7a+/evUVuf+DAgdq3b5969+6t1NRURUdHa8qUKaVVLoBSRLgB4HF//PGH+vbtq0cffVQdOnTQO++8o5SUFL399tuqUqWKGjZs6LhJ0tdff626detq1KhRio6O1tVXX60DBw7kW+9TTz0lPz8/rVy5Um+++abWrFlT5Dhq166tQYMGacmSJXrqqac0c+bMUqkXQOki3ADwuOeff165ubl69dVXJUl16tTRpEmT9Mwzz+i///1vvv4NGzbUwYMHtWjRIv3yyy968803tXTpUqc+n332mWbPnq358+erY8eOev7559W3b1/9/vvvBY5h2LBh+vzzz7V//35t27ZNa9as0bXXXuv2WgGUPk4oBuBR69atU2xsrNauXas2bdo4PdapUyedO3dOX3zxhWw2m9Njzz77rGbPnq3s7GzFx8crJiZGiYmJOnXqlI4fP66mTZtq6NChGjFihCTp3Llzat26terVq6cPPvgg3wnFTzzxhFauXKnDhw8rIiJCnTt31uuvv67IyMjL9lwAcA/CDQAAsBQOSwEAAEsh3AAAAEsh3AAAAEsh3AAAAEsh3AAAAEsh3AAAAEsh3AAAAEsh3AAAAEsh3AAAAEsh3AAAAEsh3AAAAEsh3AAAAEv5f+R8KZFDifOeAAAAAElFTkSuQmCC",
      "text/plain": [
       "<Figure size 640x480 with 1 Axes>"
      ]
     },
     "metadata": {},
     "output_type": "display_data"
    }
   ],
   "source": [
    "import matplotlib.pyplot as plt\n",
    "\n",
    "# Convert the Cartesian product to a list of points\n",
    "points = list(cartesian_product)\n",
    "x_coords = [x for x, y in points]  # Get x-coordinates\n",
    "y_coords = [y for x, y in points]  # Get y-coordinates\n",
    "\n",
    "# Plot the points on the Cartesian plane\n",
    "plt.scatter(x_coords, y_coords)  # Plot the points\n",
    "plt.title(\"Cartesian Plane\")  # Set the title of the plot\n",
    "plt.xlabel(\"X-axis\")  # Set the label for the x-axis\n",
    "plt.ylabel(\"Y-axis\")  # Set the label for the y-axis\n",
    "plt.grid(True)  # Enable grid\n",
    "plt.show()  # Display the plot\n",
    "\n",
    "points2 = list(cartesian_product2)\n",
    "x_coords2 = [x for x, y in points2]  \n",
    "y_coords2 = [y for x, y in points2]  \n",
    "\n",
    "plt.scatter(x_coords2, y_coords2)  \n",
    "plt.title(\"Cartesian Plane for A = {1, 2, 3} and B = {4, 5}\")  \n",
    "plt.xlabel(\"X-axis\")  \n",
    "plt.ylabel(\"Y-axis\")  \n",
    "plt.grid(True) \n",
    "plt.show()  \n",
    "\n",
    "# Practice: Try plotting the Cartesian product of different sets\n",
    "# Example: Use sets A and B from the previous example\n"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "32121114-08d7-4060-b837-baff62b3732c",
   "metadata": {},
   "source": [
    "### Relations\n",
    "\n",
    "A relation between two sets is a subset of the Cartesian product of those sets. It pairs elements from the first set with elements from the second set. Here is an example of a relation between two sets:\n"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 15,
   "id": "4371e044-8ea1-43d4-948a-b9331b43df6b",
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "Relation R: {(2, 4), (1, 3)}\n",
      "Relation R2: {(2, 3), (1, 4)}\n"
     ]
    }
   ],
   "source": [
    "A = {1, 2}  # Define the first set\n",
    "B = {3, 4}  # Define the second set\n",
    "\n",
    "# Define a relation as a subset of the Cartesian product\n",
    "R = {(1, 3), (2, 4)}\n",
    "print(\"Relation R:\", R)  # Print the relation\n",
    "\n",
    "R2 = {(1, 4), (2, 3)}  \n",
    "print(\"Relation R2:\", R2)  # Print the new relation\n",
    "\n",
    "# Practice: Try defining other relations and print them\n",
    "# Example: R2 = {(1, 4), (2, 3)}\n",
    "# Then print R2"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "c812d4cc-06e0-4df8-8a76-98d71777b445",
   "metadata": {},
   "source": [
    "### Functions (Mathematical Definition)\n",
    "\n",
    "In mathematics, a function is a special type of relation where each element in the domain is associated with exactly one element in the codomain. Here is how you can define a function in Python and verify its properties:\n"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 17,
   "id": "f0cfa456-3c55-47fb-b09a-fd36062bb4b6",
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "f is a function: True\n",
      "f2 is a function: False\n"
     ]
    }
   ],
   "source": [
    "def is_function(relation, domain):\n",
    "    # Check if every element in the domain has exactly one pair in the relation\n",
    "    domain_elements = [pair[0] for pair in relation]\n",
    "    return all(domain_elements.count(e) == 1 for e in domain)\n",
    "\n",
    "A = {1, 2}  # Define the domain\n",
    "B = {3, 4}  # Define the codomain\n",
    "\n",
    "# Define a function as a set of ordered pairs\n",
    "f = {(1, 3), (2, 4)}\n",
    "\n",
    "# Check if f is a function\n",
    "print(\"f is a function:\", is_function(f, A))\n",
    "\n",
    "f2 = {(1, 3), (1, 4)}  \n",
    "print(\"f2 is a function:\", is_function(f2, A))\n",
    "\n",
    "# Practice: Try defining other functions and check their properties\n",
    "# Example: f2 = {(1, 3), (1, 4)}\n",
    "# Then check is_function(f2, A)\n"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "id": "c45db932-9917-4580-876f-a812f74875be",
   "metadata": {},
   "outputs": [],
   "source": []
  }
 ],
 "metadata": {
  "kernelspec": {
   "display_name": "Python 3 (ipykernel)",
   "language": "python",
   "name": "python3"
  },
  "language_info": {
   "codemirror_mode": {
    "name": "ipython",
    "version": 3
   },
   "file_extension": ".py",
   "mimetype": "text/x-python",
   "name": "python",
   "nbconvert_exporter": "python",
   "pygments_lexer": "ipython3",
   "version": "3.12.7"
  }
 },
 "nbformat": 4,
 "nbformat_minor": 5
}




