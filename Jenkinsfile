//import groovy.sql.Sql
//import java.sql.Driver
//import java.sql.Connection
//import java.sql.DriverManager
//import java.sql.*


//
pipeline {


    agent { label 'slave' }
    stages {
        stage('Stage 1') {
            steps {
                sh 'docker ps'
                     catchError {
          sh " psql -h 172.28.0.1 -p 5432 -U postgres -c 'create user test4'"
        }
      }
      post {
        success {
          echo 'Build stage successful'
        }
        failure {
          echo 'Compile stage failed'



            timestamps {
     def runAnsible(message) {
     println(message)
     ansiColor('xterm') {
        ansiblePlaybook(
            colorized: true,
	    disableHostKeyChecking: true,
            installation: 'ansible',
            inventory: 'hosts',
            //credentialsId: env.CRED_ID,
            playbook: "config.yml",
            extras: '')
    }
}

	try {
	stage("Parsing data") {
		println("hello")
            runAnsible("Run!")
        }
	} catch (Exception ex) {
		println(ex)
		currentBuild.result = 'FAILURE'
	} finally {
		cleanWs()
	}
}
}

          //  sh 'ls'
           // sh 'ansible-playbook -i hosts config.yml'
          //  sh 'docker logs postgreql'
          //error('Build is aborted due to failure of build stage')

        }
      }
        }
    }
//}
               // SCRIPT_PATH = 'docker ps' 
                //sh " psql -h 172.28.0.1 -p 5432 -U postgres -c 'create user test3'"
                // check exit code
               // sсript {
      //   echo 'Running the exit script...'
       // rc = sh(script: "${SCRIPT_PATH}", returnStatus: true)

       // sh "echo \"exit code is : ${rc}\""

     //   if (rc != 0) 
     //   { 
          //  sh "echo 'exit code is NOT zero'"
      //  } 
     //   else 
     //   {
           // sh "echo 'exit code is zero'"
      //  
                
               // println ("\$?")
                //
                //bash -c  "echo \$?"
 
        //stage('stage 2') {
         // steps {
             // script {
                 // @GrabConfig(systemClassLoader=true)
                 // @Grab(group='org.postgresql', module='postgresql', version='9.4-1205-jdbc42')
                 // @Grab('org.hsqldb:hsqldb:2.5.1')
                 // @GrabConfig(systemClassLoader=true)
                  //def url = 'jdbc:postgresql://localhost:5432:DB:postgres'
                  //Class.forName("org.postgresql.Driver")
                  //def user = 'postgres'
                //  def password = 'shark'
                  //def driver = 'org.postgresql.jdbcDriver'
                  //def sql = Sql.newInstance(url, user, password, driver)
                  //def driver = 'database-network_docker'
                  //def driver = Class.forName('org.postgresql.Driver').newInstance() as Driver
                  //this.connection = DriverManager.getConnection("jdbc:postgresql://localhost:5432:DB:postgres", "user", "password")
                  //def conn = driver.connect("jdbc:postgresql://localhost:5432", "user", "password")
                  //def sql = new Sql(conn)
                 //def sql = Sql.newInstance(url, user, password, driver)
                  //Class.forName("org.postgresql.jdbc.Driver")
                  //def sql = Sql.newInstance("jdbc:postgresql://localhost:5432:DB:postgres", "user","password", "org.postgresql.jdbc.Driver")
                 /// def rows = sql.execute "select count(*) from test;"
                 // echo rows.dump()
               //  sql.execute'''
    //CREATE TABLE Author (
   // id          INTEGER GENERATED BY DEFAULT AS IDENTITY,
   // firstname   VARCHAR(64),
   // lastname    VARCHAR(64)
//  );
//'''
                 // sql.close()
                  //conn.close()                          
            //  }
          //}
       // }
   // }
//}
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
