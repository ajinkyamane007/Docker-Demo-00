# base
From openjdk:8

# Set the working directory
WORKDIR /app

# COPY the Main.java file | . minus working directory 
COPY Main.java .

# compile the application while building the image 
RUN javac Main.java

# run the application when container starts
CMD java Main
