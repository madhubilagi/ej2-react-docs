---
title: "Getting Started"
component: "Calendar"
description: "This getting started section briefly explains how to create a calendar component in an application."
---

# Getting started

This section explains you the steps required to create a simple Calendar and demonstrate the basic usage of the Calendar component.

## Dependencies

The below list of dependencies are required to use the `Calendar` component in your application.

```javascript
|-- @syncfusion/ej2-react-calendars
    |-- @syncfusion/ej2-react-base
        |-- @syncfusion/ej2-base
    |-- @syncfusion/ej2-data
    |-- @syncfusion/ej2-calendars
    |-- @syncfusion/ej2-inputs
        |-- @syncfusion/ej2-splitbuttons
    |-- @syncfusion/ej2-lists
    |-- @syncfusion/ej2-popups
        |-- @syncfusion/ej2-buttons
```

## Installation and configuration

You can use [`create-react-app`](https://github.com/facebookincubator/create-react-app) to setup the applications.
To install `create-react-app` run the following command.

```sh
npm install -g create-react-app
```

* To setup basic `React` sample use following commands.

```sh
create-react-app quickstart --scripts-version=react-scripts-ts

cd quickstart

```

## Adding Syncfusion packages

All the available Essential JS 2 packages are published in [`npmjs.com`](https://www.npmjs.com/~syncfusionorg) public registry.
You can choose the component that you want to install. For this application, we are going to use `Calendar` component.

To install Calendar component, use the following command

```bash
npm install @syncfusion/ej2-react-calendars –save
```

## Adding Style sheet to the Application

To render the Calendar component, need to import Calendar and its dependent component's styles as given below in `App.css`.

```css
@import "../node_modules/@syncfusion/ej2-base/styles/material.css";
@import "../node_modules/@syncfusion/ej2-buttons/styles/material.css";
@import "../node_modules/@syncfusion/ej2-react-calendars/styles/material.css";
```

>Note: If you want to refer the combined component styles, please make use of our [`CRG`](https://crg.syncfusion.com/) (Custom Resource Generator) in your application.

## Adding Calendar component to the Application

* To include the Calendar component in application import the `CalendarComponent` from `ej2-react-calendars` package in `App.tsx`.

* Then add the Calendar component as shown in below code example.

`[src/App.tsx]`

```typescript
import { CalendarComponent } from '@syncfusion/ej2-react-calendars';
import * as React from "react";
import './App.css';

export default class App extends React.Component<{}, {}> {
    public render() {
        return <CalendarComponent id="calendar" />
    }
};

```

## Run the application

Now run the `npm start` command in the console, it will run your application and open the browser window.

```cmd
npm start
```

The below examples shows the basic calendar component.

{% tab template="calendar/default", sourceFiles="app/**/*.tsx" %}

```typescript

// import the calendarcomponent
import { CalendarComponent } from '@syncfusion/ej2-react-calendars';
import * as React from "react";
import * as ReactDOM from "react-dom";

export default class App extends React.Component<{}, {}> {
    public render() {
        return <CalendarComponent id="calendar" />
    }
};
ReactDOM.render(<App />, document.getElementById('element'));

```

{% endtab %}

## Setting the value, min and max dates

The following example demonstrates how to set the value,  min and max dates on initializing the Calendar. Here the Calendar allows to select a date within a range from 9th to 15th in a month of May 2017. To know more about range restriction in Calendar, please refer this [page](./date-range).

{% tab template="calendar/default", sourceFiles="app/**/*.tsx" %}

```typescript

// import the calendarcomponent
import { CalendarComponent} from '@syncfusion/ej2-react-calendars';
import * as React from "react";
import * as ReactDOM from "react-dom";

export default class App extends React.Component<{}, {}> {

    //initialize the value, min and max
    private dateValue: Date = new Date("05/11/2017");
    private minDate: Date = new Date("05/09/2017");
    private maxDate: Date = new Date("05/15/2017");

    public render() {
        return <CalendarComponent id="calendar" value={this.dateValue} min={this.minDate} max={this.maxDate} />
    }
};
ReactDOM.render(<App />, document.getElementById('element'));

```

{% endtab %}

## See Also

* [Select multiple dates in the Calendar](./multi-select)
* [Render Calendar with specific culture](./globalization)
* [How to change the initial view of the Calendar](./calendar-views)
* [Render Calendar with week numbers](./how-to/render-the-calendar-with-week-numbers)
* [Show other month dates](./how-to/show-dates-of-other-months)