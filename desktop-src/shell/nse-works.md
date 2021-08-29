---
description: Windows L’Explorateur fournit une représentation graphique de l’espace de noms Shell associée à des outils qui permettent aux utilisateurs d’interagir avec les objets Shell.
ms.assetid: cc387338-15fa-4350-b039-61a0f1c5030a
title: Fonctionnement des extensions d’espace de noms Shell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d972239320c633a12d4d162ec1593b82b9b02fb9d15a1a0bc9ee908abc8ac64d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119820949"
---
# <a name="understanding-shell-namespace-extensions"></a>Fonctionnement des extensions d’espace de noms Shell

Windows L’Explorateur fournit une représentation graphique de l’espace de noms Shell associée à des outils qui permettent aux utilisateurs d’interagir avec les objets Shell. avec une extension d’espace de noms, vous pouvez prendre n’importe quel corps de données et faire en sorte que l’explorateur de Windows le présente à l’utilisateur comme un dossier virtuel. Quand un utilisateur accède à ce dossier, vos données sont présentées sous la forme d’une hiérarchie structurée en arborescence de dossiers et de fichiers, à l’instar du reste de l’espace de noms Shell. Les utilisateurs et les applications peuvent interagir avec le contenu de ce dossier virtuel à peu près de la même façon qu’avec tout autre objet d’espace de noms. Ce document explique comment créer une extension d’espace de noms.

-   [Fonctionnement d’une extension d’espace de noms](#how-a-namespace-extension-works)
-   [Objet de vue de dossier système par défaut (DefView)](#the-default-system-folder-view-object-defview)
-   [comment Windows Explorer interagit avec une Extension d’espace de noms](#how-windows-explorer-interacts-with-a-namespace-extension)
    -   [Arborescence](#tree-view)
    -   [Affichage des dossiers](#folder-view)
    -   [Barre de menus et barres d’outils](#menu-bar-and-toolbars)
    -   [Barre d’état](#status-bar)

## <a name="how-a-namespace-extension-works"></a>Fonctionnement d’une extension d’espace de noms

en arrière-plan, chaque dossier affiché par Windows Explorer est représenté par un objet COM (component object Model) appelé *objet dossier*. Chaque fois que l’utilisateur interagit avec un dossier ou son contenu, l’interpréteur de commandes communique avec l’objet dossier associé via l’une des nombreuses interfaces standard. l’objet folder fait ensuite ce qui est nécessaire pour répondre à l’action de l’utilisateur, et l’interpréteur de commandes met à jour l’affichage de l’explorateur de Windows.

La majorité des fichiers et dossiers avec lesquels les utilisateurs interagissent font partie du système de fichiers ou d’un dossier virtuel système tel que la corbeille. D’autres documents ont abordé la manière dont vous pouvez personnaliser le comportement de ces dossiers standard pour répondre aux exigences de votre application en modifiant le registre ou en implémentant des [gestionnaires d’extensions de Shell](handlers.md). Toutefois, l’extension de l’interpréteur de commandes est particulièrement utile lorsque vos informations peuvent être facilement empaquetées sous la forme de fichiers ou de dossiers du système de fichiers normal.

Il existe plusieurs situations où le stockage de données sous la forme d’une collection de dossiers et de fichiers de système de fichiers peut être indésirable, voire impossible. Voici quelques exemples de ce type de données :

-   Collection d’éléments qui est le plus efficacement empaqueté dans un fichier unique, tel qu’une base de données.
-   collection d’éléments stockés sur un ordinateur distant qui ne dispose pas d’un système de fichiers Windows standard. Les informations stockées sur un assistant numérique personnel (PDA) ou un appareil photo numérique sont un exemple de ces données.
-   Collection d’éléments qui ne représente pas de données stockées. Les liens d’imprimante contenus dans le dossier Imprimantes standard sont un exemple de ces données.

Une façon de présenter ce type de données à un utilisateur consiste à écrire une application pour permettre aux utilisateurs d’afficher et d’interagir avec les différents éléments. toutefois, si vos données peuvent être présentées sous la forme d’une hiérarchie de dossiers/fichiers, la plupart des fonctionnalités que vous devrez implémenter peuvent être des services d’interface utilisateur qui sont déjà fournis par Windows Explorer. une approche bien plus efficace consisterait à écrire une extension d’espace de noms et à laisser Windows Explorer devenir votre interface utilisateur graphique.

Pour implémenter une extension d’espace de noms, vos informations doivent être organisées sous la forme d’un espace de noms structuré en arborescence. La *racine* de l’espace de noms est présentée sous la forme d’un dossier virtuel dans l’espace de noms Shell. le dossier racine, ainsi que tous ses sous-dossiers et éléments de données, deviennent partie intégrante de l’espace de noms Shell et Windows Explorer devient votre interface utilisateur. Vous pouvez ainsi présenter vos informations à l’utilisateur de manière familière et facilement accessible avec une programmation d’interface utilisateur bien moins importante que celle requise pour une application personnalisée.

Une extension d’espace de noms se compose de deux composants de base :

-   Un gestionnaire de données
-   interface entre le gestionnaire de données et l’explorateur de Windows

Le premier composant de la liste dépend entièrement de vous. Vous pouvez stocker et gérer vos données de la manière la plus efficace. le deuxième composant est le code nécessaire pour empaqueter vos données sous forme d’objets de dossier et gérer l’interaction avec Windows Explorer. Windows L’Explorateur peut ensuite appeler ces objets pour permettre aux utilisateurs d’afficher et d’interagir avec vos données comme s’il s’agissait d’une collection de dossiers et de fichiers. les objets de dossier de votre extension d’espace de noms doivent interagir avec Windows Explorer comme s’il s’agissait de dossiers normaux. avant de tenter d’implémenter une extension d’espace de noms, vous devez d’abord comprendre comment Windows Explorer gère un objet dossier.

## <a name="the-default-system-folder-view-object-defview"></a>Objet de vue de dossier système par défaut (DefView)

L’interpréteur de commandes fournit une implémentation par défaut de l’affichage des dossiers, connu sous le nom de DefView, ce qui vous permet d’éviter une grande partie du travail d’implémentation de votre propre extension d’espace de noms. Étant donné que certaines fonctionnalités de vue ne peuvent pas être obtenues par le biais de vues personnalisées, il est souvent recommandé d’utiliser l’objet de vue de dossier système par défaut à la place d’une vue personnalisée. Pour plus d’informations, consultez [**SHCreateShellFolderView**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderview).

## <a name="how-windows-explorer-interacts-with-a-namespace-extension"></a>comment Windows Explorer interagit avec une Extension d’espace de noms

Windows L’Explorateur fournit aux utilisateurs une interface utilisateur graphique qui leur permet d’effectuer diverses tâches, notamment :

-   [Navigation dans](navigate.md) la hiérarchie de l’espace de noms et affichage du contenu des dossiers.
-   [Gestion](manage.md) du contenu de l’espace de noms en déplaçant, en supprimant et en copiant des objets.
-   [Récupération](folder-info.md) d’une variété d’informations sur les objets.
-   [Lancement](launch.md) d’applications.

l’interface utilisateur graphique de Windows Explorer a cinq composants de base. l’illustration suivante nomme les composants et indique où ils s’affichent généralement dans Windows Explorer.

![Illustration montrant les composants de l’interface utilisateur de l’Explorateur Windows ](images/nse1.png)

lorsqu’un utilisateur affiche un dossier qui appartient à une extension d’espace de noms dans Windows Explorer, l’objet folder a au moins le contrôle partiel sur le contenu des cinq zones.

### <a name="tree-view"></a>Arborescence

L’arborescence fournit une vue d’ensemble de l’espace de noms. Cette zone héberge un [contrôle arborescence](../controls/tree-view-controls.md) qui peut afficher chaque dossier d’espace de noms et la position du dossier dans la hiérarchie d’espace de noms. Un utilisateur peut effectuer plusieurs opérations avec la zone d’arborescence, notamment :

-   Affichage ou masquage du niveau suivant dans l’espace de noms.
-   Copier, déplacer ou supprimer des dossiers.
-   Cliquez avec le bouton droit sur un dossier pour afficher un menu contextuel.
-   Sélection d’un dossier et affichage de son contenu dans l’affichage des dossiers.

L’arborescence communique avec les objets de dossier principalement par le biais de leur interface [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) . par exemple, lorsqu’un utilisateur clique sur le signe plus (+) en regard de l’icône du dossier, Windows Explorer développe l’affichage pour afficher les sous-dossiers du dossier. Pour obtenir les informations nécessaires à la mise à jour de l’arborescence, le shell effectue plusieurs appels à l’interface **IShellFolder** de l’objet dossier :

-   Demandez les attributs du dossier.
-   Énumérer le contenu du dossier.
-   Demandez les noms d’affichage de chaque sous-dossier.
-   Demandez une icône à afficher en regard de chaque dossier.

Windows L’Explorateur met ensuite à jour l’arborescence pour afficher les sous-dossiers du dossier sélectionné. Si les sous-dossiers comportent des sous-dossiers, un caractère « + » s’affiche à côté de leur icône de dossier. Il existe un certain nombre de tâches plus sophistiquées qu’un utilisateur peut également effectuer avec l’arborescence, notamment :

-   À l’aide du presse-papiers, coupez ou copiez un dossier, puis collez-le dans un autre dossier.
-   À l’aide de la fonction glisser-déplacer pour couper ou copier un dossier et le déposer dans un autre dossier.
-   Utilisation d’un moteur de recherche pour rechercher des éléments dans un dossier ou dans ses sous-dossiers.
-   Modification des propriétés du dossier.

Pour plus d’informations sur la façon dont une extension d’espace de noms gère ces actions utilisateur, consultez [implémentation des interfaces d’objet de dossier de base](nse-implement.md).

### <a name="folder-view"></a>Affichage des dossiers

Lorsqu’un utilisateur sélectionne un dossier, le contenu du dossier s’affiche dans l’affichage des dossiers. Dans une certaine mesure, les fonctionnalités normales de l’affichage des dossiers chevauchent l’arborescence. Les utilisateurs peuvent déplacer ou copier des dossiers, modifier les propriétés des dossiers, afficher le contenu d’un sous-dossier, afficher un menu contextuel pour un dossier, et ainsi de suite. Toutefois, il existe des différences distinctes entre l’arborescence et l’affichage des dossiers :

-   L’affichage des dossiers affiche uniquement le contenu d’un dossier unique, et non une partie ou la totalité de la hiérarchie d’espaces de noms.
-   L’affichage des dossiers affiche les objets de fichier ainsi que les objets de dossier.
-   L’affichage des dossiers peut afficher plus d’informations sur les objets que l’arborescence.
-   L’affichage des dossiers permet aux extensions d’espace de noms d’avoir un contrôle presque entièrement sur les informations qui s’affichent et sur la manière dont. Seuls les aspects mineurs de l’arborescence, tels que les icônes de dossiers, peuvent être modifiés.

contrairement à l’arborescence, Windows Explorer ne contrôle pas directement le contenu de l’affichage des dossiers. l’affichage des dossiers est une zone que Windows Explorer fournit aux objets de dossier. L’affichage et la gestion du contenu d’un dossier dans l’affichage des dossiers sont la responsabilité de l’objet dossier. Bien que la plupart des affichages de dossiers suivent un format relativement standard, il existe en fait quelques limitations sur ce qui peut être affiché ou comment. Un cas extrême est le dossier Internet, qui est un navigateur complet.

quand un utilisateur sélectionne un dossier qui appartient à votre extension d’espace de noms, vous créez une fenêtre et transmettez son handle à Windows Explorer. Cette fenêtre devient un enfant de la fenêtre d’affichage des dossiers. Windows L’Explorateur fournit les dimensions de la fenêtre d’affichage des dossiers, mais n’impose aucune restriction sur le contenu de votre fenêtre enfant. Vous pouvez ensuite utiliser la fenêtre enfant pour afficher l’affichage des dossiers du dossier.

Les extensions d’espace de noms utilisent l’une des deux approches suivantes pour créer un affichage des dossiers :

-   Utilisez votre fenêtre enfant pour héberger un contrôle [List View](../controls/list-view-control-reference.md) . ce contrôle vous permet d’afficher le contenu d’un dossier à peu près de la même façon que l' [affichage classique](../lwef/web-view.md)de Windows Explorer.
-   Utilisez votre fenêtre enfant pour héberger un [contrôle WebBrowser](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752044(v=vs.85)) et utilisez un document DHTML (Dynamic HTML) pour afficher le contenu du dossier.

Les deux approches affichent une vue de dossier qui ressemble beaucoup à celle affichée pour les dossiers système. Toutefois, si vous souhaitez utiliser un autre modèle d’affichage, vous êtes libre de le faire.

### <a name="menu-bar-and-toolbars"></a>Barre de menus et barres d’outils

comme la plupart des applications Windows, Windows Explorer fournit à l’utilisateur un ensemble d’outils. Une sélection complète d’outils est disponible via la barre de menus. Les outils les plus couramment utilisés sont également représentés par des boutons ou des zones d’édition dans une barre d’outils. contrairement à de nombreuses applications Windows, la barre de menus de Windows Explorer est en fait un [contrôle de barre d’outils](../controls/toolbar-control-reference.md) qui a été personnalisé pour se comporter comme un menu conventionnel. La barre de menus et la barre d’outils sont incorporées dans un [contrôle rebar](../controls/rebar-control-reference.md) pour permettre aux utilisateurs d’organiser les contrôles en fonction de leurs besoins.

par défaut, Windows Explorer prend en charge un ensemble standard de boutons et d’éléments de menu, tels que copier et propriétés. Votre extension d’espace de noms peut personnaliser la barre de menus et les barres d’outils en supprimant les outils standard et en ajoutant des outils personnalisés. lorsque votre objet de vue de dossier est initialisé, Windows Explorer passe un pointeur vers son interface [**IShellBrowser**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellbrowser) . Cette interface prend en charge plusieurs méthodes que vous pouvez appeler pour personnaliser la barre de menus et la barre d’outils. lorsque l’utilisateur sélectionne l’un de vos éléments de menu ou boutons de barre d’outils personnalisés, Windows Explorer transfère les \_ messages de commande WM pour les éléments de menu et de barre d’outils personnalisés à la procédure de fenêtre de votre fenêtre enfant.

### <a name="status-bar"></a>Barre d’état

la barre d’état de Windows Explorer affiche des informations sur l’objet actuellement sélectionné. Votre extension d’espace de noms peut utiliser la barre d’État pour afficher des informations d’État, telles qu’une chaîne de texte. Vous pouvez personnaliser la barre d’État en appelant [**IShellBrowser**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellbrowser).

 

 
