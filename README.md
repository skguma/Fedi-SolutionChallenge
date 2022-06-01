# Google Solution Challenge 2022 : Fedi🔍
<div>
<img src="https://img.shields.io/badge/GENDER EQUALITY-FF3A21?style=for-the-badge&logoColor=white"/>
<img src="https://img.shields.io/badge/PEACE, JUSTICE AND STRONG INSTITUTIONS-00689D?style=for-the-badge&logoColor=white"/> </div>
<br><br>

![fedi](https://user-images.githubusercontent.com/70956926/160648926-7af1486e-82ec-4076-8961-f66a605205e9.png)

## 💻Project Introduction
**Find your Face, Fedi**  is a service to help victims of acquaintance insult crimes. 

With the development of the Internet, the damage of digital sex crimes is increasing year by year. And most of the victims of digital sex crimes are women.
According to the results of a survey on cyber violence conducted in South Korea, the type of crime that is most often witnessed in daily life was acquaintance insult.

A crime called **acquaintance insult** refers to stealing pictures of others without permission and publicly posting them on SNS with sexually insulting words. 
Victims of the crime should recognize the damage, find photos of their damage, track the route, and request the platform to delete them one by one. This is a hard task for an individual to handle, and the number of dedicated personnel in specialized institutions is insufficient.

We can reduce the burden that victims of acquaintance insult crimes have to go through alone. 
With Fedi, crime victims women can feel that they are not alone and feel more secure when posting photos on SNS.

<br>

## ⚙Used Technology
<p > <b>- Front-end</b> </p>
<div >
<img src="https://img.shields.io/badge/React Hooks-61DAFB?style=flat-square&logo=React&logoColor=white"/>
<img src="https://img.shields.io/badge/Meterial UI-757575?style=flat-square&logo=Material Design&logoColor=white"/>
<img src="https://img.shields.io/badge/Styled Components-DB7093?style=flat-square&logo=styled-components&logoColor=white"/>
<img src="https://img.shields.io/badge/Redux thunk-764ABC?style=flat-square&logo=Redux&logoColor=white"/>
<img src="https://img.shields.io/badge/D3.js-F9A03C?style=flat-square&logo=D3.js&logoColor=white"/></div>

<p > <b>- Back-end</b> </p>
<div >
<img src="https://img.shields.io/badge/Spring Boot-6DB33F?style=flat-square&logo=Spring Boot&logoColor=white"/>
<img src="https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=MySQL&logoColor=white"/></div>

<p > <b>- Deep-learning</b> </p>
<div>
<img src="https://img.shields.io/badge/Tensorflow-FF6F00?style=flat-square&logo=TensorFlow&logoColor=white"/>
<img src="https://img.shields.io/badge/Flask-000000?style=flat-square&logo=Flask&logoColor=white"/>
</div>

<p > <b>- RPA</b> </p>
<div>
<img src="https://img.shields.io/badge/UiPath-ff0000?style=flat-square&logoColor=white"/></div>

<p > <b>- Server</b> </p>
<div >
<img src="https://img.shields.io/badge/AWS-232F3E?style=flat-square&logo=Amazon AWS&logoColor=white"/>
<img src="https://img.shields.io/badge/Amazon S3-569A31?style=flat-square&logo=Amazon S3&logoColor=white"/>
<img src="https://img.shields.io/badge/Microsoft Azure-0078D4?style=flat-square&logo=Microsoft Azure&logoColor=white"/>
<img src="https://img.shields.io/badge/NGINX-009639?style=flat-square&logo=NGINX&logoColor=white"/>
</div>
<br>

## 🏚System Architecture
![GDSC 데모 영상 자료](https://user-images.githubusercontent.com/70956926/160659507-ac772133-a206-46c7-a7b3-4a3c575d2e54.png)
- When the user inputs her picture at the front desk, the backend requests the API to the deep learning server to receive the analysis results using the deep learning model and returns the results to the user.
- UiPath's RPA is used to pre-scrap images, scrap tweets/likes account information in tweets, and report to the platform.
- The backend is connected to the DB
- We deployed our Backend server on AWS EC2 and Deep-learning server on Microsoft Azure VM
<br>

## 🎥Demo Video Link
<a href="https://youtu.be/6ZW8f11hHBg">
<img src=https://user-images.githubusercontent.com/70956926/160649395-cd068ea8-4b90-4b93-b113-67147b5a0145.png /> </a>

<br><br>

## 🔍How to use?
![슬라이드1](https://user-images.githubusercontent.com/70956926/160650044-d160943a-18c1-4ba4-a73b-4d473473f0c0.PNG)

![슬라이드2](https://user-images.githubusercontent.com/70956926/160650132-811c1651-bb13-424a-bb1c-91b78a9b8d3a.PNG)

![슬라이드3](https://user-images.githubusercontent.com/70956926/160650201-42643408-e3fd-456a-bd21-196ff3ef3153.PNG)

![GDSC Github](https://user-images.githubusercontent.com/70956926/161062767-8ffe405e-8b6f-4d8c-8346-dc9c7e0448d0.png)

<br>

## 🏃‍♀️How to run?
### ❗Announcement❗
> Currently, we put dummy data in DB and do not connect with RPA. This is to test the results more clearly and fast.
>
> When deploying the completed service, we will connect RPA and scrap tweets that correspond to actual acquaintance insult crimes.
>
> Don't worry, we already tested the connection with RPA in our service😎
>
> And also, you can test RPA locally at any time you want. Please refer to the following.

<br>

### ✨Web application

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

#### Directory
```bash
├─AccountImage
│ Creating accounts list obtained from search results and Scraping image dataset
│
├─ReportTweet
│ Scraping `AccountId`, `AccountName`, `TweetUrl` of accounts that clicked likes and retweets in original tweets
│
└─Retweets & Likes
  Report the accounts selected by the user on Twitter
```
<br>

## 🎈Contributor

| [Hyosin Jang](https://github.com/hyosin-Jang)                                                            | [Hyuna Park](https://github.com/hak2711)                                                                | [Suji Yoon](https://github.com/Yoon-Suji)                                                               |
|:----------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------:|:------------------------------------------------------------------------------------------------------:|
| <img src = "https://user-images.githubusercontent.com/67725652/161052307-b7b10483-5645-4a00-8577-df87eaf6d99c.png" width="70%"/> | <img src = "https://user-images.githubusercontent.com/67725652/161052705-238e0e83-a690-42de-a35f-8f7c9b0e545b.png" width="70%"/> | <img src = "https://user-images.githubusercontent.com/67725652/161052139-41340000-585e-4fc7-b6e9-ab690bb05117.png" width="70%"/> |
| Frontend & RPA                | Backend & Training deep-learning model                                                                 | Backend & Collecting training dataset                                                    |
