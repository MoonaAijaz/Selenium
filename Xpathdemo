package day24;

import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.chrome.ChromeDriver;

public class XPathDemo {

	public static void main(String[] args) {
		
		WebDriver driver=new ChromeDriver();

		driver.get("https://demo.opencart.com/");
		driver.manage().window().maximize();
		
		//Xpath with single attribute
			//driver.findElement(By.xpath("//input[@placeholder='Search']")).sendKeys("TShirts");
	
		//Xpath with multiple attributes
		 //driver.findElement(By.xpath("//input[@name='search'][@placeholder='Search']")).sendKeys("Tshirts");
		 
		//xpath with 'and'  'or'  operator
		
		//driver.findElement(By.xpath("//input[@name='search' and @placeholder='Search']")).sendKeys("Tshirts");
		//driver.findElement(By.xpath("//input[@name='search' or @placeholder='xyz']")).sendKeys("Tshirts");
		
		//xpath with text() - inner text
		
		//driver.findElement(By.xpath("//*[text()='MacBook']")).click();
		//https://demo.opencart.com/
		/*boolean displaystatus=driver.findElement(By.xpath("//h3[text()='Featured']")).isDisplayed();
		System.out.println(displaystatus);
		
		String value=driver.findElement(By.xpath("//h3[text()='Featured']")).getText();
		System.out.println(value);
		*/
		
		
			
			
		//xpath with contains()
		//Search
			
		//driver.findElement(By.xpath("//input[contains(@placeholder,'Sea')]")).sendKeys("Tshirts");
		
		//xpath with start-with()
		//driver.findElement(By.xpath("//input[starts-with(@placeholder,'Sea')]")).sendKeys("Tshirts");
		
		
		
			//chianed xpath
		 boolean status=driver.findElement(By.xpath("//div[@id='logo']/a/img")).isDisplayed();
		System.out.println(status);
		
		
		
		
	}

}
