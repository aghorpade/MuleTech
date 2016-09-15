This Exmaple demonstrate usage of Velocity template engine and Parse template component to replace static content with dynamic value and use template
to send email to user's

#How To Run -
1.First replace xxxx values in muleflow .xml file with your gmail account details. So SMTP will use your gmail account to send email
2.Run this applicate as Mule Application.
3. Use postman/soapUi/rest client and hit GET http://localhost:8090/send and you will see that email has been sent to TO address with ${firstname}
replaced with amitdemo1 value(this is value is set in java component)
4. Now to test Parse Teamplate - hit POST http://localhost:8090/parser with json body as below 
{
"name":"test",
"fileName":"sa"
} and HTTP header with key - tes and value as demo
you will see email will be sent to user with given values in template.
