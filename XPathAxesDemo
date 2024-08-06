package day24;

import java.util.List;

import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.chrome.ChromeDriver;

public class XPathAxesDemo {

	public static void main(String[] args) {
			WebDriver driver=new ChromeDriver();
		
		driver.get("https://money.rediff.com/gainers/bse/daily/groupa");
		driver.manage().window().maximize();
		
		//Self  - Selects the current node
		String text=driver.findElement(By.xpath("//a[contains(text(),'Zomato')]/self::a")).getText();
		System.out.println("Self : "+ text); //Zomato
		
		
		//Parent - Selects the parent of the current node (always One)
		text=driver.findElement(By.xpath("//a[contains(text(),'Zomato')]/parent::td")).getText();// there is no text for parent, so it is same value display
		System.out.println("Parent : "+text);  //Zomato
		
		//Child - Selects all children of the current node (One or many)
		List<WebElement> childs=driver.findElements(By.xpath("//a[contains(text(),'Zomato')]/ancestor::tr/child::td"));
		System.out.println("Number of child elements:"+childs.size());//5
		
		//Ancestor - Selects all ancestors (parent, grandparent, etc.) 
		text=driver.findElement(By.xpath("//a[contains(text(),'Zomato')]/ancestor::tr")).getText();
		System.out.println("Ancestor : "+text);
		
		//Descendant - Selects all descendants (children, grandchildren, etc.) of the current node
		List<WebElement> descendants=driver.findElements(By.xpath("//a[contains(text(),'Zomato')]/ancestor::tr/descendant::*"));
		System.out.println("Number of descendant nodes:"+descendants.size()); //7
		
		//Following -Selects everything in the document after the closing tag of the current node
		List<WebElement>followingnodes=driver.findElements(By.xpath("//a[contains(text(),'Zomato')]/ancestor::tr/following::tr"));
		System.out.println("Number of following nodes:"+followingnodes.size()); //398
		
		//Preceding - Selects all nodes that appear before the current node in the document
		List<WebElement> precedings=driver.findElements(By.xpath("//a[contains(text(),'Zomato')]/ancestor::tr/preceding::tr"));
		System.out.println("Number of preceding nodes:"+precedings.size()); //41
		
		//Following-sibling : Selects all siblings after the current node
		List<WebElement> followingsiblings=driver.findElements(By.xpath("//a[contains(text(),'Zomato')]/ancestor::tr/following-sibling::tr"));
		System.out.println("Number of Following Siblings:"+followingsiblings.size());  //396
				
				
		//preceding-sibling - Selects all siblings before the current node
		List<WebElement> precedingsiblings=driver.findElements(By.xpath("//a[contains(text(),'Zomato')]/ancestor::tr/preceding-sibling::tr"));
		System.out.println("Number of preceding sibling nodes:"+precedingsiblings.size()); //40
		
		driver.quit();

	}

}
