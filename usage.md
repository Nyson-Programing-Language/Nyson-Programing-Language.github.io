# How to use
in a terminal type
```
nyson test.nys
```
you might have to change the word nyson to your nyson file location and change test.nys to any file you want that has the .nys ending

## Print
```
log("hello world");
```

## Math
```
log(math(5+5));
```

## Loop
```
loop(5) {
    log("loops");
}
```

## Variables
#### Set
```
dec str hello: "bob";
```
this makes a string variable called hello set to bob

#### Call
```
dec str name: "bob";
log("Hello, " name);
```

#### Anonymous variables
```
dec anon: "bob";
log("Hello, " bob);
```
#### Edit variables
```
dec str name: "bob";
log("Hello, " name);
name: "billy";
log("wait your name is, " name);
```


## Random Number
#### Print Random Number
```
log(math(random));
```
this will give you a float between 0 and 1

#### Print Random Number Between 0 and 10

```
log(math(random*10));
```
get something like 5.5539

#### Print Rounded Random Number
```
log(round(math(random*10)));
```
get something like 3

## Functions
#### Without Variables
```
func(sayHello()) {
    log("hello");
}
sayHello();
```

#### With Variables
```
dec str name: "bob";
func(sayHello()) {
    log("hello " name);
}
sayHello();
```

## If Statements
```
dec str condition : "true";
if (condition == "true") {
    log("true");
}
```

```
if ("1" >= "1") {
    log("true");
}
```

## Sleep
```
log("Hi");
sleep(5000);
log("I was sent 5 seconds later");
```

## Replace
```
log(replace("I am really bad", "bad", "good"));
```
will give "I am really good"

## Trim
```
log(trim("        Hello      "));
```
will give "Hello"

## Import
FILE: hello.nys
```
func(sayhello()) {
    log("hello")
}
```
FILE: main.nys
```
imp("hello.nys")
sayhello()
```
Returns: hello

## Read Files
```
log(getcont("bob.nys"));
```
will give the content of bob.nys

## Set Files
```
setcont("bob.nys", "Hello I am bob.");
```
bob.nys now has "Hello I am bob." as its contents

## Exec
#### Without Output
```
exec("/usr/bin/touch jimmy.nys");
```

#### With Output
```
log(exec("ls -a"));
```

## Input
```
log("What is your name?");
dec str name: input();
log("Hello, " name);
```

## GET Request
```
dec str code: GET("https://www.rust-lang.org/");
log("Rust Website code: " code);
```

## POST Request
```
POST("https://amtitan.free.beeceptor.com", "bob the builder");
```
this sends "bob the builder" to my beeceptor

## Music
```
audio("doom.mp3");
sleep(9325);
log("DROP");
```
Playes a file but it dose not wait for the file to end to continue. (this uses cvlc so if you want to change the volume or playing a directory see how to do it in cvlc)

## Time
```
log(time());
```
