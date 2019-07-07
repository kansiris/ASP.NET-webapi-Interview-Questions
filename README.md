# ASP.NET-webapi
Table of Contents	
Web API Question Bank	3
Dedication	4
Introduction	5
About the author	7
Table of Contents	8
ASP.NET WEB API	10
Question: What is REST?	10
Question: Explain REST principle?	10
Question: What is difference between REST and SOAP?	10
Question: What is ASP.NET WEB API?	11
Question: Why choose ASP.NET WEB API?	12
Question: What is difference between WCF and ASP.NET WEB API and WCF REST and Web Service?	13
Question: Which one to choose between WCF and WEB API?	14
Question: What is the difference between ASP.NET MVC and ASP.NET WEB API?	14
Question: Can you return view by using WEB API method?	15
Question: Can you change WEB API action name like ASP.NET MVC?	15
Question: Can you restrict a WEB API action method to be invoked only by HTTP GET, POST, PUT or DELETE?	16
Question: How to call WEB API in ASP.NETMVC?	16
Question: How ASP.NET API routing is different from ASP.NET MVC routing?	17
Question: How to enable Attribute Routing in ASP.NET WEB API2?	17
Question: How to define attribute routing in ASP.NET WEB API2?	17





































ASP.NET WEB API
Question: What is REST?	
REST stands for Representational State Transfer. This is a protocol for exchanging data over a distributed environment. REST is an architectural style which treat each service as a resource and access data by HTTP protocol methods like GET, POST, PUT, and DELETE.
REST-style architectures consist of clients and servers. Clients initiate requests to servers who process these requests and return responses based on these requests. These requests and responses are built around the transfer of representations of these resources.
Question: Explain REST principle?	
REST is a set of principles that define how Web standards, such as HTTP and URIs, are supposed to be used. There are five important REST principle as given below –
Addressable Resources - Each resource should be identified by a URI (unique identifier)
Simple and Uniform Interfaces - REST is based on HTTP protocol so use HTTP GET, POST, PUT and DELETE method to perform actions. This make REST simple and uniform.
Representation Oriented- Representation of resources are exchanged. GET is used to return a representation and PUT, POST passes representation to the server so that underlying resources may change. Representation may be in many formats like XML, JSON etc.
Communicate Stateless - An application may has state but there is no client session data stored on the server. Any session specific data should be held and maintained by the client and transferred to the server with each request as needed.
Cacheable - Clients should be able to cache the responses for further use.
Question: What is difference between REST and SOAP?	
The difference between REST and SOAP is given below:
SOAP
REST
SOAP stands for Simple Object Access Protocol
REST stands for REpresentational State Transfer.
It is an XML based protocol built on the top of HTTP or sometimes TCP/IP, SMTP.
REST is not a protocol but it is an architectural style i.e.resource-based architecture.
SOAP has specifications for both stateless and stateful implementation.
REST is completely stateless.
SOAP enforces message format as XML.
REST does not enforces message format as XML or JSON.
SOAP has a defined standard specification.For example, WS-Security is the specification for implementing security.
It has no defined standard specifications.
The SOAP message consists of an envelope which includes SOAP headers and body to store the actual information you want to send.
REST uses the HTTP build-in headers (with a variety of media-types) to carry meta information and use the GET,POST, PUT and DELETE verbs to perform CRUD operations.
SOAP uses interfaces and named operations to expose your service.
REST uses URI and methods like (GET, PUT, POST, DELETE) to expose resources.
Performance is slow as compared to REST.
REST is fast as compared to SOAP.


Question: What is ASP.NET WEB API?	
ASP.NET WEB API is a framework for building HTTP services that can be consume by a broad range of clients including browsers, mobiles, iphone and tablets. It is very similar to ASP.NET MVC since it contains the MVC features such as routing, controllers, action results, filter, model binders, IOC container or dependency injection. But it is not a part of the MVC Framework.
It is a part of the core ASP.NET platform and can be used with MVC and other types of Web applications like ASP.NET WebForms. It can also be used as a stand-alone Web services application.
ASP.NET WEB API features
    1. It supports convention-based CRUD Actions since it works with HTTP verbs GET, POST, PUT and DELETE.
    2. Responses have an Accept header and HTTP status code.
    3. Responses are formatted by WEB API’s MediaTypeFormatter into JSON, XML or whatever format you want to add as a MediaTypeFormatter.
    4. It may accepts and generates the content which may not be object oriented like images, PDF files etc.
    5. It has automatic support for OData. Hence by placing the new [Queryable] attribute on a controller method that returns IQueryable, clients can use the method for OData query composition.
    6. It can be hosted with in the applicaion or on IIS.
    7. It also supports the MVC features such as routing, controllers, action results, filter, model binders, IOC container or dependency injection that makes it more simple and robust.

Question: Why choose ASP.NET WEB API?	
Today, a web-based application is not enough to reach it's customers. People are very smart, they are using iphone, mobile, tablets etc. devices in its daily life. These devices also have a lot of apps for making the life easy. Actually, we are moving from the web towards apps world.









So, if you like to expose your service data to the browsers and as well as all these modern devices apps in fast and simple way, you should have an API which is compatible with browsers and all these devices.
For example twitter, facebook and Google API for the web application and phone apps.
WEB API is the great framework for exposing your data and service to different-different devices. Moreover WEB API is open source an ideal platform for building REST-ful services over the .NET Framework. Unlike WCF Rest service, it use the full featues of HTTP (like URIs, request/response headers, caching, versioning, various content formats) and you don't need to define any extra config settings for different devices unlike WCF Rest service.
Why to choose WEB API
    1. If we need a Web Service and don’t need SOAP, then ASP.NET WEB API is best choice.
    2. It is used to build simple, non-SOAP-based HTTP Services on top of existing WCF message pipeline.
    3. It doesn't have tedious and extensive configuration like WCF REST service.
    4. Simple service creation with WEB API. With WCF REST Services, service creation is difficult.
    5. It is only based on HTTP and easy to define, expose and consume in a REST-ful way.
    6. It is light weight architecture and good for devices which have limited bandwidth like smart phones.
    7. It is open source.

Question: What is difference between WCF and ASP.NET WEB API and WCF REST and Web Service?
.NET framework has a number of technologies that allow you to create HTTP services such as Web Service, WCF and now WEB API. There are following differences among these four:
Web Service
    1. It is based on SOAP and return data in XML form.
    2. It supports only HTTP protocol.
    3. It is not open source but can be consumed by any client that understands xml.
    4. It can be hosted only on IIS.

WCF
    1. It is also based on SOAP and return data in XML form.
    2. It is the evolution of the web service (ASMX) and support various protocols like TCP, HTTP, HTTPS, Named Pipes, MSMQ.
    3. The main issue with WCF is, its tedious and extensive configuration.
    4. It is not open source but can be consumed by any client that understands xml.
    5. It can be hosted with in the application or on IIS or using window service.

WCF Rest
    1. To use WCF as WCF Rest service you have to enable webHttpBindings.
    2. It support HTTP GET and POST verbs by [WebGet] and [WebInvoke] attributes respectively.
    3. To enable other HTTP verbs you have to do some configuration in IIS to accept request of that particular verb on .svc files
    4. Passing data through parameters using a WebGet needs configuration. The UriTemplate must be specified
    5. It support XML, JSON and ATOM data format.

WEB API
    1. This is the new framework for building HTTP services with easy and simple way.
    2. WEB API is open source an ideal platform for building REST-ful services over the .NET Framework.
    3. Unlike WCF Rest service, it use the full features of HTTP (like URIs, request/response headers, caching, versioning, various content formats)
    4. It also supports the MVC features such as routing, controllers, action results, filter, model binders, IOC container or dependency injection, unit testing that makes it more simple and robust.
    5. It can be hosted with in the application or on IIS.
    6. It is light weight architecture and good for devices which have limited bandwidth like smart phones.
    7. Responses are formatted by WEB API’s MediaTypeFormatter into JSON, XML or whatever format you want to add as a MediaTypeFormatter.

Question: Which one to choose between WCF and WEB API?	
The following points help you to choose between WCF and WEB API:
    1. Choose WCF when you want to create a service that should support special scenarios such as one way messaging, message queues, duplex communication etc.

    2. Choose WCF when you want to create a service that can use fast transport channels when available, such as TCP, Named Pipes, or maybe even UDP (in WCF 4.5), and you also want to support HTTP when all other transport channels are unavailable.
    3. Choose WEB API when you want to create resource-oriented services over HTTP that can use the full features of HTTP (like URIs, request/response headers, caching, versioning, various content formats).
    4. Choose WEB API when you want to expose your service to a broad range of clients including browsers, mobiles, iphone and tablets.


Question: What is the difference between ASP.NET MVC and ASP.NET WEB API?	
There are following differences between ASP.NET MVC and WEB API:
    1. ASP.NET MVC is used to create web applications that return both views and data but ASP.NET WEB API is used to create full blown HTTP services with easy and simple way that returns only data not view.
    2. WEB API helps to build REST-ful services over the .NET Framework and it also support content-negotiation(it's about deciding the best response format data that could be acceptable by the client. it could be JSON,XML,ATOM or other formatted data), self-hosting which are not in MVC.
    3. WEB API also takes care of returning data in particular format like JSON, XML or any other based upon the Accept header in the request and you don't worry about that. MVC only return data in JSON format using JsonResult.


    4. In WEB API the request are mapped to the actions based on HTTP verbs but in MVC it is mapped to actions name.
    5. ASP.NET WEB API is new framework and part of the core ASP.NET framework. The model binding, filters, routing and others MVC features exist in WEB API are different from MVC and exists in the new System.Web.Http assembly. In MVC, these features exist within System.Web.Mvc. Hence WEB API can also be used with ASP.NET and as a stand-alone service layer.
    6. You can mix WEB API and MVC controller in a single project to handle advanced AJAX requests which may return data in JSON, XML or any others format and building a full blown HTTP service. Typically, this will be called WEB API self-hosting.
    7. When you have mixed MVC and WEB API controller and you want to implement the authorization then you have to create two filters one for MVC and another for WEB API since both are different.
    8. Moreover, WEB API is light weight architecture and except the web application it can also be used with smart phone apps.

Question: Can you return view by using WEB API method?	
Unlike ASP.NET MVC, WEB API is used to return only data. The data can be string, JSON, XML, Text etc. It cannot return View like ASP.NET MVC.
Question: Can you change WEB API action name like ASP.NET MVC?	
Like ASP.NET MVC, you can also change WEB API action name by using ActionName attribute as given below:
[HttpGet] [ActionName("GetProducts")]
public IEnumerable<Product> ProductList()
{return db.Products.AsEnumerable();}
Question: Can you restrict a WEB API action method to be invoked only by HTTP GET, POST, PUT or DELETE?	
Like ASP.NET MVC, you can also restrict WEB API action method to be invoked only by a specific HTTP request by applying HttpGet or HttpPost or HttpPut or HttpDelete attribute.
If you want to restrict an action method for HTTP Get request only then decorate it with HttpGet action method selector attribute as given below:
[HttpGet]
public IEnumerable<Product> ProductList()
{return db.Products.AsEnumerable();}
Question: How to call WEB API in ASP.NETMVC?	
ASP.NET WEB API can be called by using HttpClient and WEB API address as given below:
public class ProductController : Controller
{HttpClient Client = new HttpClient();
Uri BaseAddress = new Uri("http://localhost:131/"); public ActionResult Index()
{Client.BaseAddress = BaseAddress;
HttpResponseMessage response =
Client.GetAsync("productservice/GetProducts").Result;
if (response.IsSuccessStatusCode)
{var data = response.Content.ReadAsAsync<IEnumerable<Product>>().Result; return View(data);}
return View();
}}
Question: How ASP.NET API routing is different from ASP.NET MVC routing?	
ASP.NET MVC and ASP.NET WEB API both use routing to monitor incoming request and at least one route is defined in order to function. The difference between these two routing is given below:
    1. In WEB API route pattern {action} parameter is optional but you can include an {action} parameter. In ASP.NET MVC {action} parameter is mandatory.
    2. The action methods defined in the API controller must either have the HTTP action verbs (GET, POST, PUT, DELETE) attribute or have one of the HTTP action verbs as a prefix for the actions methods name. In ASP.NET MVC, by default an action method can be called by HTTP GET or POST verbs and for using others HTTP verbs you need to defined as an attribute.
    3. Unlike ASP.NET MVC, Web API can receive only one complex type as a parameter.

Question: How to enable Attribute Routing in ASP.NET WEB API2?	
Enabling attribute routing in your ASP.NET WEB API2 is simple, just add a call to MapHttpAttributeRoutes()
method with in Register() method of WebApiConfig.cs file.
public static class WebApiConfig
{ public static void Register(HttpConfiguration config)
{ //enabling attribute routing config.MapHttpAttributeRoutes();}}
You can also combine attribute routing with convention-based routing.
public static class WebApiConfig
{public static void Register(HttpConfiguration config)
{//enabling attribute routing config.MapHttpAttributeRoutes();
// Convention-based routing. config.Routes.MapHttpRoute( name: "DefaultApi",
routeTemplate: "api/{controller}/{id}", defaults: new { id = RouteParameter.Optional });}}
Question: How to define attribute routing in ASP.NET WEB API2?	
Like ASP.NET MVC5, you can also define attribute routing in WEB API2 at controller level and action level as shown below:
    1. Controller level routing – You can define routes at controller level which apply to all actions within the controller unless a specific route is added to an action.

[RoutePrefix("Service/User")]
public class UserController : ApiController
{ //GET route: api/User
public IEnumerable<string> Get()
{return new string[] { "value1", "value2" };}

[Route("{id}")] //GET route: Service/User/1 public string Get(int id)
{return "value";}

[Route("")] //POST route: Service/User/ public void Post([FromBody]string value)
{}}
    • Action level routing – You can define routes at action level which apply to a specific action with in the controller.
public class UserController : ApiController
{//GET route: api/User
public IEnumerable<string> Get()
{return new string[] { "value1", "value2" };}
[Route("Service/User/{id}")] //GET route: Service/User/1 public string Get(int id)
{return "value";}
[Route("Service/User/")] //POST route: Service/User/ public void Post([FromBody]string value)
{}}
