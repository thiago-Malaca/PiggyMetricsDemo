FROM java:8-jre

ADD ./target/account-service.jar /app/
CMD ["java", "-Xmx200m", "-jar", "/app/account-service.jar"]

HEALTHCHECK --interval=30s --timeout=30s CMD curl -f http://localhost:6000/actuator/health || exit 1

EXPOSE 6000