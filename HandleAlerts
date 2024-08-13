package day30;

import org.openqa.selenium.Alert;
import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.chrome.ChromeDriver;

public class HnadleAlerts {

	public static void main(String[] args) throws InterruptedException {
		
		WebDriver driver=new ChromeDriver();
		
		driver.get("https://the-internet.herokuapp.com/javascript_alerts");
		driver.manage().window().maximize();
		
		//1) Normal alert with OK button
		/*driver.findElement(By.xpath("//button[normalize-space()='Click for JS Alert']")).click(); // opens alert box
		Thread.sleep(5000);
		
		//Alert myalert=driver.switchTo().alert();
		//myalert.accept();
		driver.switchTo().alert().accept();
		*/
		
		//2) confirmation Alert - OK & Cancel
		//driver.findElement(By.xpath("//button[normalize-space()='Click for JS Confirm']")).click();// opens alert
		//Thread.sleep(5000);
		
		//driver.switchTo().alert().accept();  // close alert window using OK button
		//driver.switchTo().alert().dismiss();  // close alert window using Cancel button
		
		//3) Prompt alert- Input box 
		
		driver.findElement(By.xpath("//button[normalize-space()='Click for JS Prompt']")).click(); //opens alert
		Thread.sleep(5000);
		
		
		Alert myalert=driver.switchTo().alert();
			
		
		System.out.println("Text msg on alert:"+myalert.getText()); //I am a JS prompt
		
		myalert.sendKeys("John");
		myalert.accept();
		
		String res=driver.findElement(By.xpath("//p[@id='result']")).getText();
		
		if(res.contains("John"))
		{
			System.out.println("test passed");
		}
		else
		{
			System.out.println("test failed");
		}
		
		
	}

}
