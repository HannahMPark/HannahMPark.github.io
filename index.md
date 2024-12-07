# Hannah Park's Portfolio 

I am a computer science major at CSUF, and I am taking CPSC 120, which is an 'Introduction to Programming'.

## Favorite CPSC 120L Labs 

### Lab 6, Part-1
The key point of Part-1 was reading command-line input and printing the output. The user needed to provide three command-line arguments, excluding the command name. This if statement helped to check the number of the arguments and was also useful for the following lab exercises: 
```c++
  if (command_line.size() != 4) {
    std::cout << "error: you must supply three arguments";
    return 1;
  }
```

The part where I initialized each argument received from the command line as a string type was particularly enjoyable. It was interesting to see how command-line arguments can be accessed as part of an array. For example:
```c++
  std::string protein{command_line[1]};
  std::string bread{command_line[2]};
  std::string condiment{command_line[3]};
```

### Lab 7, part-1
Lab 7 was a remarkable lab. By examining the parking rules for four streets, I created function for a each street. I putted each function in the ‘parking_functions.cc’ and named them ‘CanParkOnAsh’, ‘CanParkOnBeech’,  ‘CanParkOnCedar’, and ‘CanParkOnDate’. 
The ‘CanParkOnDate’ function was most interesting. Because it required specific time, including minutes. This is the function of ‘CanParkOnDate’: 
```c++
bool CanParkOnDate(const std::string& day, int hour, int min) {
  if (day != "sat" && day != "sun" &&
      ((hour == 6 && min >= 30) || (hour >= 7 && hour < 16))) {
    return false;
  }
  return true;
}
```
At first, it was confusing because it required to check each condition by referring to the parking rule signs. This process was really helpful for practicing logical operators &&(and) and ||(or). 

### Lab 10, part-2
part-2 clearly demonstrates how to use classes. Especially in hilo_function.h, the GameState class defines both public and private member variables, which are key to this lab. For example, part of the GameState class looks like this:
```c++
class GameState {
 public:
  bool GuessCorrect(int guess) const;

 private:
  int secret_;
};
```

The bool GuessCorrect(int guess) const method is used in hilo_function.cc to check if the guessed number matches the secret number:
```c++
bool GameState::GuessCorrect(int guess) const {
  if (guess == secret_) {
    return true;
  }
  return false;
}
```
The way the struct in hilo_function.h defines both methods and variables really shows how the functions in hilo_function.cc are seamlessly connected to the headers in hilo_function.h. It was fascinating to see how everything works together.

