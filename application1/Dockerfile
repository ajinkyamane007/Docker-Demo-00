#### stage 0: building the application ####
# base
From openjdk:8 AS build

# Set the working directory
WORKDIR /app

# COPY the Main.java file | . minus working directory 
COPY Main.java .

# compile the application while building the image 
RUN javac Main.java

#### stage 1: running application #####

# base
FROM alpine

# set working directory
WORKDIR /app

# install JRE
RUN apk update && apk add openjdk8-jre

# copy the Main.class 
COPY --from=build /app/Main.class .

# run the application when container starts
CMD java Main 

