# Jenkins

1. Uruchom jenkins-a:

   ```
   make build_jenkins
   make run_jenkins
   ```

2. Otwórz w przeglądarce 127.0.0.1:8080, jeśli zostaniesz poproszony o hasło dla admina, wybierz:

   ```
   make show_me_password
   # lub
   cat jenkins/secrets/initialAdminPassword
   ```

3. Wybierz *Suggested plugins*.


## Related

- https://github.com/sheehan/job-dsl-gradle-example
- https://python-jenkins.readthedocs.io/en/latest/
- https://www.jenkins.io/doc/book/pipeline/jenkinsfile/

Tu należy wprowadzić credentials w części pipeline dla se_hello_printer_app - czyli naszej aplikacji.
W części Pipeline Definition ustawiamy na "Pipeline script from SCM".
SCM > GIT > link do repezytorium i ustawiamy credetnial.


4. Jeśli już wczorja zbudowaliście u uruchomiliście jenkinsa, wystarczy wystartować dockera:
docker start jenkins-wsb

(https://github.com/wojciech11/se_teaching_jenkins/blob/master/Makefile#L8 )

5. Restart Jenkinsa > po stronie Jenkinsa należy przygotować do restartu jak w zadaniu 13 pliku 04_CD_Cloud.pdf. (potrzebne do pluginu GreenBall)
Następnie należy wpisać te komendy:
sudo docker ps
sudo docker restart <NAME as docker>

6. Do zadania 14 "znajdź kod źródłowy w folderdze jobs i workspace" przechodzimy tam z poziomu konsoli tak jak jest to opisane w zadaniu. Jednak tu, musimy dodać:
jenkins@cc7104d52579:~/workspace$ cd $JENKINS_HOME
jenkins@cc7104d52579:~/workspace$ cd se_hello_printer_app
jenkins@cc7104d52579:~/workspace/se_hello_printer_app$ make test
