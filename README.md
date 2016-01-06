# telemetryTest
hxcpp issue 333

you can see the difference (from from https://github.com/jcward/hxtelemetry/tree/master/test/DisplayingABitmap) in:
madrazo/telemetryTest@6f7b525

Added "set" flags in XML so it runs "telemetry" and "legacy". Just need to run : 
"lime test project.xml windows" or
"lime test project.xml windows -DHXCPP_GC_MOVING"
or with -DHXCPP_DEBUG_LINK

We actually call Assets.getText between each parse and store this data, but this example encapsulates the issue that is in Xml.parse. With our real XMLs, we get a crash after parsing two or three 2-4 MB xml files.

It crashes both Moving and not Moving on "9"

It crashes when opening hxScout beforehand.
