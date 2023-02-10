# **Remote Control** (V. 1.0)
## **Description**
Remote Control is a **Windows Forms** application which enables you to control an external device through **emails**. The window is minimized and does not appear in the taskbar to prevent unnecessary distraction (definitly not to hide the possible virus from the victim). After starting the executable file (.exe) for the first time, Remote Control will **run automatically** at startup.
## **Instruction**
### **Change Sender/Receiver Email**
The sender email sends commands to `guidomobil200@gmail.com`, the receiver email. It's a publicly accessible email provided by myself (be aware that multiple users could use the same receiver which might cause a mixing of data traffic. I recommend to create an own **GMAIL (!)** for your personal usage). You have to change **line 50**:
```cs
emailMessage.From.Add(new MailboxAddress("Your Name", "yourEmail@gmail.com"));
```
Changte the sender email in **line 51**:
```cs
emailMessage.To.Add(new MailboxAddress("Your Name", "yourEmail@gmail.com"));
```
### **Send commands**
After starting the program, `guidomobil200@gmail.com` will respond to following commands:
- `getMic <seconds>` -> Get a x seconds long audio recording.
- `getWebcam` -> Get a picture shot by the webcam
- `screenshot` -> Get a screenshot
- `shutdown` -> Shut down the PC
<!---->
Just write an email to `guidomobil200@gmail.com` with the command in the subject.

## **Performance**
The PC's performance will decrease. Default, Remote Control will check for commands **all 20 seconds**. If you want a slightly better performance, change **line 70**:
```cs
Thread.Sleep(20000/*amount of ms*/);
```


## **Early Version**
Be aware that this is an early version of Remote Control. The Code is not optimized well and is vulnerable for errors.

## **Disclaimer**
Remote Control is thought to be used for your own devices and educational purpose only. Do NOT abuse Remote Control to harm anyones privacy. By using my code, you agree to be liable for any legal claims generated by its use.
