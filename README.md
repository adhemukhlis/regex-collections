# regex-collections
My personal regex snippet collections for javascript. Honestly, I'm so sick dealing with regex :)


### Email
[Try](https://regex101.com/r/StcU4f/1)
``` js

const regex = new RegExp('^([\\w-]+(?:\\.[\\w-]+)*)@((?:[\\w-]+\\.)*\\w[\\w-]{0,66})\\.([a-z]{2,6}(?:\\.[a-z]{2})?)$', 'i')
const email = 'admin@company.com'
const isEmailValid = regex.test(email)

// isEmailValid will return Boolean true if email valid
```

### Password
[Try](https://regex101.com/r/0GCr4z/1)
``` js
const regex = new RegExp('^(?=.*\\d)(?=.*[A-Z])(?=.*[a-z])(?=.*[^\\w\\d\\s:])([^\\s]){8,}$', '')
const password = '^eT3rn1Ty&*!'
const isPasswordValid = regex.test(password)

// isPasswordValid will return Boolean true if password valid
```
or set length and without contain symbol
```js 
const minLength = 8
const regex = new RegExp(`^(?=.*\\d)(?=.*[A-Z])(?=.*[a-z])([^\\s]){${minLength},}$`, '')
const password = '^eT3rn1Ty&*!'
const isPasswordValid = regex.test(password)

// isPasswordValid will return Boolean true if password valid
// if the password contains only symbols, it will return false
```
