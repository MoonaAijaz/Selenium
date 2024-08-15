package day32;

import java.time.Duration;

import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.chrome.ChromeDriver;

public class StaticTable {

	public static void main(String[] args) {
	
		
		WebDriver driver =new ChromeDriver();
		driver.manage().timeouts().implicitlyWait(Duration.ofSeconds(10));
		
		driver.get("https://testautomationpractice.blogspot.com/");
		driver.manage().window().maximize();
		
		//1) find total number of rows in a table
		int rows=driver.findElements(By.xpath("//table[@name='BookTable']//tr")).size(); //multiple table
		//int rows=driver.findElements(By.tagName("tr")).size();  // single table
		
		System.out.println("Number of rows:"+rows);  //7
		
		//2) find total number of columns in a table
		
		int cols=driver.findElements(By.xpath("//table[@name='BookTable']//th")).size(); //multiple tables
		//int cols=driver.findElements(By.tagName("th")).size();  //single table
					
		System.out.println("Number of columsn is:"+cols); //4
		
		//3) Read data from specific row and column (ex: 5th row and 1st colum)
		//String bookName=driver.findElement(By.xpath("//table[@name='BookTable']//tr[5]//td[1]")).getText();
		//System.out.println(bookName);  //Master In Selenium
		
		//4) read data from all the rows and colums
		
		/*System.out.println("BookName"+"\t"+"Author"+"\t"+"Subject"+"\t"+"Price");
		
		for(int r=2;r<=rows;r++)
		{
			for(int c=1;c<=cols;c++)
			{
			String value=driver.findElement(By.xpath("//table[@name='BookTable']//tr["+r+"]//td["+c+"]")).getText();
			System.out.print(value+"\t");
			}
			System.out.println();
		}
		
		*/
		
		
		//5) Print book names whose author is Mukesh
		
		/*for(int r=2;r<=rows;r++)
		{
			String authorName=driver.findElement(By.xpath("//table[@name='BookTable']//tr["+r+"]//td[2]")).getText();
			
			if(authorName.equals("Mukesh"))
			{
				String bookName=driver.findElement(By.xpath("//table[@name='BookTable']//tr["+r+"]//td[1]")).getText();
				System.out.println(bookName+"\t"+authorName);
			}
			
		}
		*/
		
		//6) Find total price of all the books
		
		int total=0;
		for(int r=2;r<=rows;r++)
		{
			String price=driver.findElement(By.xpath("//table[@name='BookTable']//tr["+r+"]//td[4]")).getText();
			total=total+Integer.parseInt(price);
			
		}
		
		System.out.println("Total Price of the books:"+total); //7100

	}

}
