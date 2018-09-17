# iOS Design Guidelines

## Branding

When making UI choices for mockups, a common consideration is deciding between building and adopting a custom experience specific to the brand, or using out-of-the-box components native to the platform. I tend to prefer the latter because users using the app for the first time are more familiar with the platform than the brand. Also, one must consider a cost-benefit approach in order to justify the customization effort involved in building these custom components. 

A good balance between the two 'brand specific' and 'platform specific' approaches is a balanced mix of te two. 

#### Brand Specific

Icons
Colors
Typography

#### Platform Specific

Navigation
Forms
Lists
Grids
UI Components/Controls

##### Color
##### Terminology
##### Typography

## Usability

### Form Validation

- __Validate early__, preferably realtime, instead of waiting for the user to tap the *Save* or *Submit* button. 

- __Validate inline__, instead of displaying modals or alerts.  

   *[This](https://alistapart.com/article/inline-validation-in-web-forms) study provides quantitive insights into the benefits of real-time, inline validation.*  

- Use placeholders and helper text to indicate the type of input expected.

- Indicate errors by means of color and error text.   

   *[Google's Material Design Guidelines](https://material.io/guidelines/patterns/errors.html#errors-user-input-errors) does a good job of demonstrating patterns for displaying errors in input fields.* 

#### Addresses

- Provide alternatives to typing the entire address. On iOS this can be achieved by:

   1. Current User Location (this'll need the user to granting location based permissions)
   2. Add from Addressbook (this'll need the user granting permissions to access the AddressBook)
   3. MapKit's autocomplete API

- Allow the user to alter or modify any of the fields populated using any of the options above. 

- Allow the user to manually type their address if they choose to not use any of the options above.

   *[This SO question](https://stackoverflow.com/questions/134956/how-do-you-perform-address-validation) lists several approaches towards address standardization including Google/Yahoo's geocoding web services, USPS API or numerous 3rd party services. The clear advantage of using native APIs over these is that native APIs are more performant and minimally dependent on network connectivity.*

Specific address fields can be validated based on these rules:

- **Address 1**: This is meant for street and number, PO box etc. I think its best to keep client side validations to a minimum. Allow for alphanumeric and special characters. This field is **required** and must be **minimum 5 characters**.  

- **Address 2**: This field is meant for apartment, suite, building, floor etc. Like address 1, I think its best to keep validations to a minimum and allow alphanumeric and special characters. This field is **optional** and **minimum 5 characters** (if entered).    

- **City**: City is **required**, **letters** only and **minimum 2 characters**. 

- **State**: State is **required** and selectable from list (this prevents invalid entry). 

- **Zip**: Zip code is **required**, **numeric** and must always be **5 digits**.


### Authentication

### Loading

### Onboarding

### Review Prompt

### Settings

## Resources

- [Human Interface Guidelines](https://developer.apple.com/ios/human-interface-guidelines/overview/themes/)
