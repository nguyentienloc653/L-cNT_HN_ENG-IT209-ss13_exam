FROM eclipse-temurin:21-jre-alpine

WORKDIR /app

# Security best practice: Run application as non-root user
RUN addgroup -S appgroup && adduser -S appuser -G appgroup
USER appuser:appgroup

# Copy pre-built Spring Boot jar
COPY build/libs/*.jar app.jar

# Expose backend port
EXPOSE 8080

# Run Spring Boot application
ENTRYPOINT ["java", "-jar", "app.jar"]
