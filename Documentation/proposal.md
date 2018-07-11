# Crowdsourcing Picking Solution

## Thesis of this Proposal
O2O retailing is fast-developing in China and Walmart responses with JDDJ service. The procedures of Walmart JDDJ service has three rough steps, among which the picking step has relatively low capacity and concerning bottleneck problem. We propose a crowdsourcing solution, which eventually aims at empowering everyone to assume the task of picking, but can start with a trial run open to only idle Walmart salesperson. This solution can lower the cost and reduce the bottleneck, but might face time limit problem which might be checked through trial run. We will develop MVP, including relevant mini program and design detailed hardware by July 27th.

## Background
O2O retail mode refers to Online-To-Offline, meaning an upcoming sale design compared to traditional storefronts by face to face. The type of sale merged in early 2010 and experienced fast development in 2013. This new model aims to corporate the online and offline market, but weights more on online one with sale and less on offline with experience. 

This model represents more efficiency and effectiveness in market. It divers into platform and supply chain. Each offer superior service to traditional ones. For instance, it creates more various supply or speeds up delivery process. Moreover, due to the use of network, the influence of O2O expands. Stores use this idea to attract more customers in order to promote sales. It also shares information faster, allows suppliers to trace and assess. 

As predicted, the O2O will grow rapidly in the next few years. It has greater impact because of the online payment such as WeChat and Alipay. It can take over more than 46% of the market by 2035, according to one research from Baidu. 

Walmart responses to this rapid change with pushing forward the idea of opening sale portal for remote customers and delivering door-to-door service. Currently, Walmart has been operating its O2O for several years and realized its positioning. The stores have deals with JDDJ, which enables consumers to place orders via web and apps by 24 hours. 

The process of Walmart JDDJ service can be summarized into ordering → picking → packaging & delivery. Such orders will be presented to staff in Walmart as soon as app users place their demand. When received orders, staff start to pick listed goods and items from shelves and, following, gather them at the picking area within 8 minutes around. Later, goods will be separated and packaged in terms of orders, waiting to be delivered by DaDa drivers. 

## Problem
Picking step, as one of the three rough steps of JDDJ service, are especially vulnerable to market size increase. Orders are taken and processed by computer; packaging takes short time and delivery are outsourced by Dada drivers, who can increase their number as market increases. But picking step, are currently done by Walmart specialized employees.

Problems of current picking solution mainly fall into 2 regions: human cost and potential bottleneck problem. We do a simple conservative estimation that 20 workers are working at the same time with 2 turns, 2000 Yuan per month salary, that’s 80,000 Yuan for only picking and for only Shekou store. And the picking area is already barely sustaining, especially judged by the crowdedness of the layout. If the amount of orders doubles or triples in the future, such solution may not be able to continue. In other words, the flexibility and the growth potential of picking cannot match those of confirming orders and delivering goods.

## Solution(MVP)
The solution proposed by our team can be presented in 3 parts. We will introduce the working procedures, followed by hardware and software preparations of the MVP.
###I.	Working Procedures
The proposed picking solution follows crowdsourcing principle. Specialized picking employees will be substituted by idle store salesperson, or eventually by any walking customer. 
A typical online order will be accepted after automatically checking the inventory, then divided into small sub-order by the categories or the areas they are placed. For example, the order of 2 cups of yogurt, 1 tin of cola and 1 bag of chips will be divided into 2 sub-orders, beverage sub-order and snacks sub-order. Each sub-order will be then pushed as corresponding "

Anyone who logins the mini Program, supported by Wechat can check task list. A typical task will be like this: finding goods from an area to a specified picking table in that area, with a 4-minute time limit. He will be notified to place goods in a box with specified color (black, white, red, green, yellow, blue). He will be rewarded with some points (evaluated by the difficulty of the task), which can be converted into coupon or money then.

A specialized worker or a group of specialized workers will follow a routine to pick all the goods on picking tables every 4 minutes. Goods will be taken to packaging area, and be packaged based on original orders. Delivery will keep unchanged as before.

### II.	Hardware preparation
There are two kinds of hardware that need to be prepared: picking shelf and transport cart

#### 1.	Picking shelf:
We will assign one picking shelf to one “region” that is used to separate orders. They will be transformed from traditional shelves, with a plate showing their usage. They will then be painted by different colors from up to down, with white, black, blue, green, red, and yellow.

#### 2.	Transportation cart:
Transportation carts are used by specialized workers to pick goods from picking shelves to packaging area. They can be simply transformed from traditional shopping cart, with separator (like a fence) to divide the interior into 6 parts, with corresponding 6 colors painted at the bottom.
Rough design of picking shelf and transportation cart:
 
### III.	Software preparation: WeChat mini program
WeChat mini programs are “sub-applications” with WeChat, and we choose this form because 

(1) mini programs can be used without downloading or installing, users can invoke it simply on WeChat interface, 
(2) mini programs are cross-platform, thus we don’t need to develop both iOS and Android versions, 
(3) WeChat ecosystem is extremely powerful, and mini programs are capable as a solution.

It is notable that this software is specific for the Shekou Walmart store. Since it is a minimal viable product, we won’t develop a product that is suitable for all Walmart stores. So we might require the map and other essential information of Shekou store. Therefore, we can test our idea and assess the feasibility of this solution by analyzing feedbacks introduced by the MVP.

The user interface and the backend logic of our mini program is as follows. The first surface that users see will be the floor plan of Walmart store. Users could select the area in which they intend to pick the items; After choosing the area, the user interface will show the currently available task list in this area, which indicates all the picking tasks not accepted yet. Therefore, users could receive the assignment, and start picking. To implement the first-in first-out principle, the task list would primarily be a queue data structure.

The software also provides API for Create-Read-Update-Delete operations on the goods database and the e-commerce platform. By invoking these API, the mini program could access the information of orders and corresponding goods, including the item number and item names of the order, the area to which the item belongs, the bar code, the reward that users could get if they pick the item, etc.
Moreover, there will be a User Center interface within the program. This part will record the user information and rewards.

## Implementation plan:
We would like to develop a demo for crowdsourcing solution, based on Shekou store. The app will be developed with detailed hardware design, tailored to the situation at Shekou by July 27th. We might need a store map of shekou with rough goods layout within a week to develop mini program; and relevant JDDJ service statistic to estimate market growth, and determine compensation plan.
### I.	Phase 1 July 9th - 20th:
In these two weeks we will have two team:
Programming team will develop the mini Program; 
Economic team will design detailed compensation plan for participants involved in crowdsourcing, and prepare detailed hardware design.
### II.	Phase 2 July 21th-27th
Integrate two team’s results, and prepare the instruction book of crowdsourcing picking solution.

