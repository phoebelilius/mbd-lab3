FROM amazoncorretto:21 as build

WORKDIR /java-test/

COPY volumen/Main.java /java-test/

ENTRYPOINT [ "javac", "Main.java"]

RUN javac Main.java

FROM  amazoncorretto:21 as execute

WORKDIR /java-test

COPY --from=build /java-test/Main.class /java-test/Main.class

CMD ["java", "Main"]