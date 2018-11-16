In the file seacms/include/mkhtml.func.php, line 1172
![change password](1.png "")
The $topicId parameter has no single quote protection, making GPC's global single quote protection invalid. In seacms/admin/admin_makehtml.php, line 410, the makeTopicById function is called.
![change password](2.png "")

This request is called when the web page is generated in the background.
![change password](3.png "")
Then the topic parameter can be SQL injected.
![change password](4.png "")
