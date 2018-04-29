# Web-Content-Authenticator
This is a Firefox plugin which gives a confidence score to each of the links returned by the Google Search Engine.

<ul>
  <li><a href="#Intro">Introduction</a></li>
    <li><a href="Depth">In-Depth</a></li>
  </ul>
  
  <p id="Intro">This project is based on the fact of how much we can trust a link found over the Internet. This is a firefox plugin powered by a python Django framework in the backend which calculates a score for each link returned by the Google search engine after considering various factors.
  </p>
  
  <p id="Depth">
  <b>Factors Considered </b>
  The factors which are considered now is whether the links has SSL security protocol, domain of the links, Sentiment Analysis of the Web Content and then presence of any Malicious URLs.
  
  SSL Security of website is detected using the presence of http or https protocol in the URL.
  The domains in the list [org,edu etc] are given higher priorities if found in the links, then comes the government websites such as [in,uk, etc] followed by the commercial websites.
  Then Content is picked up from the Website and Sentiment Analysis is done over it inorder to check for any Negative content.
  After that presence of any Malicious URLs is detected using a model trained under logistic regression.
  Then the results are stored under a Matrix Format which is processed for each website under the google search result.
  Then a correlation function is applied on these resultset to generate a score which is in between 0 and 1 . Higher the score, better trust worthy are the links.
  </p>
  
# Future developments
This is a under-fitting model of authenticating websites. So further analysis and development is required.
We have planned to consider various number of factors to contribute to give a more appropriate score. Such as number of web trackers working in the websites, number of out going links, Using Sentimental analysis for getting the motive of the content, do a back ground search of the author who wrote it.
Application of Zipf's law and Benford's law to detect fraud webpages, Implementing the relatedness of the words in Website and URLs to the main content as more the related they are more authentic they are.
Involvement of High Level Topics like Clickabity, More Advanced Mathematics, History of the Website(background of the Website Developer and Hosting Platform) could be added to check Authenticity of the Site.
Finally Overall Improvement in the Structure and Implementation of the API can be done by adding Parallel Processing, including more Powerful Platforms for better and faster processing.
Working on more advanced model , so that more better score can be assigned on the basis of all features, To develop a neural network for assigning scores to all the links, To do cross validation for verifying the result. 
