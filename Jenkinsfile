import groovy.sql.Sql
//import java.sql.Driver
//def driver = Class.forName('org.postgresql.Driver').newInstance() as Driver


pipeline {
    agent any
    stages {
        stage('Stage 1') {
            steps {
                sh 'docker ps' 
            }
        }
    

        stage('stage 2') {
          steps {
              script {
                  def url = 'jdbc:postgresql://localhost:5432:DB:postgres'
                  def user = 'postgres'
                  def password = 'shark'
//def driver = 'org.hsqldb.jdbcDriver'
                 def sql = Sql.newInstance(url, user, password)
                 sql.execute'''
    CREATE TABLE Author (
    id          INTEGER GENERATED BY DEFAULT AS IDENTITY,
    firstname   VARCHAR(64),
    lastname    VARCHAR(64)
  );
'''
                  sql.close()
              }
          }
        }
    }
}
                 // conn.close()
            //  docker.image('postgres:12.1').withRun('-p 5432') { c ->
             // psql
            // docker.image('postgres:12.1').inside("--link postgres") {
           // -c "psql -h 127.0.0.1 -U postgres -p 5432" 
            //sh  "psql CREATE USER sonar WITH PASSWORD 'sonar'"
       // sh "docker logs postgreql"
       //    "\psql -U postgres -c \"\du"
      // sh "version"
      // }
         //    }
             //   }
      //  }
   // }
//}
//}
