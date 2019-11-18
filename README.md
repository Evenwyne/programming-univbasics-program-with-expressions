# Program With Expressions

## Learning Goals

* Write a program with conditional logic using evaluation expressions only

## Introduction

You've traveled quite a road! You started off, from a conversational
perspective, mute and unable to interact, and now you can converse with Ruby.

Not only that, but you can ask Ruby to respond with some very sophisticated
results! Let's prove it to ourselves! But take this as an important fact:

***Programming is the art of helping a computer decide which expressions to
evaluate and in which order.***

Believe it or not, the rest of your programming career will be learning to make
your messages to Ruby, and other programmers, as clear and efficient as
possible. That's the name of the game for this career ***and you're doing it
now!***  

## Write a Program with Conditional Logic Using Evaluation Expressions Only

Recall when we introduced the ternary expression, we wrote this little program:

```ruby
likely_to_rain = true
garment = likely_to_rain ? "galoshes" : "sun hat"
```

Let's expand on this idea and use our new-found knowledge of `String` to make
the output more informative. You will see many of the expressions you learned in
this module come into play. We're going to mix-and-match techniques to show you
just how much you've learned!

```ruby
name = "Your name here"
rain_percentage = 0.2
temperature_in_c = 26

likely_to_rain = rain_percentage > 0.30
sun_is_dangerous = temperature_in_c >= 26

"Hello, #{name}, with a rain chance of #{rain_percentage * 100}% and a temperature of #{temperature_in_c}C we recommend that you " + (likely_to_rain ? "take an umbrella" : "enjoy this rain-free day") +
"#{sun_is_dangerous ? ' and watch out for heat stroke!' : ' and fine weather.'}"
```

This produces:

```text
=> "Hello Your name here with a rain chance of 20.0% and a temperature of 26C we recommend that you enjoy this rain free day and watch out for heat stroke"
```

Change just a few variables and you get an entirely different scenario:

```ruby
# Input values: We could easily imagine asking a user for these values.
name = "Byron the Poodle"
rain_percentage = 0.8
temperature_in_c = 26

likely_to_rain = rain_percentage > 0.30
sun_is_dangerous = temperature_in_c >= 26

"Hello, #{name}! With a rain chance of #{rain_percentage * 100}% and a temperature of #{temperature_in_c}C we recommend that you " + (likely_to_rain ? "take an umbrella" : "enjoy this rain-free day") +
"#{sun_is_dangerous ? ' and watch out for heat stroke!' : ' and bask in this fine weather.'}"
```

This produces:

```text
=> "Hello, Byron the Poodle! With a rain chance of 80.0% and a temperature of 26C we recommend that you take an umbrella and watch out for heat stroke!"
```

As a finishing bit of advice let us share an important truth about programming
with you: ***Just because code works, doesn't mean that it communicates well;
and therefore it's not "good"*** In our example that last `String` is _valid_,
Ruby understands what to do and does it! But is that a fun line of code to
read? Is it what you want to show your colleague or your boss or yourself 3
months from now. Make sure to always make your code as clean as possible.
You'll learn more techniques to do this in the coming lessons, but let's
rewrite this code into something we can be proud of.

```ruby
# Input values: We could easily imagine asking a user for these values.
name = "Byron the Poodle"
rain_percentage = 0.8
temperature_in_c = 26

likely_to_rain = rain_percentage > 0.30
sun_is_dangerous = temperature_in_c >= 26

rain_message = likely_to_rain ? "take an umbrella" : "enjoy this rain-free day"
sun_message = sun_is_dangerous ? ' and watch out for heat stroke!' : ' and bask in this fine weather.'

"Hello, #{name}! With a rain chance of #{rain_percentage * 100}% and a temperature of #{temperature_in_c}C we recommend that you #{rain_message} #{sun_message}"
```

Wait a second, notice how weird it feels to not know how `#{rain_message}` and
`#{sun_message}` connect? We should pull the `"and"` out of `sun_message`.
Programming is all in the details. Take time to always have clean, readable
code. Here's our final implementation:

```ruby
# Input values: We could easily imagine asking a user for these values.
name = "Byron the Poodle"
rain_percentage = 0.8
temperature_in_c = 26

likely_to_rain = rain_percentage > 0.30
sun_is_dangerous = temperature_in_c >= 26

rain_message = likely_to_rain ? "take an umbrella" : "enjoy this rain-free day"
sun_message = sun_is_dangerous ? ' watch out for heat stroke!' : ' bask in this
fine weather.'

"Hello, #{name}! With a rain chance of #{rain_percentage * 100}% and a temperature of #{temperature_in_c}C we recommend that you #{rain_message} and #{sun_message}"
```

## Conclusion

Congratulations, you've learned the art of conversing with Ruby at the most
basic level. You should be proud of this accomplishment. Learning any
programming language generally follows these same steps.

From a conversational perspective, you're now like a grade-school aged child.
You are able to make simple conditional statements, understand cause and
effect, and can give directions _as well as_ get information you want.

But to take your skills to the next level, you need to learn a new type of
construction: a _statement_. Unlike an _expression_ which always returns a
value, you will now learn statements which help choose which _expressions_ to
_evaluate_ or do repetitive tasks. That's Programming as Conversation Part II:
Statements. Take a virtual high-five from us! You've come a long way!
