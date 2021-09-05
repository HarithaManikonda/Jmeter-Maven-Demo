# Jmeter-Maven-Demo
This is a demo project to invoke jmeter tests from maven

## Add jmeter-maven-plugin in pom.xml
```javascript
    <plugin>
				<groupId>com.lazerycode.jmeter</groupId>
				<artifactId>jmeter-maven-plugin</artifactId>
				<version>3.4.0</version>
				<executions>
					<!-- Generate JMeter configuration -->
					<execution>
						<id>configuration</id>
						<goals>
							<goal>configure</goal>
						</goals>
					</execution>
					<!-- Run JMeter tests -->
					<execution>
						<id>jmeter-tests</id>
						<goals>
							<goal>jmeter</goal>
						</goals>
					</execution>
					<!-- Fail build on errors in test -->
					<execution>
						<id>jmeter-check-results</id>
						<goals>
							<goal>results</goal>
						</goals>
					</execution>
				</executions>
			</plugin>
 ```
```javascript
mvn clean verify
 ```
![Screen Shot 2021-09-03 at 4 50 24 PM](https://user-images.githubusercontent.com/87215340/132075056-aeae90b5-29c1-4313-a4b4-46d3f543dcad.png)

