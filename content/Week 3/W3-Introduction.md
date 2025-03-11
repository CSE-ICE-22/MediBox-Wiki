- - -
>[!info] In week  3, We'll be taking our first step in creating our Medi-Box! 
>We'll learn,
> - Basic structure of micro-controller programming.
> - Usage of basic sensors and actuators
>
- - -
The following diagram shows the program of flow of our app.
![[Week 3 Introduction 2025-03-11 16.13.34.excalidraw.light.png|800]]

As of above diagram we'll be creating appropriate functions along the way, with different implementations and functionalities. 

Here's an overview of the functions we'll be implementing


# Medi Box Functions

## Display Functions
```cpp
void print_line(String message)
````

- Prints the message as a line on OLED Display

```cpp
void print_time_now()
```

- Prints the time as Days, Hours, Mins and Seconds on OLED Display

## Time Management

```cpp
void update_time()
```

- Updates the time using the `millis()` function in Arduino

```cpp
void update_time_with_check_alarm()
```

- Prints the time on OLED Display using the print_time_now() function
- Checks if the current time is a medicine time
- If it is medicine time, the alarm will ring until the user turns it off

## Alarm System

```cpp
void ring_alarm()
```

- Prints a message, rings the buzzer and lights up an LED when it is a medicine time

## User Interface

```cpp
int wait_for_button_press()
```

- Checks whether the user has pressed one of the push buttons
- Identifies the button which has been pressed

```cpp
void go_to_menu()
```

- Switches between modes accordingly, after identifying the pressed button through the wait_for_button_pressed() function

```cpp
void run_mode()
```

- Executes the mode which has been selected by the user

## Environmental Monitoring

```cpp
void check_temp()
```

- Checks the temperature and humidity using the DHT22
- Lights up an LED

>[!tip]- When creating functions, try to stick with [[Single Responsibility Principle]]
>Each functions should be responsible to **one functionality only**. It does one job, and that job well.