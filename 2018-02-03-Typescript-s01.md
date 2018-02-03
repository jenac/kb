# Install & config
* `npm i -g typescript` **OR** `yarn global add typescript`
* `tsc app.ts` transpile app.ts to app.js

## TS project file
**`tsconfig.json`**
* compiler options
* include/exclude files
* support configuration inheritence
```javascript
{
    "compilerOptions": {
        "target": "es5",
        "noUnusedLocals": true,
        ...
    },
    "files": [
        app.ts,
        ...
    ]
}
```
**useful compiler options**
* sourceMap: true  //good for debug
* watch: true //watch source code change
* outDir: "js" //specify the build output directory
* strictNullCheck: true //do not allow assign null to other type like string

## Create project file using command line
`ts --init`

## Multiple project files and inheritence
You can have multiple tsconfig.json on different folder
To inherient a base config file:
add 
```javascript
extends: 'some-base-tsconfig.json', 
``` 
on the project(tsconfig.json) file.

## VScode configure task
F1 -> task:configure task runner

# Built-in types
* Boolean
* Number
* String
* Enum
* Array
* Void
* Null
* Undefined
* Never
* Any

## var, let and const
* `var`: hoisting.
* `let`: no hoisting.
* `const`: cannot change once assigned

## Union type
```typescript
let value: number | string; //value is number or string
```

## Type assertion
```typescript
let value: any = 5;
let fixed: string = (<number>value).toFixed(4);
let fixed2: string = (value as number).toFixed(4);
```
**not type conversion, just ease with type: enable intellisense.**


