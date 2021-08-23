---
description: Chaque classe de fenêtre a une procédure de fenêtre associée partagée par toutes les fenêtres de la même classe. La procédure de fenêtre traite les messages de toutes les fenêtres de cette classe et contrôle leur comportement et leur apparence.
ms.assetid: db79fd4b-6a15-4bf9-a0d9-5f6415f6c75f
title: À propos des classes de fenêtre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fcb46d862bf5b9249bb4f13b111ac10c441c3e687dd3fb1784f355c40d14b72
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119932329"
---
# <a name="about-window-classes"></a>À propos des classes de fenêtre

Chaque classe de fenêtre a une procédure de fenêtre associée partagée par toutes les fenêtres de la même classe. La procédure de fenêtre traite les messages de toutes les fenêtres de cette classe et contrôle leur comportement et leur apparence. Pour plus d’informations, consultez [Window Procedures](window-procedures.md).

Un processus doit inscrire une classe de fenêtre pour pouvoir créer une fenêtre de cette classe. L’inscription d’une classe de fenêtre associe une procédure de fenêtre, des styles de classe et d’autres attributs de classe à un nom de classe. Lorsqu’un processus spécifie un nom de classe dans la fonction [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) ou [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) , le système crée une fenêtre avec la procédure de fenêtre, les styles et d’autres attributs associés à ce nom de classe.

Cette section décrit les rubriques suivantes.

-   [Types de classes de fenêtres](#types-of-window-classes)
    -   [Classes système](#system-classes)
    -   [Classes globales d’application](#application-global-classes)
    -   [Classes de l’application locale](#application-local-classes)
-   [Comment le système localise une classe de fenêtre](#how-the-system-locates-a-window-class)
-   [Inscription d’une classe de fenêtre](#registering-a-window-class)
-   [Éléments d’une classe de fenêtre](#elements-of-a-window-class)
    -   [Nom de la classe](#class-name)
    -   [Adresse de la procédure de fenêtre](#window-procedure-address)
    -   [Handle d’instance](#instance-handle)
    -   [Curseur de classe](#class-cursor)
    -   [Icônes de classe](#class-icons)
    -   [Pinceau d’arrière-plan de classe](#class-background-brush)
    -   [Menu classe](#class-menu)
    -   [Styles de la classe](#class-styles)
    -   [Mémoire de classe supplémentaire](#extra-class-memory)
    -   [Mémoire de fenêtre supplémentaire](#extra-window-memory)

## <a name="types-of-window-classes"></a>Types de classes de fenêtres

Il existe trois types de classes de fenêtres :

-   [Classes système](#system-classes)
-   [Classes globales d’application](#application-global-classes)
-   [Classes de l’application locale](#application-local-classes)

Ces types diffèrent dans l’étendue et dans le moment et la façon dont ils sont inscrits et détruits.

### <a name="system-classes"></a>Classes système

Une classe système est une classe de fenêtre inscrite par le système. De nombreuses classes système sont disponibles pour tous les processus à utiliser, tandis que d’autres sont utilisées uniquement en interne par le système. Étant donné que le système enregistre ces classes, un processus ne peut pas les détruire.

le système inscrit les classes système pour un processus la première fois que l’un de ses threads appelle un utilisateur ou une fonction Windows Graphics Device Interface (GDI).

Chaque application reçoit sa propre copie des classes système. toutes les applications de type Windows 16 bits dans le même VDM partagent les mêmes classes système, tout comme elles le font sur des Windows 16 bits.

Le tableau suivant décrit les classes système qui peuvent être utilisées par tous les processus.



| Classe     | Description                         |
|-----------|-------------------------------------|
| Bouton    | Classe pour un bouton.             |
| Liste déroulante  | Classe pour une zone de liste déroulante.          |
| Modifier      | Classe pour un contrôle d’édition.      |
| ListBox   | Classe pour une zone de liste.           |
| MDIClient | Classe pour une fenêtre cliente MDI. |
| ScrollBar | Classe d’une barre de défilement.         |
| statique    | Classe pour un contrôle statique.     |



 

Le tableau suivant décrit les classes système qui sont disponibles uniquement pour une utilisation par le système. Ils sont répertoriés ici pour des raisons d’exhaustivité.



| Classe      | Description                                                            |
|------------|------------------------------------------------------------------------|
| ComboLBox  | Classe de la zone de liste contenue dans une zone de liste déroulante.                   |
| DDEMLEvent | classe pour les événements de la bibliothèque de gestion des échange dynamique de données (DDEML). |
| Message    | Classe pour une fenêtre de message uniquement.                                   |
| \#32768    | Classe d’un menu.                                                  |
| \#32769    | Classe de la fenêtre du bureau.                                      |
| \#32770    | Classe d’une boîte de dialogue.                                            |
| \#32771    | Classe de la fenêtre du commutateur de tâche.                                  |
| \#32772    | Classe pour les titres d’icône.                                             |



 

### <a name="application-global-classes"></a>Classes globales d’application

Une [classe globale d’application](#application-global-classes) est une classe de fenêtre inscrite par un exécutable ou une dll qui est disponible pour tous les autres modules du processus. Par exemple, votre .dll pouvez appeler la fonction [**RegisterClassEx**](/windows/win32/api/winuser/nf-winuser-registerclassexa) pour inscrire une classe de fenêtre qui définit un contrôle personnalisé en tant que classe globale d’application afin qu’un processus qui charge le .dll puisse créer des instances du contrôle personnalisé.

Pour créer une classe qui peut être utilisée dans chaque processus, créez la classe de fenêtre dans un .dll et chargez le .dll dans chaque processus. Pour charger les .dll dans chaque processus, ajoutez son nom à la **valeur \_ DLL AppInit** dans la clé de Registre suivante :

**HKEY \_ logiciel de l' \_ ordinateur LOCAL** \\  \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Windows**

Chaque fois qu’un processus démarre, le système charge le .dll spécifié dans le contexte du processus qui vient d’être démarré avant d’appeler sa fonction de point d’entrée. Le .dll doit inscrire la classe pendant sa procédure d’initialisation et doit spécifier le style **cs \_ GLOBALCLASS** . Pour plus d’informations, consultez [styles de classe](#class-styles).

Pour supprimer une classe globale d’application et libérer le stockage qui lui est associé, utilisez la fonction [**UnregisterClass**](/windows/win32/api/winuser/nf-winuser-unregisterclassa) .

### <a name="application-local-classes"></a>Classes de l’application locale

Une [classe d’application locale](#application-local-classes) est une classe de fenêtre qu’un exécutable ou .dll inscrit pour son usage exclusif. Bien que vous puissiez inscrire n’importe quel nombre de classes locales, il est généralement possible de n’en inscrire qu’une seule. Cette classe de fenêtre prend en charge la procédure de fenêtre de la fenêtre principale de l’application.

Le système détruit une classe locale lorsque le module qui l’a inscrit se ferme. Une application peut également utiliser la fonction [**UnregisterClass**](/windows/win32/api/winuser/nf-winuser-unregisterclassa) pour supprimer une classe locale et libérer le stockage qui lui est associé.

## <a name="how-the-system-locates-a-window-class"></a>Comment le système localise une classe de fenêtre

Le système gère une liste de structures pour chacun des trois types de classes de fenêtres. Quand une application appelle la fonction [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) ou [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) pour créer une fenêtre avec une classe spécifiée, le système utilise la procédure suivante pour rechercher la classe.

1.  Recherchez dans la liste des classes de l’application locale une classe portant le nom spécifié dont le handle d’instance correspond au handle d’instance du module. (Plusieurs modules peuvent utiliser le même nom pour enregistrer des classes locales dans le même processus.)
2.  Si le nom ne figure pas dans la liste classe locale de l’application, recherchez la liste des classes globales de l’application.
3.  Si le nom ne figure pas dans la liste des classes globales de l’application, recherchez la liste des classes système.

Toutes les fenêtres créées par l’application utilisent cette procédure, y compris les fenêtres créées par le système au nom de l’application, telles que les boîtes de dialogue. Il est possible de substituer des classes système sans affecter d’autres applications. Autrement dit, une application peut inscrire une classe locale d’application portant le même nom qu’une classe système. Cela remplace la classe système dans le contexte de l’application, mais n’empêche pas les autres applications d’utiliser la classe système.

## <a name="registering-a-window-class"></a>Inscription d’une classe de fenêtre

Une classe de fenêtre définit les attributs d’une fenêtre, tels que son style, son icône, son curseur, son menu et sa procédure de fenêtre. La première étape de l’inscription d’une classe de fenêtre consiste à remplir une structure [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) avec les informations de classe de fenêtre. Pour plus d’informations, consultez [éléments d’une classe de fenêtre](#elements-of-a-window-class). Ensuite, transmettez la structure à la fonction [**RegisterClassEx**](/windows/win32/api/winuser/nf-winuser-registerclassexa) . Pour plus d’informations, consultez [utilisation des classes de fenêtre](using-window-classes.md).

Pour inscrire une classe globale d’application, spécifiez le \_ style cs GLOBALCLASS dans le membre **style** de la structure [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) . Lors de l’inscription d’une classe de l’application locale, ne spécifiez pas le style **cs \_ GLOBALCLASS** .

Si vous inscrivez la classe de fenêtre à l’aide de la version ANSI de [**RegisterClassEx**](/windows/win32/api/winuser/nf-winuser-registerclassexa), **RegisterClassExA**, l’application demande que le système passe les paramètres de texte des messages aux fenêtres de la classe créée à l’aide du jeu de caractères ANSI. Si vous inscrivez la classe à l’aide de la version Unicode de **RegisterClassEx**, **RegisterClassExW**, l’application demande que le système passe les paramètres de texte des messages aux fenêtres de la classe créée à l’aide du jeu de caractères Unicode. La fonction [**IsWindowUnicode**](/windows/win32/api/winuser/nf-winuser-iswindowunicode) permet aux applications d’interroger la nature de chaque fenêtre. Pour plus d’informations sur les fonctions ANSI et Unicode, consultez [conventions pour les prototypes de fonction](/windows/desktop/Intl/conventions-for-function-prototypes).

L’exécutable ou la DLL qui a inscrit la classe est le propriétaire de la classe. Le système détermine la propriété de la classe à partir du membre **HINSTANCE** de la structure [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) transmise à la fonction [**RegisterClassEx**](/windows/win32/api/winuser/nf-winuser-registerclassexa) lorsque la classe est inscrite. Pour les dll, le membre **HINSTANCE** doit être le descripteur de l’instance .dll.

La classe n’est pas détruite lorsque l' .dll qui le possède est déchargée. Par conséquent, si le système appelle la procédure de fenêtre pour une fenêtre de cette classe, cela entraîne une violation d’accès, car le .dll contenant la procédure de fenêtre n’est plus en mémoire. Le processus doit détruire toutes les fenêtres à l’aide de la classe avant que le .dll soit déchargé et appeler la fonction [**UnregisterClass**](/windows/win32/api/winuser/nf-winuser-unregisterclassa) .

## <a name="elements-of-a-window-class"></a>Éléments d’une classe de fenêtre

Les éléments d’une classe de fenêtre définissent le comportement par défaut des fenêtres appartenant à la classe. L’application qui inscrit une classe de fenêtre assigne des éléments à la classe en définissant les membres appropriés dans une structure [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) et en passant la structure à la fonction [**RegisterClassEx**](/windows/win32/api/winuser/nf-winuser-registerclassexa) . Les fonctions [**GetClassInfoEx**](/windows/win32/api/winuser/nf-winuser-getclassinfoexa) et [**GetClassLong**](/windows/win32/api/winuser/nf-winuser-getclasslonga) récupèrent des informations sur une classe de fenêtre donnée. La fonction [**SetClassLong**](/windows/win32/api/winuser/nf-winuser-setclasslonga) modifie les éléments d’une classe locale ou globale déjà inscrite par l’application.

Bien qu’une classe de fenêtre complète soit composée de nombreux éléments, le système nécessite uniquement qu’une application fournisse un nom de classe, l’adresse de la procédure de fenêtre et un handle d’instance. Utilisez les autres éléments pour définir des attributs par défaut pour les fenêtres de la classe, telles que la forme du curseur et le contenu du menu de la fenêtre. Vous devez initialiser tous les membres inutilisés de la structure [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) à zéro ou **null**. Les éléments de classe de fenêtre sont répertoriés dans le tableau suivant.



| Élément                                               | Objectif                                                                                                                                                                                                                                       |
|-------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Nom de la classe](#class-name)                             | Distingue la classe des autres classes inscrites.                                                                                                                                                                                        |
| [Adresse de la procédure de fenêtre](#window-procedure-address) | Pointeur vers la fonction qui traite tous les messages envoyés à Windows dans la classe et définit le comportement de la fenêtre.                                                                                                                      |
| [Handle d’instance](#instance-handle)                   | Identifie l’application ou .dll qui a inscrit la classe.                                                                                                                                                                                 |
| [Curseur de classe](#class-cursor)                         | Définit le curseur de la souris que le système affiche pour une fenêtre de la classe.                                                                                                                                                                  |
| [Icônes de classe](#class-icons)                           | Définit la grande icône et la petite icône.                                                                                                                                                                                                    |
| [Pinceau d’arrière-plan de classe](#class-background-brush)     | Définit la couleur et le motif qui remplissent la zone cliente lorsque la fenêtre est ouverte ou peinte.                                                                                                                                                 |
| [Menu classe](#class-menu)                             | Spécifie le menu par défaut pour les fenêtres qui ne définissent pas explicitement un menu.                                                                                                                                                                  |
| [Styles de la classe](#class-styles)                         | Définit comment mettre à jour la fenêtre après l’avoir déplacée ou redimensionnée, comment traiter les double-clics de la souris, comment allouer de l’espace pour le contexte de périphérique et d’autres aspects de la fenêtre.                                                       |
| [Mémoire de classe supplémentaire](#extra-class-memory)             | Spécifie la quantité de mémoire supplémentaire, en octets, que le système doit réserver pour la classe. Toutes les fenêtres de la classe partagent la mémoire supplémentaire et peuvent l’utiliser pour n’importe quel rôle défini par l’application. Le système initialise cette mémoire à zéro. |
| [Mémoire de fenêtre supplémentaire](#extra-window-memory)           | Spécifie la quantité de mémoire supplémentaire, en octets, que le système doit réserver pour chaque fenêtre appartenant à la classe. La mémoire supplémentaire peut être utilisée pour n’importe quelle fonction définie par l’application. Le système initialise cette mémoire à zéro.          |



 

### <a name="class-name"></a>Nom de la classe

Chaque classe de fenêtre a besoin d’un [nom de classe](#class-name) pour faire la distinction entre une classe et une autre. Assignez un nom de classe en définissant le membre **lpszClassName** de la structure [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) sur l’adresse d’une chaîne terminée par le caractère null qui spécifie le nom. Étant donné que les classes de fenêtre sont spécifiques au processus, les noms des classes de fenêtre doivent être uniques dans le même processus. En outre, étant donné que les noms de classes occupent de l’espace dans la table Atom Private du système, vous devez conserver les chaînes de noms de classe aussi courtes que possible.

La fonction [**GetClassName**](/windows/win32/api/winuser/nf-winuser-getclassname) récupère le nom de la classe à laquelle appartient une fenêtre donnée.

### <a name="window-procedure-address"></a>Adresse de la procédure de fenêtre

Chaque classe a besoin d’une adresse de procédure de fenêtre pour définir le point d’entrée de la procédure de fenêtre utilisée pour traiter tous les messages pour les fenêtres de la classe. Le système transmet des messages à la procédure lorsqu’il a besoin de la fenêtre pour effectuer des tâches, telles que la peinture de sa zone cliente ou la réponse aux entrées de l’utilisateur. Un processus affecte une procédure de fenêtre à une classe en copiant son adresse dans le membre **lpfnWndProc** de la structure [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) . Pour plus d’informations, consultez [Window Procedures](window-procedures.md).

### <a name="instance-handle"></a>Handle d’instance

Chaque classe de fenêtre requiert un handle d’instance pour identifier l’application ou .dll qui a inscrit la classe. Le système requiert des handles d’instance pour effectuer le suivi de tous les modules. Le système affecte un handle à chaque copie d’un exécutable en cours d’exécution ou .dll.

Le système passe un handle d’instance à la fonction de point d’entrée de chaque exécutable (consultez [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain)) et .dll (consultez [**DllMain**](/windows/desktop/Dlls/dllmain)). L’exécutable ou .dll affecte ce handle d’instance à la classe en le copiant dans le membre **HINSTANCE** de la structure [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) .

### <a name="class-cursor"></a>Curseur de classe

Le *curseur de classe* définit la forme du curseur lorsqu’il se trouve dans la zone cliente d’une fenêtre de la classe. Le système définit automatiquement le curseur sur la forme donnée lorsque le curseur entre dans la zone cliente de la fenêtre et s’assure qu’il conserve cette forme pendant qu’elle reste dans la zone cliente. Pour affecter une forme de curseur à une classe de fenêtre, chargez une forme de curseur prédéfinie à l’aide de la fonction [**LoadCursor**](/windows/desktop/api/winuser/nf-winuser-loadcursora) , puis affectez le handle de curseur retourné au membre **hCursor** de la structure [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) . Vous pouvez également fournir une ressource de curseur personnalisée et utiliser la fonction **LoadCursor** pour la charger à partir des ressources de l’application.

Le système ne requiert pas de curseur de classe. Si une application définit le membre **hCursor** de la structure [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) sur **null**, aucun curseur de classe n’est défini. Le système suppose que la fenêtre définit la forme du curseur chaque fois que le curseur passe dans la fenêtre. Une fenêtre peut définir la forme de curseur en appelant la fonction [**SetCursor**](/windows/desktop/api/winuser/nf-winuser-setcursor) chaque fois que la fenêtre reçoit le message [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) . Pour plus d’informations sur les curseurs, consultez [curseurs](/windows/desktop/menurc/cursors).

### <a name="class-icons"></a>Icônes de classe

Une *icône de classe* est une image que le système utilise pour représenter une fenêtre d’une classe particulière. Une application peut avoir deux icônes de classe : une grande et une petite. Le système affiche l’icône de *grande classe* d’une fenêtre dans la fenêtre de commutateur de tâches qui s’affiche lorsque l’utilisateur appuie sur Alt + Tab et dans les grandes icônes de la barre des tâches et de l’Explorateur. L' *icône petite classe* apparaît dans la barre de titre d’une fenêtre et dans les petites icônes de la barre des tâches et de l’Explorateur.

Pour assigner une grande et une petite icône à une classe de fenêtre, spécifiez les descripteurs des icônes dans les membres **HICON** et **hIconSm** de la structure [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) . Les dimensions de l’icône doivent être conformes aux dimensions requises pour les grandes et les petites icônes de classe. Pour une grande icône de classe, vous pouvez déterminer les dimensions requises en spécifiant les valeurs **SM \_ CXICON** et **SM \_ CYICON** dans un appel à la fonction [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) . Pour une petite icône de classe, spécifiez les valeurs **SM \_ CXSMICON** et **SM \_ CYSMICON** . Pour plus d’informations, consultez [icônes](/windows/desktop/menurc/icons).

Si une application définit les membres **HICON** et **hIconSm** de la structure [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) sur la **valeur null**, le système utilise l’icône d’application par défaut comme grandes et petites icônes de classe pour la classe de fenêtre. Si vous spécifiez une grande icône de classe, mais pas une petite, le système crée une petite icône de classe basée sur la grande. Toutefois, si vous spécifiez une petite icône de classe mais pas une grande, le système utilise l’icône d’application par défaut comme icône de classe importante et l’icône spécifiée comme petite icône de classe.

Vous pouvez remplacer l’icône de classe grande ou petite pour une fenêtre particulière à l’aide du message [**WM \_ SETICON**](wm-seticon.md) . Vous pouvez récupérer l’icône actuelle de petite ou petite classe en utilisant le message [**WM \_ GETICON**](wm-geticon.md) .

### <a name="class-background-brush"></a>Pinceau d’arrière-plan de classe

Un *pinceau d’arrière-plan de classe* prépare la zone cliente d’une fenêtre pour un dessin ultérieur par l’application. Le système utilise le pinceau pour remplir la zone cliente avec une couleur unie ou un motif, supprimant ainsi toutes les images précédentes de cet emplacement, qu’elles appartiennent ou non à la fenêtre. Le système avertit une fenêtre que son arrière-plan doit être peint en envoyant le message [**WM \_ ERASEBKGND**](wm-erasebkgnd.md) à la fenêtre. Pour plus d’informations, consultez [pinceaux](/windows/desktop/gdi/brushes).

Pour assigner un pinceau d’arrière-plan à une classe, créez un pinceau à l’aide des fonctions GDI appropriées et assignez le handle de pinceau retourné au membre **hbrBackground** de la structure [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) .

Au lieu de créer un pinceau, une application peut définir le membre **hbrBackground** sur l’une des valeurs de couleur système standard. Pour obtenir la liste des valeurs de couleurs système standard, consultez [**SetSysColors**](/windows/desktop/api/winuser/nf-winuser-setsyscolors).

Pour utiliser une couleur système standard, l’application doit augmenter de 1 la valeur de la couleur d’arrière-plan. Par exemple, **l' \_ arrière-plan de couleur** + 1 est la couleur d’arrière-plan du système. Vous pouvez également utiliser la fonction [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) pour récupérer un handle vers un pinceau qui correspond à une couleur système standard, puis spécifier le handle dans le membre **hbrBackground** de la structure [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) .

Le système ne requiert pas qu’une classe de fenêtre ait un pinceau d’arrière-plan de classe. Si ce paramètre a la valeur **null**, la fenêtre doit peindre son propre arrière-plan chaque fois qu’elle reçoit le message [**WM \_ ERASEBKGND**](wm-erasebkgnd.md) .

### <a name="class-menu"></a>Menu classe

Un *menu de classe* définit le menu par défaut qui sera utilisé par les fenêtres dans la classe si aucun menu explicite n’est fourni lors de la création des fenêtres. Un menu est une liste de commandes à partir desquelles un utilisateur peut choisir des actions à effectuer par l’application.

Vous pouvez assigner un menu à une classe en définissant le membre **lpszMenuName** de la structure [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) sur l’adresse d’une chaîne terminée par le caractère null qui spécifie le nom de ressource du menu. Le menu est supposé être une ressource dans l’application donnée. Le système charge automatiquement le menu quand cela est nécessaire. Si la ressource de menu est identifiée par un entier et non par un nom, l’application peut définir le membre **lpszMenuName** sur cet entier en appliquant la macro [**MAKEINTRESOURCE**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea) avant d’assigner la valeur.

Le système n’a pas besoin d’un menu de classe. Si une application définit le membre **lpszMenuName** de la structure [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) sur **null**, les fenêtres de la classe n’ont pas de barres de menus. Même si aucun menu de classe n’est fourni, une application peut toujours définir une barre de menus pour une fenêtre lorsqu’elle crée la fenêtre.

Si un menu est fourni pour une classe et qu’une fenêtre enfant de cette classe est créée, le menu est ignoré. Pour plus d’informations, consultez [menus](/windows/desktop/menurc/menus).

### <a name="class-styles"></a>Styles de la classe

Les styles de classe définissent des éléments supplémentaires de la classe de fenêtre. Plusieurs styles peuvent être combinés à l’aide de l’opérateur or au niveau du bit ( \| ). Pour assigner un style à une classe de fenêtre, assignez le style au membre de **style** de la structure [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) . Pour obtenir la liste des styles de classe, consultez [**styles de classe de fenêtre**](window-class-styles.md).

### <a name="classes-and-device-contexts"></a>Classes et contextes de périphérique

Un *contexte de périphérique* est un ensemble spécial de valeurs que les applications utilisent pour dessiner dans la zone cliente de leurs fenêtres. Le système requiert un contexte de périphérique pour chaque fenêtre de l’affichage, mais offre une certaine souplesse dans la manière dont le système stocke et traite ce contexte de périphérique.

Si aucun style de contexte de périphérique n’est explicitement donné, le système suppose que chaque fenêtre utilise un contexte de périphérique (Device Context) récupéré à partir d’un pool de contextes gérés par le système. Dans ce cas, chaque fenêtre doit récupérer et initialiser le contexte de périphérique avant de le peindre et de le libérer après la peinture.

Pour éviter de récupérer un contexte de périphérique chaque fois qu’il doit peindre dans une fenêtre, une application peut spécifier le style **cs \_ OWNDC** pour la classe de fenêtre. Ce style de classe indique au système de créer un contexte de périphérique privé, c’est-à-dire d’allouer un contexte de périphérique unique pour chaque fenêtre de la classe. L’application n’a besoin de récupérer le contexte qu’une seule fois, puis de l’utiliser pour la peinture suivante.

### <a name="extra-class-memory"></a>Mémoire de classe supplémentaire

Le système gère une structure [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) en interne pour chaque classe de fenêtre dans le système. Lorsqu’une application inscrit une classe de fenêtre, elle peut demander au système d’allouer et d’ajouter un certain nombre d’octets de mémoire supplémentaires à la fin de la structure **WNDCLASSEX** . Cette mémoire est appelée *mémoire de classe supplémentaire* et est partagée par toutes les fenêtres appartenant à la classe. Utilisez la mémoire de classe supplémentaire pour stocker toutes les informations relatives à la classe.

Étant donné que la mémoire supplémentaire est allouée à partir du tas local du système, une application doit utiliser la mémoire de classe supplémentaire avec modération. La fonction [**RegisterClassEx**](/windows/win32/api/winuser/nf-winuser-registerclassexa) échoue si la quantité de mémoire de classe supplémentaire demandée est supérieure à 40 octets. Si une application requiert plus de 40 octets, elle doit allouer sa propre mémoire et stocker un pointeur vers la mémoire dans la mémoire de classe supplémentaire.

Les fonctions [**SetClassWord**](/windows/win32/api/winuser/nf-winuser-setclassword) et [**SetClassLong**](/windows/win32/api/winuser/nf-winuser-setclasslonga) copient une valeur dans la mémoire de classe supplémentaire. Pour récupérer une valeur de la mémoire de classe supplémentaire, utilisez les fonctions [**GetClassWord**](/windows/win32/api/winuser/nf-winuser-getclassword) et [**GetClassLong**](/windows/win32/api/winuser/nf-winuser-getclasslonga) . Le membre **cbClsExtra** de la structure [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) spécifie la quantité de mémoire de classe supplémentaire à allouer. Une application qui n’utilise pas de mémoire de classe supplémentaire doit initialiser le membre **cbClsExtra** à zéro.

### <a name="extra-window-memory"></a>Mémoire de fenêtre supplémentaire

Le système gère une structure de données interne pour chaque fenêtre. Lors de l’inscription d’une classe de fenêtre, une application peut spécifier un nombre d’octets de mémoire supplémentaires, appelé *mémoire de fenêtre supplémentaire*. Lors de la création d’une fenêtre de la classe, le système alloue et ajoute la quantité de mémoire de fenêtre supplémentaire spécifiée à la fin de la structure de la fenêtre. Une application peut utiliser cette mémoire pour stocker des données spécifiques à la fenêtre.

Étant donné que la mémoire supplémentaire est allouée à partir du tas local du système, une application doit utiliser la mémoire de fenêtre supplémentaire avec modération. La fonction [**RegisterClassEx**](/windows/win32/api/winuser/nf-winuser-registerclassexa) échoue si la quantité de mémoire de fenêtre supplémentaire demandée est supérieure à 40 octets. Si une application requiert plus de 40 octets, elle doit allouer sa propre mémoire et stocker un pointeur vers la mémoire dans la mémoire de fenêtre supplémentaire.

La fonction [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) copie une valeur dans la mémoire supplémentaire. La fonction [**GetWindowLong**](/windows/win32/api/winuser/nf-winuser-getwindowlonga) récupère une valeur à partir de la mémoire supplémentaire. Le membre **cbWndExtra** de la structure [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) spécifie la quantité de mémoire de fenêtre supplémentaire à allouer. Une application qui n’utilise pas la mémoire doit initialiser **cbWndExtra** à zéro.

 

 
