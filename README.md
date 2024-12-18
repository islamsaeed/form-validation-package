# form-validation-package

this is simple from validation package

## Installation

Use npm

```bash
npm install --save form-validation-package
```

## Usage

index.html

```index
<from>
      <label for="">username</label>
      <input type="text" name="username" />
      <br />

      <label for="">password</label>
      <input type="password" name="password" />
      <br />
      <button id="submitform" type="submit">submit</button>
    </from>
```

app.js

```js
import { codeZoneFormValidation } from "./codeZoneFormValidation";
document.querySelector("#submitform").addEventListener("click", (e) => {
  e.preventDefault();
  const myform = codeZoneFormValidation([
    {
      name: "username",
      rules: [
        { name: "required", value: true, errMsg: "input required" },
        { name: "maxLength", value: 10, errMsg: "maxlength error" },
      ],
    },
    {
      name: "password",
      rules: [
        { name: "required", value: true, errMsg: "input required" },
        { name: "minLength", value: 8, errMsg: "minlength error" },
      ],
    },
  ]);
});
```
