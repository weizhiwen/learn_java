```java
package test;
import java.util.Arrays;

/**
 * 数组工具类Arrays测试
 */
import org.junit.Test;

public class Test04 {
	@Test 
	//填充遍历数组
	public void test1()
	{
		int[] i = new int[3];
		Arrays.fill(i, 2);
		for(int x : i)
		{
			System.out.println(x);
		}
	}
	
	@Test
	//复制数组
	public void test2()
	{
		int[] i = {1,2,3,4,5,6};
		int[] j = new int[5];
		System.arraycopy(i, 2, j, 2, 3);
		for(int x : j)
		{
			System.out.println(x);
		}
	}
	
	@Test
	//toString和deepToString
	public void test3()
	{
		int[] i = {1,2,3,4,5,6};
		int[][] j = {{1,1,1},{2,2,2}};
		System.out.println(Arrays.toString(i));
		System.out.println(Arrays.deepToString(j));
	}
	
	@Test
	//一维数组比较
	public void test4()
	{
		int[] a = new int[3];
		Arrays.fill(a, 1);
		int[] b = new int[3];
		Arrays.fill(b, 1);
		int[] c = new int[3];
		Arrays.fill(c, 2);
		int[] d = a;
		System.out.println(a.equals(d)); //比较数组名的引用
		System.out.println(a.equals(b)); 
		System.out.println(a.equals(c));
		System.out.println(Arrays.equals(a, b)); //比较数组的内容
		System.out.println(Arrays.equals(a, c));
	}
	
	@Test
	//二维数组比较
	public void test5()
	{
		int[][] a = {{1,1,1},{2,2,2},{3,3,3}};
		int[][] b = {{1,1,1},{2,2,2},{3,3,3}};
		int[][] c = {{1,2,3},{1,2,3},{1,2,3}};
		System.out.println(a.equals(b));
		System.out.println(a.equals(c));
		System.out.println(Arrays.equals(a, b));
		System.out.println(Arrays.equals(a, c));
		System.out.println(Arrays.deepEquals(a, b)); //二维数组要用deepEquals方法比较
		System.out.println(Arrays.deepEquals(a, c));
	}
	
	@Test
	//数组排序
	public void test6()
	{
		int[] a = {2,4,1,5,3,4,0};
		System.out.println(Arrays.toString(a));
		Arrays.sort(a); //升序
		System.out.println(Arrays.toString(a));
	}
	
	@Test
	//一维数组检索，二分查找
	public void test7()
	{
		int[] a = {2,4,1,5,3,4,0};
		Arrays.sort(a); //查找之前要先进行排序
		int index1 = Arrays.binarySearch(a, 1);
		int index2 = Arrays.binarySearch(a, 3);
		int index3 = Arrays.binarySearch(a, 4);
		System.out.println("index1="+index1+", index2="+index2+", index3="+index3);
	}
}

```