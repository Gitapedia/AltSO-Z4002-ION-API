# AltSO-Z4002 ( ION API )
The AltSO-Z4002 Standard is currently a concept being designed to establish a standard information structure for internet accessible domains over http. 

## What is ION?
`ION` is an acronym for `Information Object Notation` which is intended to create a information first `JSON` data schema that allows http clients to consume and display the information to a user without needing to know domain specific locations for the information. 

## ION and JSON
`JSON` is what `ION` is using as a data payload structure, the `Object Notation` part of `ION` is representation of that delivered structure while being indicative of information.  

## Problem
Locating information about a domain can be difficult and there is many different ways a domain owner can serve up that information, websites are the most common way to deliver information to users of a domain but it still remains inconsistent due to design preferences and layouts where consistency is only considered with respect to the users experience while attempting to maintain a good user interface that meets their design needs.
Most of the time websites do allow a close enough consistent experience where the user knows to look for things like contact information either in a menu on the top left or right of the screen or in the lower area of the page where content listings are placed, however, even in this example it can some times not be clear if such information exists or not and the user has to spend some time and multiple page clicks to finally discover that they're looking for information that does not exist.

## Solution
Create a standard information schema that can be consumed by a common interface to display information about a website domain while maintaining consistency in how a user interacts to get the information or simply informed the information is not available for the given domain.

## Interface
A common interface would be one that the user has chosen to be their preferred interface to use for browsing ION data for domains, typically this would be a desktop or mobile application that uses the domain as the landing address to then pull up the `ION` data and display in a consistent layout where the layout remains the same from domain to domain and only the presence or absence of the information is the changing factor.

## HTTP URI
`{domain.tld}/ion` would be the root path for which the interface will be developed to seek a listing of supported `ION` features. The absence of this path indicates the domain does not support `ION` and the user is easily made aware by the interface being able to indicate an unsupported domain.

## Schema
`{domain.tld}/ion` This URL should return a payload that indicates the version of `ION` being used on the given domain and the features supported.

## Features
A features is a separate section of the `ION` URI that when accessed will deliver information to the interface specific for rendering based on the given feature.
The default feature that should be supported by all domains is the `basic` feature that provides a `title` and `description` for the domain, beyond this you then have other features such as `contact` `locations` `products` and more as they get introduced with the intention that eventually a website should be able to rely on `ION` and an `ION` client to meet all the needs for a user who is not interested in a designed interface and instead a quick user experience.

## Versions
The schema will take into account a need for evolution and expansion where new schema types and keys will be added over version iterations but no previously established schema version will change allowing for that reliable consistent experience even on older interfaces not yet updated to a latest version.

## Work In Progress
I am still currently working through the designs of `ION` and will be contributing more details to this Gitapedia page to help define the overall design and even open up to contributions later as things start to take shape.
