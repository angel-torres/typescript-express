# Express Server /w TypeScript and MongoDb
I've created this repo to learn to use TypeScript with ExpressJS. 

## Getting Started

1. cd into root directory 

2. run `npm install` 

3. run `npm run watch-ts` - this starts the TypeScript compiler

4. open up a different terminal and cd into the same project. Run `npm run watch-node` - this starts the node server

## What is TypeScript?

TypeScript is a superset of JavaScript. It was created by Microsoft and was first relased in 2012. TypeScript provides optional static typing along with other features. It caught my attention a few months ago when I was learning a bit about AngularJS, which uses TypeScript. It has been increasing in popularity and it does not seem like it will be disappearing anytime soon. This project implements many of it's core features.

## Why use TypeScript?
TypeScript is a great toool to use to decrease bugs slipping into our code. It also helps make our code more maintainable making it self-documenting. If those aren't enough reasons to use it then you should also consider the intellisense that you get while useing. Just that alone can make developers much more productive and efficient. 

## What are some cool features?

### Static Typing
1. Static typing helps developers catch errors and bugs that can be introduced into our code before it even runs. The compiler gives us errors whenever the variables we define are not given the right type. 
2. By defining our types we get much help from our code editor. This means that our editor will give us better intellisense and therefore save us tons of time. If we haven't used a function in a while and are now using it. Our editor will be able to 
3. Static typing is one of the most valuable features in TypeScript. It offers several benefits. One of them being that it makes our code self-documenting. Keeping a good documentation of all our functions, the parameters they take, etc. can be difficult. By creating static types we are able to see what type each variable we define is. 

**boolean**
```
const isDone: boolean = true
```

**number**
```
const year: number = 2020
```

**string**
```
const name: string = "Robert"
```

**array**
```
const list: number[] = [1,2,3]
const list: Array<number> = [1,2,3]
```

**tuple**
```
const tuple: [string, number] = ["Jason", 43]
```

**any**
```
const doNotKnow: any = "this could be a string or a number" || 23
```

**void**
```
function warnUser(): void {
console.log("This is my warning message");
}
```

### Interfaces
Interfaces focus on the shape that values have. We can define interfaces to define these shapes and create consistancy across our code. 

```
interface UserInterface {
    name: "William";
    age?: 25;  // we can definte optional values
}
```

### Optional Chaining

This is a cool feature I found out about which helps cleans up the code. It es very useful whenever you have nested data. Sometimes it turns out that one of the objects in the chain is undefined. This can cause errors but with the `.?` we can catch those errors before runtime instead of using the `&&` operator.

**BEFORE**
```
if (data && data.customer && data.customer.address) {
   const {address} = data.customer
   const fullAddress = `${address.street}, ${address.city}, ${address.state }${address.zipcode}`
}
```

**AFTER**
```
const address = data?.customer?.address
const fullAddress = `${address?.street}, ${address?.city}, ${address?.state } ${address?.zipcode}`
```

