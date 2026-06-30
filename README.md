# Creating or download mysql db for expense project.

```
git clone https://github.com/linga-devsecops-actions/14.17.github-actions-expense-mysql.git

cd 14.17.github-actions-expense-mysql/helm

sudo vim values.yaml

deployment:
  imageURL: lingadevops/mysql
  imageVersion: v1.1

kubectl create namespace expense

helm upgrade --install mysql . -n expense

kubectl get pods -n expense

kubectl get svc -n expense

kubectl get pods -n expense

kubectl exec -it -n expense  mysql-8b749c7c8-tjwnl  -- bash

 mysql -h mysql -u root -pExpenseApp@1

use transactions;

select * from transactions;
```