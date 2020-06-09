## What is REST-Assured
It is a java library which will help us in automating the testing of RESTful API. 
REST assured is helpful in writing small Unit tests as well as large automation frameworks, where we can create test cases for large APIs. It has so many useful functions which we can use to send all types of HTTP methods, accessing public as well as private API by authenticating yourself. Storing the response and later use that response data to validate against the expected data. We can also use TestNG for better execution and generating better validation reports and assertions of your test cases.

REST Assured is a Java DSL for simplifying testing of REST based services built on top of HTTP Builder. 

Rest Assured has a gherkin type syntax which is shown in below code. If you are a fan of BDD (Behavior Driven Development), I believe that you will love this kind of syntax.
```java
@Test
public void exampleRestTest() {
    given()
        .contentType(ContentType.JSON)
        .pathParam("id", "AskJsd8Sd")
    .when()
        .get("/examplepath/{id}")
    .then()
        .statusCode(200)
        .body("firstName", equalTo("Onur"))
        .body("Surname", equalTo("Baskirt"));
}
```