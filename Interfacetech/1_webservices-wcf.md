# Web services, WCF

## Web service / webszolgáltatás

A webszolgáltatás (angolul webservice) **alkalmazások közötti adatcserére szolgáló protokollok és szabványok gyűjteménye**.

### W3C definition

> A web service is a software system designed to support interoperable machine-to-machine interaction over a network. It has an interface described in a machine-processable format (specifically WSDL). Other systems interact with the web service in a manner prescribed by its description using SOAP-messages, typically conveyed using HTTP with an XML serialization in conjunction with other web-related standards.

Klasszikus értelemben a webszolgáltatás egy rendszer aminek a segítségével szoftverek tudnak interakcióba lépni egy hálózaton keresztül.

![](Interfacetech/webservice-classic.png)

* **(Service) Transport Protocol**: responsible for transporting messages between network applications, e.g. HTTP.
* **(XML) Messaging Protocol**: encodes information into a common XML format, e.g. SOAP.
* **(Service) Description Protocol**: describe the public interface to a specific web service, e.g. WSDL.
* **(Service) Discovery Protocol**: centralizes services into a common registry so that network Web services can publish their location and description, e.g. UDDI.

## REST

## Sources

http://embeddedsystem.info/
https://www.tutorialspoint.com/webservices/what_are_web_services.htm
https://en.wikipedia.org/wiki/Web_service
https://hu.wikipedia.org/wiki/Webszolg%C3%A1ltat%C3%A1s
https://en.wikipedia.org/wiki/Web_services_protocol_stack