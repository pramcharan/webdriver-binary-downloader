
# WebDriver Binary Downloader #

WebDriver Binary Downloader conveniently downloads and configures the latest driver binaries needed for Selenium Web Driver tests with zero configuration.

## Key Features
- **Always have the latest driver binaries**as soon as its released.
- **Zero configuration**required.
- **Windows, MacOS and Linux**supported (32 bit and 64 bit)
- **Latest driver binaries**are automatically downloaded and unpacked.
- **Older driver binaries**can be automatically downloaded and unpacked.
- **All driver binaries are cached**for quicker configuration.

## Requirements
- Java 8

## Installation

#### Repository: [jcenter](https://bintray.com/bintray/jcenter?filterByPkgName=webdriver-binary-downloader)

<a href='https://bintray.com/prashantr/Courgette-JVM/courgette-jvm?source=watch' alt='Get automatic notifications about new "courgette-jvm" versions'><img src='https://www.bintray.com/docs/images/bintray_badge_color.png'></a>

#### Maven
````markdown
<dependency>
  <groupId>io.github.pramcharan</groupId>
  <artifactId>webdriver-binary-downloader</artifactId>
  <version>1.0.0</version>
  <type>pom</type>
</dependency>
````

#### Gradle
````markdown
repositories {
    jcenter()
}

compile 'io.github.pramcharan:webdriver-binary-downloader:1.0.0'
````

#### Included Dependencies
* commons-io 2.6


#### Currently Supported Driver Binaries
* ChromeDriver
* GeckoDriver


## Usage

Download the latest binary
````java
WebDriverBinaryDownloader.create().downloadLatestBinaryAndConfigure(BrowserType.CHROME);
````

Download an older binary
````java
WebDriverBinaryDownloader.create().downloadBinaryAndConfigure(BrowserType.CHROME, "2.35");
````

Once a binary is downloaded for a specific release, it will remain cached unless its manually deleted. 

Use the strictDownload() method to ensure a new copy is downloaded.
````java
WebDriverBinaryDownloader.create().strictDownload().downloadLatestBinaryAndConfigure(BrowserType.CHROME);
````


## Submitting Issues
For any issues or requests, please submit [here](https://github.com/prashant-ramcharan/courgette-jvm/issues/new)