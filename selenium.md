driver.Manage().Window.Maximize();

## Wait 
  WebDriverWait wait = new WebDriverWait(_driver, TimeSpan.FromSeconds(50));
  IWebElement elm =.Until(                            SeleniumExtras.WaitHelpers.ExpectedConditions.ElementIsVisible(
                            By.CssSelector("css.....")));


## Scroll to Elemnt
    //using OpenQA.Selenium.Interactions;
     Actions act = new Actions(_driver);
    act.MoveToElement(elm).Perform();
    
    
## Execut javascript 
 ((IJavaScriptExecutor) _driver).ExecuteScript("$(\".css\").hide();");
 
## Send Keys
    c#
     IWebElement  html = _driver.FindElement(By.TagName("html"));
                    html.SendKeys(Keys.PageDown);


    Java
       WebElement html = driver.findElement(By.tagName("html"));
                html.sendKeys(Keys.chord(Keys.PAGE_DOWN));
