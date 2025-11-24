# C24 Bank System (EXE version)

## Project summary
C24 Bank System is a simple console-based banking management application provided as a Windows executable (EXE). It stores and manages records for clients, employees, and administrators using plain text (.txt) files. The program offers interactive console menus for logging in, viewing records, performing basic operations, and clearing stored data.

## Key features
- Console (command-line) user interface.
- Data storage in plain text files (.txt) — no external database required.
- Separate files for clients, employees, and admins.
- Login system with username and password validation.
- Options to clear data for one category or all data.
- Manual admin account management via text files.

## Repository files (important)
- C24 Bank System Project.exe — main executable (may appear as BankSystem.exe when renamed).
- Clear Data Base.exe — utility executable to clear data (if provided).
- Admin.txt — administrators data file (CSV-style lines).
- AdminLastID.txt — stores the last admin ID used.
- Employee.txt — employees data file.
- EmployeeLastID.txt — stores the last employee ID used.
- Client.txt — clients data file.
- ClientLastID.txt — stores the last client ID used.
- Readme - اقرأني .txt — existing informational file in the repo.

## How the data is stored
- Each data file (Admin.txt, Employee.txt, Client.txt) contains one record per line.
- Fields are separated by commas; for example: ID,Name,Password,Salary (for admins).
- LastID files contain a single number representing the latest assigned ID for each type.

## How to run
1. Place the EXE file and all required .txt data files in the same folder.
2. Double-click the executable (e.g., "C24 Bank System Project.exe") to launch the console program.
3. Follow the on-screen menus and prompts.

If the program reports a missing file error, check that the required .txt files exist in the same directory as the EXE and are readable.

## Login requirements
- The application requires a username and password.
- Both username and password must be between 8 and 20 characters.

## Adding an admin account (manual)
Admin accounts cannot be created from inside the program. To add an admin:
1. Open Admin.txt in a text editor.
2. Add a new line in this format:
   AdminID,AdminName,AdminPassword,AdminSalary
   Example: 3001,adminUser,StrongPass123,5000
3. Update AdminLastID.txt with the new AdminID (e.g., change 3000 to 3001).
4. Save the files and restart the program if it was running.

Tip: Back up the .txt files before manual edits.

## Managing clients and employees
- Client.txt and Employee.txt follow the same CSV-like line format.
- When adding entries manually, update the corresponding LastID file to reflect the new ID.
- Validate the field order and delimiters by inspecting existing records before editing.

## Clearing data
- The program or the "Clear Data Base.exe" utility (if included) can clear records for a chosen category or all categories.
- Use caution: clearing data is irreversible unless you have backups.

## Troubleshooting
- "File not found" or similar errors: ensure all required .txt files are present in the EXE directory.
- Permission errors: try running the EXE with administrator privileges or move the folder to a writable location.
- Corrupt lines/format issues: open the .txt files and fix formatting (commas, missing fields) or restore from backups.

## Security and limitations
- This project is intended as a learning/demo tool. Storing sensitive data in plain text is insecure and not suitable for production.
- No encryption, access control, or secure password storage is implemented.
- Consider migrating to a proper database and adding secure authentication for production use.

## Suggested next steps (optional)
- Create initial sample data files and include them in the repo (with non-sensitive demo data).
- Add a proper README file to the repository root (this file).
- Consider creating a release with the EXE and a ZIP that includes required .txt files and instructions.
- Upgrade storage to a database (SQLite) and add stronger password handling.

## Contact / Author
For questions or improvements, see the repository author (Hamoodey77) on GitHub.
