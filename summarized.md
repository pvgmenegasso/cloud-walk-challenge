Summarized problem:
    
    **answer InfinitePay's clients automatically in the chat in a **
    **proper way to solve the client problem**.
    
- Details:

    * You have access to systems in the form of APIs in whih you can check client's problems and 
    the needed information to solve them.
    
    * Check what chats are opened/active, and, for each chat, check what is the client's 
    complaints. 
    
    * Using the APIs and database tables that are available, show us how you would build a 
    software to automatically answer the client in a proper way.
    
    * Consider that instead of a SQLite Database (it's attached to this email), it's a PostgreSQL 
    deployed in a GCP Cloud SQL. The APIs you have access were deployed on App Engine.
    
    * Remember that the solution needs to be **scalable in case both the number of chats and the** 
    **number of potential problems a customer may have increase (in which case it should be easy**
    **to patch the automatic solution to a frictionless new problem)**.
    
-- ## Personal Considerations :

1 - The problem requires you to *ANSWER CLIENTS AND PROPOSE A SOLUTION ?*

2 - Chats need to be polled in order to verify if clients are active or not

3 - SHOW how a software would be built. Not exaclty the software itself

4 - Solution needs to be scalable -> Microservices, Spawning servers to solve problems


---------###---###-----  First sketch :   -----###---###--------------///


Polling server manages chat activity
and spawns solvers

||===================||
||                   ||     Request       -------------
||  Polling Server   ||---------------=> ||  CHAT API ||
||                   ||                  ||           ||
||==================== <=----------------------/
          |          active conversation ID's
          |          
          |
          |
          |
          |     
          |----------------     
          
          
Problems have levels according to cost:
    level 0  : CLient just wants an information and system can respond
    level 1  :  Client needs a problem solved, but it is a flux that has
                already been predicted, so it can be solved by an autonomous agent
    level 2  : System cannot solve user's problem and it will need human intervention
    
    
    
    
    
STACKS:

    KIBANA
    KAFKA                |
    KUBERNETES           |  ->  STRIMZI
    
    
    
    
    