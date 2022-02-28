
[cs15lwi22ajl@ieng6-201]:mark-down-parse-group:153$ make test
javac -cp .:lib/junit-4.13.2.jar:lib/hamcrest-core-1.3.jar MarkdownParseTest.java
java -cp .:lib/junit-4.13.2.jar:lib/hamcrest-core-1.3.jar org.junit.runner.JUnitCore MarkdownParseTest
JUnit version 4.13.2
....E.E.E
Time: 0.016
There were 3 failures:
1) testSnippet1(MarkdownParseTest)
java.lang.AssertionError: expected:<[`google.com]> but was:<[url.com, `google.com, google.com, ucsd.edu]>
        at org.junit.Assert.fail(Assert.java:89)
        at org.junit.Assert.failNotEquals(Assert.java:835)
        at org.junit.Assert.assertEquals(Assert.java:120)
        at org.junit.Assert.assertEquals(Assert.java:146)
        at MarkdownParseTest.testSnippet1(MarkdownParseTest.java:32)
2) testSnippet2(MarkdownParseTest)
java.lang.AssertionError: expected:<[a.com,  , example.com]> but was:<[a.com, a.com((, example.com]>
        at org.junit.Assert.fail(Assert.java:89)
        at org.junit.Assert.failNotEquals(Assert.java:835)
        at org.junit.Assert.assertEquals(Assert.java:120)
        at org.junit.Assert.assertEquals(Assert.java:146)
        at MarkdownParseTest.testSnippet2(MarkdownParseTest.java:38)
3) testSnippet3(MarkdownParseTest)
java.lang.AssertionError: expected:<[https://ucsd-cse15l-w22.github.io/]> but was:<[, , ]>
        at org.junit.Assert.fail(Assert.java:89)
        at org.junit.Assert.failNotEquals(Assert.java:835)
        at org.junit.Assert.assertEquals(Assert.java:120)
        at org.junit.Assert.assertEquals(Assert.java:146)
        at MarkdownParseTest.testSnippet3(MarkdownParseTest.java:44)

FAILURES!!!
Tests run: 6,  Failures: 3
