# Discussion

## Solutions Considered
1. **Reading the Entire File into Memory**: 
   - This approach would involve loading the entire log file into memory and then filtering the logs based on the date. 
   - **Pros**: Simple implementation and fast access to logs.
   - **Cons**: Not feasible for large files (1 TB) due to memory constraints.

2. **Using a Database**:
   - Importing logs into a database and querying for specific dates.
   - **Pros**: Efficient querying and indexing.
   - **Cons**: Requires additional setup and complexity, which may not be necessary for a one-time extraction.

3. **Line-by-Line Processing** (Final Solution):
   - Read the log file line by line and write matching entries to an output file.
   - **Pros**: Memory efficient, simple implementation, and directly addresses the problem without unnecessary complexity.
   - **Cons**: Slightly slower than reading the entire file at once, but acceptable given the constraints.

## Final Solution Summary
I chose the line-by-line processing approach because it is the most efficient in terms of memory usage, which is critical given the size of the log file (1 TB). This method allows us to handle large files without running into memory issues, and it is straightforward to implement. The solution meets the requirements of extracting logs for a specific date while ensuring that we do not overload the system's resources.

## Steps to Run
1. **Clone the Repository**:
   ```bash
   git clone https://github.com/yourusername/your-forked-repo.git
   cd your-forked-repo


Download the Log File: Use the following command to download the log file:
curl -L -o test_logs.log "https://limewire.com/d/90794bb3-6831-4e02-8a59-ffc7f3b8b2a3#X1xnzrH5s4H_DKEkT_dfBuUT1mFKZuj4cFWNoMJGX98"

Run the Script: Make sure you have Python installed. Run the script with the desired date:
python src/extract_logs.py YYYY-MM-DD

