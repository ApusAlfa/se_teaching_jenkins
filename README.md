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
