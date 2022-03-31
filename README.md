# Sorting-Algorithms-

code : 
#include<iostream>
#include<ctime>
#include<cstdlib>
#include <bits/stdc++.h>
#include <sys/time.h>
using namespace std;
class sorte{
	public:
		int arr[50],arr2[100],arr3[200],arr4[300],arr5[400],arr6[500],arr7[1000];
	public:
		void fillarray(int n)
		{
			if(n==50)
			{
				for(int i=0; i<50; i++)
				{
					int check =0;
					int temp = (rand() %(1000 - 0 + 1)) + 0;
					for(int j=0; j<i; j++)
					{
						if(temp == arr[j])
						{
							i--;
							check = 1;
									break;
						}
					}
					if(check == 0)
					{
						arr[i] = temp;
					}
				}
			}
			if(n==100)
			{
				for(int i=0; i<100; i++)
				{
					int check =0;
					int temp = (rand() %(1000 - 0 + 1)) + 0;
					for(int j=0; j<i; j++)
					{
						if(temp == arr2[j])
						{
							i--;
							check = 1;
							break;
						}
					}
					if(check == 0)
					{
						arr2[i] = temp;
					}
				}
			}
			if(n==200)
			{
				for(int i=0; i<200; i++)
				{
					int check =0;
					int temp = (rand() %(1000 - 0 + 1)) + 0;
					for(int j=0; j<i; j++)
					{
						if(temp == arr3[j])
						{
							i--;
							check = 1;
							break;
						}
					}
					if(check == 0)
					{
						arr3[i] = temp;
					}
				}
			}
			if(n==300)
			{
				for(int i=0; i<300; i++)
				{
					int check =0;
					int temp = (rand() %(1000 - 0 + 1)) + 0;
					for(int j=0; j<i; j++)
					{
						if(temp == arr4[j])
						{
							i--;
							check = 1;
							break;
						}
					}
					if(check == 0)
					{
						arr4[i] = temp;
					}
				}
			}
			if(n==400)
			{
				for(int i=0; i<400; i++)
				{
					int check =0;
					int temp = (rand() %(1000 - 0 + 1)) + 0;
					for(int j=0; j<i; j++)
					{
						if(temp == arr5[j])
						{
							i--;
							check = 1;
							break;
						}
					}
					if(check == 0)
					{
						arr5[i] = temp;
					}
				}
			}
			if(n==500)
			{
				for(int i=0; i<500; i++)
				{
					int check =0;
					int temp = (rand() %(1000 - 0 + 1)) + 0;
					for(int j=0; j<i; j++)
					{
						if(temp == arr6[j])
						{
							i--;
							check = 1;
							break;
						}
					}
					if(check == 0)
					{
						arr6[i] = temp;
					}
				}	
			}
			if(n==1000)
			{
				for(int i=0; i<1000; i++)
				{
					int check =0;
					int temp = (rand() %(1000 - 0 + 1)) + 0;
					for(int j=0; j<i; j++)
					{
						if(temp == arr7[j])
						{
							i--;
							check = 1;
							break;
						}
					}
					if(check == 0)
					{
						arr7[i] = temp;
					}
				}
			}
		}
		void display(int n)
		{
			if(n==50)
			{
				cout<<endl<<"Array of 50 : "<<endl;
				for(int i =0; i<50; i++)
					cout<<arr[i]<<" ";
			}
			if(n==100)
			{
				cout<<endl<<"Array of 100 : "<<endl;
				for(int i =0; i<100; i++)
					cout<<arr2[i]<<" ";
			}
			if(n==200)
			{
				cout<<endl<<"Array of 200 : "<<endl;
				for(int i =0; i<200; i++)
					cout<<arr3[i]<<" ";
			}
			if(n==300)
			{
				cout<<endl<<"Array of 300 : "<<endl;
				for(int i =0; i<300; i++)
					cout<<arr4[i]<<" ";
			}
			if(n==400)
			{
				cout<<endl<<"Array of 400 : "<<endl;
				for(int i =0; i<400; i++)
					cout<<arr5[i]<<" ";
			}
			if(n==500)
			{
				cout<<endl<<"Array of 500 : "<<endl;
				for(int i =0; i<500; i++)
					cout<<arr6[i]<<" ";
			}
			if(n==1000)
			{
				cout<<endl<<"Array of 1000 : "<<endl;
				for(int i =0; i<1000; i++)
					cout<<arr7[i]<<" ";
			}
		}
		void insertionSort(int arra[],int n)
		{
		    	int i, key, j;
			    for (i = 1; i < n; i++)
			    {
			        key = arra[i];
			        j = i - 1;
			        while (j >= 0 && arra[j] > key)
			        {
			            arra[j + 1] = arra[j];
			            j = j - 1;
			        }
			        arra[j + 1] = key;
			    }
		}
		void merge(int array[], int const left, int const mid, int const right)
		{
		    int const subArrayOne = mid - left + 1;
		    int const subArrayTwo = right - mid;
		    int *leftArray = new int[subArrayOne],
		         *rightArray = new int[subArrayTwo];
		    for (int i = 0; i < subArrayOne; i++)
		        leftArray[i] = array[left + i];
		    for (int j = 0; j < subArrayTwo; j++)
		        rightArray[j] = array[mid + 1 + j];
		  
		    int indexOfSubArrayOne = 0,
		        indexOfSubArrayTwo = 0;
		    int indexOfMergedArray = left;
		    while (indexOfSubArrayOne < subArrayOne && indexOfSubArrayTwo < subArrayTwo) {
		        if (leftArray[indexOfSubArrayOne] <= rightArray[indexOfSubArrayTwo]) {
		            array[indexOfMergedArray] = leftArray[indexOfSubArrayOne];
		            indexOfSubArrayOne++;
		        }
		        else {
		            array[indexOfMergedArray] = rightArray[indexOfSubArrayTwo];
		            indexOfSubArrayTwo++;
		        }
		        indexOfMergedArray++;
		    }
		    while (indexOfSubArrayOne < subArrayOne) {
		        array[indexOfMergedArray] = leftArray[indexOfSubArrayOne];
		        indexOfSubArrayOne++;
		        indexOfMergedArray++;
		    }
		    while (indexOfSubArrayTwo < subArrayTwo) {
		        array[indexOfMergedArray] = rightArray[indexOfSubArrayTwo];
		        indexOfSubArrayTwo++;
		        indexOfMergedArray++;
		    }
		}
		void mergeSort(int array[], int const begin, int const end)
		{
		    if (begin >= end)
		        return;
		  
		    int mid = begin + (end - begin) / 2;
		    mergeSort(array, begin, mid);
		    mergeSort(array, mid + 1, end);
		    merge(array, begin, mid, end);
		}
		void swap(int* a, int* b)
		{
		    int t = *a;
		    *a = *b;
		    *b = t;
		}
		int partition4 (int arra[], int low, int high)////Quick sort 4 has some issue
		{
			insertionSort(arra,high+1);
			int med = arra[high/2]*14;
		    int pivot = med+56;
		    int i = (low - 1);
		    for (int j = low; j <= high - 1; j++)
		    {
		        if (arra[j] < pivot)
		        {
		            i++;
		            swap(&arra[i], &arra[j]);
		        }
		    }
		    swap(&arra[i + 1], &arra[high]);
		    return (i + 1);
		}
		int partition3 (int arra[], int low, int high)/////quick sort 3 has some issue
		{
			insertionSort(arra,high+1);
			int med = arra[high/2];
			fillarray(high);
		    int pivot = med;
		    int i = (low - 1);
		    for (int j = low; j <= high - 1; j++)
		    {
		        if (arra[j] < pivot)
		        {
		            i++;
		            swap(&arra[i], &arra[j]);
		        }
		    }
		    swap(&arra[i + 1], &arra[high]);
		    return (i + 1);
		}
		int partition2 (int arra[], int low, int high)
		{
			int num = (rand() %(high - 0 + 1)) + 0;
		    int pivot = num;
		    int i = (low - 1);
		    for (int j = low; j <= high - 1; j++)
		    {
		        if (arra[j] < pivot)
		        {
		            i++;
		            swap(&arra[i], &arra[j]);
		        }
		    }
		    swap(&arra[i + 1], &arra[high]);
		    return (i + 1);
		}
		int partition1 (int arra[], int low, int high)
		{
		    int pivot = arra[high/2];
		    int i = (low - 1);
		    for (int j = low; j <= high - 1; j++)
		    {
		        if (arra[j] < pivot)
		        {
		            i++;
		            swap(&arra[i], &arra[j]);
		        }
		    }
		    swap(&arra[i + 1], &arra[high]);
		    return (i + 1);
		}
		void quickSort(int arra[], int low, int high,int n)
		{
		    if (low < high)
		    {
		    	int pi;
		    	if(n==1)
		    	{
		    		pi = partition1(arra, low, high);
				}
		        if(n==2)
		    	{
		    		pi = partition2(arra, low, high);
				}
				if(n==3)
		    	{
		    		pi = partition3(arra, low, high);
				}
				if(n==4)
		    	{
		    		pi = partition4(arra, low, high);
				}
		        quickSort(arra, low, pi - 1,n);
		        quickSort(arra, pi + 1, high,n);
		    }
		}
		void caltime(int n)
		{
			if(n==50)
			{
				double ct[6];
				for(int i=0; i<6; i++)
				{
					if(i==0)
					{
					    fillarray(n);
						struct timespec start, end;
					    clock_gettime(CLOCK_MONOTONIC, &start);
					    ios_base::sync_with_stdio(false);
					    insertionSort(arr,n);
					    clock_gettime(CLOCK_MONOTONIC, &end);
					    ct[i] = (end.tv_sec - start.tv_sec) * 1e9;
					    ct[i] = (ct[i] + (end.tv_nsec - start.tv_nsec)) * 1e-9;
					    cout << "Time taken by program is : " << fixed
					         << ct[i] << setprecision(9);
					    cout << " sec" << endl;
					}
					if(i==1)
					{
						fillarray(n);
						struct timespec start, end;
					    clock_gettime(CLOCK_MONOTONIC, &start);
					    ios_base::sync_with_stdio(false);
					    mergeSort(arr,0,n-1);
					    cout<<"blabla";
					    clock_gettime(CLOCK_MONOTONIC, &end);
					    ct[i] = (end.tv_sec - start.tv_sec) * 1e9;
					    ct[i] = (ct[i] + (end.tv_nsec - start.tv_nsec)) * 1e-9;
					    cout << "Time taken by program is : " << fixed
					         << ct[i] << setprecision(9);
					    cout << " sec" << endl;
					}
					if(i==2)
					{
						fillarray(n);
						struct timespec start, end;
					    clock_gettime(CLOCK_MONOTONIC, &start);
					    ios_base::sync_with_stdio(false);
					    quickSort(arr,0,n-1,1);
					    clock_gettime(CLOCK_MONOTONIC, &end);
					    double time_taken;
					    ct[i] = (end.tv_sec - start.tv_sec) * 1e9;
					    ct[i] = (ct[i] + (end.tv_nsec - start.tv_nsec)) * 1e-9;
					    cout << "Time taken by program is : " << fixed
					         << ct[i] << setprecision(9);
					    cout << " sec" << endl;
					}
					if(i==3)
					{
						fillarray(n);
						struct timespec start, end;
					    clock_gettime(CLOCK_MONOTONIC, &start);
					    ios_base::sync_with_stdio(false);
					    quickSort(arr7,0,n-1,2);
					    clock_gettime(CLOCK_MONOTONIC, &end);
					    ct[i] = (end.tv_sec - start.tv_sec) * 1e9;
					    ct[i] = (ct[i] + (end.tv_nsec - start.tv_nsec)) * 1e-9;
					    cout << "Time taken by program is : " << fixed
					         << ct[i] << setprecision(9);
					    cout << " sec" << endl;
					}
					if(i==4)
					{
						fillarray(n);
						struct timespec start, end;
					    clock_gettime(CLOCK_MONOTONIC, &start);
					    ios_base::sync_with_stdio(false);
					    quickSort(arr7,0,n-1,3);
					    clock_gettime(CLOCK_MONOTONIC, &end);
					    ct[i] = (end.tv_sec - start.tv_sec) * 1e9;
					    ct[i] = (ct[i] + (end.tv_nsec - start.tv_nsec)) * 1e-9;
					    cout << "Time taken by program is : " << fixed
					         << ct[i] << setprecision(9);
					    cout << " sec" << endl;
					}
					if(i==5)
					{
						fillarray(n);
						struct timespec start, end;
					    clock_gettime(CLOCK_MONOTONIC, &start);
					    ios_base::sync_with_stdio(false);
					    quickSort(arr7,0,n-1,4);
					    clock_gettime(CLOCK_MONOTONIC, &end);
					    ct[i] = (end.tv_sec - start.tv_sec) * 1e9;
					    ct[i] = (ct[i] + (end.tv_nsec - start.tv_nsec)) * 1e-9;
					    cout << "Time taken by program is : " << fixed
					         << ct[i] << setprecision(9);
					    cout << " sec" << endl;
					}
				}
				for(int i =0; i <6; i++)
				{
					if(i==0)
					{
						cout<<endl<<"time by insertion in "<<n<<" elements : "<<ct[i]<<endl;
					}
					if(i==1)
					{
						cout<<endl<<"time by merge sort in "<<n<<" elements : "<<ct[i]<<endl;
					}
					if(i==2)
					{
						cout<<endl<<"time by Quick Sort I in "<<n<<" elements : "<<ct[i]<<endl;
					}
					if(i==3)
					{
						cout<<endl<<"time by Quick Sort II in "<<n<<" elements : "<<ct[i]<<endl;
					}
					if(i==4)
					{
						cout<<endl<<"time by Quick Sort III in "<<n<<" elements : "<<ct[i]<<endl;
					}
					if(i==4)
					{
						cout<<endl<<"time by Quick Sort IIII "<<n<<" elements : "<<ct[i]<<endl;
					}
				}
			}
			if(n==100)
			{
				double ct[6];
				for(int i=0; i<6; i++)
				{
					if(i==0)
					{
					    fillarray(n);
						struct timespec start, end;
					    clock_gettime(CLOCK_MONOTONIC, &start);
					    ios_base::sync_with_stdio(false);
					    insertionSort(arr2,n);
					    clock_gettime(CLOCK_MONOTONIC, &end);
					    ct[i] = (end.tv_sec - start.tv_sec) * 1e9;
					    ct[i] = (ct[i] + (end.tv_nsec - start.tv_nsec)) * 1e-9;
					    cout << "Time taken by program is : " << fixed
					         << ct[i] << setprecision(9);
					    cout << " sec" << endl;
					}
					if(i==1)
					{
						fillarray(n);
						struct timespec start, end;
					    clock_gettime(CLOCK_MONOTONIC, &start);
					    ios_base::sync_with_stdio(false);
					    mergeSort(arr2,0,n-1);
					    clock_gettime(CLOCK_MONOTONIC, &end);
					    ct[i] = (end.tv_sec - start.tv_sec) * 1e9;
					    ct[i] = (ct[i] + (end.tv_nsec - start.tv_nsec)) * 1e-9;
					    cout << "Time taken by program is : " << fixed
					         << ct[i] << setprecision(9);
					    cout << " sec" << endl;
					}
					if(i==2)
					{
						fillarray(n);
						struct timespec start, end;
					    clock_gettime(CLOCK_MONOTONIC, &start);
					    ios_base::sync_with_stdio(false);
					    quickSort(arr2,0,n-1,1);
					    clock_gettime(CLOCK_MONOTONIC, &end);
					    double time_taken;
					    ct[i] = (end.tv_sec - start.tv_sec) * 1e9;
					    ct[i] = (ct[i] + (end.tv_nsec - start.tv_nsec)) * 1e-9;
					    cout << "Time taken by program is : " << fixed
					         << ct[i] << setprecision(9);
					    cout << " sec" << endl;
					}
					if(i==3)
					{
						fillarray(n);
						struct timespec start, end;
					    clock_gettime(CLOCK_MONOTONIC, &start);
					    ios_base::sync_with_stdio(false);
					    quickSort(arr7,0,n-1,2);
					    clock_gettime(CLOCK_MONOTONIC, &end);
					    ct[i] = (end.tv_sec - start.tv_sec) * 1e9;
					    ct[i] = (ct[i] + (end.tv_nsec - start.tv_nsec)) * 1e-9;
					    cout << "Time taken by program is : " << fixed
					         << ct[i] << setprecision(9);
					    cout << " sec" << endl;
					}
					if(i==4)
					{
						fillarray(n);
						struct timespec start, end;
					    clock_gettime(CLOCK_MONOTONIC, &start);
					    ios_base::sync_with_stdio(false);
					    quickSort(arr7,0,n-1,3);
					    clock_gettime(CLOCK_MONOTONIC, &end);
					    ct[i] = (end.tv_sec - start.tv_sec) * 1e9;
					    ct[i] = (ct[i] + (end.tv_nsec - start.tv_nsec)) * 1e-9;
					    cout << "Time taken by program is : " << fixed
					         << ct[i] << setprecision(9);
					    cout << " sec" << endl;
					}
					if(i==5)
					{
						fillarray(n);
						struct timespec start, end;
					    clock_gettime(CLOCK_MONOTONIC, &start);
					    ios_base::sync_with_stdio(false);
					    quickSort(arr7,0,n-1,4);
					    clock_gettime(CLOCK_MONOTONIC, &end);
					    ct[i] = (end.tv_sec - start.tv_sec) * 1e9;
					    ct[i] = (ct[i] + (end.tv_nsec - start.tv_nsec)) * 1e-9;
					    cout << "Time taken by program is : " << fixed
					         << ct[i] << setprecision(9);
					    cout << " sec" << endl;
					}
				}
				for(int i =0; i <6; i++)
				{
					if(i==0)
					{
						cout<<endl<<"time by insertion in "<<n<<" elements : "<<ct[i]<<endl;
					}
					if(i==1)
					{
						cout<<endl<<"time by merge sort in "<<n<<" elements : "<<ct[i]<<endl;
					}
					if(i==2)
					{
						cout<<endl<<"time by Quick Sort I in "<<n<<" elements : "<<ct[i]<<endl;
					}
					if(i==3)
					{
						cout<<endl<<"time by Quick Sort II in "<<n<<" elements : "<<ct[i]<<endl;
					}
					if(i==4)
					{
						cout<<endl<<"time by Quick Sort III in "<<n<<" elements : "<<ct[i]<<endl;
					}
					if(i==4)
					{
						cout<<endl<<"time by Quick Sort IIII "<<n<<" elements : "<<ct[i]<<endl;
					}
				}
			}
			if(n==200)
			{
				double ct[6];
				for(int i=0; i<6; i++)
				{
					if(i==0)
					{
					    fillarray(n);
						struct timespec start, end;
					    clock_gettime(CLOCK_MONOTONIC, &start);
					    ios_base::sync_with_stdio(false);
					    insertionSort(arr3,n);
					    clock_gettime(CLOCK_MONOTONIC, &end);
					    ct[i] = (end.tv_sec - start.tv_sec) * 1e9;
					    ct[i] = (ct[i] + (end.tv_nsec - start.tv_nsec)) * 1e-9;
					    cout << "Time taken by program is : " << fixed
					         << ct[i] << setprecision(9);
					    cout << " sec" << endl;
					}
					if(i==1)
					{
						fillarray(n);
						struct timespec start, end;
					    clock_gettime(CLOCK_MONOTONIC, &start);
					    ios_base::sync_with_stdio(false);
					    mergeSort(arr3,0,n-1);
					    clock_gettime(CLOCK_MONOTONIC, &end);
					    ct[i] = (end.tv_sec - start.tv_sec) * 1e9;
					    ct[i] = (ct[i] + (end.tv_nsec - start.tv_nsec)) * 1e-9;
					    cout << "Time taken by program is : " << fixed
					         << ct[i] << setprecision(9);
					    cout << " sec" << endl;
					}
					if(i==2)
					{
						fillarray(n);
						struct timespec start, end;
					    clock_gettime(CLOCK_MONOTONIC, &start);
					    ios_base::sync_with_stdio(false);
					    quickSort(arr3,0,n-1,1);
					    clock_gettime(CLOCK_MONOTONIC, &end);
					    double time_taken;
					    ct[i] = (end.tv_sec - start.tv_sec) * 1e9;
					    ct[i] = (ct[i] + (end.tv_nsec - start.tv_nsec)) * 1e-9;
					    cout << "Time taken by program is : " << fixed
					         << ct[i] << setprecision(9);
					    cout << " sec" << endl;
					}
					if(i==3)
					{
						fillarray(n);
						struct timespec start, end;
					    clock_gettime(CLOCK_MONOTONIC, &start);
					    ios_base::sync_with_stdio(false);
					    quickSort(arr7,0,n-1,2);
					    clock_gettime(CLOCK_MONOTONIC, &end);
					    ct[i] = (end.tv_sec - start.tv_sec) * 1e9;
					    ct[i] = (ct[i] + (end.tv_nsec - start.tv_nsec)) * 1e-9;
					    cout << "Time taken by program is : " << fixed
					         << ct[i] << setprecision(9);
					    cout << " sec" << endl;
					}
					if(i==4)
					{
						fillarray(n);
						struct timespec start, end;
					    clock_gettime(CLOCK_MONOTONIC, &start);
					    ios_base::sync_with_stdio(false);
					    quickSort(arr7,0,n-1,3);
					    clock_gettime(CLOCK_MONOTONIC, &end);
					    ct[i] = (end.tv_sec - start.tv_sec) * 1e9;
					    ct[i] = (ct[i] + (end.tv_nsec - start.tv_nsec)) * 1e-9;
					    cout << "Time taken by program is : " << fixed
					         << ct[i] << setprecision(9);
					    cout << " sec" << endl;
					}
					if(i==5)
					{
						fillarray(n);
						struct timespec start, end;
					    clock_gettime(CLOCK_MONOTONIC, &start);
					    ios_base::sync_with_stdio(false);
					    quickSort(arr7,0,n-1,4);
					    clock_gettime(CLOCK_MONOTONIC, &end);
					    ct[i] = (end.tv_sec - start.tv_sec) * 1e9;
					    ct[i] = (ct[i] + (end.tv_nsec - start.tv_nsec)) * 1e-9;
					    cout << "Time taken by program is : " << fixed
					         << ct[i] << setprecision(9);
					    cout << " sec" << endl;
					}
				}
				for(int i =0; i <6; i++)
				{
					if(i==0)
					{
						cout<<endl<<"time by insertion in "<<n<<" elements : "<<ct[i]<<endl;
					}
					if(i==1)
					{
						cout<<endl<<"time by merge sort in "<<n<<" elements : "<<ct[i]<<endl;
					}
					if(i==2)
					{
						cout<<endl<<"time by Quick Sort I in "<<n<<" elements : "<<ct[i]<<endl;
					}
					if(i==3)
					{
						cout<<endl<<"time by Quick Sort II in "<<n<<" elements : "<<ct[i]<<endl;
					}
					if(i==4)
					{
						cout<<endl<<"time by Quick Sort III in "<<n<<" elements : "<<ct[i]<<endl;
					}
					if(i==4)
					{
						cout<<endl<<"time by Quick Sort IIII "<<n<<" elements : "<<ct[i]<<endl;
					}
				}
			}
			if(n==300)
			{
				double ct[6];
				for(int i=0; i<6; i++)
				{
					if(i==0)
					{
					    fillarray(n);
						struct timespec start, end;
					    clock_gettime(CLOCK_MONOTONIC, &start);
					    ios_base::sync_with_stdio(false);
					    insertionSort(arr4,n);
					    clock_gettime(CLOCK_MONOTONIC, &end);
					    ct[i] = (end.tv_sec - start.tv_sec) * 1e9;
					    ct[i] = (ct[i] + (end.tv_nsec - start.tv_nsec)) * 1e-9;
					    cout << "Time taken by program is : " << fixed
					         << ct[i] << setprecision(9);
					    cout << " sec" << endl;
					}
					if(i==1)
					{
						fillarray(n);
						struct timespec start, end;
					    clock_gettime(CLOCK_MONOTONIC, &start);
					    ios_base::sync_with_stdio(false);
					    mergeSort(arr4,0,n-1);
					    clock_gettime(CLOCK_MONOTONIC, &end);
					    ct[i] = (end.tv_sec - start.tv_sec) * 1e9;
					    ct[i] = (ct[i] + (end.tv_nsec - start.tv_nsec)) * 1e-9;
					    cout << "Time taken by program is : " << fixed
					         << ct[i] << setprecision(9);
					    cout << " sec" << endl;
					}
					if(i==2)
					{
						fillarray(n);
						struct timespec start, end;
					    clock_gettime(CLOCK_MONOTONIC, &start);
					    ios_base::sync_with_stdio(false);
					    quickSort(arr4,0,n-1,1);
					    clock_gettime(CLOCK_MONOTONIC, &end);
					    double time_taken;
					    ct[i] = (end.tv_sec - start.tv_sec) * 1e9;
					    ct[i] = (ct[i] + (end.tv_nsec - start.tv_nsec)) * 1e-9;
					    cout << "Time taken by program is : " << fixed
					         << ct[i] << setprecision(9);
					    cout << " sec" << endl;
					}
					if(i==3)
					{
						fillarray(n);
						struct timespec start, end;
					    clock_gettime(CLOCK_MONOTONIC, &start);
					    ios_base::sync_with_stdio(false);
					    quickSort(arr7,0,n-1,2);
					    clock_gettime(CLOCK_MONOTONIC, &end);
					    ct[i] = (end.tv_sec - start.tv_sec) * 1e9;
					    ct[i] = (ct[i] + (end.tv_nsec - start.tv_nsec)) * 1e-9;
					    cout << "Time taken by program is : " << fixed
					         << ct[i] << setprecision(9);
					    cout << " sec" << endl;
					}
					if(i==4)
					{
						fillarray(n);
						struct timespec start, end;
					    clock_gettime(CLOCK_MONOTONIC, &start);
					    ios_base::sync_with_stdio(false);
					    quickSort(arr7,0,n-1,3);
					    clock_gettime(CLOCK_MONOTONIC, &end);
					    ct[i] = (end.tv_sec - start.tv_sec) * 1e9;
					    ct[i] = (ct[i] + (end.tv_nsec - start.tv_nsec)) * 1e-9;
					    cout << "Time taken by program is : " << fixed
					         << ct[i] << setprecision(9);
					    cout << " sec" << endl;
					}
					if(i==5)
					{
						fillarray(n);
						struct timespec start, end;
					    clock_gettime(CLOCK_MONOTONIC, &start);
					    ios_base::sync_with_stdio(false);
					    quickSort(arr7,0,n-1,4);
					    clock_gettime(CLOCK_MONOTONIC, &end);
					    ct[i] = (end.tv_sec - start.tv_sec) * 1e9;
					    ct[i] = (ct[i] + (end.tv_nsec - start.tv_nsec)) * 1e-9;
					    cout << "Time taken by program is : " << fixed
					         << ct[i] << setprecision(9);
					    cout << " sec" << endl;
					}
				}
				for(int i =0; i <6; i++)
				{
					if(i==0)
					{
						cout<<endl<<"time by insertion in "<<n<<" elements : "<<ct[i]<<endl;
					}
					if(i==1)
					{
						cout<<endl<<"time by merge sort in "<<n<<" elements : "<<ct[i]<<endl;
					}
					if(i==2)
					{
						cout<<endl<<"time by Quick Sort I in "<<n<<" elements : "<<ct[i]<<endl;
					}
					if(i==3)
					{
						cout<<endl<<"time by Quick Sort II in "<<n<<" elements : "<<ct[i]<<endl;
					}
					if(i==4)
					{
						cout<<endl<<"time by Quick Sort III in "<<n<<" elements : "<<ct[i]<<endl;
					}
					if(i==4)
					{
						cout<<endl<<"time by Quick Sort IIII "<<n<<" elements : "<<ct[i]<<endl;
					}
				}
			}
			if(n==400)
			{
				double ct[6];
				for(int i=0; i<6; i++)
				{
					if(i==0)
					{
					    fillarray(n);
						struct timespec start, end;
					    clock_gettime(CLOCK_MONOTONIC, &start);
					    ios_base::sync_with_stdio(false);
					    insertionSort(arr5,n);
					    clock_gettime(CLOCK_MONOTONIC, &end);
					    ct[i] = (end.tv_sec - start.tv_sec) * 1e9;
					    ct[i] = (ct[i] + (end.tv_nsec - start.tv_nsec)) * 1e-9;
					    cout << "Time taken by program is : " << fixed
					         << ct[i] << setprecision(9);
					    cout << " sec" << endl;
					}
					if(i==1)
					{
						fillarray(n);
						struct timespec start, end;
					    clock_gettime(CLOCK_MONOTONIC, &start);
					    ios_base::sync_with_stdio(false);
					    mergeSort(arr5,0,n-1);
					    clock_gettime(CLOCK_MONOTONIC, &end);
					    ct[i] = (end.tv_sec - start.tv_sec) * 1e9;
					    ct[i] = (ct[i] + (end.tv_nsec - start.tv_nsec)) * 1e-9;
					    cout << "Time taken by program is : " << fixed
					         << ct[i] << setprecision(9);
					    cout << " sec" << endl;
					}
					if(i==2)
					{
						fillarray(n);
						struct timespec start, end;
					    clock_gettime(CLOCK_MONOTONIC, &start);
					    ios_base::sync_with_stdio(false);
					    quickSort(arr5,0,n-1,1);
					    clock_gettime(CLOCK_MONOTONIC, &end);
					    double time_taken;
					    ct[i] = (end.tv_sec - start.tv_sec) * 1e9;
					    ct[i] = (ct[i] + (end.tv_nsec - start.tv_nsec)) * 1e-9;
					    cout << "Time taken by program is : " << fixed
					         << ct[i] << setprecision(9);
					    cout << " sec" << endl;
					}
					if(i==3)
					{
						fillarray(n);
						struct timespec start, end;
					    clock_gettime(CLOCK_MONOTONIC, &start);
					    ios_base::sync_with_stdio(false);
					    quickSort(arr7,0,n-1,2);
					    clock_gettime(CLOCK_MONOTONIC, &end);
					    ct[i] = (end.tv_sec - start.tv_sec) * 1e9;
					    ct[i] = (ct[i] + (end.tv_nsec - start.tv_nsec)) * 1e-9;
					    cout << "Time taken by program is : " << fixed
					         << ct[i] << setprecision(9);
					    cout << " sec" << endl;
					}
					if(i==4)
					{
						fillarray(n);
						struct timespec start, end;
					    clock_gettime(CLOCK_MONOTONIC, &start);
					    ios_base::sync_with_stdio(false);
					    quickSort(arr7,0,n-1,3);
					    clock_gettime(CLOCK_MONOTONIC, &end);
					    ct[i] = (end.tv_sec - start.tv_sec) * 1e9;
					    ct[i] = (ct[i] + (end.tv_nsec - start.tv_nsec)) * 1e-9;
					    cout << "Time taken by program is : " << fixed
					         << ct[i] << setprecision(9);
					    cout << " sec" << endl;
					}
					if(i==5)
					{
						fillarray(n);
						struct timespec start, end;
					    clock_gettime(CLOCK_MONOTONIC, &start);
					    ios_base::sync_with_stdio(false);
					    quickSort(arr7,0,n-1,4);
					    clock_gettime(CLOCK_MONOTONIC, &end);
					    ct[i] = (end.tv_sec - start.tv_sec) * 1e9;
					    ct[i] = (ct[i] + (end.tv_nsec - start.tv_nsec)) * 1e-9;
					    cout << "Time taken by program is : " << fixed
					         << ct[i] << setprecision(9);
					    cout << " sec" << endl;
					}
				}
				for(int i =0; i <6; i++)
				{
					if(i==0)
					{
						cout<<endl<<"time by insertion in "<<n<<" elements : "<<ct[i]<<endl;
					}
					if(i==1)
					{
						cout<<endl<<"time by merge sort in "<<n<<" elements : "<<ct[i]<<endl;
					}
					if(i==2)
					{
						cout<<endl<<"time by Quick Sort I in "<<n<<" elements : "<<ct[i]<<endl;
					}
					if(i==3)
					{
						cout<<endl<<"time by Quick Sort II in "<<n<<" elements : "<<ct[i]<<endl;
					}
					if(i==4)
					{
						cout<<endl<<"time by Quick Sort III in "<<n<<" elements : "<<ct[i]<<endl;
					}
					if(i==4)
					{
						cout<<endl<<"time by Quick Sort IIII "<<n<<" elements : "<<ct[i]<<endl;
					}
				}
			}
			if(n==500)
			{
				double ct[6];
				for(int i=0; i<6; i++)
				{
					if(i==0)
					{
					    fillarray(n);
						struct timespec start, end;
					    clock_gettime(CLOCK_MONOTONIC, &start);
					    ios_base::sync_with_stdio(false);
					    insertionSort(arr6,n);
					    clock_gettime(CLOCK_MONOTONIC, &end);
					    ct[i] = (end.tv_sec - start.tv_sec) * 1e9;
					    ct[i] = (ct[i] + (end.tv_nsec - start.tv_nsec)) * 1e-9;
					    cout << "Time taken by program is : " << fixed
					         << ct[i] << setprecision(9);
					    cout << " sec" << endl;
					}
					if(i==1)
					{
						fillarray(n);
						struct timespec start, end;
					    clock_gettime(CLOCK_MONOTONIC, &start);
					    ios_base::sync_with_stdio(false);
					    mergeSort(arr6,0,n-1);
					    clock_gettime(CLOCK_MONOTONIC, &end);
					    ct[i] = (end.tv_sec - start.tv_sec) * 1e9;
					    ct[i] = (ct[i] + (end.tv_nsec - start.tv_nsec)) * 1e-9;
					    cout << "Time taken by program is : " << fixed
					         << ct[i] << setprecision(9);
					    cout << " sec" << endl;
					}
					if(i==2)
					{
						fillarray(n);
						struct timespec start, end;
					    clock_gettime(CLOCK_MONOTONIC, &start);
					    ios_base::sync_with_stdio(false);
					    quickSort(arr6,0,n-1,1);
					    clock_gettime(CLOCK_MONOTONIC, &end);
					    double time_taken;
					    ct[i] = (end.tv_sec - start.tv_sec) * 1e9;
					    ct[i] = (ct[i] + (end.tv_nsec - start.tv_nsec)) * 1e-9;
					    cout << "Time taken by program is : " << fixed
					         << ct[i] << setprecision(9);
					    cout << " sec" << endl;
					}
					if(i==3)
					{
						fillarray(n);
						struct timespec start, end;
					    clock_gettime(CLOCK_MONOTONIC, &start);
					    ios_base::sync_with_stdio(false);
					    quickSort(arr7,0,n-1,2);
					    clock_gettime(CLOCK_MONOTONIC, &end);
					    ct[i] = (end.tv_sec - start.tv_sec) * 1e9;
					    ct[i] = (ct[i] + (end.tv_nsec - start.tv_nsec)) * 1e-9;
					    cout << "Time taken by program is : " << fixed
					         << ct[i] << setprecision(9);
					    cout << " sec" << endl;
					}
					if(i==4)
					{
						fillarray(n);
						struct timespec start, end;
					    clock_gettime(CLOCK_MONOTONIC, &start);
					    ios_base::sync_with_stdio(false);
					    quickSort(arr7,0,n-1,3);
					    clock_gettime(CLOCK_MONOTONIC, &end);
					    ct[i] = (end.tv_sec - start.tv_sec) * 1e9;
					    ct[i] = (ct[i] + (end.tv_nsec - start.tv_nsec)) * 1e-9;
					    cout << "Time taken by program is : " << fixed
					         << ct[i] << setprecision(9);
					    cout << " sec" << endl;
					}
					if(i==5)
					{
						fillarray(n);
						struct timespec start, end;
					    clock_gettime(CLOCK_MONOTONIC, &start);
					    ios_base::sync_with_stdio(false);
					    quickSort(arr7,0,n-1,4);
					    clock_gettime(CLOCK_MONOTONIC, &end);
					    ct[i] = (end.tv_sec - start.tv_sec) * 1e9;
					    ct[i] = (ct[i] + (end.tv_nsec - start.tv_nsec)) * 1e-9;
					    cout << "Time taken by program is : " << fixed
					         << ct[i] << setprecision(9);
					    cout << " sec" << endl;
					}
				}
				for(int i =0; i <6; i++)
				{
					if(i==0)
					{
						cout<<endl<<"time by insertion in "<<n<<" elements : "<<ct[i]<<endl;
					}
					if(i==1)
					{
						cout<<endl<<"time by merge sort in "<<n<<" elements : "<<ct[i]<<endl;
					}
					if(i==2)
					{
						cout<<endl<<"time by Quick Sort I in "<<n<<" elements : "<<ct[i]<<endl;
					}
					if(i==3)
					{
						cout<<endl<<"time by Quick Sort II in "<<n<<" elements : "<<ct[i]<<endl;
					}
					if(i==4)
					{
						cout<<endl<<"time by Quick Sort III in "<<n<<" elements : "<<ct[i]<<endl;
					}
					if(i==4)
					{
						cout<<endl<<"time by Quick Sort IIII "<<n<<" elements : "<<ct[i]<<endl;
					}
				}
			}
			if(n==1000)
			{
				double ct[6];
				for(int i=0; i<6; i++)
				{
					if(i==0)
					{
					    fillarray(n);
						struct timespec start, end;
					    clock_gettime(CLOCK_MONOTONIC, &start);
					    ios_base::sync_with_stdio(false);
					    insertionSort(arr7,n);
					    clock_gettime(CLOCK_MONOTONIC, &end);
					    ct[i] = (end.tv_sec - start.tv_sec) * 1e9;
					    ct[i] = (ct[i] + (end.tv_nsec - start.tv_nsec)) * 1e-9;
					    cout << "Time taken by program is : " << fixed
					         << ct[i] << setprecision(9);
					    cout << " sec" << endl;
					}
					if(i==1)
					{
						fillarray(n);
						struct timespec start, end;
					    clock_gettime(CLOCK_MONOTONIC, &start);
					    ios_base::sync_with_stdio(false);
					    mergeSort(arr7,0,n-1);
					    clock_gettime(CLOCK_MONOTONIC, &end);
					    ct[i] = (end.tv_sec - start.tv_sec) * 1e9;
					    ct[i] = (ct[i] + (end.tv_nsec - start.tv_nsec)) * 1e-9;
					    cout << "Time taken by program is : " << fixed
					         << ct[i] << setprecision(9);
					    cout << " sec" << endl;
					}
					if(i==2)
					{
						fillarray(n);
						struct timespec start, end;
					    clock_gettime(CLOCK_MONOTONIC, &start);
					    ios_base::sync_with_stdio(false);
					    quickSort(arr7,0,n-1,1);
					    clock_gettime(CLOCK_MONOTONIC, &end);
					    double time_taken;
					    ct[i] = (end.tv_sec - start.tv_sec) * 1e9;
					    ct[i] = (ct[i] + (end.tv_nsec - start.tv_nsec)) * 1e-9;
					    cout << "Time taken by program is : " << fixed
					         << ct[i] << setprecision(9);
					    cout << " sec" << endl;
					}
					if(i==3)
					{
						fillarray(n);
						struct timespec start, end;
					    clock_gettime(CLOCK_MONOTONIC, &start);
					    ios_base::sync_with_stdio(false);
					    quickSort(arr7,0,n-1,2);
					    clock_gettime(CLOCK_MONOTONIC, &end);
					    ct[i] = (end.tv_sec - start.tv_sec) * 1e9;
					    ct[i] = (ct[i] + (end.tv_nsec - start.tv_nsec)) * 1e-9;
					    cout << "Time taken by program is : " << fixed
					         << ct[i] << setprecision(9);
					    cout << " sec" << endl;
					}
					if(i==4)
					{
						fillarray(n);
						struct timespec start, end;
					    clock_gettime(CLOCK_MONOTONIC, &start);
					    ios_base::sync_with_stdio(false);
					    quickSort(arr7,0,n-1,3);
					    clock_gettime(CLOCK_MONOTONIC, &end);
					    ct[i] = (end.tv_sec - start.tv_sec) * 1e9;
					    ct[i] = (ct[i] + (end.tv_nsec - start.tv_nsec)) * 1e-9;
					}
					if(i==5)
					{
						fillarray(n);
						struct timespec start, end;
					    clock_gettime(CLOCK_MONOTONIC, &start);
					    ios_base::sync_with_stdio(false);
					    quickSort(arr7,0,n-1,4);
					    clock_gettime(CLOCK_MONOTONIC, &end);
					    ct[i] = (end.tv_sec - start.tv_sec) * 1e9;
					    ct[i] = (ct[i] + (end.tv_nsec - start.tv_nsec)) * 1e-9;
					    cout << "Time taken by program is : " << fixed
					         << ct[i] << setprecision(9);
					    cout << " sec" << endl;
					}
				}
				for(int i =0; i <6; i++)
				{
					if(i==0)
					{
						cout<<endl<<"time by insertion in "<<n<<" elements : "<<ct[i]<<endl;
					}
					if(i==1)
					{
						cout<<endl<<"time by merge sort in "<<n<<" elements : "<<ct[i]<<endl;
					}
					if(i==2)
					{
						cout<<endl<<"time by Quick Sort I in "<<n<<" elements : "<<ct[i]<<endl;
					}
					if(i==3)
					{
						cout<<endl<<"time by Quick Sort II in "<<n<<" elements : "<<ct[i]<<endl;
					}
					if(i==4)
					{
						cout<<endl<<"time by Quick Sort III in "<<n<<" elements : "<<ct[i]<<endl;
					}
					if(i==4)
					{
						cout<<endl<<"time by Quick Sort IIII "<<n<<" elements : "<<ct[i]<<endl;
					}
				}
			}
		}
};
using namespace std;
int main(){
    srand(time(0));
	sorte obj;
	obj.caltime(1000);
	obj.caltime(500);
	obj.caltime(400);
	obj.caltime(300);
	obj.caltime(200);
	obj.caltime(100);
	obj.caltime(50);
	obj.display(1000);
	return 0;
}
