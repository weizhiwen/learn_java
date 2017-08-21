```
package test;

import java.util.Arrays;
import java.util.List;

import org.junit.Test;



public class Test02 {
	//可变参数，要作为函数的参数必须是最后一个参数
	
	//正确写法
	public void sum1(int size, int ...nums){
		
	}
	//错误写法
	/*public void sum2(int ...nums, int size){
		
	}*/
	
	public int sum(int ...nums)
	{
		int sum = 0;
		for(int num : nums)
		{
			sum += num;
		}
		return sum;
	}
	
	@Test
	public void test01()
	{
		int[] nums1 = {1,2,3,4,5,6}; //这里不能自动装箱
		List<int[]> list1 = Arrays.asList(nums1);
		System.out.println(list1);
		Integer[] nums2 = {1,2,3,4,5,6};
		List<Integer> list2 = Arrays.asList(nums2);
		System.out.println(list2);
		System.out.println(sum(1,2,3,4,5,6));
	}
}
```
