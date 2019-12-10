FROM java:8-jre

ADD ./target/statistics-service.jar /app/
CMD ["java", "-Xmx200m", "-jar", "/app/statistics-service.jar"]

HEALTHCHECK --interval=30s --timeout=30s CMD curl -f http://localhost:7000/actuator/health || exit 1

EXPOSE 7000