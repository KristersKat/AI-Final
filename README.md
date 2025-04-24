## **Script Features**

- **Performs 200 random exploration steps using floating-point coordinates within [-100, 100].**
    
- **Handles API communication, including JSON parsing ({"z": value}) and basic error handling (timeouts, non-200 status codes, invalid JSON).**
    
- **Determines the best integer starting point for exploitation based on the highest 'z' value found during exploration.**
    
- **Executes a 10-step exploitation path using integer coordinates.**
    
- **The exploitation strategy prioritizes moving to unvisited adjacent coordinates that have the highest estimated 'z' value (based on the nearest point found during exploration).**
    
- **If all adjacent coordinates have already been visited in the current exploitation path, it moves to the visited neighbour with the highest estimated 'z' value.**
    
- **Logs exploration coordinates (x,y) to explore_PORT.csv.**
    
- **Logs exploitation moves (int x, int y) to moves_PORT.csv.**
    
- **Prints the final summed 'z' value from the 10 exploitation steps to the console.**
    
- **Accepts the target API base URL and student names via command-line arguments.**
    

## **Prerequisites**

- **Python 3.x**
    
- **requests library**
    

## **Installation**

1. **Ensure you have Python 3 installed.**
    
2. **Install the requests library using pip:**
    

pip install requests
or
pip3 install requests

## Usage

Run the script from your terminal, providing the base URL of the target API endpoint.

General Format:
python explore_exploit.py <base_url>