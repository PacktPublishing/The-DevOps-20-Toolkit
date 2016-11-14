Before looking into the code, you need to follow the steps mentioned below:

Build Tests

sudo docker build -t vfarcic/books-ms-tests -f Dockerfile.test .

sudo docker push vfarcic/books-ms-tests
Test and Build

sudo docker-compose -f docker-compose-dev.yml run testsLocal

sudo docker build -t vfarcic/books-ms .

sudo docker push vfarcic/books-ms
Run Front-End Tests Watcher

sudo docker-compose -f docker-compose-dev.yml up feTests
Run Integration Tests

sudo docker-compose -f docker-compose-dev.yml up integ