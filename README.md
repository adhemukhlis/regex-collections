# regex-collections
My personal regex snippet collections for javascript. Honestly, I'm so sick dealing with regex :)


### Email
``` js

const regex = new RegExp('^([\\w-]+(?:\\.[\\w-]+)*)@((?:[\\w-]+\\.)*\\w[\\w-]{0,66})\\.([a-z]{2,6}(?:\\.[a-z]{2})?)$', 'i')
const email = 'admin@company.com'
const isEmailValid = regex.test(email)

// isEmailValid will return Boolean true if email valid
```
