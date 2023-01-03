# Symfony-FullCalendar
EDT app using FullCalendar and Symfony 5

# FullCalendar
FullCalendar is a popular JavaScript library for rendering interactive calendars on websites. It can be used with the Symfony web framework to add calendar functionality to your Symfony application.

To use FullCalendar with Symfony 5, you will need to include the FullCalendar library in your project and configure it to work with your Symfony application. Here are the general steps you can follow to do this:

1. Install FullCalendar using npm:
```bash
npm install fullcalendar
```
2. Include the FullCalendar JavaScript and CSS files in your Symfony application. You can do this by adding the following lines to your template file:
```php
<link href='fullcalendar/main.css' rel='stylesheet' />
<script src='fullcalendar/main.js'></script>
```
3. Create a calendar element in your template file where the calendar will be displayed:
```php
<div id='calendar'></div>
```
4. Initialize FullCalendar in your JavaScript file:
```php
document.addEventListener('DOMContentLoaded', function() {
  var calendarEl = document.getElementById('calendar');

  var calendar = new FullCalendar.Calendar(calendarEl, {
    // options here
  });

  calendar.render();
});
```
5. Configure FullCalendar options as needed. For example, you can set the calendar's date range, events, and other options. For a complete list of available options, refer to the FullCalendar documentation.

6. If you need to retrieve data from your Symfony application to display in the calendar (e.g. a list of events), you can use an AJAX request to fetch the data and pass it to FullCalendar.
