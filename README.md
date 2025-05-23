# note-book

def notebook():
    j = {}
    print("Welcome to the contract notebook\n")
    print("select the operation to perform: (1/2/3/4/5/6)\n")
    print("1. Add contract")
    print("2. Remove contract")
    print("3. Update contract")
    print("4. View contract")
    print("5. Search contract")
    print("6. Exit")
    

    while True:

       choice = int(input("\nEnter your choice: "))
       if choice == 1:
          key = input("Add your contract name: ")
          value = int(input("contract number: "))
          print()
          j[key] = value  
          print()
          print("contract added successfully", j)
          print()
          if key in j:
             print("this contract already exists, try anthoer one\n")

          else:
             value = int(input("contract number: "))
             j[key] = value
             print("contract added successfully", j)
       elif choice == 2:
          keys = input("Enter the contract name to remove: ")
          if keys in j:
             del j[keys]
             print("contract removed successfully")

       elif choice == 3:
          keyss = input("Enter the contract name to update: ")
          j.update({keyss: int(input("Enter the new contract number: "))})
          print("contract updated successfully")

       elif choice == 4:
          print("contracts: ", j)

       elif choice == 5:
          keysss = input("Enter the contract name to search: ")
          if keysss in j:
             print("contract found: ", j[keysss])

          else:
             print("contract not found")

      
       else:
          print("Exit sucsessfully")
          break

notebook()
