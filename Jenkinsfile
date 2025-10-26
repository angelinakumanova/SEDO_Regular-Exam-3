pipeline{
    agent any

    // .NET 8 SDK must be installed
    stages{
        stage("Build .NET Project") {
          steps {
            bat 'dotnet build' // For Windows (per requirement, no seperate restore stage)
          }
        }
        stage("Run Unit and Integration Tests") {
          steps {
            bat 'dotnet test --no-build --verbosity normal' // For Windows
          }
        }
    }

}
