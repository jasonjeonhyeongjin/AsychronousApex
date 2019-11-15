# UseFutureMethods

Create an Apex class that uses the @future annotation to update Account records.
Create an Apex class with a method using the @future annotation that accepts a List of Account IDs and updates a custom field on the Account object with the number of contacts associated to the Account. Write unit tests that achieve 100% code coverage for the class.
Create a field on the Account object called 'Number_of_Contacts__c' of type Number. This field will hold the total number of Contacts for the Account.
Create an Apex class called 'AccountProcessor' that contains a 'countContacts' method that accepts a List of Account IDs. This method must use the @future annotation.
For each Account ID passed to the method, count the number of Contact records associated to it and update the 'Number_of_Contacts__c' field with this value.
Create an Apex test class called 'AccountProcessorTest'.
The unit tests must cover all lines of code included in the AccountProcessor class, resulting in 100% code coverage.
Run your test class at least once (via 'Run All' tests the Developer Console) before attempting to verify this challenge.

# Use Batch Apex
Create an Apex class that uses Batch Apex to update Lead records.
Create an Apex class that implements the Database.Batchable interface to update all Lead records in the org with a specific LeadSource. Write unit tests that achieve 100% code coverage for the class.
Create an Apex class called 'LeadProcessor' that uses the Database.Batchable interface.
Use a QueryLocator in the start method to collect all Lead records in the org.
The execute method must update all Lead records in the org with the LeadSource value of 'Dreamforce'.
Create an Apex test class called 'LeadProcessorTest'.
In the test class, insert 200 Lead records, execute the 'LeadProcessor' Batch class and test that all Lead records were updated correctly.
The unit tests must cover all lines of code included in the LeadProcessor class, resulting in 100% code coverage.
Run your test class at least once (via 'Run All' tests the Developer Console) before attempting to verify this challenge.

# Control Processes with Queueable Apex
Create an Queueable Apex class that inserts Contacts for Accounts.
Create a Queueable Apex class that inserts the same Contact for each Account for a specific state. Write unit tests that achieve 100% code coverage for the class.
Create an Apex class called 'AddPrimaryContact' that implements the Queueable interface.
Create a constructor for the class that accepts as its first argument a Contact sObject and a second argument as a string for the State abbreviation.
The execute method must query for a maximum of 200 Accounts with the BillingState specified by the State abbreviation passed into the constructor and insert the Contact sObject record associated to each Account. Look at the sObject clone() method.
Create an Apex test class called 'AddPrimaryContactTest'.
In the test class, insert 50 Account records for BillingState "NY" and 50 Account records for BillingState "CA". Create an instance of the AddPrimaryContact class, enqueue the job and assert that a Contact record was inserted for each of the 50 Accounts with the BillingState of "CA".
The unit tests must cover all lines of code included in the AddPrimaryContact class, resulting in 100% code coverage.
Run your test class at least once (via 'Run All' tests the Developer Console) before attempting to verify this challenge.

# Schedule Jobs Using the Apex Scheduler
Create an Apex class that uses Scheduled Apex to update Lead records.
Create an Apex class that implements the Schedulable interface to update Lead records with a specific LeadSource. Write unit tests that achieve 100% code coverage for the class. This is very similar to what you did for Batch Apex.
Create an Apex class called 'DailyLeadProcessor' that uses the Schedulable interface.
The execute method must find the first 200 Leads with a blank LeadSource field and update them with the LeadSource value of 'Dreamforce'.
Create an Apex test class called 'DailyLeadProcessorTest'.
In the test class, insert 200 Lead records, schedule the DailyLeadProcessor class to run and test that all Lead records were updated correctly.
The unit tests must cover all lines of code included in the DailyLeadProcessor class, resulting in 100% code coverage.
Run your test class at least once (via 'Run All' tests the Developer Console) before attempting to verify this challenge.
