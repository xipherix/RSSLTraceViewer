# RSSLTraceViewer

This project provide binary file for RSSLTraceViewer application with sample xml tracing log from RFA and EMA C++ or .NET API. You can find more details about the API from [https://developers.thomsonreuters.com/](https://developers.thomsonreuters.com/)

This is beta version of the tool and it support the following functionality

1) This tool can open and parse xml fragments from RSSL tracing log from RFA C++/.NET and EMA C++/ETA C. It's not support trace file from RFA/EMA java becuase currently java version of the APIs cannot provide valid XML trace log like the C++ version. However, there is some workaround for EMA Java, user can use text editor to search and replace invalid XML tag from .xml before use it with the tools.

2) It can decode primitive data from RDM domain which contains fieldEntry element which contains attribute named fidId and data. It can docode only field id which available in data dictionary files (RDMFieldDictionary and enumtype.def). If the tracing log contains negative fid or custom fid, user can set location of custom dictionary in app.config.json which is application configuration file.

3) The tool was designed to read the RSSL tracing log and decode MRN real-time news data and shows the Json data inside compressed buffer. You can also save unpacked Json data to file.

4) There are some options to filter data such as stream id, RDM Domain name and key name(item name, user name in request or refresh message). Also user can search GUID in the XML file using search function.

Note that we also provide sample tracing log in SampleTrace.zip file. You can unpack the file and test it with RSSLTraceViewer.

Screenshot.

**MRN Data**
![sceen shot](https://raw.githubusercontent.com/xipherix/RSSLTraceViewer/master/Images/screenshot.jpg)

**Market Price**
![sceen shot](https://raw.githubusercontent.com/xipherix/RSSLTraceViewer/master/Images/screenshot2.png)

**Market By Order**
![sceen shot](https://raw.githubusercontent.com/xipherix/RSSLTraceViewer/master/Images/screenshot3.png)

## Installation

You can just unpack RsslTraceViewer.zip to folder of your choice. 
The tool was created using WPF UI with C# 7.0 so that it required .NET Framework 4.6.1. You can download .NET Framework from [.NET Framework 4.6.1](https://support.microsoft.com/en-sg/help/3102436/the-net-framework-4-6-1-offline-installer-for-windows) or using latest version of .NET Framework.
