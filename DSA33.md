1. For an array containing 100 elements, provide the number of steps the
   following operations would take:

   The array would look something like [1, 2, 3, 4, 5, 6, 7, 8, 9...100]

   Note that an Array allows for repetition of elements. Strictly speaking, an array is homogenous (it only allows data of one data type, unlike Python's list)

   a. Reading
   b. Searching for a value not contained within the array
   c. Insertion at the beginning of the array
   d. Insertion at the end of the array
   e. Deletion at the beginning of the array
   f. Deletion at the end of the array

- Answer:
 - a, To read means to check a particular index to see if a particular value exists in that array. Random Access is the defining feature of an array, given an index, the computer computes the address directly (base_address + (index \(*\) element_size)) and reads it in 1 (step), don't be disturb by the address computation, we don't count it as a step, it is assumed, we only count the operations that manipulate data not the operations that compute addresses directly. That is 1 step, regardless of array size. The number of steps it would take would be **1 (one)**.

 - b, To search means to check if a value exists in that array.
Let's say we are searching for the value **33**, and **it is not** there, you have to check **every element** before concluding it's absent. So the answer is **100 steps**, the full array. Generalizing, it would be **N** steps.

 - c. Insertion means putting something into that array. If we are to insert at the beginning of the array, it would take us the whole count of the elements of the array and 1 (one) step to insert into that array; that is, 100 + 1 steps (100 steps to move each element to the right, starting from 100, and 1 step to do the insertion at the beginning.) [1, 2, 3, ..., 100] remember the value 1 has its index at 0 (array index counting,) the value 100 therefore has its index at 99, value 100 shifts to index 100 to create space for insertion at the index where value 1 is at. Value 1 will be at index 1 after the 100 shifts to the right. Generalizing it would be **N + 1**

 - d. Insertion at the end of that array is done in a single step as the computer memory can get to the last index of the array in 1 (one) step. 

 - e. Deletion means to remove a value from an array. If we are to delete at the beginning of the array, it would take us 1 step to delete that value at the beginning index and 99 steps to fill up each space to the left, starting from the empty space after deletion. In total, 100 steps. Generalizing, it would take **N** steps.

 - f. Deletion at the end of the array would take just **1 (one)** step, as locating the last element's position is done in one step.



2. For an array-based set containing 100 elements, provide the number of
   steps the following operations would take:

   Note: A array-based set only allows for one unique data (no duplicates.) We use array-based set to help you accommodate your understanding of set in Python and it not being indexable, albeit, in the computer hardware, a set is indexable.

   a. Reading
   b. Searching for a value not contained within the array
   c. Insertion of a new value at the beginning of the set
   d. Insertion of a new value at the end of the set
   e. Deletion at the beginning of the set
   f. Deletion at the end of the set

- Answer:
 - a, Reading in a set is the same as reading in an array. It takes just **1 (one)** step to read (check the value of an index.)

 - b. Searching for a value not contained within the array would take **N** steps, where **N** is the total elements in the set. With 100 elements and the value absent, it takes 100 steps, the full set, before concluding it doesn't exist.

 - c. Insertion of a new value at the beginning of the set would take, firstly, **N** steps in searching to ensure that the element about to be inserted is not already in the set, and then it would take **N** steps to shift the elements to the right to make space for the new element, and then in **1 (one)** step it writes (inserts) the new element. That is **2N + 1** steps in total.

 - d. Insertion of a new value at the end of the set would take, firstly, **N** steps in searching to ensure that the element about to be inserted is not already in the set, and then **1 (one)** step to write (insert) the value into at the end of the set. **N + 1** steps in total.

 - e. Deletion at the beginning of the set would take **1 (one)** step to delete the value and **99 (ninety-nine) steps** to shift the remaining elements to the left. 1 removal + 99 shifts = 100 steps total, which is **N**.

 - f. Deletion at the end of the set will take **1 (one)** step. The last element's position is computed as part of the operation, and removing it takes 1 step, no shifting required.



3. Normally the search operation in an array looks for the first instance of a given value. But sometimes we may want to look for every instance of a given value. For example, say we want to count how many times the value “apple” is found inside an array. How many steps would it take to find all the “apples”? Give your answer in terms of N.

- Answer:
 - The total number of steps it would take to find all the "apples" in an array would take **N** steps. As we would need to search the whole array from index 0 up to index N-1 or index 1 up to index N, inclusive if the array is 1-indexed.


### Why Algorithms Matter
1. How many steps would it take to perform a linear search for the number **8** in the ordered array, [2, 4, 6, 8, 10, 12, 13]?

- Answer:
 - It would take 4 steps to linear search for the number 8 in the ordered array.

2. How many steps would binary search take for the previous example?

- Answer:
 - It would take 1 step to binary search for the number 8 ordered array.

3. What is the maximum number of steps it would take to perform a binary
search on an array of size 100,000?

- Answer:
 - It would take 17 steps to perform a binary search on an array of size 100,000. N.B: For a binary search, the steps increase by 1 for every time the size doubles and crosses a power of 2, e.g 2 = 1 step, 4 = 2 steps, 8 = 3 steps, e.t.c


