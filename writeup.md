# Assignment 3 - Write UP

## Description
This assignment completes our movie chatbot system by implementing action functions that query our movie database and building a natural language interface. You implemented functions to search for movies by year, director, and actors, as well as the core search system that matches user queries to appropriate database operations. This builds directly on the pattern matching work from Assignment 2 to create a functional conversational AI system.

## What to complete
1. Complete all action functions in `a3.py` (title_by_year, title_by_year_range, etc.)
2. Implement the `search_pa_list` function to handle pattern matching and responses  
3. Add at least one new movie to the database with proper formatting
4. Create a new pattern/action pair and add it to the pa_list
5. Ensure all provided assert statements pass
6. Complete the reflection questions below
7. Push your code to github for grading

## Reflection Questions

1. What are some key programming concepts or techniques that you learned while completing this assignment?
    Applying tuples and list data structures to represent and query a movie database, applying pattern matching with wildcards (% and _) to match on patterns, applying higher-order functions by combining patterns with action callback functions in pa_list, and applying list filtering techniques to search and extract specific movie information based on user queries.


2. How does the overall movie chatbot system work? Explain the flow from when a user types a query to when they receive an answer.
The user inputs a query that is processed by query_loop (removes punctuation, lowercases, word splits) and then passed to search_pa_list() which iterates over pa_list calling match() on every pattern until the first match is found that extracts wildcard values (e.g., movie titles or years), calls the matching action function with those extracted values to search movie_db and filter results, and returns answers to output or returns ["No answers"] if the pattern matched but no results or ["I don't understand"] if no pattern matched.


3. What are some real-world applications where this type of pattern-matching chatbot system could be useful? How might you extend or improve this system for practical use?
This pattern-matching system is appropriate for restaurant menu queries, library catalog searches, university course searches, product inventory queries, hotel reservation systems, and customer support FAQs, and could be extended by adding fuzzy string matching to handle typos, compound query support to enable multiple filters to be used in combination, conversation memory to enable follow-up questions, database extension with additional fields like genres and ratings, external API integration for live information, and natural language processing to enable more variation in query wordings beyond pre-defined patterns.