
---
#  <======<----------->=========~===========(Bubble Sort)=============~=======<------------>==>
---
# Bubble Sort



![alt-text](https://upload.wikimedia.org/wikipedia/commons/c/c8/Bubble-sort-example-300px.gif)


![bubble sort](![](https://s3-us-west-1.amazonaws.com/appacademy-open-assets/data_structures_algorithms/naive_sorting_algorithms/bubble_sort/images/BubbleSort.gif)


This project contains a skeleton for you to implement Bubble Sort. In the
file **lib/bubble_sort.js**, you should implement the Bubble Sort. This is a
description of how the Bubble Sort works (and is also in the code file).

```
Bubble Sort: (array)
  n := length(array)
  repeat
  swapped = false
  for i := 1 to n - 1 inclusive do

      /* if this pair is out of order */
      if array[i - 1] > array[i] then

        /* swap them and remember something changed */
        swap(array, i - 1, i)
        swapped := true

      end if
    end for
  until not swapped
```

* Clone the project from
  https://github.com/appacademy-starters/algorithms-bubble-sort-starter.
* `cd` into the project folder
* `npm install` to install dependencies in the project root directory
* `npm test` to run the specs
* You can view the test cases in `/test/test.js`. Your job is to write code in
  the `/lib/bubble_sort.js` that implements the Bubble Sort.
  


---
  #  <======<---------->=======~===========(Selection Sort)============~=======<---------->=====>
---

![selection](![](https://s3-us-west-1.amazonaws.com/appacademy-open-assets/data_structures_algorithms/naive_sorting_algorithms/selection_sort/images/SelectionSort.gif)




# Selection Sort

This project contains a skeleton for you to implement Selection Sort. In the
file **lib/selection_sort.js**, you should implement the Selection Sort. You
can use the same `swap` function from Bubble Sort; however, try to implement it
on your own, first.

The algorithm can be summarized as the following:

1. Set MIN to location 0
2. Search the minimum element in the list
3. Swap with value at location MIN
4. Increment MIN to point to next element
5. Repeat until list is sorted

This is a description of how the Selection Sort works (and is also in the code
file).

```
procedure selection sort(list)
   list  : array of items
   n     : size of list

   for i = 1 to n - 1
   /* set current element as minimum*/
      min = i

      /* check the element to be minimum */

      for j = i+1 to n
         if list[j] < list[min] then
            min = j;
         end if
      end for

      /* swap the minimum element with the current element*/
      if indexMin != i  then
         swap list[min] and list[i]
      end if
   end for
end procedure
```

* Clone the project from
  https://github.com/appacademy-starters/algorithms-selection-sort-starter.
* `cd` into the project folder
* `npm install` to install dependencies in the project root directory
* `npm test` to run the specs
* You can view the test cases in `/test/test.js`. Your job is to write code in
  the `/lib/selection_sort.js` that implements the Selection Sort.




---
  #  <=======<---------->=======~=========(Insertion Sort)===========~=======<------------>=====>
---
# Insertion Sort

![insertion](https://upload.wikimedia.org/wikipedia/commons/0/0f/Insertion-sort-example-300px.gif)


![insertion](![](https://s3-us-west-1.amazonaws.com/appacademy-open-assets/data_structures_algorithms/naive_sorting_algorithms/insertion_sort/images/InsertionSort.gif)


This project contains a skeleton for you to implement Insertion Sort. In the
file **lib/insertion_sort.js**, you should implement the Insertion Sort.

The algorithm can be summarized as the following:

1. If it is the first element, it is already sorted. return 1;
2. Pick next element
3. Compare with all elements in the sorted sub-list
4. Shift all the elements in the sorted sub-list that is greater than the
   value to be sorted
5. Insert the value
6. Repeat until list is sorted

This is a description of how the Insertion Sort works (and is also in the code
file).

```
procedure insertionSort( A : array of items )
   int holePosition
   int valueToInsert

   for i = 1 to length(A) inclusive do:

      /* select value to be inserted */
      valueToInsert = A[i]
      holePosition = i

      /*locate hole position for the element to be inserted */

      while holePosition > 0 and A[holePosition-1] > valueToInsert do:
         A[holePosition] = A[holePosition-1]
         holePosition = holePosition -1
      end while

      /* insert the number at hole position */
      A[holePosition] = valueToInsert

   end for

end procedure
```

* Clone the project from
  https://github.com/appacademy-starters/algorithms-insertion-sort-starter.
* `cd` into the project folder
* `npm install` to install dependencies in the project root directory
* `npm test` to run the specs
* You can view the test cases in `/test/test.js`. Your job is to write code in
  the `/lib/insertion_sort.js` that implements the Insertion Sort.


---
  #  <=======<------------>=======~===========(Merge Sort)=============~=======<------------>=====>
---

# Merge Sort

![merge sort](https://s3-us-west-1.amazonaws.com/appacademy-open-assets/data_structures_algorithms/efficient_sorting_algorithms/merge_sort/images/MergeSort.gif)

This project contains a skeleton for you to implement Merge Sort. In the
file **lib/merge_sort.js**, you should implement the Merge Sort.

The algorithm can be summarized as the following:

1. if there is only one element in the list, it is already sorted. return that
   array.
2. otherwise, divide the list recursively into two halves until it can no more
   be divided.
3. merge the smaller lists into new list in sorted order.

This is a description of how the Merge Sort works (and is also in the code
file).

```
procedure mergesort( a as array )
   if ( n == 1 ) return a

   /* Split the array into two */
   var l1 as array = a[0] ... a[n/2]
   var l2 as array = a[n/2+1] ... a[n]

   l1 = mergesort( l1 )
   l2 = mergesort( l2 )

   return merge( l1, l2 )
end procedure

procedure merge( a as array, b as array )
   var result as array
   while ( a and b have elements )
      if ( a[0] > b[0] )
         add b[0] to the end of result
         remove b[0] from b
      else
         add a[0] to the end of result
         remove a[0] from a
      end if
   end while

   while ( a has elements )
      add a[0] to the end of result
      remove a[0] from a
   end while

   while ( b has elements )
      add b[0] to the end of result
      remove b[0] from b
   end while

   return result
end procedure
```

* Clone the project from
  https://github.com/appacademy-starters/algorithms-merge-sort-starter.
* `cd` into the project folder
* `npm install` to install dependencies in the project root directory
* `npm test` to run the specs
* You can view the test cases in `/test/test.js`. Your job is to write code in
  the `/lib/merge_sort.js` that implements the Merge Sort.

---
  #  <=======<------------>=======~===========(Quick Sort)=============~=======<------------>=====>
---


# Quick Sort


![quick sort](https://s3-us-west-1.amazonaws.com/appacademy-open-assets/data_structures_algorithms/efficient_sorting_algorithms/quick_sort/images/QuickSort.gif)

This project contains a skeleton for you to implement Quick Sort. In the
file **lib/quick_sort.js**, you should implement the Quick Sort. This is a
description of how the Quick Sort works (and is also in the code file).

```
procedure quick sort (array)
  if the length of the array is 0 or 1, return the array

  set the pivot to the first element of the array
  remove the first element of the array

  put all values less than the pivot value into an array called left
  put all values greater than the pivot value into an array called right

  call quick sort on left and assign the return value to leftSorted
  call quick sort on right and assign the return value to rightSorted

  return the concatenation of leftSorted, the pivot value, and rightSorted
end procedure quick sort
```

* Clone the project from
  https://github.com/appacademy-starters/algorithms-quick-sort-starter.
* `cd` into the project folder
* `npm install` to install dependencies in the project root directory
* `npm test` to run the specs
* You can view the test cases in `/test/test.js`. Your job is to write code in
  the `/lib/quick_sort.js` that implements the Quick Sort.




---
  #  <=======<---------->=======~===========(Binary Search)=============~=======<---------->=====>
---


# Binary Search

This project contains a skeleton for you to implement Binary Search. In the
file **lib/binary_search.js**, you should implement the Binary Search and its
cousin Binary Search Index.

The Binary Search algorithm can be summarized as the following:

1. If the array is empty, then return false
2. Check the value in the middle of the array against the target value
3. If the value is equal to the target value, then return true
4. If the value is less than the target value, then return the binary search on
   the left half of the array for the target
5. If the value is greater than the target value, then return the binary search
   on the right half of the array for the target

This is a description of how the Binary Search works (and is also in the code
file).

```
procedure binary search (list, target)
  parameter list: a list of sorted value
  parameter target: the value to search for

  if the list has zero length, then return false

  determine the slice point:
    if the list has an even number of elements,
      the slice point is the number of elements
      divided by two
    if the list has an odd number of elements,
      the slice point is the number of elements
      minus one divided by two

  create an list of the elements from 0 to the
    slice point, not including the slice point,
    which is known as the "left half"
  create an list of the elements from the
    slice point to the end of the list which is
    known as the "right half"

  if the target is less than the value in the
    original array at the slice point, then
    return the binary search of the "left half"
    and the target
  if the target is greater than the value in the
    original array at the slice point, then
    return the binary search of the "right half"
    and the target
  if neither of those is true, return true
end procedure binary search
```

Then you need to adapt that to return _the index_ of the found item rather than
a Boolean value. The pseudocode is also in the code file.

```
procedure binary search index(list, target, low, high)
  parameter list: a list of sorted value
  parameter target: the value to search for
  parameter low: the lower index for the search
  parameter high: the upper index for the search

  if low is equal to high, then return -1 to indicate
    that the value was not found

  determine the slice point:
    if the list has an even number of elements,
      the slice point is the number of elements
      divided by two
    if the list has an odd number of elements,
      the slice point is the number of elements
      minus one divided by two

  if the target is less than the value in the
    original array at the slice point, then
    return the binary search of the array,
    the target, low, and the slice point
  if the target is greater than the value in the
    original array at the slice point, then return
    the binary search of the array, the target,
    the slice point plus one, and high
  if neither of those is true, return true
end procedure binary search index
```


* Clone the project from
  https://github.com/appacademy-starters/algorithms-binary-search-starter.
* `cd` into the project folder
* `npm install` to install dependencies in the project root directory
* `npm test` to run the specs
* You can view the test cases in `/test/test.js`. Your job is to write code in
  the `/lib/binary_search.js` that implements the Binary Search and Binary
  Search Index.
