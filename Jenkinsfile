import groovy.sql.Sql
import java.sql.*
//
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
                 // def url = 'jdbc:postgresql://localhost:5432:DB:postgres'
                  Class.forName("org.postgresql.Driver");
                  def user = 'postgres'
                  def password = 'shark'
                  //def driver = 'database-network_docker'
                  def driver = Class.forName('org.postgresql.Driver').newInstance() as Driver
                  connection connection = DriverManager.getConnection("jdbc:postgresql://localhost:5432:DB:postgres", "user", "password")
                  //def conn = driver.connect("jdbc:postgresql://localhost:5432", "user", "password")
                  //def sql = new Sql(conn)
                 //def sql = Sql.newInstance(url, user, password, driver)
                 connection.execute'''
    CREATE TABLE Author (
    id          INTEGER GENERATED BY DEFAULT AS IDENTITY,
    firstname   VARCHAR(64),
    lastname    VARCHAR(64)
  );
'''
                  //sql.close()
                  connection.close()                          
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
