## Make customizables Date Countdowns with this simple and easy angular 8 component.

(`--prod` compatible)

## Instalation

`npm install ng2-date-countdown --save`

In your `app.module`, add `CountdownModule` to your imports:

```
import { CountdownModule } from "ng2-date-countdown";

@NgModule({
   declarations: [
     AppComponent
   ],
   imports: [
     BrowserModule,
     CountdownModule
   ],
   bootstrap: [AppComponent]
 })
 ```

## Usage

 `(reached)="someFunction($event)" You can use a Callback function for when it reaches 0" `

 `[text]: Change the text displayed in the date `

 `[units]: Choose which units do you want to display `

 `[divider]: Choose what you want to divide the dates with ` 

 `[showZeros]: Choose if you want to show a zero before the number '01 Days'`

 In your html template:

 ```
 <countdown units="Year | Month | Days | Hours | Minutes | Seconds"  end="July 22, 2019"></countdown>
 ```

 To set a custom Language and divider, set this variable in your component.ts file:

 ```
 text:any = {
     Year: 'Year',
     Month: 'Month',
     Weeks: "Weeks",
     Days: "Days",
     Hours: "Hours",
     Minutes: "Minutes",
     Seconds: "Seconds",
     MilliSeconds: "MilliSeconds"
   };
 ```

In your .html:

 ```
 <countdown (reached)="callback($event)" [text]="text" units="Year | Month | Days | Hours | Minutes | Seconds"  end="July 22, 2019"></countdown>
 ```

To customize the Countdown (.scss), use the class from it (you can inspect from chrome elements) and put the '/deep/' before them, example:

```
    /deep/ .countdown {
      width: 100%;
      height: 100px;
      background: black;

      .measurements {
        color: white;
        margin-right: 5px;
        padding: 10px;
     }

     .divider {
      font-size: 30px;
     }
```

(inspired on [angular-simple-countdown](https://github.com/previousdeveloper/angular2-simple-countdown))
