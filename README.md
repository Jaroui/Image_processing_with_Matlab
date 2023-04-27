# Image_processing_with_Matlab


Traitement d’images sur MATLAB

 

Etudiante :	Assia Jaroui 	
Professeur-responsable du projet : Dr. Meryam ELMOUHTADI	



Introduction:

Le traitement d’images est un domaine très vaste qui a connu, et qui connait encore, un développement important depuis quelques dizaines d’années. On désigne par traitement d’images numériques l’ensemble des techniques permettant de modifier une image numérique afin d’améliorer ou d’en extraire des informations. De ce fait, le traitement d’images est l’ensemble des méthodes et techniques opérant sur celles-ci, dans le but de rendre cette opération possible, plus simple, plus efficace et plus agréable, d’améliorer l’aspect visuel de l’image et d’en extraire des informations jugées pertinentes.
	Matlab est un logiciel qui est pertinent dans le domaine du traitement d’image, il est parmi les outils les plus utilisés dans ce domaine. MATLAB est une abréviation de Matrix LABoratory, il a été conçu par Cleve Moler à la fin des années 1970, c’est un environnement puissant, complet et facile à utiliser. Il apporte aux ingénieurs, chercheurs et à tout scientifique un systéme interactif intégrant calcul numérique et visualisation. C’est un environnement performant, ouvert et programmable qui permet de remarquer les gains de productivité et de créativité. MATLAB comprend un ensemble d’outils spécifiques à des domaines, en particulier en traitement de l’image, appelés Toolboxes (Boites à Outils).
Le but de ce mémoire est d’illustrer en détail les commandes et instructions contenues dans la boite d’outils dédiée au traitement de l’image, notamment la manipulation des images .
	 

Définitions :
1.1.	Image mathématique : 
Une image est plutôt difficile à décrire d’une façon générale. En traitement d’image, la majorité du temps, on considère qu’il s’agit d’une fonction mathématique de R x R dans R ou le couplet d’entrée est considéré comme une position spatiale, le singleton de sortie comme l’intensité (couleur ou niveaux de gris) du phénomène physique. Il arrive cependant que l’image soit dite "3D" donc la fonction est de R x R x R dans R. Les images couleurs peuvent être représentées soit par trois images représentant les trois couleurs fondamentales, soit par une image de R x R dans R x R x R . Soit un Ω ouvert borné de R , une image est définie comme une fonction

![image](https://user-images.githubusercontent.com/86842189/234878917-569319f0-55c6-4f3d-8d6f-98b718a67435.png)

		   		 
1.2.	Image numérique :
L’image numérique est l’image dont la surface est divisée en éléments de tailles fixes appelés cellules ou pixels, ayant chacun comme caractéristique un niveau de gris ou de couleurs prélevé à l’emplacement correspondant dans l’image réelle, ou calculé à partir d’une description interne de la scène à représenter.

![image](https://user-images.githubusercontent.com/86842189/234878852-4ecbf174-a555-46e2-a8b4-eb99040ffe69.png)

Figure 1: Représentation du pixel



1.3.	Les types d’image :
a)	Image binaire :
Une image binaire est une image M x N où  chaque point peut prendre uniquement la valeur 0 ou 1. Les pixels sont noirs (0) ou blancs (1).
 
![image](https://user-images.githubusercontent.com/86842189/234879027-41bcc76b-1695-4a38-a592-7adbf4c76abb.png)

Figure 2: une image binaire

b)	 Image en niveaux de gris :
Niveaux de gris est une gamme de monochromatique nuances du noir au blanc. Par conséquent, une image en niveaux de gris ne contient que des nuances de gris et aucune couleur.
Tandis que numérique, les images peuvent être enregistrées en niveaux de gris (ou en noir et blanc), même les images couleur contiennent des informations en niveaux de gris. C'est parce que chaque pixel a une valeur de luminance, quelle que soit sa couleur. La luminance peut également être décrite comme une luminosité ou une intensité, qui peut être mesurée sur une échelle allant du noir (intensité nulle) au blanc (intensité maximale)

![image](https://user-images.githubusercontent.com/86842189/234879068-f8fb080b-0920-4550-aae3-2786006bea50.png)
 
Figure 3: image en niveaux de gris





c)	Image en couleur :
Même s’il est parfois utile de pouvoir représenter des images en noir et blanc, les applications multimédias utilisent le plus souvent des images en couleurs. La représentation des couleurs s’effectue de la même manière que les images monochromes avec cependant quelques particularités. En effet, il faut tout d’abord choisir un modèle de représentation. On peut représenter les couleurs à l’aide de leurs composantes primaires. Une image couleur est la composition de trois (ou plus) images en niveaux de gris sur trois (ou plus) composantes. On définit donc trois plans de niveaux de gris, un rouge, un vert et un bleu. La couleur finale est obtenue par synthèse  additive des ces trois (ou plus) composantes.
 
![image](https://user-images.githubusercontent.com/86842189/234879124-5eb3a312-7d41-435d-a4a7-6e94a9a403e7.png)

Figure 4: décomposition d'une image couleur  en RGB












Manipulation :

1-	Ouverture et lecture d’une image :
A l’aide du Matlab , lire l’image « Flowers.jpg» puis l’afficher
	Code Matlab 
![image](https://user-images.githubusercontent.com/86842189/234879190-3a4dc1c6-0881-494d-98fe-5849983a2fa2.png)

![image](https://user-images.githubusercontent.com/86842189/234879237-1ba32822-9d43-4b60-9e6c-ed72f8190ed5.png)

Figure 5 : Affichage d'image originale


2-	Inverse d’une image :
Faire pivoter une image à l'aide de la fonction imrotate. Lorsqu’on  fait pivoter une image, On spécifie l'image à faire pivoter et l'angle de rotation, en degrés. Si on spécifie un angle de rotation positif, l'image pivote dans le sens inverse des aiguilles d'une montre ; Sinon, l'image pivote dans le sens des aiguilles d'une montre. Par défaut, l'image de sortie est suffisamment grande pour inclure l'intégralité de l'image d'origine.
	Code Matlab
![image](https://user-images.githubusercontent.com/86842189/234879354-e1230eb1-fdf5-4b78-b4f4-031d7dd0e080.png)

 
![image](https://user-images.githubusercontent.com/86842189/234879404-462acc03-ceb2-409b-9950-3975259bfd3f.png)
 
Figure 6 : Rotation d'image




3-	Conversion et affichage d’image en niveaux de gris :
Pour convertir une image RGB en une image en niveaux de gris, vous pouvez utiliser la fonction rgb2gray de l'Image processing Toolbox.
	Code Matlab
![image](https://user-images.githubusercontent.com/86842189/234879485-19bccae4-6b95-427b-b297-216b5cd23299.png)

 

![image](https://user-images.githubusercontent.com/86842189/234879524-e39f6276-7aec-4626-abaf-803b92a11f77.png)
 
Figure 7: Conversion d'image en niveaux de gris





4-	Conversion et affichage d’image en blanc et noir :
im2bw (I, niveau) convertit l'image en niveaux de gris I en image binaire BW, en remplaçant tous les pixels de l'image d'entrée avec une luminance supérieure au niveau par la valeur 1 (blanc) et en remplaçant tous les autres pixels par la valeur 0 (noir).
	Code Matlab
![image](https://user-images.githubusercontent.com/86842189/234879577-2b15982c-d673-4caf-989b-d964c2997e57.png)

 
![image](https://user-images.githubusercontent.com/86842189/234879619-73de9850-e4f2-4699-81bd-95eb838298a3.png)
 
Figure 8 : conversion d'image en blanc et noir (binaire)






Intégration des programmes dans une seule interface GUI :
I.	Définition d’une interface sous Matlab :
Les interfaces graphiques sont appelées GUI (Graphical User Interface) sous MATLAB. Elles permettent à l’utilisateur d’interagir avec un programme informatique, grâce aux différents objets graphiques (bouton,  menus, cases à cocher, texte statique, des axes ….).Ces objets sont généralement actionnés à l’aide de la souris ou du clavier.














II.	Création d’une interface GUI sous MATLAB :

Le placement des objets est réalisé par sélection dans une boite à outils. Leur mise en place et leur dimensionnement se font à l'aide de la souris.
![image](https://user-images.githubusercontent.com/86842189/234879770-4224273c-ce14-49c1-aaf1-59c5761e7667.png)

 
Un double-clique sur un objet permet de faire apparaître le Property Inspector où les propriétés des objets sont facilement éditables. Leurs modifications et la visualisation de ces modifications sont immédiates.

![image](https://user-images.githubusercontent.com/86842189/234879826-6ce109df-81d8-4a4f-865a-90dda4fcb767.png)

 
+ Le GUIDE possède également des outils pour gérer l'alignement des objets et pour créer des barres d'outils ou des menus.
+ Une fois l'interface graphique terminée, son enregistrement donne deux fichiers portant le même nom mais dont les deux extensions sont .fig et .m.
+ Le fichier .fig contient la définition des objets graphiques (positions et propriétés). Ce fichier peut être ouvert ultérieurement avec le GUIDE pour modifier les objets graphiques.
+ Le fichier .m contient les lignes de code qui assurent le fonctionnement de l'interface graphique (actions des objets). Ce fichier peut être édité dans le MATLAB Editor pour y ajouter des actions à la main. C'est ce fichier qui doit être lancé pour utiliser l'interface graphique.
III.	Intégrations des programmes au dessus dans une seule interface GUI :

![image](https://user-images.githubusercontent.com/86842189/234880000-42c5b640-f07c-4f02-85e7-4e870bfc25a9.png)

 
-	 Choisir  push button et ajouter les boutons nécessaires pour le traitement , on les fait déplacer vers « Panel» que j’ai nommé Operations comme le montre la figure ci-dessus .
-	Choisir « Axes» et dessiner deux fenêtres  d’acquisition et de traitement , l’une va afficher l’image originale et l’autre l’autre après modification .
-	On double click sur chaque objet  pour le personnaliser (String , tag , fontsize, background color…..)
-	Une fois l’interface est terminée , le sauvegarde du fichier « GUIDE» donne un autre fichier .m  Interface1.m qui est le programme principal qui fait appelle des sous programmes sous formes de fonctions :
 
Présentation des fonctions utilisées dans chaque objet :
![image](https://user-images.githubusercontent.com/86842189/234880059-b5eb89dc-f3bf-4699-ad04-c9376abec017.png)
![image](https://user-images.githubusercontent.com/86842189/234880084-603acd16-b170-4fa8-a5b7-22b5713c0b92.png)


   
-	uigetfile :  permet à l'utilisateur de sélectionner un ou plusieurs fichiers dans un dossier de son choix. 
-	setappdata  :   stocke le contenu de val pour une récupération ultérieure.
-	imread (nom de fichier) :  lit l'image à partir du fichier spécifié par nom de fichier, en déduisant le format du fichier à partir de son contenu
-	Axes (handles.axes1) : Cela signifie que les axes actuels doivent être réglés sur axes1. Tout ce que vous faites comme title(), xlabel(), ylabel(), plot(), bar(), legend() ou autre, sera désormais appliqué à axes1 (à moins que vous ne passiez explicitement un axe différent dans la fonction qui remplacerait les axes courants par défaut).
+Reset :
 
Imshow : affiche l'image dans une figure

![image](https://user-images.githubusercontent.com/86842189/234880164-29b1cd02-699f-4e85-ab00-ac43c93edc9b.png)
![image](https://user-images.githubusercontent.com/86842189/234880199-dbde9e47-d38d-4743-bcf0-029d33c0291f.png)


Les résultats des fonctions utilisées seront affichés sur l’axe 2 grâce à axes(handles.axes2).


![image](https://user-images.githubusercontent.com/86842189/234880329-09adc508-e51d-4813-92dc-01641eedbc15.png)


+ Inverse :

•	90° :  
![image](https://user-images.githubusercontent.com/86842189/234880380-26bf525a-6e0d-4ab5-9e76-815daec245fa.png)

•	180° :
 ![image](https://user-images.githubusercontent.com/86842189/234880419-42909936-a228-423e-b5bd-9c4c1a8aa2be.png)

•	360° :
 ![image](https://user-images.githubusercontent.com/86842189/234880461-3eba4a18-669c-4d22-b9a4-de769c8fdc36.png)

+RGB vers Gris :
 ![image](https://user-images.githubusercontent.com/86842189/234880499-d89530f1-ac90-4e60-b5fe-58865c05bc69.png)


+RGB vers Binaire
  ![image](https://user-images.githubusercontent.com/86842189/234880565-22717135-96d6-412e-8071-e7bbec1895ca.png)
 
Les fonctions utilisées au dessus sont expliquées dans le chapitre de manipulation (imrotate, rgb2gray,im2bw).
Getappdata() : On utilise cette fonction pour récupérer les données stockées à l'aide de la fonction setappdata. Ces deux fonctions offrent un moyen pratique de partager des données entre des rappels ou entre des interfaces utilisateur distinctes.




Conclusion :

Le traitement d'images permet de modifier le contenu des images afin de tirer l'information utile pour une application particulière. Matlab offre de nombreuses possibilités de traitement avec une palette très fournie d'outils prêts à l'emploi. Toutefois Matlab permet de déployer rapidement des tests pour vérifier la validité d'une méthode de traitement d'images. La manipulation d'images revient à la manipulation de matrices qui est très facile grâce au langage de haut niveau de Matlab.
Bibliographie :
https://www.mathworks.com/?s_tid=gn_logo
http://www.numerical-tours.com/matlab/introduction_6_elementary_fr/
https://fr.slideshare.net/HajerDahech/traitement-dimage-sous-matlab
file:///C:/Users/ASSIA/Desktop/bourahla%20houda-%20rabhi%20chaima.pdf
http://matlab.izmiran.ru/help/techdoc/ref/uigetfile.html
https://matlab.developpez.com/faq/?page=gui#:~:text=uigetfileDocumentation%20de%20la%20fonction,le%20menu%20Fichier%20%E2%86%92%20Ouvrir.
http://www-lagis.univ-lille1.fr/~bonnet/Outils_Simul/Complements_GUI.pdf



