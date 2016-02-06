# Amazon-SNS

Amazon Simple Notification Service (SNS) is a push messaging service that makes it simple & cost-effective to push to mobile devices & distributed services. The ITX Amazon SNS adapter allows users to send PUSH notifications from a map.  The Adapter supports only outbound services. 

## Minimum Requirements : 

ITX v9.0.0.x

## Command Alias : 

Adapter commands can be specified by using a command string on the command line or creating a command file that contains adapter commands. The execution command syntax is:

-IM[alias] card_num <br>
-OM[alias] card_num


where 

-IM is the Input Source Override execution command 

-OM is the Output Target Override execution command

alias is the adapter alias, 

card_num is the number of the input or output card. 


The following table shows the adapter alias and its execution command.

Adapter 	:  Amazon Simple Notification Service 

Alias 	        :  ASNS 

As Input        :  -**IMASNS**card_num 

As Output       :  -**OMASNS**card_num 



## Amazon SNS Adapter commands

The following table lists valid commands for the Amazon SNS Adapter. The adapter supports only outbound. 


Topic Name (-C)     : SNS Topic Name  - String (required)

Access Key (-A)	  : Access Key to connect to the SNS Service  - String (required)

Secret Key (-S )  : Secret Key  - String (required)


Region -R : Region - Integer (optional, default is 1)

Values for Region are


US_EAST_1                 1
US_WEST_1                 2
US_WEST_2                 3
EU_WEST_1                 4
EU_CENTRAL_1              5
AP_SOUTHEAST_1            6
AP_SOUTHEAST_2            7
AP_NORTHEAST_1            8
SA_EAST_1                 9
CN_NORTH_1                10
DEFAULT_REGION            11


## Amazon SNS Adapter Command Line Examples

###Outbound Adapter : 

Line :-A ****  -S *** -C ITXIN 

PUT RULE : PUT("ASNS", "-A ****  -S *** -C ITXIN  -T", Input)) 



## Amazon Adapter Installation Instructions 

a) create a folder com.ibm.itx.amazon.sns under WTX INSTALL/jars directory

b) Drop m4sns.jar in to WTX INSTALL/jars/com.ibm.itx.amazon.sns

c) Edit adapters.xml and add the following line


M4Adapter name="Amazon Simple Notificaiton Service" alias="ASNS" id="174" type="app" class="com/ibm/itx/amazon/sns"


d) Download Amazon SNS SDK Java artifacts from [Tools for Amazon Web Services](https://aws.amazon.com/tools/). 

From the zip file, Copy 

aws-java-sdk-1.xxx.jar

commons-codec-1.xx.jar

commons-lang3-xxx.jar.jar

commons-logging-1.xx.jar

pofluent-hc-4.xx.jar

httpclient-xx.jar

httpclient-cache-4.xx.jar

httpcore-4.xx.jar

httpmime-4.xx.jar

jackson-annotations-2.xx.jar

jackson-core-2.xx.jar

jackson-databind-2.x.jar 

joda-time-2.x.jar 


to WTX INSTALL DIR/jars/com.ibm.itx.amazon.sns <br>


d) Invoke cleanextenderstudio.bat to invoke Design Studio
 

####Note : For any defects or usage concerns, please open an issue ticket and shall be addressed. 
