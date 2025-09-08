### CS525 - Advanced Database Organization<br>
### Assignment 1 - Storage Manager

Team Members<br>
Meghana Rabba                   A20572009<br>
Rohan Singh Rajendra Singh      A20572007<br>

This assignment implements the functionalities of the store manager.It supports creating,opening,reading,writing,closing,,destroying and managing page files<br>

Let's walk through the functions.<br>

-->FILE OPERATIONS<br>
createPageFile - creates a new page that's currently not existing<br>
openPageFile - opens an existing file and initializes teh handle<br>
closePageFile - closes the page and frees up the resources<br>
destroyPageFile - deletes the make from the storage<br>

-->READING OPERATIONS<br>
readBlock - reads a specific file from the memory,includes all the error message implementations so that all the other functions can be wrapped around this function.<br>
getBlockPos - returns the position of current page in the file<br>
readFirstBlock - reads the first page in the file<br>
readCurrentBlock - reads the current page in the file<br>
readPreviousBlock - reads the previous page in the file<br>
readNextBlock - reads the next page in the file<br>
readLastBlock - reads teh last page of the file<br>

-->WRITING OPERATIONS
writeBlock - writes a block to a specific page<br>
writeCurrentBlock - writes to the current block<br>
appendEmptyBlock - appends an empty page at the end of the file<br>
ensureCapacity - ensures that the file has a minimum number of pages<br>


To run the test cases follow the below steps in terminal<br>
->make clean<br>
->make <br>
->make run<br>

I have generated a couple of test cases to have 3 sub-testcases for each function implemented.It is stored in test_storage_functions.c file<br>

--> to test the code with testcases in test_storage_functions.c<br>
  -> change the line "SRCS = test_assign1_1.c storage_mgr.c dberror.c" in Makefile to "SRCS = test_storage_functions.c storage_mgr.c dberror.c"<br>
  ->follow the above method to run the test cases.<br>


This is the screenshot of the files 20 lines of the output of test cases in test_assign1_1.c file<br>
<img width="1962" height="820" alt="image" src="https://github.com/user-attachments/assets/e820d006-e4db-4270-aa68-d0918d6cc422" />

This is the screenshot of the last 20 lines of the output of test cases in test_assign1_1.c file<br>
<img width="1910" height="780" alt="image" src="https://github.com/user-attachments/assets/f6cb9923-4a05-4fb3-ab6b-6819bd0c10a1" />


