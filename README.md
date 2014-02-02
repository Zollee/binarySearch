binarySearch
============

二分查找
//written in Java;
//仅适用于数组有序时；


	public static void main(String[] args)
	{
		int[] arr = {9, 14, 24, 35, 44, 77, 90};
		int index = binarySearch(arr, 77);
		System.out.println("index=" + index);
	}
	
	
	
	public static int binarySearch(int[] arr, int key)
	{
		int min, max, mid;
		min = 0;
		max = arr.length -1;
		
		while(min <= max)
		{
			//获取中间脚标，进行元素比较，以确定新的查找范围
			mid = (max + min)/2;
			if(key > arr[mid])
				min = mid + 1;
			else if(key < arr[mid])
				max = mid -1;
			else
				return mid;
		}
		return -1;
	}

