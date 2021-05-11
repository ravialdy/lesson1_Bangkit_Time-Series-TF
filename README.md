## Lesson Learned 1 Bangkit Academy : Time Series using Tensorflow (Synthetic Data)

Bangkit is an academy led Google, Gojek, Tokopedia, and Traveloka that has a unique career readiness program delivered with support from industry experts and industry partners. (More info : https://grow.google/intl/id_id/bangkit/)

#### *) Here, I want to create time series model based on my own synthetic time series using tensorflow. Check it out :)

### A Brief Explanation about Generated Synthetic Time Series.

In this case, I use baseline value equals to 100, amplitude equals to 40, noise_level equals to 7, and range time 5 years. I also use seasonal pattern using cosine function
when seasonal time is less than 0.5 and using sine function when seasonal time is more than or equal to 0,5.

![image](https://user-images.githubusercontent.com/68768305/117802623-e7886b00-b27f-11eb-8c85-9db161c6a713.png)

### Split to Training and Validation.

I determined training time to be 1200, and the rest of it is belong to validation time.

![image](https://user-images.githubusercontent.com/68768305/117802909-38985f00-b280-11eb-84b4-a661d3c381d2.png)

![image](https://user-images.githubusercontent.com/68768305/117802978-4a7a0200-b280-11eb-9ede-e26601805257.png)

### First Method : Using Naive Forecast!

![image](https://user-images.githubusercontent.com/68768305/117803085-6c738480-b280-11eb-91cd-06071b9e68d7.png)

![image](https://user-images.githubusercontent.com/68768305/117803178-87de8f80-b280-11eb-91d8-c535a2dd4aea.png)

Notice that our result using this method is not excellent, but it's also not bad at all :)

### Second Method : Using Moving Average Forecast!

![image](https://user-images.githubusercontent.com/68768305/117803418-d2f8a280-b280-11eb-8d40-d99d9b2ebf7e.png)

![image](https://user-images.githubusercontent.com/68768305/117803471-df7cfb00-b280-11eb-85ce-71b1f3e55786.png)

### Third Method : Using Moving Average Forecast with differencing!

![image](https://user-images.githubusercontent.com/68768305/117824435-b10b1a00-b298-11eb-91b2-848066882089.png)

![image](https://user-images.githubusercontent.com/68768305/117824503-bd8f7280-b298-11eb-9364-a25f45f6efb3.png)

### Fourth Method : Using Moving Average with Differencing + Past Values Forecast!

![image](https://user-images.githubusercontent.com/68768305/117824631-da2baa80-b298-11eb-93ec-09acfd15e4e7.png)

![image](https://user-images.githubusercontent.com/68768305/117824717-e6b00300-b298-11eb-93ec-1f582a388dd7.png)

**Conclusion : Using Naive Forecast is still very good compared with other three methods. Maybe we can still minimize the error by implementing a moving averaging on past values to remove some of the noise in our data.**

#### For complete work, please take a look to my notebook. I am open for receiving some feedbacks and suggestions if I made mistakes :)

### Reference : 

* https://github.com/lmoroney/dlaicourse.git




