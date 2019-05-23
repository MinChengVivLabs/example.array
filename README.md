<p align="Center">
  <img src="https://bixbydevelopers.com/dev/docs-assets/resources/dev-guide/bixby_logo_github-11221940070278028369.png">
  <br/>
  <h1 align="Center">Bixby Example Capsule -- example.array</h1>
</p>

**Purpose**

The purpose of this example is to demonstrate how Bixby action and view handles array of objects (both primitive type and structure)

  - No actual API calls, only fixed lookup in /code/lib/lib.js
  - max (One) or max (Many) determines the argument type in linked JS 
  - ActionCallContact
    - Takes a single `StructContact` object, and pass such object to JS as a single object
    - Try utterance like "call paul", and Bixby is able to feed "paul" as `TypeContactName` to ActionGetContactByName and then feed the output as `StructContact` to ActionCallContact
    - Try utterance like "call paul and sarah", and Bixby will ask for selection since ActionCallContact set `max(One)`
  - ActionConferenceCall
    - It is very similar to ActionCallContact, except `max (Many)`
    - Takes single or multiple objects of `StructContact`, and pass such object(s) to JS as an array of objects
    - Try utterance like "conference call simon" and "conference call paul and simon"
  - StructContact.view.bxb
    - Although view is not the focus in this example, it is clear that `list-of` handles single object and array of objects with NO additional coding required
  - Good luck and have fun with Bixby

**Resources**

Bixby Developer Resources:
  - Bixby Developer Center: https://bixbydevelopers.com/
  - Bixby Developer Support Help Center: https://support.bixbydevelopers.com/hc/en-us
  - You may find the  FAQ section useful as it contains articles that provide insight into common pitfalls first-time developers may encounter.

**Need Help?**
  - If you are stuck or need assistance, feel free to reach out to us. We are here to help you with any questions or point you to the right areas of the Bixby Developer Center or the Bixby Help Center. You can reach us by sending your questions via the "Contact Support" option in the Help menu or via email to support@bixbydevelopers.com.
