# WebDTest
Learling WebDriver
package drivers;

import java.util.List;

import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.firefox.FirefoxDriver;
import org.openqa.selenium.support.ui.Select;


public class WebD {

	public static void main(String[] args) {
	
		
			     WebDriver driver = new FirefoxDriver();
			     driver.get("http://www.priceline.com/");
			     
			     driver.findElement(By.xpath("//*[@id='tab-flights']")).click();
			     
			     List <WebElement> rb = driver.findElements(By.xpath("//*[@type='radio']"));
			     System.out.println(rb.size());
			     
			     rb.get(2).click();
			     
			     driver.findElement(By.xpath("//*[@id='vacation-type-AHC-button']/label")).click();
			     
			     driver.findElement(By.xpath("//*[@id='vacation-orig']")).click();
			     driver.findElement(By.xpath("//*[@id='vacation-orig']")).sendKeys("DCA");
			     driver.findElement(By.xpath("//*[@id='vacation-dest']")).click();
			     driver.findElement(By.xpath("//*[@id='vacation-dest']")).sendKeys("SFO");
			     
			     driver.findElement(By.xpath("//*[@id='vacation-ts']")).click();
			     driver.findElement(By.xpath("//*[@id='vacation-ts']")).sendKeys("11/25/2015");
			     driver.findElement(By.xpath("//*[@id='vacation-te']")).click();
			     driver.findElement(By.xpath("//*[@id='vacation-te']")).sendKeys("11/29/2015");
 			     
			     WebElement rm = driver.findElement(By.xpath("//*[@id='vacation-rooms']"));
			     Select rmt = new Select(rm);
			     
			     System.out.println(rm.getSize()); 
			     
			     rmt.selectByVisibleText("6 Rooms"); //Selecting Number of rooms 
			     

			     WebElement ps = driver.findElement(By.xpath("//*[@id='vacation-adults']"));
			     Select psg = new Select(ps);
			     
			     
			     psg.selectByValue("5"); //Selecting Number of Passenger
			     
			     WebElement ch = driver.findElement(By.xpath("//*[@id='vacation-children']"));
			     Select chl = new Select(ch);
			     
			     
			     chl.selectByIndex(6); //Selecting Number of Children
			     
			   //  driver.findElement(By.xpath("//*[@id='vac-btn-retl']")).click();
			     
//			     Close the browser
//			     driver.quit();
	     }
	}
	



