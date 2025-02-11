## Code

```
class Database {
   public Database(String URL, String username, String password) {
       // Creates the database connection and returns Database instance.
   }
  
   public String executeQuery(String query) {
       // Executes the query and returns the result.
   }
}

class Driver {
  
   public void callerOne() {
       Database db = new Database("jdbc:mysql://localhost", "root", "password");
       String data1 = db.executeQuery("Query1");
       // process data
   }
  
   public void callerTwo() {
       Database db = new Database("jdbc:mysql://localhost", "root", "password");
       String data2 = db.executeQuery("Query2");
       // process data
   }

   public static void main(String[] args) {
       Driver driver = new Driver();
       driver.callerOne();
       driver.callerTwo();
   }
}
```

## Prompt

\```
{{Paste your code here}}
\```

Can you refactor the above code to make it clean, maintainable code by applying Singleton Design Pattern?