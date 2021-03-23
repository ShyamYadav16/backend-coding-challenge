# Savemate Backend Code Challenge


## Introduction

Hey there! Welcome to Savemate's Backend code challenge. We are happy you are interested in our company and are taking your time to solve this challenge.

The primary goal of this challenge is to assess, without using too much of your time, how comfortable you are with basic aspects of Backend Software development and Software development in general, especially within the context of Savemate's tech stack.

## Deadline

You have 5 days to return this challenge to our HR department, however, this challenge was designed not to take much more than a few hours (hopefully). We are mindful of your time.

In order to deliver the challenge, simply push it to a private git repository with access to https://github.com/ShyamYadav16

## Objectives

As mentioned, we want to assess your expertise as a developer and give you a small taste of what we do here at Savemate.

Here is what you need to deliver:

1. A backend application that follows product and technical requirements.
2. A document briefly explaining how to deploy your code and also explaining your decisions, especially if you deviated from any specific point on the specs.

This is how we will be grading your challenge:

1. Did you follow the specs? If not, did you have a good reason for it?
2. How did you fill the gaps in the specs?
3. How easy is to follow your code (clean, documented, good commit messages, etc)
4. Is your code tested?
5. Is it easy to deploy your solution to the cloud provider of your choice?
5. How you communicate difficulties or feedback back to the Product team.

## Specs

Here you find the specs of the project.

### **Product requirements**

Here at Savemate, we want to advertise the best merchants with our customers so they can shop and earn cash backs. For this, we want to create an API that allows our frontend admins to query for merchants in the system and to create new merchants if need be.

The endpoint URLs are expected to be the following:

1. `GET /merchants`, which should return the list of all merchants, with ordering, sorting and pagination capabilities.
2. `GET /merchants/{id}`, which should return the details of the merchant identified by the `id`
3. `POST /merchant`, which should save the merchant represented by the payload in the body in the database.

The merchants should have attributes like name, description, cashback(%), slug, merchant_redirection_url, country 

#### `GET /merchants`

This endpoint should return the list of all merchants, with ordering, sorting and pagination capabilities. The following parameters should be accepted via query parameters:

* `limit`: max number of records to return
* `offset`: number of records to skip when returning the results
* `orderBy:{field}`: field to order the results by. It should accept only -1 (for descending sorting) and 1 (ascending sorting)

#### `GET /merchants/{id}`

This endpoint should return the merchant represented by the id `id`.

#### `POST /merchants`

This endpoint should simply receive the payload of a merchant, validate and add it to the database.

**This endpoint should not take more than 300ms to return a response. 

**IMPORTANT:** Merchants should have a dynamic property called `cashbackRate`. It is the percentage amount we pay back to the customer based on the `cashback` level. As of now, the mapping is the following (however, we don't want to store this in a database so we are able to change the mapping easily):

* 50%: 0 <= `cashback` < 5
* 40%: 5 <= `cashback` < 10
* 30%: 10 <= `cashback` < 15
* 20%: `cashback` > 15

### **Technical requirements**

1. You are expected to use NodeJS and Typescript (Typescript must be running on [strict](https://www.typescriptlang.org/tsconfig#strict) mode).
2. You are expected to describe how to deploy your application 
4. You are expected to use a SQL database.
5. You are expected to write test cases for all APIs.
7. (Optional) Protect the endpoints with an API Key.

## Contact us

In case you have any doubts, please do not hesitate to contact our HR team, which will forward your message to us.

We wish you the best of luck!
