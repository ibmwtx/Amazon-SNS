# Amazon-SNS

Amazon Simple Notification Service (SNS) is a push messaging service that makes it simple & cost-effective to push to mobile devices & distributed services. The ITX Amazon SNS adapter allows users to send PUSH notifications from a map.  The Adapter supports only outbound services. 

## Minimum Requirements : 

ITX v9.0.0.x

## Command Alias : 

Adapter commands can be specified by using a command string on the command line or creating a command file that contains adapter commands. The execution command syntax is:

-IM[alias] card_num <br>
-OM[alias] card_num


where -IM is the Input Source Override execution command and -OM is the Output Target Override execution command, alias is the adapter alias, and card_num is the number of the input or output card. The following table shows the adapter alias and its execution command.


Adapter 	:  EXCEL <br>
Alias 	        :  EXCEL <br>
As Input        :  -**IMASNS**card_num <br>
As Output       :  -**OMASNS**card_num <br>    	  


## Amazon SNS Adapter commands

The following table lists valid commands for the Amazon SNS Adapter. The adapter supports only outbound. 

Topic Name (-C)     : SNS Topic Name<br>
Access Key (-A)	  : Access Key to connect to the SNS Service <br>
Secret Key (-S )  : Secret Key <br>

## Amazon SNS Adapter Command Line Examples

###Outbound Adapter : 

Line :-A ****  -S *** -C ITXIN <br>
PUT RULE : PUT("ASNS", "-A ****  -S *** -C ITXIN  -T", Input)) <br>


## Amazon Adapter Installation Instructions 

a) create a folder com.ibm.itx.amaxon.sns under <WTX INSTALL>/jars directory
b) Drop m4sns.jar in to <WTX INSTALL>/jars/com.ibm.itx.amaxon.sns <br>
c) Edit adapters.xml and add the following line <br>

<M4Adapter name="Amazon Simple Notificaiton Service" alias="ASNS" id="174" type="app" class="com/ibm/itx/amazon/sns"/> <br>

d) Download Amazon SNS SDK Java artifacts from [Tools for Amazon Web Services](https://aws.amazon.com/tools/). From the zip file, Copy aws-java-sdk-1.xxx.jar, ccommons-codec-1.xx.jar, commons-lang3-xxx.jar.jar, commons-logging-1.xx.jar, pofluent-hc-4.xx.jar,httpclient-xx.jar, httpclient-cache-4.xx.jar, httpcore-4.xx.jar, httpmime-4.xx.jar, jackson-annotations-2.xx.jar, jackson-core-2.xx.jar, jackson-databind-2.x.jar and joda-time-2.x.jar to <WTX INSTALL DIR>/jars/com.ibm.itx.amaxon.sns <br>

d) Invoke cleanextenderstudio.bat to invoke Design Studio
 

####Note : For any defects or usage concerns, please open an issue ticket and shall be addressed. 
