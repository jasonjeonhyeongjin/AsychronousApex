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
