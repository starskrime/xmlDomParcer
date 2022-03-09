# xmlDomParcer
Sample application for parsing xml response


Parsing Alexa API XML Response
This example shows how to use the DOM parser to parse the XML response from Alexa’s API.

1.1 Send a request to the following Alexa API.

Terminal

https://data.alexa.com/data?cli=10&url=day.az  
1.2 The Alexa API will return the following XML response. The Alexa ranking is inside the POPULARITY element, the TEXT attribute.

<!--
 Need more Alexa data?  Find our APIs here: https://aws.amazon.com/marketplace/seller-profile?id=4a9dbf38-88b1-4e87-a459-271154a77d2e 
-->
<ALEXA VER="0.9" URL="day.az/" HOME="0" AID="=" IDN="day.az/">
<SD>
<POPULARITY URL="day.az/" TEXT="5011" SOURCE="panel"/>
<REACH RANK="4815"/>
<RANK DELTA="+802"/>
<COUNTRY CODE="AZ" NAME="Azerbaijan" RANK="63"/>
</SD>
</ALEXA>
1.3 We using a DOM parser to directly select the POPULARITY element and print out the value of the TEXT attribute.

