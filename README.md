# xmlselectiontable
Table design template
MobileElement elem = (MobileElement) driver.findElement(By.id(“loginButton”));

	org.openqa.selenium.Point point = elem.getCenter();
	int centerx = point.getX();
	int centerY = point.getY();
	
	File scrFile = ((TakesScreenshot)driver).getScreenshotAs(OutputType.FILE);
	
	 BufferedImage image = ImageIO.read(scrFile);
	  // Getting pixel color by position x and y 
	  int clr=  image.getRGB(centerx,centerY); 
	  int  red   = (clr & 0x00ff0000) >> 16;
	  int  green = (clr & 0x0000ff00) >> 8;
	  int  blue  =  clr & 0x000000ff;
	  System.out.println("Red Color value = "+ red);
	  System.out.println("Green Color value = "+ green);
	  System.out.println("Blue Color value = "+ blue);
