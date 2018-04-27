# **JSF**

* It stands for Java Server Faces.
* It's a server-side java framework for web development.
* JSF such as features,example,validation,bean validation,managed bean,facelets etc.

## **JavaServer Faces**

* To develop web applications & it is writtern in java.
* It also provides server-side validation,data conversion,accessibility etc.
* JSF Tag libraries are used to add components on the web page.

## **JSF Installation**

* To download java IDE  higher version used NetBean IDE 8.2.
* The default server install ed along with NetBean IDE 8.2.
* Latest JSF libraries are automatically installed with the IDE & don't need to install it manually.

## **JSF Features**

* Component Based Framework.
* Support HTML5.
* Bean Annotations.
* Inbuilt AJAX Support.
* Default Exception Handling.

## **JavaServer Faces LifeCycle**

1. Execute Phase
2. Render Phase

To refer this link [https://www.javatpoint.com/jsf-life-cycle](https://www.javatpoint.com/jsf-life-cycle)

## **JSF Managed Bean**

* It's a pure java class.
* It contains set of properties & set of getter,setter methods.

#### **Functions that managed bean methods:**

1. Validation.
2. Handling some event.
3. Performing process to the next page.

#### **Ex:**

```
public class User{
private String name;
public String getName(){
return name;
}
public void setName(String name){
this.name=name;
}
}
```

You can use this bean by folowing ways.

1. By conifiguring into xml file.
2. By using annotations.

#### **Configuring Managed Bean into XML file**

```
<managed-bean>
<managed-bean-name>user</managed-bean-name>
<managed-bean-class>User</managed-bean-class>
<managed-bean-scope>session</managed-bean-scope>
</managed-bean>
```

#### **Configuring Managed Bean Using Annotations**

```
import javax.faces.bean.ManagedBean;
import javax.faces.bean.RequestScoped;
@ManagedBean
@RequestScoped
public class User{
private String name;
public String getName(){
return name;
}
public void setName(String name){
this.name=name;
}
}
```

@ManagedBean annotation in a class automatically registers that class as a resource with the JSF.

@RequestScoped annotation is used to provide scope for ManagedBean.

#### **Scopes for a bean class by the following:**

* **Application\(@ApplicationScoped\): ** Across all users Interactions with a web app.
* **Session\(@SessionScoped\): ** Across multiple HTTP requests in a web app.
* **View\(@ViewScoped\): **Interactions with a single page of a web app.
* **Request\(@ReuestScoped\): ** During a  single HTTP request in aweb app.
* **None\(@NoneScoped\): **Scope is not defined for the app.
* **Custom\(@CustomScoped\): ** A userdefined,nonstandable scope.

#### **Eager Managed Bean**

It's lazy by default.

```
@ManagedBean(eager=true)
```

## **JSF Example**

To refer this link [https://www.javatpoint.com/jsf-example](https://www.javatpoint.com/jsf-example)

### **Create a new project**

By using NetBeans IDE 8.2

#### **steps**

1. Choose Project--&gt;Java Web--&gt;Web Application--&gt;Next
2. Name and Location--&gt;Enter Project Name--&gt;Next
3. Server and Setting--&gt;Select Server--&gt;Java EE Version--&gt;Next
4. Frameworks--&gt;JavaServer Faces--&gt;Registered Libraries--&gt;Finish

### **JSF User Interface Component Model**

* Rendering model -To render the components in various ways.
* Conversion model -To register data converters onto a components.
* Event and Listener model -To handle component events.
* Validation model -To register validators onto a components.

### **JSF User Interface Components**

* It represents HTML form components and other basic HTML elements.

| Tag | Rendered as |
| :--- | :--- |
| h:inputText | An HTML &lt;input type="text"&gt; element |
| h:outputText | Plain text |
| h:form | An HTML &lt;form&gt; element |
| h:commandButton | An HTML &lt;input type=vaue&gt; element |
| h:inputSecret | An HTML &lt;input type="password"&gt; element |
| h:inputTextArea | An HTML &lt;input type="textarea"&gt; element |
| h:commandLink | An HTML &lt;a href&gt; element |
| h:inputHidden | An HTML &lt;input type="hidden"&gt; element |
| h:inputFile | An HTML&lt;input type="file"&gt; element |
| h:graphicImage | An HTML &lt;img&gt; element |
| h:dataTable | An HTML &lt;table&gt; element |
| h:message | An HTML &lt;span&gt; tag if styles are used |
| h:messages | A set of HTML &lt;span&gt; tags if styles are used |
| h:outputFormat | Plain text |
| h:outputLabel | An HTML &lt;label&gt; element |
| h:outputLink | An HTML &lt;a&gt; element |
| h:panelGrid | An HTML &lt;table&gt; element with &lt;tr&gt; and &lt;td&gt; |
| h:panelGroup | A HTML &lt;div&gt; or &lt;span&gt; element |
| h:selectBooleanCheckbox | An HTML &lt;input type="checkbox"&gt; element |
| h:selectManyCheckbox | A set of HTML &lt;input&gt; elements of type checkbox |
| h:selectManyListbox | An HTML&lt;select&gt; element |
| h:selectManyMenu | An HTML &lt;select&gt; element |
| h:selectOneListbox | An HTML&lt;select&gt; element |
| h:selectOneMenu | An HTML&lt;select&gt; element |
| h:selectOneRadio | &lt;input type="radio"&gt; element |
| h:column | A column of data in an HTML table |

To refer this link [https://www.javatpoint.com/jsf-ui-components](https://www.javatpoint.com/jsf-ui-components)

### **UI Components Ex**

To refer this link [https://www.javatpoint.com/jsf-ui-components-example](https://www.javatpoint.com/jsf-ui-components-example)

#### **JSF Validation**

* A set of standard classes and associated tags use to validate elements data.

| Validator class | Tag |
| :--- | :--- |
| BeanValidator | &lt;f:validateBean&gt; |
| DoubleRangeValidator | &lt;f:validateDoubleRange&gt; |
| LengthValidator | &lt;f:validateLength&gt; |
| LongRangeValidator | &lt;f:validateLongRange&gt; |
| RegexValidator | &lt;f:validateRegex&gt; |
| RequiredVaidator | &lt;f:validateRequired&gt; |

For more details to refer this link [https://www.javatpoint.com/jsf-validation](https://www.javatpoint.com/jsf-validation)

### **JSF Standard Converters**

* To convert component data.
* The purpose is to take String-based data from Servlet API and convert it to strongly typed java object.

#### **JSF Converters**

| Class | Converter ID |
| :--- | :--- |
| BigDecimalConverter | javax.faces.BigDecimal |
| BigIntegerConverter | javax.faces.BigInteger |
| BooleanConverter | javax.faces.Boolean |
| ByteConverter | javax.faces.Byte |
| CharacterConverter | javax.faces.Character |
| DateTimeConverter | javax.faces.Datetime |
| DoubleConverter | javax.faces.Double |
| EnumConverter | javax.faces.Enum |
| FloatConverter | javax.faces.Float |
| IntegerConverter | javax.faces.Integer |
| LongConverter | javax.faces.Long |
| NumberConverter | javax.faces.Number |
| ShortConverter | javax.faces.Short |

#### **JSF Data-Conversion Core Tags**

| Tag | Function |
| :--- | :--- |
| f:converter | To add an arbitrary converter to the parent component |
| f:convertDateTime | To add DateTimeConverter instance to  parent component |
| f:convertNumber | To add NumberConverter instance to the parent component |

For ex to refer this link [https://www.javatpoint.com/jsf-standard-converters](https://www.javatpoint.com/jsf-standard-converters)

#### **JSF f:convertDateTime**

For ex to refer this link [https://www.javatpoint.com/jsf-convertdatetime](https://www.javatpoint.com/jsf-convertdatetime)

#### **JSF f:convertNumber**

For ex to refer this link [https://www.javatpoint.com/jsf-convertnumber](https://www.javatpoint.com/jsf-convertnumber)

### **JSF Referencing Bean**

#### **Referencing Attributes**

| Attribute | Function |
| :--- | :--- |
| action | To performs navigation processing for the component   and returns a logical outcome String |
| actionListner | To handles action events |
| validator | To perform validation on the component's value |
| valueChangedListner | To handles value-change events |

For ex to refer this link [https://www.javatpoint.com/jsf-referencing-managed-bean-method](https://www.javatpoint.com/jsf-referencing-managed-bean-method)

## **Facelets**

* It's a light weight page declaration language.
* Used to built JavaServer Faces views using HTML style.

To refer this link [https://www.javatpoint.com/facelets](https://www.javatpoint.com/facelets)

### **Facelets Templates**

* It's a tool which provides the facility to implement the user interface.

#### **Templates Tags**

| Tag | Function |
| :--- | :--- |
| ui:component | Created and added to the component tree |
| ui:composition | Optionally uses a template.Outside of this tag is ignored |
| ui:debug | To define a debug component create & add to the tree |
| ui:decorate | Similar to composition tag but not disregard outside this tag |
| ui:define | Inserted into a page by a template |
| ui:fragment | Similar to component tag but not disregard outside this tag |
| ui:include | Encapsulate and reuse content for multiple pages |
| ui:insert | Insert content into a template |
| ui:param | Pass parameters to an included file |
| ui:repeat | An aternative for loop tags,such as c:forEach or h:dataTable |
| ui:remove | To remove content from a page |

For ex to refer this link [https://www.javatpoint.com/facelets-templates](https://www.javatpoint.com/facelets-templates)

## **JSF Comoposite Component**

* The concept of composite components with Facelets.
* It's a special type of template that acts as a component in your appication.

For ex to refer this link [https://www.javatpoint.com/jsf-composite-components](https://www.javatpoint.com/jsf-composite-components)

## **JSF Web Resourses**

* It includes image,script files and any user-created component libraries.
* It provides &lt;h:graphicimage/&gt;tag to access image in web application.

For ex to refer this link [https://www.javatpoint.com/jsf-web-resources](https://www.javatpoint.com/jsf-web-resources)

### **JSF Relocatable Resources**

#### **Following attributes**

**head :**Used to render the resource in head section.

**body :**Used to render the resource in the body section.

**form :**Used to render the resource in the form section.

For ex to refer this link [https://www.javatpoint.com/jsf-relocatable-resources](https://www.javatpoint.com/jsf-relocatable-resources)

### **HTML5-Friendly Markup**

JSF supports for HTML falls into two categories:

* Pass-through elements
* Pass-through attributes
