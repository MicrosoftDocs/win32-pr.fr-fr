---
description: Cette rubrique décrit les éléments de programmation que les applications utilisent pour créer et utiliser Windows. gérer les relations entre les fenêtres ; et taille, déplacement et affichage des fenêtres.
ms.assetid: e325f8dc-004f-44a9-9122-3be5e44764d6
title: À propos de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e2df510deea689d70bd1ebf5e59cafc92b0389d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104202920"
---
# <a name="about-windows"></a>À propos de Windows

Cette rubrique décrit les éléments de programmation que les applications utilisent pour créer et utiliser Windows. gérer les relations entre les fenêtres ; et taille, déplacement et affichage des fenêtres.

La vue d’ensemble comprend les rubriques suivantes.

-   [Fenêtre du Bureau](#desktop-window)
-   [Fenêtres d’application](#application-windows)
    -   [Zone cliente](#client-area)
    -   [Zone non cliente](#nonclient-area)
-   [Contrôles et boîtes de dialogue](#controls-and-dialog-boxes)
-   [Attributs de fenêtre](#window-attributes)
    -   [Nom de la classe](#class-name)
    -   [Nom de fenêtre](#window-name)
    -   [Style de la fenêtre](#window-style)
    -   [Style de fenêtre étendu](#extended-window-style)
    -   [Position](#position)
    -   [Taille](#size)
    -   [Handle de fenêtre parente ou propriétaire](#parent-or-owner-window-handle)
    -   [Handle de menu ou identificateur de Child-Window](#menu-handle-or-child-window-identifier)
    -   [Handle d’instance d’application](#application-instance-handle)
    -   [Données de création](#creation-data)
    -   [Handle de la fenêtre](#window-handle)
-   [Création de fenêtres](#creation-data)
    -   [Création de la fenêtre principale](#main-window-creation)
    -   [Messages de création de fenêtre](#window-creation-messages)
    -   [Applications multithread](#multithread-applications)

## <a name="desktop-window"></a>Fenêtre du Bureau

Lorsque vous démarrez le système, celui-ci crée automatiquement la fenêtre du bureau. La *fenêtre du Bureau* est une fenêtre définie par le système qui peint l’arrière-plan de l’écran et sert de base pour toutes les fenêtres affichées par toutes les applications.

La fenêtre du Bureau utilise une image bitmap pour peindre l’arrière-plan de l’écran. Le modèle créé par la bitmap est appelé le *Papier peint du Bureau*. Par défaut, la fenêtre du Bureau utilise l’image bitmap d’un fichier. bmp spécifié dans le registre en tant que papier peint du bureau.

La fonction [**GetDesktopWindow**](/windows/win32/api/winuser/nf-winuser-getdesktopwindow) retourne un handle vers la fenêtre du bureau.

Une application de configuration système, telle qu’un élément du panneau de configuration, modifie le papier peint du Bureau à l’aide de la fonction [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) avec le paramètre *WAction* défini sur **SPI \_ SETDESKWALLPAPER** et le paramètre *lpvParam* en spécifiant un nom de fichier bitmap. **SystemParametersInfo** charge ensuite le bitmap à partir du fichier spécifié, utilise l’image bitmap pour peindre l’arrière-plan de l’écran et entre le nouveau nom de fichier dans le registre.

## <a name="application-windows"></a>Fenêtres d’application

Chaque application graphique Windows crée au moins une fenêtre, appelée *fenêtre principale*, qui sert d’interface principale entre l’utilisateur et l’application. La plupart des applications créent également d’autres fenêtres, directement ou indirectement, pour effectuer les tâches associées à la fenêtre principale. Chaque fenêtre joue un rôle dans l’affichage de la sortie et la réception de l’entrée de l’utilisateur.

Lorsque vous démarrez une application, le système associe également un bouton de barre des tâches à l’application. Le *bouton de la barre des tâches* contient l’icône et le titre du programme. Lorsque l’application est active, son bouton de la barre des tâches est affiché dans l’État pushd.

Une fenêtre d’application comprend des éléments tels qu’une barre de titre, une barre de menus, le menu fenêtre (anciennement appelé « menu système »), le bouton réduire, le bouton Agrandir, le bouton restaurer, le bouton Fermer, une bordure de redimensionnement, une zone cliente, une barre de défilement horizontale et une barre de défilement verticale. La fenêtre principale d’une application comprend généralement tous ces composants. L’illustration suivante montre ces composants dans une fenêtre principale classique.

![fenêtre classique](images/cswin-02.png)

### <a name="client-area"></a>Zone cliente

La *zone cliente* est la partie d’une fenêtre dans laquelle l’application affiche la sortie, par exemple du texte ou des graphiques. Par exemple, une application de publication de bureau affiche la page active d’un document dans la zone cliente. L’application doit fournir une fonction, appelée procédure de fenêtre, pour traiter l’entrée dans la fenêtre et afficher la sortie dans la zone cliente. Pour plus d’informations, consultez [Window Procedures](window-procedures.md).

### <a name="nonclient-area"></a>Zone non cliente

La barre de titre, la barre de menus, le menu fenêtre, les boutons réduire et agrandir, la bordure de redimensionnement et les barres de défilement sont désignés collectivement comme la *zone non cliente* de la fenêtre. Le système gère la plupart des aspects de la zone non cliente. l’application gère l’apparence et le comportement de sa zone cliente.

La *barre de titre* affiche une icône et une ligne de texte définies par l’application. en règle générale, le texte spécifie le nom de l’application ou indique l’objectif de la fenêtre. Une application spécifie l’icône et le texte lors de la création de la fenêtre. La barre de titre permet également à l’utilisateur de déplacer la fenêtre à l’aide d’une souris ou d’un autre dispositif de pointage.

La plupart des applications incluent une *barre de menus* qui répertorie les commandes prises en charge par l’application. Les éléments de la barre de menus représentent les principales catégories de commandes. Le fait de cliquer sur un élément dans la barre de menus ouvre généralement un menu contextuel dont les éléments correspondent aux tâches d’une catégorie donnée. En cliquant sur une commande, l’utilisateur indique à l’application d’effectuer une tâche.

Le *menu fenêtre* est créé et géré par le système. Il contient un ensemble standard d’éléments de menu qui, lorsqu’il est choisi par l’utilisateur, définissent la taille ou la position d’une fenêtre, ferme l’application ou effectue des tâches. Pour plus d’informations, consultez [menus](/windows/desktop/menurc/menus).

Les boutons situés dans l’angle supérieur droit affectent la taille et la position de la fenêtre. Lorsque vous cliquez sur le *bouton Agrandir*, le système agrandit la fenêtre à la taille de l’écran et positionne la fenêtre, de sorte qu’elle couvre l’ensemble du bureau, moins la barre des tâches. En même temps, le système remplace le bouton Agrandir par le bouton restaurer. Lorsque vous cliquez sur le *bouton Restaurer*, le système restaure la fenêtre à sa taille et à sa position précédentes. Lorsque vous cliquez sur le *bouton réduire*, le système réduit la fenêtre à la taille du bouton de la barre des tâches, positionne la fenêtre sur le bouton de la barre des tâches et affiche le bouton de la barre des tâches dans son état normal. Pour restaurer l’application à sa taille et à sa position précédentes, cliquez sur le bouton de la barre des tâches. Lorsque vous cliquez sur le *bouton Fermer*, l’application se ferme.

La *bordure de redimensionnement* est une zone autour du périmètre de la fenêtre qui permet à l’utilisateur de dimensionner la fenêtre à l’aide d’une souris ou d’un autre dispositif de pointage.

La *barre de défilement horizontale* et la *barre de défilement verticale* convertissent l’entrée de souris ou de clavier en valeurs utilisées par une application pour déplacer le contenu de la zone cliente horizontalement ou verticalement. Par exemple, une application de traitement de texte qui affiche un long document fournit généralement une barre de défilement verticale pour permettre à l’utilisateur d’effectuer une page vers le haut et vers le haut dans le document.

## <a name="controls-and-dialog-boxes"></a>Contrôles et boîtes de dialogue

Une application peut créer plusieurs types de fenêtres en plus de sa fenêtre principale, y compris les contrôles et les boîtes de dialogue.

Un *contrôle* est une fenêtre utilisée par une application pour obtenir une information spécifique de l’utilisateur, telle que le nom d’un fichier à ouvrir ou la taille de point souhaitée d’une sélection de texte. Les applications utilisent également des contrôles pour obtenir les informations nécessaires pour contrôler une fonctionnalité particulière d’une application. Par exemple, une application de traitement de texte fournit généralement un contrôle pour permettre à l’utilisateur d’activer et de désactiver le retour automatique à la main. Pour plus d’informations, consultez [contrôles Windows](/windows/desktop/Controls/window-controls).

Les contrôles sont toujours utilisés conjointement à une autre fenêtre, généralement, une boîte de dialogue. Une *boîte de dialogue* est une fenêtre qui contient un ou plusieurs contrôles. Une application utilise une boîte de dialogue pour inviter l’utilisateur à entrer les données nécessaires à l’exécution d’une commande. Par exemple, une application qui comprend une commande permettant d’ouvrir un fichier affiche une boîte de dialogue qui comprend des contrôles dans lesquels l’utilisateur spécifie un chemin d’accès et un nom de fichier. Les boîtes de dialogue n’utilisent généralement pas le même jeu de composants de fenêtre qu’une fenêtre principale. La plupart disposent d’une barre de titre, d’un menu fenêtre, d’une bordure (sans redimensionnement) et d’une zone client, mais elles ne disposent généralement pas d’une barre de menus, de boutons réduire et agrandir, ni de barres de défilement. Pour plus d’informations, consultez [boîtes de dialogue](/windows/desktop/dlgbox/dialog-boxes).

Une boîte de *message* est une boîte de dialogue spéciale qui affiche une note, une attention ou un avertissement à l’utilisateur. Par exemple, une boîte de message peut informer l’utilisateur d’un problème rencontré par l’application lors de l’exécution d’une tâche. Pour plus d’informations, consultez [boîtes de message](/windows/desktop/dlgbox/about-dialog-boxes).

## <a name="window-attributes"></a>Attributs de fenêtre

Une application doit fournir les informations suivantes lors de la création d’une fenêtre. (À l’exception du [handle de fenêtre](#window-handle), que la fonction de création retourne pour identifier de manière unique la nouvelle fenêtre.)

-   [Nom de la classe](#class-name)
-   [Nom de fenêtre](#window-name)
-   [Style de la fenêtre](#window-style)
-   [Style de fenêtre étendu](#extended-window-style)
-   [Position](#position)
-   [Taille](#size)
-   [Handle de fenêtre parente ou propriétaire](#parent-or-owner-window-handle)
-   [Handle de menu ou identificateur de Child-Window](#menu-handle-or-child-window-identifier)
-   [Handle d’instance d’application](#application-instance-handle)
-   [Données de création](#creation-data)
-   [Handle de la fenêtre](#window-handle)

Ces attributs de fenêtre sont décrits dans les sections suivantes.

### <a name="class-name"></a>Nom de la classe

Chaque fenêtre appartient à une classe de fenêtre. Une application doit inscrire une classe de fenêtre avant de créer des fenêtres de cette classe. La *classe de fenêtre* définit la plupart des aspects de l’apparence et du comportement d’une fenêtre. Le composant principal d’une classe de fenêtre est la *procédure de fenêtre*, une fonction qui reçoit et traite toutes les entrées et demandes envoyées à la fenêtre. Le système fournit les entrées et les demandes sous la forme de *messages*. Pour plus d’informations, consultez [classes de fenêtre](window-classes.md), procédures de [fenêtre](window-procedures.md), et [messages et files d’attente de messages](messages-and-message-queues.md).

### <a name="window-name"></a>Nom de fenêtre

Un *nom de fenêtre* est une chaîne de texte qui identifie une fenêtre pour l’utilisateur. Une fenêtre principale, une boîte de dialogue ou une boîte de message affiche généralement son nom de fenêtre dans sa barre de titre, le cas échéant. Un contrôle peut afficher son nom de fenêtre, en fonction de la classe du contrôle. Par exemple, les boutons, les contrôles d’édition et les contrôles statiques affichent leurs noms de fenêtre dans le rectangle occupé par le contrôle. Toutefois, les contrôles tels que les zones de liste et les zones de liste déroulante n’affichent pas leurs noms de fenêtre.

Pour modifier le nom de la fenêtre après avoir créé une fenêtre, utilisez la fonction [**SetWindowText**](/windows/win32/api/winuser/nf-winuser-setwindowtexta) . Cette fonction utilise les fonctions [**GetWindowTextLength**](/windows/win32/api/winuser/nf-winuser-getwindowtextlengtha) et [**GetWindowText**](/windows/win32/api/winuser/nf-winuser-getwindowtexta) pour récupérer la chaîne de nom de fenêtre active à partir de la fenêtre.

### <a name="window-style"></a>Style de la fenêtre

Chaque fenêtre possède un ou plusieurs styles de fenêtre. Un style de fenêtre est une constante nommée qui définit un aspect de l’apparence et du comportement de la fenêtre qui n’est pas spécifié par la classe de la fenêtre. Une application définit généralement des styles de fenêtre lors de la création de fenêtres. Elle peut également définir les styles après la création d’une fenêtre à l’aide de la fonction [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) .

Le système et, dans une certaine mesure, la procédure de fenêtre pour la classe, interpréter les styles de fenêtre.

Certains styles de fenêtre s’appliquent à toutes les fenêtres, mais s’appliquent le plus aux fenêtres de classes de fenêtres spécifiques. Les styles de fenêtre généraux sont représentés par des constantes qui commencent par le \_ préfixe WS ; elles peuvent être combinées avec l’opérateur or pour former différents types de fenêtres, y compris les fenêtres principales, les boîtes de dialogue et les fenêtres enfants. Les styles de fenêtre spécifiques à la classe définissent l’apparence et le comportement des fenêtres appartenant aux classes de contrôle prédéfinies. Par exemple, la classe **ScrollBar** spécifie un contrôle de barre de défilement, mais les styles d’arrière-plan de [**SBS \_ Horiz**](../controls/scroll-bar-control-styles.md) et **SBS \_** déterminent si un contrôle de barre de défilement horizontal ou vertical est créé.

Pour obtenir la liste des styles qui peuvent être utilisés par Windows, consultez les rubriques suivantes :

-   [**Styles de fenêtre**](window-styles.md)
-   [Styles de bouton](../controls/button-styles.md)
-   [Styles de zone de liste déroulante](../controls/combo-box-styles.md)
-   [Modifier les styles de contrôle](../controls/edit-control-styles.md)
-   [Styles de zone de liste](../controls/list-box-styles.md)
-   [Styles de contrôle RichEdit](../controls/rich-edit-control-styles.md)
-   [Styles de contrôle de barre de défilement](../controls/scroll-bar-control-styles.md)
-   [Styles de contrôle statiques](../controls/static-control-styles.md)

### <a name="extended-window-style"></a>Style de fenêtre étendu

Chaque fenêtre peut éventuellement avoir un ou plusieurs styles de fenêtre étendus. Un *style de fenêtre étendu* est une constante nommée qui définit un aspect de l’apparence et du comportement de la fenêtre qui n’est pas spécifié par la classe de fenêtre ou les autres styles de fenêtre. Une application définit généralement des styles de fenêtre étendus lors de la création de fenêtres. Elle peut également définir les styles après la création d’une fenêtre à l’aide de la fonction [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) .

Pour plus d’informations, consultez [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa).

### <a name="position"></a>Position

La position d’une fenêtre est définie en tant que coordonnées de son coin supérieur gauche. Ces coordonnées, parfois appelées coordonnées de fenêtre, sont toujours relatives à l’angle supérieur gauche de l’écran ou, pour une fenêtre enfant, au coin supérieur gauche de la zone cliente de la fenêtre parente. Par exemple, une fenêtre de niveau supérieur ayant les coordonnées (10, 10) est placée 10 pixels à droite du coin supérieur gauche de l’écran et 10 pixels vers le haut. Une fenêtre enfant ayant les coordonnées (10, 10) est placée à 10 pixels à droite du coin supérieur gauche de la zone cliente de la fenêtre parente et se trouve à 10 pixels en dessous.

La fonction [**WindowFromPoint**](/windows/win32/api/winuser/nf-winuser-windowfrompoint) récupère un handle vers la fenêtre occupant un point particulier sur l’écran. De même, les fonctions [**ChildWindowFromPoint**](/windows/win32/api/winuser/nf-winuser-childwindowfrompoint) et [**ChildWindowFromPointEx**](/windows/win32/api/winuser/nf-winuser-childwindowfrompointex) récupèrent un handle vers la fenêtre enfant qui occupe un point particulier dans la zone cliente de la fenêtre parente. Bien que **ChildWindowFromPointEx** puisse ignorer les fenêtres enfants invisibles, désactivées et transparentes, **ChildWindowFromPoint** ne peut pas.

### <a name="size"></a>Taille

La taille d’une fenêtre (largeur et hauteur) est donnée en pixels. Une fenêtre peut avoir une largeur ou une hauteur égale à zéro. Si une application définit la largeur et la hauteur d’une fenêtre sur zéro, le système définit la taille sur la taille de fenêtre minimale par défaut. Pour découvrir la taille de fenêtre minimale par défaut, une application utilise la fonction [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) avec les indicateurs **SM \_ CXMIN** et **SM \_ CYMIN** .

Une application peut avoir besoin de créer une fenêtre avec une zone cliente d’une taille particulière. Les fonctions [**AdjustWindowRect**](/windows/win32/api/winuser/nf-winuser-adjustwindowrect) et [**AdjustWindowRectEx**](/windows/win32/api/winuser/nf-winuser-adjustwindowrectex) calculent la taille requise d’une fenêtre en fonction de la taille souhaitée pour la zone cliente. L’application peut passer les valeurs de taille résultantes à la fonction [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) .

Une application peut dimensionner une fenêtre de manière à ce qu’elle soit extrêmement volumineuse ; Toutefois, la taille d’une fenêtre ne doit pas être supérieure à celle de l’écran. Avant de définir la taille d’une fenêtre, l’application doit vérifier la largeur et la hauteur de l’écran à l’aide de [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) avec les indicateurs **SM \_ CXSCREEN** et **SM \_ CYSCREEN** .

### <a name="parent-or-owner-window-handle"></a>Handle de fenêtre parente ou propriétaire

Une fenêtre peut avoir une fenêtre parente. Une fenêtre ayant un parent est appelée une *fenêtre enfant*. La *fenêtre parente* fournit le système de coordonnées utilisé pour positionner une fenêtre enfant. Avoir une fenêtre parente affecte les aspects de l’apparence d’une fenêtre ; par exemple, une fenêtre enfant est découpée afin qu’aucune partie de la fenêtre enfant ne puisse apparaître en dehors des bordures de sa fenêtre parente.

Une fenêtre qui n’a pas de parent, ou dont le parent est la fenêtre du bureau, est appelée une *fenêtre de niveau supérieur*. Une application peut utiliser la fonction [**EnumWindows**](/windows/win32/api/winuser/nf-winuser-enumwindows) pour obtenir un handle pour chaque fenêtre de niveau supérieur à l’écran. **EnumWindows** passe le handle à chaque fenêtre de niveau supérieur, à son tour, à une fonction de rappel définie par l’application, [**EnumWindowsProc**](/previous-versions/windows/desktop/legacy/ms633498(v=vs.85)).

Une fenêtre de niveau supérieur peut être propriétaire ou détenue par une autre fenêtre. Une *fenêtre enfant* s’affiche toujours devant sa fenêtre propriétaire, est masquée lorsque sa fenêtre propriétaire est réduite et est détruite lorsque sa fenêtre propriétaire est détruite. Pour plus d’informations, consultez [fenêtres détenues](window-features.md#owned-windows).

### <a name="menu-handle-or-child-window-identifier"></a>Handle de menu ou identificateur de Child-Window

Une fenêtre enfant peut avoir un identificateur de *fenêtre enfant* , une valeur unique, définie par l’application, associée à la fenêtre enfant. Les identificateurs de fenêtre enfant sont particulièrement utiles dans les applications qui créent plusieurs fenêtres enfants. Lors de la création d’une fenêtre enfant, une application spécifie l’identificateur de la fenêtre enfant. Après la création de la fenêtre, l’application peut modifier l’identificateur de la fenêtre à l’aide de la fonction [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) , ou elle peut récupérer l’identificateur à l’aide de la fonction [**GetWindowLong**](/windows/win32/api/winuser/nf-winuser-getwindowlonga) .

Chaque fenêtre, à l’exception d’une fenêtre enfant, peut avoir un menu. Une application peut inclure un menu en fournissant un handle de menu lors de l’inscription de la classe de la fenêtre ou lors de la création de la fenêtre.

### <a name="application-instance-handle"></a>Handle d’instance d’application

Chaque application est associée à un handle d’instance. Le système fournit le descripteur d’instance à une application au démarrage de l’application. Étant donné qu’il peut exécuter plusieurs copies de la même application, le système utilise des handles d’instance en interne pour distinguer une instance d’une application d’une autre. L’application doit spécifier le handle d’instance dans de nombreuses fenêtres différentes, y compris celles qui créent des fenêtres.

### <a name="creation-data"></a>Données de création

Toutes les fenêtres peuvent être associées à des données de création définies par l’application. Lorsque la fenêtre est créée pour la première fois, le système passe un pointeur vers les données dans la procédure de fenêtre de la fenêtre en cours de création. La procédure de fenêtre utilise les données pour initialiser des variables définies par l’application.

### <a name="window-handle"></a>Handle de la fenêtre

Après la création d’une fenêtre, la fonction de création retourne un *handle de fenêtre* qui identifie de façon unique la fenêtre. Un handle de fenêtre a le type de données **HWND** ; une application doit utiliser ce type lors de la déclaration d’une variable qui contient un handle de fenêtre. Une application utilise ce handle dans d’autres fonctions pour diriger ses actions vers la fenêtre.

Une application peut utiliser la fonction [**FindWindow**](/windows/win32/api/winuser/nf-winuser-findwindowa) pour déterminer si une fenêtre portant le nom de classe ou le nom de fenêtre spécifié existe dans le système. Si une telle fenêtre existe, **FindWindow** retourne un handle à la fenêtre. Pour limiter la recherche aux fenêtres enfants d’une application particulière, utilisez la fonction [**FindWindowEx**](/windows/win32/api/winuser/nf-winuser-findwindowexa) .

La fonction [**IsWindow**](/windows/win32/api/winuser/nf-winuser-iswindow) détermine si un handle de fenêtre identifie une fenêtre valide existante. Il existe des constantes spéciales qui peuvent remplacer un handle de fenêtre dans certaines fonctions. Par exemple, une application peut utiliser **la \_ diffusion HWND** dans les fonctions [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) et [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) , ou le **\_ Bureau HWND** dans la fonction [**MapWindowPoints**](/windows/desktop/api/winuser/nf-winuser-mapwindowpoints) .

## <a name="window-creation"></a>Création de fenêtres

Pour créer des fenêtres d’application, utilisez la fonction [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) ou [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) . Vous devez fournir les informations requises pour définir les attributs de la fenêtre. **CreateWindowEx** a un paramètre, *DwExStyle*, que **CreateWindow** n’a pas ; dans le cas contraire, les fonctions sont identiques. En fait, **CreateWindow** appelle simplement **CreateWindowEx** avec le paramètre *dwExStyle* défini à zéro. Pour cette raison, le reste de cette vue d’ensemble fait uniquement référence à **CreateWindowEx**.

Cette section contient les rubriques suivantes :

-   [Création de la fenêtre principale](#main-window-creation)
-   [Messages de création de fenêtre](#window-creation-messages)
-   [Applications multithread](#multithread-applications)

> [!Note]  
> Il existe des fonctions supplémentaires pour créer des fenêtres à usage spécifique, telles que les boîtes de dialogue et les boîtes de message. Pour plus d’informations, consultez [**DialogBox**](/windows/desktop/api/winuser/nf-winuser-dialogboxa), [**createDialog**](/windows/desktop/api/winuser/nf-winuser-createdialoga)et [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox).

 

### <a name="main-window-creation"></a>Création de la fenêtre principale

Chaque application Windows doit avoir [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) comme fonction de point d’entrée. **WinMain** effectue un certain nombre de tâches, y compris l’inscription de la classe de fenêtre pour la fenêtre principale et la création de la fenêtre principale. **WinMain** inscrit la classe de fenêtre principale en appelant la fonction [**registerClass**](/windows/win32/api/winuser/nf-winuser-registerclassa) et crée la fenêtre principale en appelant la fonction [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) .

Votre fonction [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) peut également limiter votre application à une seule instance. Créez un mutex nommé à l’aide de la fonction [**CreateMutex**](/windows/desktop/api/synchapi/nf-synchapi-createmutexa) . Si [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne une erreur, une autre instance de votre application existe (elle a créé le mutex) et vous devez quitter **WinMain**. **\_ \_**

Le système n’affiche pas automatiquement la fenêtre principale après l’avoir créée. au lieu de cela, une application doit utiliser la fonction [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) pour afficher la fenêtre principale. Après la création de la fenêtre principale, la fonction [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) de l’application appelle **ShowWindow**, en lui transmettant deux paramètres : un handle vers la fenêtre principale et un indicateur spécifiant si la fenêtre principale doit être réduite ou agrandie lorsqu’elle est affichée pour la première fois. Normalement, l’indicateur peut être défini sur l’une des constantes commençant par le \_ préfixe SW. Toutefois, lorsque **ShowWindow** est appelé pour afficher la fenêtre principale de l’application, l’indicateur doit avoir la valeur **SW \_ SHOWDEFAULT**. Cet indicateur indique au système d’afficher la fenêtre telle qu’elle est dirigée par le programme qui a démarré l’application.

Si une classe de fenêtre a été inscrite avec la version Unicode de [**registerClass**](/windows/win32/api/winuser/nf-winuser-registerclassa), la fenêtre reçoit uniquement des messages Unicode. Pour déterminer si une fenêtre utilise ou non le jeu de caractères Unicode, appelez [**IsWindowUnicode**](/windows/win32/api/winuser/nf-winuser-iswindowunicode).

### <a name="window-creation-messages"></a>Messages Window-Creation

Lors de la création d’une fenêtre, le système envoie des messages à la procédure de fenêtre pour la fenêtre. Le système envoie le message [**WM \_ NCCREATE**](wm-nccreate.md) après la création de la zone non cliente de la fenêtre et le message [**WM \_ Create**](wm-create.md) après la création de la zone cliente. La procédure de fenêtre reçoit les deux messages avant que le système n’affiche la fenêtre. Les deux messages incluent un pointeur vers une structure [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) qui contient toutes les informations spécifiées dans la fonction [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) . En règle générale, la procédure de fenêtre effectue des tâches d’initialisation lors de la réception de ces messages.

Lors de la création d’une fenêtre enfant, le système envoie le message [**WM \_ PARENTNOTIFY**](/previous-versions/windows/desktop/inputmsg/wm-parentnotify) à la fenêtre parente après l’envoi des messages [**WM \_ NCCREATE**](wm-nccreate.md) et [**WM \_ Create**](wm-create.md) . Il envoie également d’autres messages lors de la création d’une fenêtre. Le nombre et l’ordre de ces messages dépendent de la classe et du style de la fenêtre et de la fonction utilisée pour créer la fenêtre. Ces messages sont décrits dans d’autres rubriques de ce fichier d’aide.

### <a name="multithread-applications"></a>Applications multithread

Une application Windows peut avoir plusieurs threads d’exécution, et chaque thread peut créer des fenêtres. Le thread qui crée une fenêtre doit contenir le code de la procédure de fenêtre.

Une application peut utiliser la fonction [**EnumThreadWindows**](/windows/win32/api/winuser/nf-winuser-enumthreadwindows) pour énumérer les fenêtres créées par un thread particulier. Cette fonction passe le handle à chaque fenêtre de thread, à son tour, à une fonction de rappel définie par l’application, [**EnumThreadWndProc**](/previous-versions/windows/desktop/legacy/ms633496(v=vs.85)).

La fonction [**GetWindowThreadProcessId**](/windows/win32/api/winuser/nf-winuser-getwindowthreadprocessid) retourne l’identificateur du thread qui a créé une fenêtre particulière.

Pour définir l’état d’affichage d’une fenêtre créée par un autre thread, utilisez la fonction [**ShowWindowAsync**](/windows/win32/api/winuser/nf-winuser-showwindowasync) .

 

 
