package pack;
import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.firefox.FirefoxDriver;
import org.openqa.selenium.support.ui.Select;

public class Sample {

	public static void main(String[] args) {
		// TODO Auto-generated method stub

		WebDriver driver = new FirefoxDriver();
		driver.get("https://edit.europe.yahoo.com/registration");
		driver.manage().window().maximize();
		/*String title = driver.getTitle();
		System.out.println(title);
		String url = driver.getCurrentUrl();
		System.out.println(url);
		driver.close();*/
		WebElement ele = driver.findElement(By.id("country-lang"));
		Select sel = new Select(ele);
		sel.selectByVisibleText("English (India)");
		driver.findElement(By.id("first-name")).sendKeys("sankar");
		driver.findElement(By.id("last-name")).sendKeys("A");
		driver.findElement(By.id("user-name")).sendKeys("sankar.arivarasu");
		driver.findElement(By.id("password")).sendKeys("google123");
		driver.findElement(By.id("mobile")).sendKeys("9789474001");
		WebElement mon = driver.findElement(By.id("month"));
		Select mont = new Select(mon);
		mont.selectByIndex(1);
		WebElement dat = driver.findElement(By.id("day"));
		Select date = new Select(dat);
		date.selectByValue("16");
		WebElement yr = driver.findElement(By.id("year"));
		Select year = new Select(yr);
		year.selectByValue("1988");
		driver.findElement(By.id("male")).click();
		driver.findElement(By.id("mobile-rec")).sendKeys("9442631448");
		driver.findElement(By.id("relationship")).sendKeys("Brother");
		driver.findElement(By.className("submit")).click();
		
		
	}

}

