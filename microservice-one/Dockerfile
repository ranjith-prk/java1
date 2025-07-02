FROM eclipse-temurin:17

# Create working directory
WORKDIR /app

# Copy WAR file to working directory
COPY target/works-with-heroku-1.0.war app.war

# Download Jetty runner
RUN curl -Lo jetty-runner.jar https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-runner/9.3.3.v20150827/jetty-runner-9.3.3.v20150827.jar

# Expose default Jetty port
EXPOSE 80

# Run Jetty with WAR file
ENTRYPOINT ["java", "-jar", "jetty-runner.jar", "app.war"]
