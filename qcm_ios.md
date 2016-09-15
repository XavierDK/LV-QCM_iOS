#QCM iOS LinkValue


*Choisissez la ou les bonnes réponses dans les questions suivantes. Cet exercice est composé de 40 questions. La difficulté évoluera au fur et a mesure des questions. Vous aurez approximativement 40 min pour terminer cette épreuve.* 


### I) question de contrôle, base de la prog

#### 1) Quelles sont les valeurs finales de “var1” et ”var2” (Objective-C)?

	NSInteger var1 = 2;
	NSInteger var2 = 3;
	var2 += 2;
	var1 += var2++;

* var1 = 7, var2 = 6 // OK
* var1 = 8, var2 = 6
* var1 = 7, var2 = 5
* var1 = 8, var2 = 5
* Ce code ne compile pas

#### 2) La gestion de mémoire est-elle correcte (Objective-C)?

	- (void)func {
		char *ptr = malloc(sizeof(char*));
	}

* Oui, le pointeur ptr est libéré à la fin de la fonction.
* Non, il faut libéré la mémoire manuellement. // OK


#### 3) Quel format permet d'afficher un float avec 2 chiffres après la virgule (Objective-C)?

* NSLog(@"%@", VALUE);
* NSLog(@"%d", VALUE);
* NSLog(@"%.2d", VALUE);
* NSLog(@"%f", VALUE);
* NSLog(@"%.2f", VALUE); // OK

#### 4) NSInteger est un typedef sur quel type (Objective-C)?

* short
* int
* unsigned int
* long // OK
* unsigned long int

#### 5) Quel est la valeur de la variable "res" (Objective-C)?

	- (void)main {
		NSInteger val = 3;
		const NSInteger res = 3;
		
		res += val;
		NSLog("res = %d", res)
	}
	
* 3
* 6
* 0
* Ce code ne compile pas // OK

#### 6) Cet enum est-il correcte?

	typedef enum {
		TestEnumA = 3,
		TestEnumB,
		TestEnumC,
		TestEnumD
	} testEnum;

* Non, la syntax de cet enum est incorrect 
* Non, on ne peux pas assigner de valeur à un enum il commence forcément par 0
* Oui, cet enum est correcte  // OK

#### 7) Quel est la valeur de la variable "varC" (Objective-C)?

	NSInteger	varA = 3;
	NSInteger	varB = 5;
	
	NSInteger	varC = (varB > varA) ? varA : varB;
	
* 0
* 2
* 5
* 3 // OK
* Ce code ne compile pas

#### 8) Quel est la valeur de la variable "res" lors du second appel (Objective-C)?

	- (void)addVal:(NSInteger)val {
		static NSInteger res = 3;
		
		res += val;
		NSLog("res = %d", res)
	}
	
	- (void)viewDidLoad {
		[self addVal:3];
		[self addVal:5];
	}
	
* 3
* 6
* 11 // OK
* 12
* Ce code ne compile pas

### II) niveau école, notions de base du langage

#### 9) Comment peut on allouer une chaine de caracteres non vide en Objective-C ?

* ```NSString *str = [NSString new]; str = "Hello World";```
* ```NSString *str = [NSString new]; str = @"Hello World";```
* ```NSString *str = [[NSString alloc] init]; str = @"Hello World";```
* ```NSString *str = [[NSString alloc] initWithFormat:@"Hello World"];``` // OK
* ```NSString *str = @"Hello World";``` // OK

#### 10) Quel est le type de base de données que iOS supporte ?

* MySQL
* Oracle
* SQLite // OK
* PostgreSQL

#### 11) Que fait la commande "Command-R" sur XCode?

* Build l'application
* Build et exécute l'application // OK
* clean puis build l'application
* clean puis build et enfin exécute l'application

#### 12) Quel fichier contient les données de configuration de l'application ?

* info.xml
* info.plist // OK
* info.xib
* plist.xml

#### 13) Un indexPath est composé d'une section et de ?

* Une row // OK
* Un path
* Un index
* Un integer

#### 14) Une propriété de classe peut être ...

* readonly // OK
* readwrite // OK
* writeonly
* executeonly
* readwriteexecute

#### 15) Une propriété atomic permet de ...

* Optimiser les performances d'accès à la propriété 
* Rendre la propriété Thread safe // OK
* Rendre la propriété readwrite

#### 16) Quelles sont les classes utiles pour faire une requêtes ?

* NSUrlRequest // OK
* NSUrlOperation
* NSSession
* NSUrlSession // OK
* NSRequest 

<br/>

###III) 1 an d'exp (junior), cas courants monde pro

#### 17) Quels sont les classes utiles pour faire fonctionner CoreData ?

* NSManagedObjectContext // OK
* NSManagedObject // OK
* NSCoreData
* NSCoreContext

#### 18) Qu’est ce que l’ARC ?

* Le garbage collector de l’objectiveC
* Une fonctionnalité du compilateur // OK
* Automatic Reference Counting // OK
* Atomic Retain Core

#### 19) Qu’est ce qu’un protocole ?

* Une interface en java // OK
* Un design pattern
* La même chose qu’une norme de codage
* Une liste de méthodes et de propriétés

#### 20) En Objective-C, que se passe t’il quand on envoie un message a un objet nil ?

* Un message d’erreur apparait dans la console
* L’application crash
* Il y a un warning à la compilation
* Rien // OK


#### 21) Quel sont les outils disponibles sur iOS pour la gestion de dépendances

* UIDependencyManager
* Cocoapods // OK
* Carthage // OK
* Reveal


#### 22) Quel(s) callback est appellé pour chaque cellule dans une tableView ?

* ```numberOfSectionsInTableView:```
* ```tableView:heightForRowAtIndexPath:``` // OK
* ```tableView:numberOfRowsInSection:```
* ```tableView:cellForRowAtIndexPath:```// OK


#### 23) Comment ajouter un élément dans un NSArray ?

* ```[array appendObject:object];```
* ```[array addObject:object];```
* ```[array insertObject:object];```
* ```array = [array arrayByAddingObject:object]``` // OK

#### 24) Quel object permet le mieux de modifier un timestamp

* NSInteger // OK
* CGFLoat
* NSTimestamp
* NSDate

<br/>


###IV) 3 ans d'exp (confirmé), cas avancés, sources de bugs etc...

#### 25) Quels sont les design patterns utilisés sur iOS?

* La KVO // OK
* Le MVC // OK
* Le MVVM // OK
* Le KVA
* Le KVC // OK
* La délégation // OK
* Les notifications // OK
* Les singletons // OK

#### 26) Avec quelle(s) classe(s) peut on temporairement désactiver les actions d’un layer en CoreAnimation ?

* UITransaction
* NSTransaction
* CATransaction // OK
* IOTransaction

#### 27) Quel est le type de retour de ce prototype ?
	
```-weardMethod:(NSString*)str;	```

* void
* id // OK
* NSString*
* Ce prototype n’est pas valide


#### 28) A quoi sert la fonction XCTAssert ?
	
* Insérer du texte dans un endroit précis d’un fichier
* Tester un morceau de code unitairement
* Tester qu'une expression renvoie bien "false" ou affiche un message d'erreur // OK
* La même chose que XCTAssertTrue // OK


#### 29) Quel est l'ordre d'héritage d'un UIButton ?

* NSObject -> UIResponder -> UIView -> UIControl -> UIButton // OK
* NSObject -> UIView -> UIResponder -> UIControl -> UIButton
* NSObject -> NSResponder -> UIControl -> UIView -> UIButton
* NSObject -> NSResponder -> UIView -> UIControl -> UIButton

#### 30) Les opérateurs suivants sont des opérateurs de collection. Vrai ou faux?

* @count
* @unionOfObject
* @explodeObject
* @min

#### 31) Quels types de fichiers sont nécessaires à la soumission d'une application

* Un certificat de développement
* Un certificat de distribution // OK
* Une clef privé/clef publique (PEM) // OK
* App File Id (AFI)
* Un provisionning Profile // OK

#### 32) Qu'est ce qu'une NSOperationQueue

* La liste des actions se déroulant actuellement dans le main thread
* Une pile d'opérations s'executant les unes a la suite des autres // OK
* Quelque chose de manquant à GCD // OK
* Une pile d'actions a traiter par une vue en background

<br/>


###V) expert, questions de veille, de parti pris


#### 33) Qu’est ce que ReactiveCocoa ?

* Un framework OpenSource // OK
* Un framework inspiré de la programmation fonctionnelle // OK
* Un framework permettant l’injection de dépendance
* API permettant de composer et de transformer des flux de valeurs // OK
* Une alternative à RxSwift // OK
* Une manière d'optimiser son code afin de rentre l'experience utilisateur plus fluide

#### 34) Qu’est ce que Typhoon ?

* Un outil disponible dans Instruments
* Un framework OpenSource // OK
* Un framework inspiré de la programmation fonctionnelle
* Un framework permettant l’injection de dépendance // OK

#### 35) Qu’est ce que Realm ?
	
* Un outil d’analyse des données de l’application
* Une base de donnée // OK
* Un outil de test “temps réel”
* Un outils de gestion de tests fonctionnels
* Un site mettant à disponibilité de très bonnes conférences // OK

#### 36) Qu'est ce que le MVVM ?

* Un remplacement du MVC // OK
* Une maniére de penser permettant de soulagé le ViewController // OK
* Une alternative à VIPER // OK
* Le Model Versionning View Model

#### 37) Qu'est ce que Tweak?

* Une librairie développée par Facebook // OK
* Une manière d'architecturer ses modeles
* Une solution afin de switcher entre différentes versions des composants de son application // OK
* Un blog très connu de veille informatique

#### 38) Sélectionner dans la liste les nouveaux frameworks introduits avec iOS9

* SpriteKit
* SceneKit // OK
* GameplayKit // OK
* MetalKit // OK
* SwiftOpenGLKit
* ContactsUI // OK
* Model I/O
* ReplayKit // OK

#### 39) Dans les librairies ci-dessous quelles sont celles développées par Facebook?

* AsyncDisplayKit // OK
* Bolts // OK
* PureLayout
* ComponentKit // OK
* ReactNative// OK

#### 40) Dans les noms suivants quels sont les développeurs très présents sur la scene des librairies OpenSources/Conférences

* Chris Eidhof // OK
* Mattt Thompson // OK
* Marck Ziwensky
* Ray Wenderlich // OK
* Zach Lumberg
* Ash Furrow // OK




