# painting-recommendation
<p align="left">
  <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=Python&logoColor=white"/></a>&nbsp
  <img src="https://img.shields.io/badge/GoogleColab-F9AB00?style=flat-square&logo=GoogleColab&logoColor=white"/></a>&nbsp 
  <img src="https://img.shields.io/badge/Mysql-4479A1?style=flat-square&logo=MySql&logoColor=white"/></a>&nbsp 
  <img src="https://img.shields.io/badge/Django-092E20?style=flat-square&logo=Django&logoColor=white"/></a>&nbsp 
  <img src="https://img.shields.io/badge/aws-FF9900?style=flat-square&logo=AmazonAWS&logoColor=white"/></a>&nbsp
</p>
<b><i>Painting Recommendation</i></b> is a service that recommends famous paintings based on the color of the user's interior. Our team and project is named <b>'DaChae'</b>(다채), which means various colors of homes(다채로운 집), is a startup with a vision of popularizing interior curating service. The service aims to provide cheap, convenient, and customized AI interior curating service to consumers with self-home interior needs.
<br>
<br>
The overall painting recommendation algorithm works by firstly extracting the <b>representative</b> colors of the photos uploaded by the user. Then, it recommends several famous paintings stored in our database with representative colors similar and complementary to the representative colors of the interior photo. The similarity between the colors is measured by CNN similarity and clustered by Mean shift clustering. The technical composition can be largely divided into three parts.<br>
<br>

- Famous painting database
- Color combination algorithm
- Recommendation system

The painting database is constructed by the crawled image data and HSV of the main three colors for each painting. It is built as an EC2 database on AWS. From the interior photo uploaded by the user, k-representative colors are extracted through the Mean shift clustering. Then, the color combination algorithm is implemented to predict the paintings in a similar, complementary, and monochrome color relationship with the interior photo.
<br>
After calculating the CNN-based cosine similarity between the interior photo and the painting image, the final painting with minimum parameters between image pixels are recommended. Based on these algorithms, we have created a Django-based web prototype. In the website, it can automatically recommend famous paintings that suits the user-uploaded interior photo.


<h2> major Contributions </h2>

- Construction of an **EC2** (aws) database
- Built our own color combination algorithm based on **CNN** and **Meanshift** clustering
- Trial-and-error of the (beta-version) demo
- Sucessfully launched django-based **website**
- Provision of marketing insights of the service

<h2> Start-up </h2>

- <a href='https://piville.kr/team/piville_view.asp?p_idx=177&KeyOrder2=cs01&KeyOrderYear=0'>pi-ville</a>
- <a href='https://www.startupstation.kr/?teams=%eb%8b%a4%ec%b1%84'>startup express</a>

<h2> Directory </h2>

### _algorithms_
- **database**
  - **artwork_info**: 명화정보 데이터
  - **product_info**: 명화 구매가격 데이터
  - **setting**: EC3 데이터베이스 구축에 필요한 데이터 크롤링 코드
- **color_extraction**: 업로드한 인테리어 이미지와 유사색/보색/단색 관계의 명화 추천


### _data_
- crawled_painting: 크롤링한 작가/명화명/HSV/url 데이터

### _ppt_
- 1차 사업계획서
- 2차 사업계획서


<h2> Demo </h2>
<a href=https://da-chae.com/><b>Demo</b></a> (beta-version) is now released in our website !
