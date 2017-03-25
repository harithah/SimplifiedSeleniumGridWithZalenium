# SimplifiedSeleniumGridWithZalenium

Comming soon.......

Simplifying Selenium grid using Zalenium. This uses docker.
Instead of assigning and registering nodes using docker or having to setup docker compose with the port in yml, Zalenium provides as easier way to setup the nodes.
We can run our Selenium tests in parallel just by changing the Webdriver to RemoteDriver.
protected static WebDriver startDriver() {
        DesiredCapabilities desiredCapabilities = new DesiredCapabilities();
        desiredCapabilities.setBrowserName("firefox");
        WebDriver driver = null;
        try {
            driver= new RemoteWebDriver(new URL(DOCKER_SELENIUM_URL),desiredCapabilities);
        } catch (MalformedURLException e) {
            e.printStackTrace();
        }
        return driver;
}

Live preview of nodes available at:
http://localhost:4444/grid/admin/live
