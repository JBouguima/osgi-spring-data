
# Spring Data 2.0.0.M1 OSGi features for Karaf 4.1

----------

We will use Spring 4.3.7.RELEASE and Blueprint Gemini 2.1.0.M2 to install and use Spring Data 2.0.0.M1
on Karaf 4.1 Container.

1 - Build osgi-spring-data project: mvn clean install

2 - Install servicemix spring bundles using feature file 'spring-4.3.7-features.xml':

    feature:repo-add file:<path_to_current_directory>/spring-4.3.7-features.xml
     feature:install spring/4.3.7.RELEASE_1
     feature:install spring-aspects/4.3.7.RELEASE_1
     feature:install spring-jdbc/4.3.7.RELEASE_1
     feature:install spring-orm/4.3.7.RELEASE_1
     feature:install spring-oxm/4.3.7.RELEASE_1
     feature:install spring-instrument/4.3.7.RELEASE_1
     feature:install spring-tx/4.3.7.RELEASE_1
     
3 - Install blueprint-gemini 2.1.0.M2 using feature file 'gemini-blueprint-features.xml':

    feature:repo-add file:<path_to_current_directory>/gemini-blueprint-features.xml
     feature:install gemini-blueprint
     
4 - Install Spring Data 2.0.0.M1 using generated feature file 'features.xml' in target directory of features project:
    
    feature:repo-add file:<path_to_current_directory>/features/target/feature/feature.xml
       feature:install spring-data-commons
       feature:install spring-data-jpa
       feature:install spring-data-mongodb


------
