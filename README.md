# Why Apache Airflow

## Member
- Nathachai Thongniran, ณัฐชัย ทองนิรันดร์, 6071009021
- Sirichart Gobpradit, สิริชาติ กอบประดิษฐ์ 6170970021
- Sittichai Tirasaengaroon, สิทธิชัย ติรแสงอรุณ, 6071033021

## Content
1. Study
2. Install the tools in Big Data ecosystem
3. How to use
4. Shared VM images
5. Link to access your VMs for demo
6. VDOs Presentation: 12 mins
7. Report
    - Installation manual (to prevent copying VM from the class)
    - Architecture diagram & Data flow diagram
    - Explanation on your solution to the objective of your project
    - Result (if any)
    - Demo (screen capture with explanation)

## CMD
```bash
ssh admin@mongo
ssh admin@airflow-project
airflow version
lsof -n -i:8080 | grep LISTEN

# print the list of active DAGs
airflow list_dags
# prints the list of tasks the "tutorial" dag_id
airflow list_tasks my_simple_dag_direction2
# prints the hierarchy of tasks in the tutorial DAG
airflow list_tasks my_simple_dag_direction2 --tree
airflow test <dag_id> <task_id> <date>
airflow test my_tutorial templated 2015-06-01
airflow test airflow_tutorial_v01 print_world 2017-07-01
airflow test airflow_tutorial_v02 greet 2017-07-01
airflow test airflow_tutorial_v02 greet 2017-07-04
airflow test my_cryptocurrency save_data 2017-07-04
airflow backfill my_tutorial -s 2015-06-01 -e 2015-06-07
airflow test my_cryptocurrency save_data 2015-06-01
```

## Reference
### Official document
- https://airflow.apache.org/
- https://airflow.apache.org/docs/apache-airflow/stable/faq.html
- https://airflow.apache.org/docs/apache-airflow/stable/start.html

### Comparison
- http://bytepawn.com/luigi-airflow-pinball.html
- https://www.quora.com/Which-is-a-better-data-pipeline-scheduling-platform-Airflow-or-Luigi

### Others / Tutorial
- https://github.com/hgrif/airflow-tutorial
- https://gtoonstra.github.io/etl-with-airflow/
- https://airflow.incubator.apache.org/tutorial.html
- https://medium.com/@mozesr/basic-airflow-73361b62814f
- https://hackernoon.com/airflow-the-missing-context-1a04b3a9475c
- https://cloud.google.com/composer/docs/how-to/using/writing-dags
- https://cwiki.apache.org/confluence/display/AIRFLOW/Common+Pitfalls
- https://robinhood.engineering/why-robinhood-uses-airflow-aed13a9a90c8
- https://engineering.pandora.com/apache-airflow-at-pandora-1d7a844d68ee
- https://medium.com/handy-tech/airflow-tips-tricks-and-pitfalls-9ba53fba14eb
- https://guptakumartanuj.wordpress.com/2018/01/08/airflow-installation-on-airflow/
- https://medium.com/airbnb-engineering/airflow-a-workflow-management-platform-46318b977fd8
- https://medium.com/wbaa/datas-inferno-7-circles-of-data-testing-hell-with-airflow-cef4adff58d8
- https://towardsdatascience.com/getting-started-with-apache-airflow-df1aa77d7b1b
- http://michal.karzynski.pl/blog/2017/03/19/developing-workflows-with-apache-airflow/
- https://medium.com/@dustinstansbury/how-quizlet-uses-apache-airflow-in-practice-a903cbb5626d
- https://medium.com/@dustinstansbury/understanding-apache-airflows-key-concepts-a96efed52b1a
- https://medium.com/bluecore-engineering/were-all-using-airflow-wrong-and-how-to-fix-it-a56f14cb0753
- https://towardsdatascience.com/why-quizlet-chose-apache-airflow-for-executing-data-workflows-3f97d40e9571
- https://medium.com/@dustinstansbury/beyond-cron-an-introduction-to-workflow-management-systems-19987afcdb5e
- https://blog.insightdatascience.com/airflow-101-start-automating-your-batch-workflows-with-ease-8e7d35387f94
- https://blog.usejournal.com/testing-in-airflow-part-1-dag-validation-tests-dag-definition-tests-and-unit-tests-2aa94970570c
- https://medium.com/inside-socialcops/how-to-create-a-workflow-in-apache-airflow-to-track-disease-outbreaks-in-india-8a7abb13bd41

### Example code
- https://github.com/kadnan/airflow-scraping
- https://github.com/gtoonstra/etl-with-airflow
- https://github.com/GoogleCloudPlatform/airflow-operator

### Misc
- https://github.com/puckel/docker-airflow

### Others
- Hooks concept
