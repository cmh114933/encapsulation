### Encapsulation

+++

Remember `public` & `private`?

```js
class ChatService implements OnInit {
    currentUser
    private users
    private messages

    public getUser(){}

    public getMessages(){}

    private setUser(){}
}
```

+++

**public :** variables/functions are accessible outside of the class and within the class

**private :** variables/functions are only accessible within the class**

+++

#### Encapsulation is about
- Controlling access to data and functions within a class

---

### Why Encapsulation?
- Prevent access by **class** that should not be concerned with said variable/function
- Information / functions should be on a need to know/use basis
- **Classes** should only be concerned with the immediate variables/function they require

+++

#### By default, keep things private
- Only when something else requires access, should you consider making it public, and even then, may need to set a separate layer, e.g: `getUser()`
- Consider what should become private

---

### Exercise 1
User Login

+++

```java
Website nextacademy = new Website("NextAcademy");
User user = new User("test", "password");

String password = "hacking";
nextacademy.login(user, password);
// Unsuccessful login!
nextacademy.isLoggedIn; // false

String password = "password";
nextacademy.login(user, password);
// test has logged in successfully to NextAcademy
nextacademy.isLoggedIn; // true

// user.password returns error
// user.username returns error
user.username(); // "test"
user.setUserName('newUserName','password');
user.username(); // "newUsername"
```

---

### Exercise 2
OAuth

+++

![Landlord](https://kroki.io/mermaid/svg/eNptzlEKwjAMBuD3nSIX2AX6MBgICk4UbxDWrAa2Fpt0sNubDWWI5i2QL_8v9CwUezowhoxTBTYdRj-m7Ou6adpAUR0ceSYBLPpImQWVU4SRVClvYruy6490cF__ikL7l-wITMEFIwaabL0OA_fk4JbTzN4iv323R_4gWOvCu-8pFSE40yKWVb0AQ_9NCg==)

+++

![Oauth](https://kroki.io/mermaid/svg/eNp1jkEKwjAURPeeYi7QC2RRKEjdiYge4Jt8NJTmY_JT6u2bCBaFOuv3ZibxM3OwvPd0jzTuUHJNHJumbY88K1lyPL4MDn7iBMr6kOgTqZeAiwwc3soXWsRaYHCu1UnRbTgbEnqyfBMZDE5RJu_KXPdnbmXrTfz8XN0PglzewJHSAsgZUbg=)


---

### Exercise 3 - Group
Credit card system

+++

Making Purchases on Ebay
- Create Customer, Ebay, Transaction, Visa class
- When a Customer makes a purchase, Ebay creates a Transaction
- Transaction has transactionId, platform, status and amountPayable
- Customer can go to Visa and input transaction details and credit card details

+++ 

- Visa executes payment
- If payment does not exceed credit limit, payment is successful
- Visa notifies Ebay of payment status
- Ebay marks transactions as paid