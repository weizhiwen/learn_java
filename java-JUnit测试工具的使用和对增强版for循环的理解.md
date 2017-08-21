```
package test;


import java.util.ArrayList;
import java.util.List;

import org.junit.After;
import org.junit.AfterClass;
import org.junit.Before;
import org.junit.BeforeClass;
import org.junit.Test;

public class Test01 {
	//JUnit测试框架使用
	@BeforeClass
	public static void beforeClass()
	{
		System.out.println("Test01这个类加载时被调用");
	}
	
	@Before
	public void before()
	{
		System.out.println("每个方法被执行前调用");
	}
	
	//增強版的for循环测试，只适合取数据，不能改变数据的值，增强版for循环的局限性
	@Test
	public void test1()
	{
		int[] arr = {1,2,3};
		for(int num : arr)
		{
			System.out.println(num);
		}
	}
	
	@Test
	public void test2()
	{
		List<String> list = new ArrayList<String>();
		list.add("1");
		list.add("2");
		list.add("3");
		for(Object obj : list)
		{
			System.out.println(obj);
		}
	}
	
	@After
	public void after()
	{
		System.out.println("每个方法被执行后调用");
	}
	
	@AfterClass
	public static void afterClass()
	{
		System.out.println("该类被销毁时调用");
	}
}

```


![image.png](http://upload-images.jianshu.io/upload_images/5763525-6ea84a639ed90ac0.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

