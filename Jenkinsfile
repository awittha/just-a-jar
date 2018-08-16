node( "legacy" ) {
	ws( UUID.randomUUID().toString() ) {
		stage( "Setup" ) {
			checkout scm
		}
		
		stage( "Build" ) {
			sh( "./mvnw clean deploy" )
		}
		
		stage( "Run" ) {
			sh( "java -jar target/just-a-jar*.jar" )
		}
	}
}