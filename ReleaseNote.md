# Quick Start Guide
## 🔍How to use?
![슬라이드1](https://user-images.githubusercontent.com/70956926/160650044-d160943a-18c1-4ba4-a73b-4d473473f0c0.PNG)

![슬라이드2](https://user-images.githubusercontent.com/70956926/160650132-811c1651-bb13-424a-bb1c-91b78a9b8d3a.PNG)

![GDSC Github](https://user-images.githubusercontent.com/67725652/171861115-4fdc61d9-71a3-4494-b47c-5548c0560204.png)

![Slide4](https://user-images.githubusercontent.com/67725652/171832570-e6db30b0-b26b-408b-aa63-689ef1e24297.PNG)


<br>

## 🏃‍♀️How to run?

### ✨Web application

You can use our web service in two ways.

 1. Go to https://fedi.link/

<br>

 2. Run our code on localhost.

```
$ git clone --recurse-submodules https://github.com/skguma/Fedi-SolutionChallenge.git

$ cd Fedi-SolutionChallenge/Fedi-front

$ npm install

$ npm start
```

you can also use `yarn install` and `yarn start` if npm does not work well.

<br>


### ✨RPA
 1. Read [how to install the UiPATH Studio](https://uipath.tistory.com/81) and download the Studio version

2. Git clone
```
$ git clone https://github.com/skguma/Fedi-image-scraper.git
```

3. Execute `.XAML` files in each folder (You can run it by double-clicking it)

4. Please modify the following variables and arguments to suit your environment

<br/>

**AccountImage > Main.xaml > variables tab**
```
- "baseURL": Folder path where the scraped image is stored

- "imageDataExcelFile": Excel file name to store the account where the image was uploaded and the tweet data.

- "savePath": Folder path where the list of accounts you scraped will be stored

- "excelFileName" : Excel file name to store the scraping account list
```

<br/>

**Retweets & Likes > Main.xaml > arguments tab**

```
"InputArgument" > "tweetUrl": Tweet url that you want to scrap the list of likes/retweets accounts (InputArguments is JSON Array type, and tweetUrl is the key)
```

<br/>

**ReportTweet > Main.xaml > arguments tab**

```
"InputArgument" > "tweetUrl": Tweet url that you want to report on Twitter (InputArguments is JSON Array type, and tweetUrl is the key)
```

