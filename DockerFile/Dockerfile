# Use an official OpenJDK runtime as a parent image
FROM openjdk:17-jdk-slim

# Install Maven and Git
RUN apt-get update && \
    apt-get install -y maven git

# Set the working directory inside the container
WORKDIR /app

# Copy the local project files to the container (optional for initial setup)
COPY . .

# Create a volume for the Maven repository to persist dependencies
VOLUME /root/.m2

# Expose the port that the Spring Boot application runs on
EXPOSE 8080

# Expose a port for remote debugging (optional)
EXPOSE 5005

# Default command to keep the container running
CMD ["bash"]


#CMD to run docker container
# docker run -it \
# -p 8080:8080 \
# -p 5005:5005 \
# -v $(pwd)/DevProject:/app \
# -v ~/.m2:/root/.m2 \
# --name spring-boot-dev-env \
# spring-boot-dev-env
