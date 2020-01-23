# Web services, WCF

## Web service / webszolgáltatás

A webszolgáltatás (angolul webservice) **alkalmazások közötti adatcserére szolgáló protokollok és szabványok gyűjteménye**.

### W3C definition

> A web service is a software system designed to support interoperable machine-to-machine interaction over a network. It has an interface described in a machine-processable format (specifically WSDL). Other systems interact with the web service in a manner prescribed by its description using SOAP-messages, typically conveyed using HTTP with an XML serialization in conjunction with other web-related standards.

Klasszikus értelemben a webszolgáltatás egy rendszer aminek a segítségével szoftverek tudnak interakcióba lépni egy hálózaton keresztül.

![](/Interfacetech/webservice-classic.png)

* **(Service) Transport Protocol**: responsible for transporting messages between network applications, e.g. HTTP.
* **(XML) Messaging Protocol**: encodes information into a common XML format, e.g. SOAP.
* **(Service) Description Protocol**: describe the public interface to a specific web service, e.g. WSDL.
* **(Service) Discovery Protocol**: centralizes services into a common registry so that network Web services can publish their location and description, e.g. UDDI.

## REST

Representational state transfer (REST) is a software architectural style that defines a set of constraints to be used for creating Web services. RESTful Web services allow the requesting systems to access and manipulate textual representations of Web resources by using a uniform and predefined set of stateless operations. Uses standard HTTP methods to retrieve data usually as a JSON file.

* Simple
* Scalable
* Portable

## REST and SOAP

> REST is much more limited than SOAP, which is its strength and the reason for its popularity.

> In SOAP, the set of operations allowed and the set of data types allowed is essentially limitless. SOAP is a remote procedure protocol, which you use to expose local API's across the network without losing any fidelity. This made SOAP popular in enterprise environments where complex transactional systems needed to interact across the network without losing any fidelity along the way. This richness in ability is also SOAP's downfall, because it makes SOAP API's so cumbersome to understand and use that it necessitated automated tooling in the form of WSDL and SOAP client libraries to make sense of things. More so, exposing the full richness of the underlying system is unattractive in public-facing API's, where you want to provide abstractions that let you evolve the underlying system without having to break or version your API.

> REST+JSON gained popularity specifically because of its simplicity. It defines a limited set of operations with a limited set of data types, requiring the API designer to carefully design abstractions that fit inside this limited vocabulary and really think through the mapping of business domain to REST resources. A REST API is easy to understand and easy to use without any special tooling. For a public-facing API where your API users may have all levels of skill and knowledge this is exactly what you want, which is why all of the API's you see around the web have been transitioning to REST. SOAP is relegated to enterprise situations where there is still a desire and need to share complex API's between systems. However, with architectural trends towards independently versioned micro-services developed by separate teams even that domain is losing ground.

> Essentially, what people have realized is that the set of constraints that you must apply to your API design to make the API simple and abstract enough that it is maintainable and easy to use is exactly the set of constraints that REST introduces, which effectively neutralizes SOAP's benefits leaving you with only its downsides. You could build a simplified API with SOAP, but it would never be as easy to use as REST, so in practice everybody just chooses REST.

https://softwareengineering.stackexchange.com/a/336577

## Windows Communication Foundation (WCF)

A tool developed by Microsoft used to implement service oriented applications. WCF is a .net library used to have two programs talk to each other using SOAP. Which consists of two very familiar programs trading class info.

## Sources

http://embeddedsystem.info/
https://www.tutorialspoint.com/webservices/what_are_web_services.htm
https://en.wikipedia.org/wiki/Web_service
https://hu.wikipedia.org/wiki/Webszolg%C3%A1ltat%C3%A1s
https://en.wikipedia.org/wiki/Web_services_protocol_stack
https://softwareengineering.stackexchange.com/questions/336565/what-is-the-present-day-significance-of-soap
http://www.looah.com/source/view/2284