FROM eclipse-temurin:17.0.6_10-jdk

# Create app directory
RUN mkdir -p /usr/app
WORKDIR /usr/app

COPY . .

RUN chmod +x gradlew
RUN ./gradlew
CMD ./gradlew run
