# TMDB Movie Data Fetch 🍿

A simple Python project for fetching popular movie data from The Movie Database (TMDB) API. This script is designed to run in a Google Colab environment, and it processes the JSON response into a clean pandas DataFrame.

## 🚀 What It Does

* **Fetches Popular Movies:** Gets the current list of the most popular movies from the TMDB API.
* **Handles Pagination:** Includes a loop to fetch data from multiple pages (e.g., the top 50 pages of popular movies).
* **Processes JSON:** Parses the complex JSON response from the API.
* **Saves to DataFrame:** Cleans and organizes the relevant data (like title, overview, release date, and vote average) into a pandas DataFrame.
* **Exports Data:** (Optional) Shows how to save the final DataFrame to a `.csv` file.

## 🛠️ Technologies Used

* **Python 3**
* **Requests:** For making all HTTP API calls.
* **Pandas:** For cleaning and structuring the data.
* **Google Colab:** As the development environment.
* **TMDB API:** The data source for all movie information.

## ⚙️ Setup and How to Use

Follow these steps to get the project running.

### 1. Get Your TMDB API Key

This script will not work without an API key.

1.  Create a free account on [The Movie Database (TMDB)](https://www.themoviedb.org/).
2.  Go to your account **Settings** > **API**.
3.  Register for a developer key (v3 auth).
4.  Copy your **API Key** (it's a long string).

### 2. Run in Google Colab

1.  Download the `Tmdb_Movies_API_Fetch.ipynb` file from this repository.
2.  Open [Google Colab](https://colab.research.google.com/) and upload the notebook.
3.  Find the following line in the code:

    ```python
    api_key = 'YOUR_KEY_HERE'
    ```

4.  Paste your own API key in place of `YOUR_KEY_HERE`.

    **Important:** For security, it's best to use Colab's "Secrets" feature (look for the 🔑 icon in the left sidebar) to store your API key. This prevents you from accidentally sharing your key.

5.  Run the cells in the notebook from top to bottom.

### 3. See the Output

The script will print the final pandas DataFrame and (if you've enabled it) save a `movies.csv` file that you can download from the Colab environment.

## 📈 Example Data

The final DataFrame will look something like this:

| id    | title                             | release_date | vote_average | overview                                               |
| ----- | --------------------------------- | ------------ | ------------ | ------------------------------------------------------ |
| 653346 | Kingdom of the Planet of the Apes | 2024-05-08   | 6.8          | Several generations in the future following Caesar's... |
| 1022789 | Inside Out 2                      | 2024-06-11   | 7.7          | Teenager Riley's mind headquarters is undergoing a...   |
| ...   | ...                               | ...          | ...          | ...                                                    |
