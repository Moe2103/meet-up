

This is a serverless, progressive web application (PWA) built with React. The application uses the Google Calendar API to fetch events for a given city the user can specify.

# Features
## FEATURE 1: FILTER FOR EVENTS BY CITY

### As a user I should be able to “filter events by city” so that I can see the list of events that take place in that city.

**Scenario 1: When user hasn’t searched for a city, show upcoming events from all cities.**
GIVEN user hasn’t searched for any city  
WHEN the user opens the app  
THEN the user should see a list of all upcoming events

**Scenario 2: User should see a list of suggestions when they search for a city.**  
GIVEN the main page is open  
WHEN user starts typing in the city textbox  
THEN the user should see a list of cities (suggestions) that match what they’ve typed

**Scenario 3: User can select a city from the suggested list.**  
GIVEN the user was typing “Berlin” in the city textbox  
And the list of suggested cities is showing  
WHEN the user selects a city (e.g., “Berlin, Germany”) from the list  
THEN their city should be changed to that city (i.e., “Berlin, Germany”)

## FEATURE 2: SHOW/HIDE AN EVENT'S DETAILS

### As a user I want to be able to to show and hide event details so I can easily switch between getting an overview and getting more information about a particular event.

**Scenario 1: An event element is collapsed by default**  
GIVEN upcoming events where fetched
WHEN the user opens the meet app  
THEN the user will see a list of the events each with a "show details" button

**Scenario 2: User can expand an event to see its details**  
GIVEN there is a list of upcoming events  
WHEN the user clicks the “show details” of a particular event
THEN then the user will see more details of that event

**Scenario 3: User can collapse an event to hide its details**  
GIVEN the user has expanded the details of an event  
WHEN the user clicks the "hide details" button
THEN the event details will collapse and the user will see only the detail overview

## FEATURE 3: SPECIFY NUMBER OF EVENTS

### As a user I want to be able to specify the number of events that are displayed in the app so I can choose if I see more or less events in the list at once.

**Scenario 1: When user hasn’t specified a number, 32 is the default number**  
GIVEN the app is open  
WHEN the user has not entered a number in the “number of events” field  
THEN the user will see the default number 32

**Scenario 2: User can change the number of events they want to see**  
GIVEN there are that many upcoming events available 
WHEN the user enters a number in the "number of events" field 
THEN the user will see a list of that number of events

## FEATURE 4: USE THE APP WHEN OFFLINE

### As a user I want to be able to use the app offline so I can see the events I looked at the last time I was online.

**Scenario 1: Show cached data when there’s no internet connection**  
GIVEN the the app has no internet connection
WHEN the user opens the app  
THEN the user will see the events she has viewed the last time the app was online

**Scenario 2: Show error when user changes the settings (city, time range)**  
GIVEN the app has no internet connection
WHEN user starts a new event search   
THEN the user will see an error message informing the user that the app has no internet connection and new search is only possible when the app is online

## FEATURE 5: DATA VISUALIZATION

### As a user I want to see charts visualizing information about upcoming events in each city so I have a better overview.

**Scenario 1: Show a chart with the number of upcoming events in each city**  
GIVEN the app has internet connection 
WHEN the user chooses a city
THEN the user will see charts visualizing the kind and number of events in that city and comparing this city to other cities
