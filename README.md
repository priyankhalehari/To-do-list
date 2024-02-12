# To-do-list
tasks = []
def add_task():
    task = input("Enter new task:")
    tasks.append(task)
    print("Task added successfully.")
def view_tasks():
    if len(tasks) == 0: 
     print('No tasks')
    else:
     print('List of tasks:')
     for i, task in enumerate(tasks):
         print(f"{i+1}. {task}")
def delete_task():
    if len(tasks) == 0:
        print("no tasks to delete.")
    else:
        choice=int(input('Enter the task number to delete:'))
        if 0 < choice <= len(tasks):
            del tasks[choice-1]
            print("Task deleted successfully")
        else:
            print("Invalid")
def main():
    while True: 
      print("\n______TO-DO LIST______")
      print("\n1.Add task\n2.view task\n3.delete task\n4.exit")
      choice=int(input("Enter your choice:"))
      if choice == 1:
        add_task()
      elif choice == 2:
        view_tasks()
      elif choice == 3:
        delete_task()
      elif choice == 4:
        print("Exit")
      else:
        print("Invalid choice")
if __name__ == "__main__":
    main()

