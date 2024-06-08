<!-- запрос(ы) для вставки данных минимум о двух книгах в коллекцию books, -->
db.books.insertMany(
  {
  title: "Harry Potter and Philosopher's stone",
  description: "Description of Harry Potter book",
  authors: "J.K.Rowling"
  },
  {
  title: "Harry Potter and Chamber of secrets",
  description: "Description of Harry Potter book",
  authors: "J.K.Rowling"
  }
)

<!-- запрос для поиска полей документов коллекции books по полю title, -->
db.books.find(
  { title: "Harry Potter and the Prisoner of Azkaban" }
)

<!-- запрос для редактирования полей: description и authors коллекции books по _id записи. -->
db.books.updateOne(
  { _id: 1 },
  { $set: {"description" : "New description", "authors" : "Joanne Rowling"} }
)

