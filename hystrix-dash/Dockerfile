FROM java:8-jre

ADD ./target/hystrix-dash.jar /app/
CMD ["java", "-Xmx200m", "-jar", "/app/hystrix-dash.jar"]

HEALTHCHECK --interval=30s --timeout=30s CMD curl -f http://localhost:9999/actuator/health || exit 1

EXPOSE 9999