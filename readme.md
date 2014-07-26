shows how to "override" default project dependency configuration
<code>
dependencies { 
compile project(':baseLibrary') 
  // which is essentially compile project(path: ':baseLibrary', configuration:'runtime') 
} 
into 
dependencies { 
compile project(path: ':baseLibrary', configuration:'compile') 
runtime project(path: ':baseLibrary', configuration:'runtime') 
}
</code>
http://forums.gradle.org/gradle/topics/changing_default_dependency_handling_of_project_dependencies
