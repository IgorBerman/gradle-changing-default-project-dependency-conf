shows how to "override" default project dependency configuration

  dependencies { 
    compile project(':baseLibrary') 
    // which is essentially compile project(path: ':baseLibrary', configuration:'runtime') 
  } 
  into 
  dependencies { 
    compile project(path: ':baseLibrary', configuration:'compile') 
    runtime project(path: ':baseLibrary', configuration:'runtime') 
    compile project(path: ':baseLibrary', configuration:'archives') 
    runtime project(path: ':baseLibrary', configuration:'archives') 
  }

http://forums.gradle.org/gradle/topics/changing_default_dependency_handling_of_project_dependencies
