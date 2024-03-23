# My-Money-Tracker-App
This a project on Tracking input and output of your money


//SCRIPT.JS
/*Certainly! This JavaScript code is for a basic money tracker app. Let's break it down into simple terms:

1. **Variables Setup**:
   - `expenses`: An array to store all the expenses or incomes.
   - `totalAmount`: Keeps track of the total amount (initially set to 0).

2. **Element Selection**:
   - `categorySelect`, `amountInput`, `infoInput`, `dateInput`, `addBtn`: These variables represent different elements on the web page that users interact with.
   - `expenseTableBody`, `totalAmountCell`: Elements used to display and update expense/income entries and the total amount on the web page.

3. **Event Listener**:
   - `addBtn.addEventListener('click', function() { ... })`: Listens for a click event on the "Add" button. When clicked, it executes the code inside the function.

4. **Add Button Click Event**:
   - Gets values from the input fields (category, info, amount, date).
   - Validates the inputs (ensures category is selected, amount is valid, info is provided, date is selected).
   - Updates the `expenses` array with a new entry.
   - Updates the `totalAmount` based on whether it's an expense or income.
   - Updates the total amount displayed on the web page.
   - Adds a new row to the expenses/incomes table with the entered data and a delete button for each entry.

5. **Delete Button Click Event**:
   - Inside the `addEventListener` function for the delete button:
     - Removes the corresponding expense/income from the `expenses` array.
     - Updates the `totalAmount` accordingly (adds back the deleted amount if it was an expense, subtracts if it was an income).
     - Updates the total amount displayed on the web page.
     - Removes the row from the expenses/incomes table.

6. **Loop for Displaying Existing Expenses/Incomes**:
   - The code includes a loop (`for...of`) that iterates through existing expenses/incomes and displays them in the table.
   - It also includes delete button functionality for each existing entry, similar to the delete button functionality for new entries.

Overall, this code creates a simple money tracker app where users can add expenses or incomes, view them in a table, and delete entries if needed. The total amount is automatically updated based on the type of entry (expense or income).
*/






//INDEX.JS
/*
This code is for a basic web application using Node.js with Express for server-side handling, MongoDB for database storage, and bodyParser for parsing HTTP request bodies. Here's a simple explanation of each part:

1. **Dependencies Import**:
   - `express`: A Node.js web application framework for creating server-side applications.
   - `body-parser`: Middleware for parsing incoming request bodies in middleware before your handlers, available under the req.body property.
   - `mongoose`: A MongoDB object modeling tool designed to work in an asynchronous environment.

2. **App Setup**:
   - Creates an instance of the Express application.
   - Configures middleware:
     - `bodyParser.json()`: Parses incoming JSON requests.
     - `express.static('public')`: Serves static files (like HTML, CSS, JS) from the "public" directory.
     - `bodyParser.urlencoded({ extended: true })`: Parses incoming URL-encoded form data.

3. **Database Connection**:
   - Connects to a MongoDB database named "MoneyList" on the localhost (port 27017).

4. **Database Event Handling**:
   - `db.on('error', ...)`: Handles errors that occur during the database connection.
   - `db.once('open', ...)`: Runs once when the database connection is successfully established.

5. **POST Route ("/add")**:
   - Handles POST requests to "/add" (typically used for adding data to the server/database).
   - Retrieves data from the request body (`req.body`), specifically `category_select`, `amount_input`, `info`, and `date_input`.
   - Constructs a data object with the retrieved values.
   - Inserts this data object into the "users" collection in the MongoDB database.
   - Logs a message if the insertion is successful.

6. **GET Route ("/")**:
   - Handles GET requests to the root path ("/").
   - Sets headers to allow access from any origin (`'*'`).
   - Redirects the user to the "index.html" page.

7. **Server Listening**:
   - Starts the server and listens on port 5000.
   - Logs a message to the console indicating that the server is running.

In summary, this code sets up a basic Express server with routes for adding data to a MongoDB database via POST requests and serving static files. It also includes error handling for the database connection and sets headers for allowing cross-origin requests.
*/



//PACKAGE.JSON
/*
This is a `package.json` file, which is used in Node.js projects to manage dependencies, scripts, and other metadata related to the project. Here's an explanation of the different fields in this `package.json` file:

1. **name**: `"my-projects"`
   - This field specifies the name of the project. In this case, it's named "my-projects."

2. **version**: `"1.0.0"`
   - Specifies the version of the project. The version number follows the Semantic Versioning (SemVer) convention, which typically includes major, minor, and patch version numbers.

3. **description**: `""`
   - This field provides a brief description of the project. In this case, it's empty, but usually, it would describe what the project does or its purpose.

4. **main**: `"index.js"`
   - Specifies the entry point for the Node.js application. When the application is started, Node.js looks for this file (`index.js` in this case) to begin execution.

5. **scripts**:
   - `"test": "echo \"Error: no test specified\" && exit 1"`
     - Defines a script named "test" that echoes an error message indicating that no tests are specified (`echo "Error: no test specified"`) and exits with an exit code of 1 (`exit 1`).

6. **author**: `""`
   - Specifies the author of the project. In this case, it's empty, but it would typically include the name or contact information of the project's author.

7. **license**: `"ISC"`
   - Specifies the license under which the project is distributed. In this case, it's the ISC (Internet Systems Consortium) license.

8. **dependencies**:
   - Specifies the dependencies required by the project. Dependencies are external packages or modules that the project relies on to function correctly.
   - Here are the dependencies listed along with their versions:
     - `"body-parser": "^1.20.2"`: Middleware for parsing incoming request bodies in Express.js applications.
     - `"express": "^4.19.1"`: Fast, unopinionated, minimalist web framework for Node.js.
     - `"mongoose": "^8.2.3"`: MongoDB object modeling tool designed to work in an asynchronous environment.
     - `"nodemon": "^3.1.0"`: Utility that automatically restarts the Node.js application when changes are detected, commonly used in development environments.

Overall, this `package.json` file provides essential information about the Node.js project, including its dependencies, versioning, scripts, and licensing information.
*/