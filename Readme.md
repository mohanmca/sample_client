## How to execute the program

```bash
chmod a+x run.sh
./run.sh 
```

## List of tasks, how I did it, and time taken

1. Initially followed the guideline https://spring.io/guides/gs/reactive-rest-service/
2. Hit with netty-DNS error, and googled and updated dependency with classifier for Mac-M1 processor
3. Wasted time in Intercepting WebClient Junit Test and I tried to intercept the request and produce response (without mockserver)
   1. After 2hrs, I gave-it-up, and fallen back to time-tested mock web server
   2. I had other choice to use MockBean and expect the API, but generally I felt mocking API is very ugly and useless for my work
   3. Too much of mock-api eventually becomes useless, I am not able to reproduce production problems using mock-api heavy test-cases
4. 30 Minutes with mock-test  and mock-web-server
5. Add bells and whistles - 45 minutes
   1. run.sh
   2. Update Junit failure  message
   3. Test with wrong url
   4. Answer the question

## Answers


1. How long did it take you to solve the above exercise? Please be honest, we evaluate your answer to this question based on your experience.

I spent 4 hours due to spring magic, but I chose to use Spring since it would be useful to me in another task at office. I couldn't use the UserClient itself Main as well a class under test

2. Please describe, in your own words, the main difference between a monolithic system and a microservice architecture.

MicroService architecture is collection of services, work together as one-service and highly resilient and fault tolerant. The cost of building and maintaining is higher compared to monolithic systems, Hence requires lots are consideration before choosing MicroService architecture.
Generally they follow 12 factors defined at https://12factor.net/. Generally they are not suitable for smaller startups. It gives bit of freedom for team (2-pizza team), As long as they keep their services backward compatible and ensure the availability they can build application on any platform. Mostly they are communicated using HTTP/HTTPS and read using REST-ful and GraphQL based 


## Modern UI Frameworks?
Is it javascript ui frameworks?

1. React
2. Vue.js

How play the words container, docker and Kubernetes together?

Containers were nothing but basic namespace process level isolation inside Linux, it was initially implemented using c-groups by google. Docker provided higher level APIs and CLI and Provided a way of to pack everything required to run a process, later many other implementation were introduced, containers are now standardized and supported by default in Linux. Containers across the system should be co-ordinated for distributed systems, despite there were docker-swarm, mesos and kubernetes were competing in this space. K8S emerged as industry standard and supported by multiple cloud vendors. 
    1. Two famous commercial vendor that supports hybrid implementations are RedHat OpenShift and Pivotal CloudFoundry
    1. Apache Mesos already died, and Docker swarm still being used rarely for local development setups
 


```
git branch --set-upstream-to=origin/main main
