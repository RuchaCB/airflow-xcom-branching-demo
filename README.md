# ⚡ Airflow XCom + Branching DAG

This project demonstrates the use of **XComs** and **Branching** in Apache Airflow to dynamically control the DAG flow based on runtime conditions. Only one of the downstream tasks will execute based on the condition — the other will be skipped automatically.

---

## 🔧 Features

- Uses `PythonOperator` to push/pull data via XComs
- Utilizes `BranchPythonOperator` to make a runtime decision
- Executes a specific task based on branching logic
- Skips tasks that don’t meet the branching criteria
- Built for clarity and learning

---

## 🧩 DAG Structure

`t1`: Pushes value into XCom

`branch`: Decides between `t2` and `t3` based on the XCom value

`t2` / `t3`: One runs, the other gets skipped

---

##📸 Output

Here are some screenshots showcasing the key outputs and results from running the pipeline.
![xcom_branching gif](https://github.com/user-attachments/assets/97ab38ba-1a62-488a-9cef-51385a11d941)

---

## 📚 Acknowledgment

This project is based on a learning exercise from the Udemy course:  
**[The Complete Hands-On Course to Master Apache Airflow](https://www.udemy.com/course/the-complete-hands-on-course-to-master-apache-airflow/)** by *Marc Lamberti*.

I recreated and extended the project for practice and personal learning. All credits for the original project structure and logic go to the course instructor.
