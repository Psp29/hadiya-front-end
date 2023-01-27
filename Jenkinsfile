pipeline
{
	// agent {label 'jenkins-slave-1'}
	// environment
	// {
		
	// }
	stages
	{
		// stage('Login')
		// {
		// 	steps
		// 	{
		// 		sh 'echo $DOCKERHUB_CREDENTIALS_PSW | docker login -u $DOCKERHUB_CREDENTIALS_USR --password-stdin'
		// 	}
		// }
		stage('Install Node 16.x')
		{
			steps
			{
				sh 'curl -sL https://deb.nodesource.com/setup_16.x | sudo bash -'
				sh 'sudo apt-get install nodejs -y'
				sh 'node --version'
			}
		}
		stage('Install Angular-Cli')
		{
			steps
			{
				sh 'sudo npm install -g @angular/cli'
				// sh 'docker compose ps'
			}
		}
		stage('Build and Run Front-End')
		{
			steps
			{
				sh 'cd hadiya-front-end'
				sh 'npm install'
				sh 'npm start'
			}
		}

		// stage('Push')
		// {
		// 	steps
		// 	{
		// 		sh 'docker compose push'
		// 	}
		// }
		// stage('Deploy')
		// {
		// 	steps
		// 	{
		// 		sh 'docker compose up'
		// 	}
		// }
	}
post
	{
		always
		{
			sh 'Done :)'
		}
	}
}
