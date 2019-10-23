# AltSO-Z4002 ( ION API )
The AltSO-Z4002 Standard is currently a concept being designed to establish a standard information structure for internet accessible domains over http. 

## What is ION?
`ION` is an acronym for `Information Object Notation` which is intended to create a information first `JSON` data schema that allows http clients to consume and display the information to a user without needing to know domain specific locations for the information. 

## ION and JSON
`JSON` is what `ION` is using as a data payload structure, the `Object Notation` part of `ION` is representation of that delivered structure while being indicative of information.  

## Problem
Locating information about a domain can be difficult and there is many different ways a domain owner can serve up that information, websites are the most common way to deliver information to users of a domain but it still remains inconsistent due to design preferences and layouts where consistency is only considered with respect to the users experience while attempting to maintain a good user interface that meets their design needs.

Most of the time websites do allow a close enough consistent experience where the user knows to look for things like contact information either in a menu on the top left or right of the screen or in the lower area of the page where content listings are placed, however, even in this example it can some times be unclear if such information exists and the user is forced to spend time clicking around multiple pages only to discover that they're looking for information that does not exist.

## Solution
Create a standard information schema that can be consumed by a common interface to display information about a website domain while maintaining consistency in how a user interacts to get the information or simply inform the user that the information is not available for the given domain.

## Interface/Client
An Interface/Client is simply a desktop or mobile application chosen by the user to be their preferred consistent experience for browsing `ION` supported domains, it is the interface's responsibility to ensure the users experience is not altered from domain to domain and remains consistent. Only the information should be what changes and the interface remains functionally the same.

## HTTP URI
`{domain.tld}/ion` would be the root path for which the interface will be developed to seek a listing of supported `ION` features. The absence of this path indicates the domain does not support `ION` and the user is easily made aware by the interface being able to indicate an unsupported domain.

## Schema
`{domain.tld}/ion` This URL should return a payload that indicates the version of `ION` being used on the given domain and the features supported.

The version may be used by the interface to inform the user when their client is out of date with the version of `ION` data being delivered and that new features may be available to them if a client update is available.

## Features
A feature is a separate section of the `ION` URI that when accessed will deliver information to the interface specific for rendering based on the given feature.

The default feature that should be supported by all domains is the `basic` feature that provides a `title` and `description` for the domain.

Other features such as `contact` `locations` `products` will be designed and documented for interfaces to follow.
Eventually a domain owner may be able to rely on `ION` and an `ION` client to meet all the needs for their users and a website wont need to be anything other than a landing page that directs the user to download an `ION` client.

## Versions
All version changes with the `ION` schema will be backwards compatible within both minor and patched versions for the specifications, only major version changes may deprecate or even remove schema but with full focus on never changing the schema unless absolutely necessary.

## Work In Progress
I am still currently working through the designs and specifications of `ION` and will be contributing more details to this Gitapedia page to help define the initial schema for starting the first wave of `ION` responses.

I will also be opening things up soon for other contributions but please feel free to reach out should you wish to start contributing sooner.
