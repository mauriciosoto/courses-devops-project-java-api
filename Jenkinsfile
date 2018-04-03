node {
    stage 'Checkout'
    checkout scm

    stage 'Compilar'
    sh "./gradlew compileJava"

    // stage 'Test'
    //sh "./gradlew test"

    stage 'Build'
    sh "./gradlew build"

    stage 'Release'
    archiveArtifacts artifacts: 'build/**/*.jar', fingerprint: true
}
