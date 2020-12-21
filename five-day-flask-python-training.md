Below is a list of flask tutorial exercises to do.

What Is Flask, How To Setup
---------
**What is Flask** - Flask is a Python web framework we use here to write APIs used for various different reasons. It is crucial you have an understanding of how to write simple Flask APIs, calling those APIs, how data transfer works between them.

**How to setup** - A good link to follow is https://programminghistorian.org/en/lessons/creating-apis-with-python-and-flask#setting-up

Flask Exercises
---------

**Setup localserver** - Flask server running on your localhost and custom port number.

**Python exercise APIS** - All the below Python exercises to be made into their own APIs. For example, an API which will take an ineteger via GET method and return the nth Pi digit based on the GET parameter.

Code sample for API to take two numbers and return their sum (follow this format for all the APIs)
~~~
def adder():
  result = {}
  try:
    num_1 = int(request.args['num_1'])
    num_2 = int(request.args['num_2'])

    result["status"] = 1
    result["sum"] = num_1 + num_2
    result_json = json.dumps(result)
    return result_json
  except Exception as e:
    print(traceback.format_exc())
    result["status"] = -99
    result['errorName'] = type(e).__name__
    result['errorMsg'] = str(e)
    result_json = json.dumps(result)
    return str(result_json)
~~~

-- **Find PI to the Nth Digit** - Enter a number and have the program generate PI up to that many decimal places. Keep a limit to how far the program will go.

-- **Find e to the Nth Digit** - Just like the previous problem, but with e instead of PI. Enter a number and have the program generate e up to that many decimal places. Keep a limit to how far the program will go.

-- **Fibonacci Sequence** - Enter a number and have the program generate the Fibonacci sequence to that number or to the Nth number.

-- **Prime Factorization** - Have the user enter a number and find all Prime Factors (if there are any) and display them.

-- **Next Prime Number** - Have the program find prime numbers until the user chooses to stop asking for the next one.

-- **Find Cost of Tile to Cover W x H Floor** - Calculate the total cost of tile it would take to cover a floor plan of width and height, using a cost entered by the user.

-- **Coin Flip Simulation** - Write some code that simulates flipping a single coin however many times the user decides. The code should record the outcomes and count the number of tails and heads.

-- **Fizz Buzz** - Write a program that prints the numbers from 1 to 100. But for multiples of three print “Fizz” instead of the number and for the multiples of five print “Buzz”. For numbers which are multiples of both three and five print “FizzBuzz”.

-- **Reverse a String** - Enter a string and the program will reverse it and print it out.

-- **Pig Latin** - Pig Latin is a game of alterations played on the English language game. To create the Pig Latin form of an English word the initial consonant sound is transposed to the end of the word and an ay is affixed (Ex.: "banana" would yield anana-bay). Read Wikipedia for more information on rules.

-- **Sorting** - Implement two types of sorting algorithms: Merge sort and bubble sort.

-- **Page Scraper** - Create an application which connects to a site and pulls out all links, or images, and saves them to a list. *Optional: Organize the indexed content and don’t allow duplicates. Have it put the results into an easily searchable index file.*
