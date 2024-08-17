# library-management-system

def check_in(students):
    name=input("Enter your Name: ")
    roll=int(input("Enter your Collage ID: "))
    students[roll]=name
    print(f"\n{roll} Entered Succesfully\n")
    shelf()
    
def check_out(students):
    name=input("Enter your Name: ")
    roll=int(input("Enter your Collage ID: "))
    if name or roll in students:
        del students[roll]
        print(f"\n{roll}, Check-out succesfully\n")
    else:
        print(f"\n{name} is not present\n")
    shelf()    

def check_stu(students):
    for name,roll in students.items():
        print(f"{roll}, {name}")
    shelf()

def Checkin_book(books):
    name=input("Enter book name:\n")
    bid=int(input("Enter book id:"))
    books[bid]=name
    if name or bid in books:
        print(f"\n{name} issued succesfully")
    else:
        print(f"\n{name} not present")
    shelf()
    
def Checkout_book(books):
    name=input("Enter book name:\n")
    bid=int(input("Enter book id:"))
    books[bid]=name
    if name or bid in books:
        print(f"\n{name} returned succesfully")
    else:
        print(f"\n{name} not present")
    shelf()    
    
def shelf():
    print(">Press 1 to  Check-in library")
    print(">Press 2 to Check-out from library")
    print(">Press 3 to Issue a book")
    print(">Press 4 to return a book")
    print(">Press 5 to check no. students in library")
    n=int(input("Enter:"))
    
    if n==1:
        check_in(students)
    elif n==2:
        check_out(students)
    elif n==5:
        check_stu(students)
    elif n==3:
        print("\nAvailable books-->\n")
        print("Book name: Calculas, Book id=1\n")
        print("Book name: science, Book id=2\n")
        print("Book name: graphs, Book id=3\n")
        print("Book name: pyq, Book id=4\n")
        print("Book name: html, Book id=5\n")
        print("Book name: css, Book id=6\n")
        print("Book name: js, Book id=7\n")
        print("Book name: Backend, Book id=8\n")
        print("Book name: Full stack web development, Book id=9\n")
        print("Book name: object oriented programming, Book id=10\n")
        print("Book name: Data stuctures and algorithm, Book id=11\n")
        print("Book name: React js, Book id=12\n")
        Checkin_book(books)
    elif n==4:
        print("\nAvailable books-->\n")
        print("Book name: Calculas, Book id=1\n")
        print("Book name: science, Book id=2\n")
        print("Book name: graphs, Book id=3\n")
        print("Book name: pyq, Book id=4\n")
        print("Book name: html, Book id=5\n")
        print("Book name: css, Book id=6\n")
        print("Book name: js, Book id=7\n")
        print("Book name: Backend, Book id=8\n")
        print("Book name: Full stack web development, Book id=9\n")
        print("Book name: object oriented programming, Book id=10\n")
        print("Book name: Data stuctures and algorithm, Book id=11\n")
        print("Book name: React js, Book id=12\n")
        Checkout_book(books)
    
students={}
books={
  1:"Calculas",
  2:"science",
  3:"graphs",
  4:"pyq",
  5:"html",
  6:"css",
  7:"js",
  8:"Backend",
  9:"Full stack web development",
  10:"object oriented programming",
  11:"Data stuctures and algorithm",
  12:"React js"
}
shelf()
