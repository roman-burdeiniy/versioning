node
{
    stage('Checkout')
        Map scmVars = checkout
        scm commit = scmVars.GIT_COMMIT
        def packageJson = readJSON file: 'package.json'
        String version = packageJson['version']
        String qualifier = packageJson['qualifier']
        def qualifierIsRCRegex = ~/^RC\d+$/
        echo ${BUILD_NUMBER};
    }
}

    git checkout -b