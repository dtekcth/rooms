FROM openjdk:17

# Create app directory
RUN mkdir -p /usr/app
WORKDIR /usr/app

COPY . .

RUN chmod +x gradlew
RUN ./gradlew
CMD ./gradlew run

