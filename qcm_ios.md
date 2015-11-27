#QCM iOS LinkValue


*Choisissez la ou les bonnes réponses dans les questions suivantes. Cet exercice est composé de 40 questions. La difficulté évoluera au fur et a mesure des questions. Vous aurez approximativement 40 min pour terminer cette épreuve.* 


### I) question de contrôle, base de la prog

#### 1) Quelles sont les valeurs finales de “var1” et ”var2” (Objective-C)?

	NSInteger var1 = 2;
	NSInteger var2 = 3;
	var2 += 2;
	var1 += var2++;

* var1 = 7, var2 = 6
* var1 = 8, var2 = 6
* var1 = 7, var2 = 5
* var1 = 8, var2 = 5
* Ce code ne compile pas

<br/>

#### 2) La gestion de mémoire est-elle correcte (Objective-C)?

	- (void)func {
		char *ptr = malloc(sizeof(char*));
	}

* Oui, le pointeur ptr est libéré à la fin de la fonction.
* Non, il faut libéré la mémoire manuellement.


#### 3) Quel format permet d'afficher un float avec 2 chiffres après la virgule (Objective-C)?

* NSLog(@"%@", VALUE);
* NSLog(@"%d", VALUE);
* NSLog(@"%.2d", VALUE);
* NSLog(@"%f", VALUE);
* NSLog(@"%.2f", VALUE);

#### 4) NSInteger est un typedef sur quel type (Objective-C)?

* short
* int
* unsigned int
* long int
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
* Ce code ne compile pas

#### 6) Cet enum est-il correcte?

	typedef enum {
		TestEnumA = 3,
		TestEnumB,
		TestEnumC,
		TestEnumD
	} testEnum;

* Non, la syntax de cet enum est incorrect 
* Non, on ne peux pas assigner de valeur à un enum il commence forcément par 0
* Oui, cet enum est correcte 

#### 7) Quel est la valeur de la variable "varC" (Objective-C)?

	NSInteger	varA = 3;
	NSInteger	varB = 5;
	
	NSInteger	varC = (varB > varA) ? varA : varB;
	
* 0
* 2
* 5
* 3
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
* 11
* 12
* Ce code ne compile pas

### II) niveau école, notions de base du langage

#### 9) Comment peut on allouer une chaine de caracteres non vide en Objective-C ?

* ```NSString *str = [NSString new]; str = "Hello World";```
* ```NSString *str = [NSString new]; str = @"Hello World";```
* ```NSString *str = [[NSString alloc] init]; str = @"Hello World";```
* ```NSString *str = [[NSString alloc] initWithFormat:@"Hello World"];```
* ```NSString *str = @"Hello World";```

#### 10) Quel est le type de base de données que iOS supporte ?

* MySQL
* Oracle
* SQLite
* PostgreSQL

#### 11) Quel est le raccourci clavier pour lancer l’application ?

* Command + S
* Command + R
* Option + S
* Option + R

#### 12) Quel fichier contient les données de configuration de l'application ?

* info.xml
* info.plist
* info.xib
* plist.xml

#### 13) Un indexPath est composé d'une section et de ?

* Une row
* Un path
* Un index
* Un integer

#### 14) Une propriété de classe peut être ...

* readonly
* readwrite
* writeonly
* executeonly
* readwriteexecute

#### 14) Différence entre une propriété atomic et nonatomic Vrai ou faux ?

* atomic est "Thread safe" comparé à nonatomic
* 

<br/>

###III) 1 an d'exp (junior), cas courants monde pro

#### 17) Quels sont les classes utiles pour faire fonctionner CoreData ?

* NSManagedObjectContext
* NSManagedObject
* NSCoreData
* NSCoreContext

#### 18) Qu’est ce que l’ARC ?

* Le garbage collector de l’objectiveC
* Une fonctionnalité du compilateur
* Automatic Reference Counting
* Atomic Retain Core

#### 19) Qu’est ce qu’un protocole ?

* Une interface en java
* Un design pattern
* La même chose qu’une norme de codage
* Une liste de méthodes et de propriétés

#### 20) En Objective-C, que se passe t’il quand on envoie un message a un objet nil ?

* Un message d’erreur apparait dans la console
* L’application crash
* Il y a un warning à la compilation
* Rien

#### 21) Quels sont les design patterns utilisés sur iOS?

* La KVO
* Le MVC
* Le MVVM
* Le KVA
* Le KVC
* La délégation
* Les notifications
* Les singletons


#### 22) Quel(s) callback est appellé pour chaque cellule dans une tableView ?

* ```numberOfSectionsInTableView:```
* ```tableView:heightForRowAtIndexPath:```
* ```tableView:numberOfRowsInSection:```
* ```tableView:cellForRowAtIndexPath:```


#### 23) Comment ajouter un élément dans un NSArray ?

* ```[array appendObject:object];```
* ```[array addObject:object];```
* ```[array insertObject:object];```
* ```array = [array arrayByAddingObject:object]```

#### 24) Quel object permet le mieux de stocker un timestamp

* NSInteger
* CGFLoat
* NSTimestamp
* NSDate

<br/>


###IV) 3 ans d'exp (confirmé), cas avancés, sources de bugs etc...

#### 25) Avec quelle(s) classe(s) peut on temporairement désactiver les actions d’un layer en CoreAnimation ?

* UITransaction
* NSTransaction
* CATransaction
* IOTransaction

#### 26) Quel est le type de retour de ce prototype ?
	
```-weardMethod:(NSString*)str;	```

* void
* id
* NSString*
* Ce prototype n’est pas valide


#### 27) A quoi sert la fonction XCTAssert ?
	
* Insérer du texte dans un endroit précis d’un fichier
* Tester un morceau de code unitairement
* Tester qu'une expression renvoie bien "false" ou affiche un message d'erreur
* La même chose que XCTAssertTrue


#### 28) Quel est l'ordre d'héritage d'un UIButton ?

* NSObject -> UIResponder -> UIView -> UIControl -> UIButton
* NSObject -> UIView -> UIResponder -> UIControl -> UIButton
* NSObject -> NSResponder -> UIControl -> UIView -> UIButton
* NSObject -> NSResponder -> UIView -> UIControl -> UIButton

#### 29)

#### 30)

#### 31)

#### 32)



<br/>


###V) expert, questions de veille, de parti pris


#### 33) Qu’est ce que ReactiveCocoa ?

* Un outil disponible dans Instruments
* Un framework OpenSource
* Un framework inspiré de la programmation fonctionnelle
* Un framework permettant l’injection de dépendance

#### 34) Qu’est ce que Typhoon ?

* Un outil disponible dans Instruments
* Un framework OpenSource
* Un framework inspiré de la programmation fonctionnelle
* Un framework permettant l’injection de dépendance

#### 35) Qu’est ce que Realm ?
	
* Un outil d’analyse des données de l’application
* Une base de donnée
* Un outil de test “temps réel”
* Un outils de gestion de tests fonctionnels

#### 36) Qu'est ce que le MVVM ?

#### 37) Qu'est ce que le "Protocol-Oriented Programming"?

#### 38)

#### 39)

#### 40)   



