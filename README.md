#to do list

def add_task(tasks):
  task=input("Enter the task: ")  
  tasks.append(task)
  print("\n\nTask added successfully!")

def view_tasks(tasks):
  
  if not tasks:
    print("\n\n  ur task list is empty")
  
  else:
    print("tasks")
    for index,task in enumerate(tasks):#adds the task
      print(f"\n\n{index+1}.{task}") #the tasks and prints each task with its number.

def remove_task(tasks):
  
  view_tasks(tasks)
  
  task_index =int(input("enter the task number to remove:  "))
  
  if 0>=task_index<len(tasks):
    del tasks[task_index]
    print("task removed successfully")
  
  else:
    print("invalid task number")

def main():
  
  tasks=[]
  
  while True:
    
    print("\nTo-Do List App")
    print("1. Add task")
    print("2. View tasks")
    print("3. remove task")
    print("4. exit")
    
    choice=input("enter your choice: ")
    
    if choice == "1":
      add_task(tasks)
    elif choice == "2":
      view_tasks(tasks)
    elif choice == "3":
      remove_task(tasks)
    elif choice == "4":
      print("goodbye")
      break
    else:
      print("invalid choice. please try again")

if __name__ == "__main__":
  main()


  
