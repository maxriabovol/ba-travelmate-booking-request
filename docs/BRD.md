Business Requirements Document(BRD) Template

Project/Initiative

Month 20YY

Version X.XX

Company Information





# Document Revisions







Date



Version Number



Document Changes





05/02/20xx



0.1



Initial Draft





















































































































# Approvals







Role



Name



Title



Signature



Date





















































































































































































# Introduction





## Project Summary





### Objectives

Structure the process of selecting a room, making a payment, and confirming a reservation by creating a reservation form. The goal is to increase reservation conversion rates by improving the user experience and reducing the time it takes to fill out the form to 5 minutes.





### Background

Provide a brief history of how the project came to be proposed and initiated, including the business issues/problems identified, and expected benefit of implementing the project/developing the product.





#### Business Drivers

[List the business drivers that make development of this product important. These can be financial, operational, market or environmental.*



## Project Scope

The hotel is restructuring and improving its booking process.





### In Scope Functionality





Displaying a full breakdown of service costs prior to payment.  



Displaying cancellation policies and a list of what is included in the price.  



Making Online Payments: Apple Pay and Credit/Debit Cards  



Sending the user a PDF receipt via email along with the booking confirmation.  



Displaying the booking status in the user's account.  



Allowing the user 15 minutes to retry the payment if the first attempt failed,while the room remains unavailable for booking by other users.  



Processing payments via a secure payment gateway.





### Out of Scope Functionality



Processing refunds for cancelled reservations.



Paying for a reservation with cryptocurrency



User Support Chat.



And anything not specifically mentioned in scope





## System Perspective*\[Provide a complete description of the factors that could prevent successful implementation or accelerate the projects, particularly factors related to legal and regulatory compliance, existing technical or operational limitations in the environment, and budget/resource constraints.\]*





Assumptions



Constraints









Risks









.





### Issues









# Business Process Overview

Describe how the current process(es) work, including the interactions between systems and various business units. Include visual process flow diagrams to further illustrate the processes the new product will replace or enhance.

 Use case documentation and accompanying activity or process flow diagrams can be used to create the description(s) of the proposed or “To-Be” processes.





## Current Business Process (As-Is)

At any point during or after deployment of web apps or web sites (internal or external) to support business activities, development/support teams may create and deploy widgets. 





CMS / database administrators for the employee portal use the CMS tool to create widgets. They can test widgets in the designated staging environment, then register them and deploy to production.



Development teams may deploy widgets to development and testing environments set up for their development projects. They must check widget code into and out of the source code repository according to their projects’ development schedule.







## Proposed Business Process (To-Be)



Technical Lead searches repository



If widget is not found, user creates a new widget name record.



WINS validates that all fields have been completed.



WINS confirms that no similar widgets exist



User confirms record to be created.





User searches repository to locate existing widget description.



WINS displays record



User selects Edit to open and modify record



WINS validates all fields completed correctly



User confirms changes.



WINS confirms changes and updates Audit table.





# Stakeholder Requirements

SR-001

Users want to receive a transparent breakdown of the cost of their stay before confirming their reservation.

SR-002

Users want access to complete information about the cancellation policy and what is included in the cost of their stay.

SR-003

Users expect to be able to view the current status of their reservation at any time.

SR-004

Users expect to receive a reservation confirmation email immediately after making a reservation.

SR-005

The business owner expects users to be able to make payments through a reliable payment gateway.

SR-006

The business owner expects that user data will be protected from unauthorized access.

SR-007

The business owner expects the room to remain reserved for 15 minutes after a failed booking so that the user can book it again.

The requirements in this document are prioritized as follows:







Value



Rating



Description





1



Critical



This requirement is critical to the success of the project. The project will not be possible without this requirement.





2



High



This requirement is high priority, but the project can be implemented at a bare minimum without this requirement.





3



Medium



This requirement is somewhat important, as it provides some value but the project can proceed without it.





4



Low



This is a low priority requirement, or a “nice to have” feature, if time and cost allow it.





5



Future



This requirement is out of scope for this project, and has been included here for a possible future release.





## Functional Requirements







Req



Priority



Description



Rationale



Use Case Reference



Impacted Stakeholders





General / Base Functionality

























FR-G-001



1



After successfully completing the reservation form and before making a payment, the user must receive information about the cancellation policy, a complete list of services included in the reservation price, and a detailed breakdown of the cost, including the room rate, taxes, and other additional fees.



To provide users with detailed information about pricing and cancellation policies, and to minimize misunderstandings.







Guest,Hotel management





FR-G-002



1



The system must allow users to pay for reservations online using Apple Pay, Google Pay, or a credit card through an integrated payment gateway: Stripe/PayPal.



To provide users with a convenient payment method







Guest,Hotel management





FR-G-003



1



Once the user fills out the reservation form and successfully completes the online payment, the system should send them an email confirming the reservation and a PDF receipt.



. To inform the customer that their reservation was successful.







Guest,Hotel management





FR-G-004







If the online reservation is completed successfully, the system automatically changes the status of the corresponding reservation to “Reserved” and removes the room from the list of rooms available for reservation, changing its status to “Unavailable” and reflecting the latest changes in the user’s account.



To prevent double bookings.







Guest,Hotel management





FR-G-005







If the booking process fails due to a technical error or a failed payment, the system temporarily reserves the room the user attempted to book for 15 minutes, changing its status to “Temporarily Reserved,” to give the user time to make a new booking.



To ensure that the customer can book the exact room they intended to book.







Guest,Hotel management





Security Requirements

























FR-S-001



1





















Reporting Requirements

























FR-R-001



2





















Usability Requirements

























FR-U-001



1





















Audit Requirements

























FR-A-001



1





















Non-Functional Requirements



   Include technical and operational requirements that are not specific to a function. This typically includes requirements such as processing time, concurrent users, availability, etc.







ID



Requirement





NFR-001



The system must confirm a reservation no later than 3 seconds after it is created.





NFR-002



The system must support 100 concurrent users.





NFR-003



The time it takes for the system to respond after the user clicks the “Pay” button should not exceed 2 seconds.





NFR-004



The system must hold the user's funds on the card until the hotel confirms payment.





NFR-005



The system must ensure full compliance with the PCI DSS standard, prohibit the storage of CVV codes in the database, and encrypt user data to protect personal information.





# Appendices





## List of Acronyms

[If needed, create a list of acronyms used throughout the BRD document to aid in comprehension.*



## Glossary of Terms

[If needed, identify and define any terms that may be unfamiliar to readers, including terms that are unique to the organization, the technology to be employed, or the standards in use.*



## Related Documents

[Provide a list of documents or web pages, including links, which are referenced in the BRD.*

