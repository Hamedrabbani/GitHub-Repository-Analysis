# GitHub-Repository-Analysis
GitHub Repository Analysis with Python:

This project demonstrates how to collect, process, and visualize GitHub repository data using the GitHub REST API
and Python libraries such as requests, pandas, matplotlib, and plotly.
You can explore the most-starred repositories by programming language and compare popularity trends between multiple languages.

Project Structure:
api_extract_data.py— Data Extraction and Export
•	Makes a request to the GitHub API for the most-starred Python repositories.
•	Parses key information from each repository:
o	Repository name
o	Owner username
o	Description
o	Date created and last updated
o	Number of stars
•	Outputs a summary of the top repositories to api_extract_data.csv using pandas.

Key Concepts:
•	requests.get() for API calls
•	.json() for JSON parsing
•	List aggregation and dictionary-to-DataFrame conversion

api_git_repo_plot.py— Interactive Visualization with Plotly:
•	Prompts the user to input a programming language (e.g. Python, JavaScript).
•	Fetches the top repositories in that language using the GitHub API.
•	Processes data and creates an interactive bar chart with:
o	Repository names (as clickable links) on the X-axis
o	Star counts on the Y-axis
o	Owner names, descriptions, and update timestamps as hover text
•	Generates a browser-based visualization with plotly and saves it as python_repos.html.
Highlights:
•	Dynamic language input
•	Use of Plotly Bar for rich, browser-based visualizations
•	Custom styling via axis configuration and color settings

Comparison_pro_languages.py— Language Comparison Chart with Matplotlib:
•	Independently fetches the most-starred repositories in two languages
o	Python
o	C++
•	Extracts repository names and star counts for each
•	Generates a line plot comparing star distributions:
o	Red line for Python projects
o	Blue line for C++ projects
•	Useful for side-by-side visual popularity comparison

Highlights:
•	Use of matplotlib.pyplot for static, high-quality plotting
•	Multiple data series plotted on a single axis
•	Custom plot styling with titles, labels, tick adjustments

How to Run:
1.	Install required packages (if not already installed)

pip install requests pandas plotly matplotlib 

1.	Run each script from the terminal or your IDE:
python api_extract_data.py # Extract and save raw data to CSV python
api_git_repo_plot.py # Visualize most-starred repos by language python
Comparison_pro_languages.py # Compare Python vs C++ repository popularity 
1.	Open generated HTML charts (python_repos.html) or view line plots rendered by matplotlib.

Notes:
•	Make sure you have internet access to communicate with the GitHub API.
•	GitHub API rate limits may apply for unauthenticated requests. For higher limits, consider using a personal access token.
•	You can extend the comparison in Comparison_pro_languages.py by including more languages or analyzing over time.

Future Enhancements:
•	Add error handling for API failures or empty responses.
•	Cache API responses locally to avoid repeated calls during testing.
•	Display creation/update dates in a timeline chart or scatter plot.
•	Build a streamlit/web interface for interactive exploration.
