How to use the $from and $from_name parameters:

In the example usage section, you'll see these lines:

$senderEmail = "your_email@example.com";
$senderName = "Your Name";

This is where you set the sender email address and name. Then, when you call the sendEmail() function, you pass these variables as arguments:

if (sendEmail($recipientEmail, $emailSubject, $emailMessage, $senderEmail, $senderName)) {
    // ...
}

Important Reminder:

Provide a $senderEmail! If you don't, the code falls back to using noreply@example.com, which you must change to a valid email address that you control, and which is from your own domain. Not providing a From: header (or providing an invalid one) is the #1 reason why mail() function calls fail.

Sanitize Inputs: The code already sanitizes the $from and $from_name parameters using filter_var(). This is a critical security measure to prevent header injection attacks.

Domain Alignment (SPF/DKIM): For best deliverability, ensure that the $senderEmail is an address from your own domain and that your domain has properly configured SPF and DKIM records.

Therefore, the code already does what you asked. You just need to replace the placeholder values in the example usage section with your desired sender email and name. If you're still having trouble, please provide more details about what you're trying to do and what's not working.
