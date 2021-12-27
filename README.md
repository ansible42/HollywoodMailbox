# HollywoodMailbox
This is a extension to that LabVIEW actor-framework which adds the concept of message registration and mailboxes. 

## Concept 

Adds the ability for mailbox clients to register for a message type, all messages of that type that are sent to the post office are delivered to the actors that have registered for them.  This means that these actors must implement the interface for that particular message type.  

The idea behind this is that an actor need not know where a message might come from but it knows how to handel that actor.  

The idea being that when an application is built around this logical groupings of actors would register for the same set of messages, and each actor would implement that message in it's own way.  


###  Additional concepts 

Message interface properties 

*    Using interfaces it is possible to give messages the ability to interface with non actor-framework messages such as a STM message.  The idea being that while all messages within the app are actor messages, those messages may impliment the interface for a different system.  

### Thanks 

@AristosQueue got me thinking about this and made me think about systems like this in a more abstract way and helping me get to the next level of understanding with AF. 
