---
description: Chaque document d’une application d’interface multidocument (MDI) est affiché dans une fenêtre enfant distincte dans la zone cliente de la fenêtre principale de l’application.
ms.assetid: 35dff281-3b11-4954-85cf-a0f1c9ed346a
title: À propos de l’interface multidocument
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0397127d7ec343ebdb7696c2dd7d57204a5d5ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529466"
---
# <a name="about-the-multiple-document-interface"></a>À propos de l’interface multidocument

Chaque document d’une application d’interface multidocument (MDI) est affiché dans une fenêtre enfant distincte dans la zone cliente de la fenêtre principale de l’application. Les applications MDI classiques incluent des applications de traitement de texte qui permettent à l’utilisateur de travailler avec plusieurs documents texte et des applications de tableur qui permettent à l’utilisateur de travailler avec plusieurs graphiques et feuilles de calcul. Pour plus d'informations, consultez les rubriques ci-dessous.

-   [Fenêtres Frame, client et enfant](#frame-client-and-child-windows)
-   [Création de fenêtre enfant](#child-window-creation)
-   [Activation de la fenêtre enfant](#child-window-activation)
-   [Menus à plusieurs documents](#multiple-document-menus)
-   [Accélérateurs de documents multiples](#multiple-document-accelerators)
-   [Taille et disposition de la fenêtre enfant](#child-window-size-and-arrangement)
-   [Fenêtres titre des icônes](#icon-title-windows)
-   [Données de fenêtre enfant](#child-window-data)
    -   [Structure de la fenêtre](#window-structure)
    -   [Propriétés de la fenêtre](#window-properties)

## <a name="frame-client-and-child-windows"></a>Fenêtres Frame, client et enfant

Une application MDI comporte trois types de fenêtres : une fenêtre frame, une fenêtre cliente MDI, ainsi qu’un certain nombre de fenêtres enfants. La *fenêtre frame* est semblable à la fenêtre principale de l’application : elle a une bordure de redimensionnement, une barre de titre, un menu fenêtre, un bouton réduire et un bouton Agrandir. L’application doit inscrire une classe de fenêtre pour la fenêtre frame et fournir une procédure de fenêtre pour la prendre en charge.

Une application MDI n’affiche pas la sortie dans la zone cliente de la fenêtre frame. Au lieu de cela, il affiche la fenêtre cliente MDI. Une *fenêtre cliente MDI* est un type spécial de fenêtre enfant appartenant à la classe de fenêtre préinscrite **MdiClient**. La fenêtre cliente est un enfant de la fenêtre frame ; Il sert d’arrière-plan pour les fenêtres enfants. Il prend également en charge la création et la manipulation de fenêtres enfants. Par exemple, une application MDI peut créer, activer ou agrandir des fenêtres enfants en envoyant des messages à la fenêtre cliente MDI.

Lorsque l’utilisateur ouvre ou crée un document, la fenêtre cliente crée une fenêtre enfant pour le document. La fenêtre cliente est la fenêtre parente de toutes les fenêtres enfants MDI de l’application. Chaque fenêtre enfant a une bordure de redimensionnement, une barre de titre, un menu fenêtre, un bouton réduire et un bouton Agrandir. Comme une fenêtre enfant est découpée, elle est limitée à la fenêtre du client et ne peut pas apparaître en dehors de celle-ci.

Une application MDI peut prendre en charge plusieurs types de document. Par exemple, une application de feuille de calcul standard permet à l’utilisateur de travailler avec des graphiques et des feuilles de calcul. Pour chaque type de document qu’il prend en charge, une application MDI doit inscrire une classe de fenêtre enfant et fournir une procédure de fenêtre pour prendre en charge les fenêtres appartenant à cette classe. Pour plus d’informations sur les classes de fenêtre, consultez [classes de fenêtre](window-classes.md). Pour plus d’informations sur les procédures de fenêtre, consultez [procédures de fenêtre](window-procedures.md).

Voici une application MDI classique. Il s’intitule MULTIPAD.

![fenêtre frame d’application MDI MULTIPAD et fenêtre cliente](images/csmdi-01.png)

## <a name="child-window-creation"></a>Création de fenêtre enfant

Pour créer une fenêtre enfant, une application MDI appelle la fonction [**CreateMDIWindow**](/windows/win32/api/winuser/nf-winuser-createmdiwindowa) ou envoie le message [**WM \_ MDICREATE**](wm-mdicreate.md) à la fenêtre cliente MDI. Une façon plus efficace de créer une fenêtre enfant MDI consiste à appeler la fonction [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) , en spécifiant le style étendu **WS \_ ex \_ MDICHILD** .

Pour détruire une fenêtre enfant, une application MDI envoie un message [**WM \_ MDIDESTROY**](wm-mdidestroy.md) à la fenêtre cliente MDI.

## <a name="child-window-activation"></a>Activation de la fenêtre enfant

Un nombre quelconque de fenêtres enfants peuvent s’afficher dans la fenêtre du client à un moment donné, mais un seul peut être actif. La fenêtre enfant active est positionnée devant toutes les autres fenêtres enfants et sa bordure est mise en surbrillance.

L’utilisateur peut activer une fenêtre enfant inactive en cliquant dessus. Une application MDI active une fenêtre enfant en envoyant un message [**WM \_ MDIACTIVATE**](wm-mdiactivate.md) à la fenêtre cliente MDI. Lorsque la fenêtre cliente traite ce message, elle envoie un message **WM \_ MDIACTIVATE** à la procédure de fenêtre de la fenêtre enfant à activer et à la procédure de fenêtre de la fenêtre enfant qui est désactivée.

Pour empêcher l’activation d’une fenêtre enfant, gérez le message [**WM \_ NCACTIVATE**](wm-ncactivate.md) dans la fenêtre enfant en retournant **false**.

Le système effectue le suivi de la position de chaque fenêtre enfant dans la pile des fenêtres superposées. Cette pile est connue sous le nom d' [ordre de plan](window-features.md). L’utilisateur peut activer la fenêtre enfant suivante dans l’ordre de plan en cliquant sur **suivant** dans le menu fenêtre de la fenêtre active. Une application active la fenêtre enfant suivante (ou précédente) dans l’ordre de plan en envoyant un message [**WM \_ MDINEXT**](wm-mdinext.md) à la fenêtre du client.

Pour récupérer le handle de la fenêtre enfant active, l’application MDI envoie un message [**WM \_ MDIGETACTIVE**](wm-mdigetactive.md) à la fenêtre du client.

## <a name="multiple-document-menus"></a>Menus à plusieurs documents

La fenêtre frame d’une application MDI doit inclure une barre de menus avec un menu fenêtre. Le menu fenêtre doit inclure des éléments qui réorganisent les fenêtres enfants dans la fenêtre cliente ou qui ferment toutes les fenêtres enfants. Le menu fenêtre d’une application MDI classique peut inclure les éléments du tableau suivant.



| Élément de menu         | Objectif                                                                                                                  |
|-------------------|--------------------------------------------------------------------------------------------------------------------------|
| **Vignette**          | Réorganise les fenêtres enfants dans un format de vignette afin que chacune apparaisse dans son intégralité dans la fenêtre du client.                       |
| **Répercuté**       | Réorganise les fenêtres enfants dans un format en cascade. Les fenêtres enfants se chevauchent les unes des autres, mais la barre de titre de chaque est visible. |
| **Réorganiser les icônes** | Réorganise les icônes des fenêtres enfants réduites en bas de la fenêtre du client.                                     |
| **Fermer tout**     | Ferme toutes les fenêtres enfants.                                                                                                |



 

Chaque fois qu’une fenêtre enfant est créée, le système ajoute automatiquement un nouvel élément de menu au menu fenêtre. Le texte de l’élément de menu est le même que le texte de la barre de menus de la nouvelle fenêtre enfant. En cliquant sur l’élément de menu, l’utilisateur peut activer la fenêtre enfant correspondante. Quand une fenêtre enfant est détruite, le système supprime automatiquement l’élément de menu correspondant dans le menu fenêtre.

Le système peut ajouter jusqu’à dix éléments de menu au menu fenêtre. Lorsque la dixième fenêtre enfant est créée, le système ajoute le **plus grand élément Windows** au menu fenêtre. Cliquez sur cet élément pour afficher la boîte de dialogue **Sélectionner une fenêtre** . La boîte de dialogue contient une zone de liste avec les titres de toutes les fenêtres MDI enfants actuellement disponibles. L’utilisateur peut activer une fenêtre enfant en cliquant sur son titre dans la zone de liste.

Si votre application MDI prend en charge plusieurs types de fenêtres enfants, personnalisez la barre de menus pour qu’elle reflète les opérations associées à la fenêtre active. Pour ce faire, fournissez des ressources de menu distinctes pour chaque type de fenêtre enfant que l’application prend en charge. Lorsqu’un nouveau type de fenêtre enfant est activé, l’application doit envoyer un message [**WM \_ MDISETMENU**](wm-mdisetmenu.md) à la fenêtre cliente, en lui transmettant le handle vers le menu correspondant.

Lorsqu’il n’existe aucune fenêtre enfant, la barre de menus ne doit contenir que les éléments utilisés pour créer ou ouvrir un document.

Lorsque l’utilisateur navigue dans les menus d’une application MDI à l’aide de clés de curseur, les clés se comportent différemment de l’utilisateur qui navigue dans les menus d’une application classique. Dans une application MDI, le contrôle passe du menu fenêtre de l’application au menu fenêtre de la fenêtre enfant active, puis au premier élément de la barre de menus.

## <a name="multiple-document-accelerators"></a>Accélérateurs de documents multiples

Pour recevoir et traiter des touches accélérateur pour ses fenêtres enfants, une application MDI doit inclure la fonction [**TranslateMDISysAccel**](/windows/win32/api/winuser/nf-winuser-translatemdisysaccel) dans sa boucle de message. La boucle doit appeler **TranslateMDISysAccel** avant d’appeler la fonction [**TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) ou [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) .

Les touches d’accès rapide dans le menu fenêtre pour une fenêtre enfant MDI sont différentes de celles d’une fenêtre enfant non MDI. Dans une fenêtre enfant MDI, la combinaison de touches ALT + – (moins) ouvre le menu fenêtre, la combinaison de touches CTRL + F4 ferme la fenêtre enfant active et la combinaison de touches CTRL + F6 active la fenêtre enfant suivante.

## <a name="child-window-size-and-arrangement"></a>Taille et disposition de la fenêtre enfant

Une application MDI contrôle la taille et la position de ses fenêtres enfants en envoyant des messages à la fenêtre cliente MDI. Pour maximiser la fenêtre enfant active, l’application envoie le message [**WM \_ MDIMAXIMIZE**](wm-mdimaximize.md) à la fenêtre du client. Quand une fenêtre enfant est agrandie, sa zone client remplit complètement la fenêtre du client MDI. En outre, le système masque automatiquement la barre de titre de la fenêtre enfant et ajoute l’icône de menu fenêtre et le bouton restaurer de la fenêtre enfant à la barre de menus de l’application MDI. L’application peut restaurer la fenêtre cliente à sa taille et à sa position d’origine (préagrandie) en envoyant la fenêtre cliente un message [**WM \_ MDIRESTORE**](wm-mdirestore.md) .

Une application MDI peut réorganiser ses fenêtres enfants dans un format en cascade ou en mosaïque. Lorsque les fenêtres enfants sont mises en cascade, les fenêtres s’affichent dans une pile. La fenêtre située en bas de la pile occupe le coin supérieur gauche de l’écran, tandis que les fenêtres restantes sont décalées verticalement et horizontalement, de sorte que la bordure gauche et la barre de titre de chaque fenêtre enfant sont visibles. Pour réorganiser les fenêtres enfants dans le format cascade, une application MDI envoie le message [**WM \_ MDICASCADE**](wm-mdicascade.md) . En règle générale, l’application envoie ce message lorsque l’utilisateur clique sur **cascade** dans le menu fenêtre.

Lorsque les fenêtres enfants sont affichées en mosaïque, le système affiche chaque fenêtre enfant dans son intégralité, en se chevauchant à aucune des fenêtres. Toutes les fenêtres sont dimensionnées, si nécessaire, pour tenir dans la fenêtre du client. Pour réorganiser les fenêtres enfants dans le format de la vignette, une application MDI envoie un message [**WM \_ MDITILE**](wm-mditile.md) à la fenêtre du client. En règle générale, l’application envoie ce message lorsque l’utilisateur clique sur la **vignette** dans le menu fenêtre.

Une application MDI doit fournir une icône différente pour chaque type de fenêtre enfant qu’elle prend en charge. L’application spécifie une icône lors de l’inscription de la classe de fenêtre enfant. Le système affiche automatiquement l’icône d’une fenêtre enfant dans la partie inférieure de la fenêtre cliente lorsque la fenêtre enfant est réduite. Une application MDI indique au système d’organiser les icônes des fenêtres enfants en envoyant un message [**WM \_ MDIICONARRANGE**](wm-mdiiconarrange.md) à la fenêtre du client. En règle générale, l’application envoie ce message lorsque l’utilisateur clique sur **Réorganiser les icônes** dans le menu fenêtre.

## <a name="icon-title-windows"></a>Fenêtres titre des icônes

Étant donné que les fenêtres enfants MDI peuvent être réduites, une application MDI doit éviter la manipulation des fenêtres de titre d’icône comme s’il s’agissait de fenêtres enfants MDI normales. Les fenêtres de titre d’icône s’affichent lorsque l’application énumère les fenêtres enfants de la fenêtre cliente MDI. Les fenêtres de titre d’icône diffèrent des autres fenêtres enfants, en ce qu’elles appartiennent à une fenêtre enfant MDI.

Pour déterminer si une fenêtre enfant est une fenêtre de titre d’icône, utilisez la fonction [**GetWindow**](/windows/win32/api/winuser/nf-winuser-getwindow) avec l' \_ index de propriétaire GW. Les fenêtres qui ne sont pas des titres retournent la **valeur null**. Notez que ce test est insuffisant pour les fenêtres de niveau supérieur, car les menus et les boîtes de dialogue sont des fenêtres détenues.

## <a name="child-window-data"></a>Données de fenêtre enfant

Étant donné que le nombre de fenêtres enfants varie selon le nombre de documents que l’utilisateur ouvre, une application MDI doit être en mesure d’associer des données (par exemple, le nom du fichier actuel) à chaque fenêtre enfant. Il existe deux façons d'effectuer cette opération :

-   Stocke les données de fenêtre enfant dans la structure de la fenêtre.
-   Utilisez les propriétés de la fenêtre.

### <a name="window-structure"></a>Structure de la fenêtre

Quand une application MDI inscrit une classe de fenêtre, elle peut réserver de l’espace supplémentaire dans la structure de la fenêtre pour les données d’application spécifiques à cette classe de Windows particulière. Pour stocker et récupérer des données dans cet espace supplémentaire, l’application utilise les fonctions [**GetWindowLong**](/windows/win32/api/winuser/nf-winuser-getwindowlonga) et [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) .

Pour conserver une grande quantité de données pour une fenêtre enfant, une application peut allouer de la mémoire pour une structure de données, puis stocker le descripteur dans la mémoire qui contient la structure dans l’espace supplémentaire associé à la fenêtre enfant.

### <a name="window-properties"></a>Propriétés de la fenêtre

Une application MDI peut également stocker des données par document à l’aide des propriétés de la fenêtre. Les *données par document* sont des données spécifiques au type de document contenu dans une fenêtre enfant particulière. Les propriétés sont différentes de l’espace supplémentaire dans la structure de la fenêtre, car vous n’avez pas besoin d’allouer de l’espace supplémentaire lors de l’inscription de la classe de fenêtre. Une fenêtre peut avoir un nombre quelconque de propriétés. En outre, lorsque des décalages sont utilisés pour accéder à l’espace supplémentaire dans les structures de fenêtre, les propriétés sont référencées par des noms de chaînes. Pour plus d’informations sur les propriétés des fenêtres, consultez Propriétés de la [fenêtre](window-properties.md).

 

 
