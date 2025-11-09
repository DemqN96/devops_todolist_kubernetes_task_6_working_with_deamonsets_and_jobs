1. Застосування DaemonSet

Застосуйте маніфест:

kubectl apply -f deamonset.yml


Перевірте стан усіх подів:

kubectl get pods -o wide


Під’єднайтесь до контейнера busybox:

kubectl exec -it -n mateapp busybox -- sh

2. Застосування CronJob

Застосуйте маніфест:

kubectl apply -f cronJob.yml


Перевірте стан CronJob:

kubectl get cronjobs -o wide


Приклад виводу:

NAME            SCHEDULE      SUSPEND   ACTIVE   LAST SCHEDULE   AGE   CONTAINERS   IMAGES    SELECTOR
hello-cronjob   */1 * * * *   False     0        <none>          29s   hello        busybox   <none>


Перегляньте логи останнього запущеного пода:

kubectl logs hello-cronjob-28476958-vnkgh