# java-bittrex-2

####_Use version 1.1 until further notice, as various endpoints used for initial development of this wrapper are now failing._####

Java wrapper for the beta 2.0 version of the Bittrex API (version 1.1 [here](https://github.com/platelminto/java-bittrex)).  Methods return a Response object with the following variables:

 - ```responseCode``` - int set to the response code
 - ```success``` - boolean set to true if the request succeded
 - ```message``` - String with details if the request is invalid
 - ```response``` - String with the actual response

### Usage
```
public static void main(String...args) {

	Bittrex wrapper = new Bittrex();
	wrapper.setAuthKeysFromTextFile("keys.txt");

	Response response = wrapper.getOpenOrders();
	
	if(response.isSuccessful())
	
	  System.out.println(response.getResult());
}
```
### Key & Secret

Please attach your key & secret in a text file and place it in the same folder as your source code. It should be formatted like so:

```
 - apikey: "key"
 - secret: "secret"
```

### Dependencies

- Apache HttpClient

```
<dependency>
  <groupId>org.apache.httpcomponents</groupId>
  <artifactId>httpclient</artifactId>
  <version>4.5.2</version>
</dependency>
```

### Donate

Donations are appreciated!

- BTC: 1P2RobdwhT5QmdDqDudXSJ81v4ZKpNWXSb
- DOGE: DCdisnbNQeAaTtdRvwgvu9pL8SVAtZR9Mm
