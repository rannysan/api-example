# api-example
Simple api example using C # and MongoDb.

How to run the application:

1. Choose a directory on your development machine for storing the data. For example, C:\BooksData on Windows. Create the directory if it doesn't exist. The mongo Shell doesn't create new directories.
2. Open a command shell. Run the following command to connect to MongoDB on default port 27017. Remember to replace <data_directory_path> with the directory you chose in the previous step.
    *mongod --dbpath <data_directory_path>*
3. Open another command shell instance. Connect to the default test database by running the following command:
    *mongo*
4. Run the following in a command shell, If it doesn't already exist, a database named BookstoreDb is created. If the database does exist, its connection is opened for transactions.
    *use BookstoreDb*
5. Create a Books collection using following command:
    *db.createCollection('Books')*
6. Define a schema for the Books collection and insert two documents using the following command:
    *db.Books.insertMany([{'Name':'Design Patterns','Price':54.93,'Category':'Computers','Author':'Ralph Johnson'}, {'Name':'Clean Code','Price':43.15,'Category':'Computers','Author':'Robert C. Martin'}])*
7. View the documents in the database using the following command:
    *db.Books.find({}).pretty()*



**reference and complete guide:** https://docs.microsoft.com/pt-br/aspnet/core/tutorials/first-mongo-app?view=aspnetcore-3.1&tabs=visual-studio

