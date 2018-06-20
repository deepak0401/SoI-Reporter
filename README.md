# SoI-Reporter
I have created a python script “SoI Reporter" - report plugin to export issue list from from Sonar's Issues tab.

How to generate Sonar Issue report:
1.	Login into Sonar portal and go to 'Issues' tab.
2.	To get complete report it is IMPORTANT to load web page fully. To load web page completely, keep scrolling downside to load all issues otherwise generated report will not have all defects.
3.	Once web page is completely loaded, go to HTML code of Issue page. [IMPORTANT: DO NOT USE 'VIEW SOURCE' OPTION.]
	a.	For IE - press F12 key or go to Tools > F12 Developer Tools > 'DOM Explorer' tab.
	b.	For Chrome - press F12 key or press three vertical dots upper right corner of browser > More tools > Developer Tools > 'Elements' tab.
4.	Now select and copy contents starting from <html> tag to </html> tag.
5.	Paste copied contents into txt file and name it 'SonarInput.html'. Please use 'SonarInput.html' name only because as of now it is hard coded in python scripts.
6.	Now go to script folder and open command prompt from this folder and run "GenerateSonarIssuesReport.bat" file.
7.	If you are running this script first time, please choose ‘n’ for “Have you installed all python packages mentioned in README_v2 file?” question. It will automatically download all required plugins
8.	If 'SonarInput.html' file is big in size, script will take long in processing and report generation.
9.	After script execution, it will generated two report formats – HTML and EXCEL in the python script folder.


Known Issues:
1.	For some of the defects where all details are not present that row’s content may shift towards right or left.
