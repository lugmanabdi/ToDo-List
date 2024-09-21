# To-Do List Program in Python

def display_menu():
    print("\n--- To-Do List Menu ---")
    print("1. Add a task")
    print("2. View tasks")
    print("3. Mark task as completed")
    print("4. Remove a task")
    print("5. Exit")

def add_task(to_do_list):
    task = input("Enter the task you want to add: ")
    to_do_list.append({"task": task, "completed": False})
    print(f"Task '{task}' added successfully!")

def view_tasks(to_do_list):
    if not to_do_list:
        print("Your to-do list is empty.")
    else:
        print("\n--- To-Do List ---")
        for idx, task_info in enumerate(to_do_list, 1):
            status = "Completed" if task_info["completed"] else "Pending"
            print(f"{idx}. {task_info['task']} - {status}")

def mark_task_completed(to_do_list):
    view_tasks(to_do_list)
    if to_do_list:
        try:
            task_num = int(input("Enter the task number to mark as completed: "))
            if 1 <= task_num <= len(to_do_list):
                to_do_list[task_num - 1]["completed"] = True
                print(f"Task '{to_do_list[task_num - 1]['task']}' marked as completed!")
            else:
                print("Invalid task number.")
        except ValueError:
            print("Please enter a valid number.")

def remove_task(to_do_list):
    view_tasks(to_do_list)
    if to_do_list:
        try:
            task_num = int(input("Enter the task number to remove: "))
            if 1 <= task_num <= len(to_do_list):
                removed_task = to_do_list.pop(task_num - 1)
                print(f"Task '{removed_task['task']}' removed successfully!")
            else:
                print("Invalid task number.")
        except ValueError:
            print("Please enter a valid number.")

def main():
    to_do_list = []
    while True:
        display_menu()
        choice = input("Choose an option (1-5): ")

        if choice == '1':
            add_task(to_do_list)
        elif choice == '2':
            view_tasks(to_do_list)
        elif choice == '3':
            mark_task_completed(to_do_list)
        elif choice == '4':
            remove_task(to_do_list)
        elif choice == '5':
            print("Exiting the program.")
            break
        else:
            print("Invalid choice. Please choose a number between 1 and 5.")

if __name__ == "__main__":
    main()
