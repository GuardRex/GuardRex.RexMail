# RexMail
.NET Core E-mail client library.\r\nCommonly used types:\r\nGuardRex.RexMail.Message

### Ports
The client works with port 465 or port 587 E-mail servers.

### Method
```c#
string serverResult = await GuardRex.RexMail.Message.Send(
    string name, 
    string email, 
    string phone, 
    string department, 
    string message, 
    string server, 
    int port, 
    string smtpServerAccountName, 
    string smtpServerUsername, 
    string smtpServerPassword, 
    string destinationName, 
    string destinationEmail, 
    string destinationSubjectLine);
```

### Response
+===================+=====================================================+
| serverResult Code | Server Response                                     |
+===================+=====================================================+
| x000              | The server response was empty                       |
+-------------------+-----------------------------------------------------+
| x001              | The server responded with fewer than 3 characters   |
+-------------------+-----------------------------------------------------+
| xyyy              | The server responded with a code (yyy) that doesn't |
|                   | match the success code expected                     |
+-------------------+-----------------------------------------------------+

### Version History
Version | Changes Made
------- | ------------
1.0.0   | Initial Release
