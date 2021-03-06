### Topics  
**Description**:   
AS User   
I WANT to see the list of available topics and add my own topics  
SO THAT I can contribuite to an existing discussion or create a new one  

**Scenarios**:   

#### I see the new topic form  
GIVEN I visit _D-BOARD URL_ /index.php  
WHEN I login in as User  
THEN I see the _ADD NEW TOPIC_ box  
AND I see the _TOPIC TITLE_ field in the _ADD NEW TOPIC_  
AND I see the _ADD_ disabled button in the _ADD NEW TOPIC_ box  

#### I see the available topics  
GIVEN I visit _D-BOARD URL_ /index.php  
AND I have some topics into the DB  
WHEN I login in as User  
THEN I see the _AVAILABLE TOPICS LIST_   
AND I see the topics ordered from the most recent to oldest based on the topic's _CREATED AT_ date  
AND I see the most recent 10 topics  
AND I see each topic has an _OWNER_ label showing the username who created the topic  
AND I see each topic has a _CREATED AT_ label showing the date when the topic has been created  
AND I see each topic has a _TOPIC TITLE_ label in bold showing the title of the topic  
(_OPTIONAL_)  
AND I see at the end of the _AVAILABLE TOPICS LIST_ the _PAGINATION CONTROLS_  
(_OPTIONAL_)  
  
(_OPTIONAL_)  
#### I see the topics _PAGINATION CONTROLS_  
GIVEN I visit _D-BOARD URL_ /index.php  
AND I have 28 topics into the DB  
AND I login in as User  
AND I see the _AVAILABLE TOPICS LIST_   
WHEN I see at the end of the _AVAILABLE TOPICS LIST_ the _PAGINATION CONTROLS_  
THEN I see a '<' link grayed out (_OPTIONAL_)  
AND I see the numbers '1', '2' and '3' clickable links  
AND I see the '>' clickable link  
(_OPTIONAL_)  

(_OPTIONAL_)  
#### I go to the next topic page  
GIVEN I visit _D-BOARD URL_ /index.php  
AND I login in as User  
AND I have 28 topics into the DB  
AND I see the _AVAILABLE TOPICS LIST_   
AND I see at the end of the _AVAILABLE TOPICS LIST_ the _PAGINATION CONTROLS_  
AND I see a '<' link grayed out (_OPTIONAL_)  
AND I see the numbers '1','2' and '3' clickable links  
AND I see the '>' clickable link  
WHEN I click '<'  
THEN I'm redirected to /index.php?page=1  
AND I see the page has the same content of the previous page  
AND  
WHEN I click '>'  
THEN I'm redirected to /index.php?page=2  
AND I see the same page _AVAILABLE TOPICS LIST_   
AND I see the topics are ordered from the most recent to oldest based on the topic's _CREATED AT_ date  
AND I see the most recent 10 topics oldest then the last topic visible in the previous page (/index.php?page=1)  
(_OPTIONAL_)  

(_OPTIONAL_)  
#### I navigate in the topic page  
GIVEN I visit _D-BOARD URL_ /index.php  
AND I login in as User  
AND I have 28 topics into the DB  
AND I see the _AVAILABLE TOPICS LIST_   
AND I see the _PAGINATION CONTROLS_   
WHEN I click on the '3' link into the _PAGINATION CONTROLS_   
THEN I'm redirected to /index.php?page=3  
AND I see the _AVAILABLE TOPICS LIST_   
AND I see the last 8 topics ordered from the most recent to the oldest  
AND  
WHEN I click on the '2' link into the _PAGINATION CONTROLS_   
THEN I'm redirected to /index.php?page=2  
AND I see the _AVAILABLE TOPICS LIST_   
AND I see the topics are ordered from the most recent to oldest based on the topic's _CREATED AT_ date  
AND I see the most recent 10 topics oldest then the last topic visible in the first topic list (/index.php?page=1)  
AND  
WHEN I click on the '<' link into the _PAGINATION CONTROLS_   
THEN I'm redirected to /index.php?page=1  
AND I see the first 10 topics ordered from the most recent to oldest based on the topic's _CREATED AT_ date  
(_OPTIONAL_)  

#### I add a new topic  
GIVEN I visit _D-BOARD URL_ /index.php  
AND I login in as User  
AND I see the _ADD NEW TOPIC_ box  
AND I see the _TOPIC TITLE_ field in the _ADD NEW TOPIC_  
AND I see the _ADD_ button in the _ADD NEW TOPIC_ box  
WHEN type 'My new wonderful topic' in the _TOPIC TITLE_ field  
THEN I see the _ADD_ button enabled  
AND  
WHEN I click the _ADD_ button  
THEN I see the message 'Your topic has been shared in the _D-BOARD_.'  
AND I'm redirected to /index.php after few seconds  
AND I see my new topic at the top of the _AVAILABLE TOPICS LIST_   


#### Click on a topic title  
GIVEN I visit _D-BOARD URL_ /index.php  
AND I have some topics into the DB  
AND I login in as User  
AND I see the _AVAILABLE TOPICS LIST_   
AND I see the topic 'My new wonderful topic'  
AND I know 'My new wonderful topic' has topic ID 10  
WHEN I click on the topic title 'My new wonderful topic'  
THEN I'm redirected to /topic.php?topicID=10  


