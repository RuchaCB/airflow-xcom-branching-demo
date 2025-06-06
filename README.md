##⚡ Airflow XCom + Branching DAG
This project demonstrates the use of XComs, Branching, and Trigger Rules in Apache Airflow to control the DAG flow based on runtime conditions dynamically. Only one of the downstream tasks (t2 or t3) will execute based on the branching logic — the other will be skipped automatically. A final task (t4) runs if either path completes successfully.

---

##🔧 Features
Uses PythonOperator to push and pull data via XComs
Utilizes BranchPythonOperator to make a runtime decision
Executes a specific downstream task based on branching logic
Automatically skips the task that doesn't meet the branching condition
Uses trigger_rule='one_success' to ensure the final task runs if any upstream task succeeds
Clear and minimal DAG structure for learning and demonstration

---

## 🧩 DAG Structure

`t1`: Pushes a value into XCom

`branch`: Evaluates the value and decides which task to execute

`t2`: Runs if a specific condition is met

`t3`: Runs otherwise (fallback)

`t4`: Runs if either t2 or t3 is successful, thanks to trigger_rule='one_success'

---

##📸 Output

Here are some screenshots showcasing the key outputs and results from running the pipeline.
![xcom_branching gif](https://github.com/user-attachments/assets/97ab38ba-1a62-488a-9cef-51385a11d941)
![xcom_branching](https://github.com/user-attachments/assets/358184df-66e4-4859-9555-267e1bd1857d)

---

## 📚 Acknowledgment

This project is based on a learning exercise from the Udemy course:  
**[The Complete Hands-On Course to Master Apache Airflow](https://www.udemy.com/course/the-complete-hands-on-course-to-master-apache-airflow/)** by *Marc Lamberti*.

I recreated and extended the project for practice and personal learning. All credits for the original project structure and logic go to the course instructor.
