FROM java:8-jre

ADD ./target/turbine.jar /app/
CMD ["java", "-Xmx200m", "-jar", "/app/turbine.jar"]

HEALTHCHECK --interval=30s --timeout=30s CMD curl -f http://localhost:8989/actuator/health || exit 1

EXPOSE 8989