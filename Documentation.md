# IMDb Ratings Analysis

### Version 1.0
## Overview

This document provides an overview of the Movie Analysis Web App project. The project allows users to upload their movie ratings data in CSV format downloaded from IMDb Your Ratings, perform various analyses on the data, and visualize the results. It consists of three HTML pages and a Django application.

## Project Structure

- `search_result.html`: HTML page for displaying search results.
- `upload.html`: HTML page for uploading CSV files.
- `result.html`: HTML page for displaying analysis results.
- `views.py`: Django views and request handlers.
- `forms.py`: Django form for file upload.
- `movie_analysis.py`: Python module for data analysis.
- `csvFiles/`: Directory to store uploaded CSV files.

## Functionality

### Uploading CSV Files

- Users can upload CSV files containing their movie ratings data through the "Upload" page.
- The `FileUploadForm` form is used to handle file uploads.
- Uploaded files are stored in the `csvFiles/Media/` directory.

### Processing CSV Files

- Uploaded CSV files are processed in the `process_csv` view in `views.py`.
- The uploaded CSV file is read and processed using the `MovieAnalysis` class from `movie_analysis.py`.
- The processed data is then displayed on the "Result" page.

### Searching and Analysis

- Users can perform various searches and analyses on their movie data through the "Search Result" page.
- Searches can be performed based on movie year, genre, or month of watching.
- The `MovieAnalysis` class provides methods for data filtering and analysis.

### Data Visualization

- The project includes data visualization capabilities using Matplotlib.
- Users can view plots and graphs depicting movie data statistics, such as mean ratings and count.

## MovieAnalysis Class

- The `MovieAnalysis` class in `movie_analysis.py` is responsible for reading and processing CSV files, as well as performing data analysis.
- It provides methods for searching, filtering, and computing statistics on movie data.
- Data analysis includes calculations for mean ratings, genre statistics, year statistics, and more.
- Data Vistualization is Down in methods `getPlots()` and `getGraphs` which uses `matplotlib` for Plotting.
    - Each of the `getStats()` methods takes different opitional argument for you can get your stats for.
    - For example:
        if `irating = True` then the grouped Data returned is related to column `IMDb rating`, same goes for all the **Stats** Methods.

## Security

- The project implements basic security measures for file uploads and data processing.

## Dependencies

- Django 4.2.4
- pandas 1.5.3
- matplotlib 3.8.0
- adjustText 0.8

## Usage

1. Install the required dependencies using `pip install -r requirements.txt`.
2. Run the Django development server using `python manage.py runserver`.
3. Access the web application in a web browser at `http://localhost:8000`.

## Future Enhancements

- Implement user authentication and user-specific data storage.
- Add support for more advanced data visualization options.
- Improve error handling and user feedback for CSV file uploads.

## Contributors

- Brightlat

## License

This project is licensed under the [License Name] License - see the [LICENSE](LICENSE.md) file for details.