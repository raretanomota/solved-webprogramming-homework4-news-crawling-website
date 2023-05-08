Download Link: https://assignmentchef.com/product/solved-webprogramming-homework4-news-crawling-website
<br>
In this homework, you will design a news crawling website that parse news from a particular RSS and instantly updates itself.

You have to design <strong>one</strong> web page (<strong>RSSparsing.aspx</strong>) and a class page (<strong>News.cs</strong>) that holds news information.

News .cs

<ol>

 <li>Add a class file named <strong>News.cs</strong> into your project (Add New Item, Class). This file will contain information about the news. If you encounter a message which states that this file should be in <strong>App_Code</strong> folder, then select <strong>Yes</strong> and let Visual Studio create the</li>

</ol>

<strong>App_Code</strong> folder for you and put <strong>News.cs</strong> file in this folder. After then, you will be able <sub> </sub>to use the <strong>News</strong> class in your application like any other classes of .NET library.

public class News

{ public int NewsID; public string Title; public string Description; public string Category; public string Author;

public DateTime PubDate; public string ImageUrl;




public News(int NewsID, string Title, string Description, string Category, string Author, string PubDate, string ImageUrl)

{

this.NewsID = NewsID; this.Title = Title; this.Description = Description; this.Category = Category; this.Author = Author; this.PubDate = PubDate; this.ImageUrl = ImageUrl;

}

}




<h2>Design of <sub>  </sub>RSSparsing.aspx</h2>

This website will be use to parse the xml in the  <a href="http://ajans.dha.com.tr/dha_public_rss.php">http://ajans.dha.com.tr/dha_public_rss.php</a><a href="http://ajans.dha.com.tr/dha_public_rss.php">.</a> The following information about news will be downloaded and stored in a ArrayList. You can consider up to 20 news. Each news should be saved with unique id, which is called as <strong>NewsID</strong>. Information that are needed to be parsed are:

<ul>

 <li><strong>Description </strong></li>

 <li><strong>Category </strong></li>

 <li><strong>Author </strong></li>

 <li><strong>PubDate </strong></li>

 <li><strong>ImageUrl </strong></li>

</ul>

This information of news are located in &lt;item&gt; tag. Therefore, you should consider only &lt;item&gt; tags when parsing the xml file.




<strong>Check List of HW4: </strong>

<ol>

 <li>You should retrieve all information of news from database.</li>

 <li>Then store each news into a news object by using News.cs</li>

 <li>Store each news object into an ArrayList.</li>

 <li>Then bind the ArrayList into your gridview.</li>

 <li>Your gridview should only show the <sub>NewsID, </sub>Title and</li>

 <li>You should use a Nuget logging package. You should write the exception message into logger file by using Nuget logging</li>

</ol>




You can use any Nuget logger package, but I found a special one, which is <a href="https://github.com/serilog/serilog-extensions-logging-file">https://github.com/serilog/serilog</a><a href="https://github.com/serilog/serilog-extensions-logging-file">–</a><a href="https://github.com/serilog/serilog-extensions-logging-file">extensions</a><a href="https://github.com/serilog/serilog-extensions-logging-file">–</a><a href="https://github.com/serilog/serilog-extensions-logging-file">logging</a><a href="https://github.com/serilog/serilog-extensions-logging-file">–</a><a href="https://github.com/serilog/serilog-extensions-logging-file">file</a>