---
title: À propos des zones de liste modifiable
description: Cette section décrit les différents types de zones de liste déroulante.
ms.assetid: 76410a87-aa0e-4da9-9e78-c80ac485e3cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 497bc6fc7e9254feb58ef95051ba1278e135ff241d3af93781f611373d2d096c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119922510"
---
# <a name="about-combo-boxes"></a>À propos des zones de liste modifiable

Une zone de liste déroulante combine une zone d’édition ou du texte statique et une liste.

Cette rubrique contient les sections suivantes.

-   [Types et styles de zone de liste déroulante](#combo-box-types-and-styles)
-   [Liste de zones de liste modifiable](#combo-box-list)
    -   [Sélection actuelle](#current-selection)
    -   [Listes déroulantes](#drop-down-lists)
    -   [Lister le contenu](#list-contents)
-   [Modifier les champs de sélection du contrôle](#edit-control-selection-fields)
-   [Zones de liste déroulante owner-drawn](#owner-drawn-combo-boxes)
-   [Zones de liste déroulante sous-classées](#subclassed-combo-boxes)

## <a name="combo-box-types-and-styles"></a>Types et styles de zone de liste déroulante

Une zone de liste déroulante se compose d’une liste et d’un champ de sélection. La liste présente les options qu’un utilisateur peut sélectionner et le champ de sélection affiche la sélection actuelle. Si le champ de sélection est un contrôle d’édition, l’utilisateur peut entrer des informations non disponibles dans la liste ; dans le cas contraire, l’utilisateur ne peut sélectionner que les éléments de la liste.

La bibliothèque de contrôles communs comprend trois styles principaux de zone de liste déroulante, comme indiqué dans le tableau suivant.



| Type de zone de liste déroulante             | Style, constante                                                 | Description                                                                                  |
|----------------------------|----------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| Simple                     | [**CBS \_ simple**](combo-box-styles.md)             | Affiche la liste à tout moment et affiche l’élément sélectionné dans un contrôle d’édition.              |
| Drop-down                  | [**\_liste déroulante CBS**](combo-box-styles.md)         | Affiche la liste lorsque l’utilisateur clique sur l’icône et affiche l’élément sélectionné dans un contrôle d’édition.  |
| Liste déroulante (liste déroulante) | [**\_DropDownList SCC**](combo-box-styles.md) | Affiche la liste lorsque l’utilisateur clique sur l’icône et affiche l’élément sélectionné dans un contrôle statique. |



 

les captures d’écran suivantes montrent chacune les trois sortes de zone de liste déroulante telles qu’elles peuvent apparaître dans Windows Vista. Dans la première capture d’écran, l’utilisateur a sélectionné un élément dans la zone de liste déroulante simple. L’utilisateur peut également taper une nouvelle valeur dans la zone d’édition de ce contrôle. la liste a été dimensionnée dans l’éditeur de ressources Microsoft Visual Studio et n’est suffisante que pour accueillir deux éléments.

![capture d’écran montrant un élément sélectionné dans une zone de liste modifiable simple](images/simplecombo.png)

Dans la deuxième capture d’écran, l’utilisateur a tapé un nouveau texte dans le contrôle d’édition de la zone de liste déroulante. L’utilisateur peut également avoir sélectionné un élément existant. La zone de liste se développe pour accueillir autant d’éléments que possible.

![capture d’écran montrant le texte tapé dans une zone de liste déroulante](images/dropdown.png)

Dans la troisième capture d’écran, l’utilisateur a ouvert la zone de liste déroulante de liste déroulante. La zone de liste se développe pour accueillir autant d’éléments que possible. L’utilisateur ne peut pas entrer de nouveau texte.

![capture d’écran montrant un élément sélectionné dans une zone de liste déroulante de liste déroulante](images/droplist.png)

Il existe également un certain nombre de styles de zone de liste déroulante qui définissent des propriétés spécifiques. Les styles de zone de liste modifiable définissent des propriétés spécifiques d’une zone de liste modifiable. Vous pouvez combiner des styles. Toutefois, certains styles s’appliquent uniquement à certains types de zone de liste déroulante. Pour obtenir un tableau des styles de zone de liste déroulante, consultez [styles de zone de liste déroulante](combo-box-styles.md).

> [!Note]  
> Pour utiliser des styles visuels avec des zones de liste déroulante, une application doit inclure un manifeste et doit appeler [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) au début du programme. Pour plus d’informations sur les styles visuels, consultez [styles visuels](themes-overview.md). Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).

 

## <a name="combo-box-list"></a>Liste de zones de liste modifiable

La liste est la partie d’une zone de liste déroulante qui affiche les éléments qu’un utilisateur peut sélectionner. En règle générale, une application initialise le contenu de la liste lorsqu’elle crée une zone de liste déroulante. Tout élément de liste sélectionné par l’utilisateur est la *sélection actuelle*. Impossible de sélectionner plusieurs éléments. Dans les zones de liste modifiable simples et déroulantes, l’utilisateur peut taper dans le champ de sélection au lieu de sélectionner un élément de liste. Dans ce cas, il n’y a aucune sélection actuelle, et il incombe à l’application d’ajouter l’élément à la liste et de le faire passer à la sélection actuelle, s’il y a lieu.

Cette section aborde les sujets suivants :

-   [Sélection actuelle](#current-selection)
-   [Listes déroulantes](#drop-down-lists)
-   [Lister le contenu](#list-contents)

### <a name="current-selection"></a>Sélection actuelle

La sélection actuelle est un élément de liste que l’utilisateur a sélectionné ; le texte sélectionné s’affiche dans le champ de sélection de la zone de liste déroulante. Toutefois, dans le cas d’une zone de liste modifiable simple ou d’une zone de liste déroulante, la sélection actuelle n’est qu’une forme d’entrée utilisateur possible dans une zone de liste déroulante. L’utilisateur peut également taper du texte dans le champ de sélection.

La sélection actuelle est identifiée par l’index de base zéro de l’élément de liste sélectionné. Une application peut la définir et la récupérer à tout moment. La fenêtre parente ou la procédure de boîte de dialogue reçoit une notification lorsque l’utilisateur modifie la sélection actuelle pour une zone de liste déroulante. La fenêtre parente ou la boîte de dialogue n’est pas avertie lorsque l’application modifie la sélection.

Lorsqu’une zone de liste déroulante est créée, il n’y a aucune sélection actuelle. C’est également le cas pour une zone de liste modifiable simple ou déroulante, si l’utilisateur a modifié le contenu du champ de sélection. Pour définir la sélection actuelle, une application envoie le message [**CB \_ SETCURSEL**](cb-setcursel.md) à la zone de liste déroulante. Une application peut également utiliser le message [**CB \_ SELECTSTRING**](cb-selectstring.md) pour définir la sélection actuelle sur un élément de liste dont la chaîne commence par une chaîne spécifiée. Pour déterminer la sélection actuelle, une application envoie le message [**CB \_ GETCURSEL**](cb-getcursel.md) à la zone de liste déroulante. S’il n’y a aucune sélection actuelle, ce message retourne CB \_ Err.

Lorsque l’utilisateur modifie la sélection actuelle dans une zone de liste déroulante, la fenêtre parente ou la procédure de boîte de dialogue reçoit un message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) avec le code de notification [CBN \_ selChange](cbn-selchange.md) dans le mot de poids fort du paramètre *wParam* . Ce code de notification n’est pas envoyé lorsque la sélection actuelle est définie à l’aide du message [**CB \_ SETCURSEL**](cb-setcursel.md) .

Une zone de liste déroulante ou une zone de liste déroulante déroulante envoie le code de notification [CBN \_ gros plan](cbn-closeup.md) à la fenêtre parente ou à la procédure de boîte de dialogue lorsque la liste déroulante se ferme. Si l’utilisateur a modifié la sélection actuelle, la zone de liste déroulante envoie également le code de notification [CBN \_ selChange](cbn-selchange.md) lorsque la liste déroulante se ferme. Pour exécuter un processus spécifique chaque fois que l’utilisateur sélectionne un élément de liste, vous pouvez gérer le \_ Code de notification CBN selChange ou CBN \_ gros plan. En général, vous attendez le code de \_ notification CBN gros plan avant de traiter une modification dans la sélection actuelle. Cela peut être particulièrement important si une quantité importante de traitement est nécessaire.

Une application peut également traiter les codes de notification [CBN \_ SELENDOK](cbn-selendok.md) et [CBN \_ SELENDCANCEL](cbn-selendcancel.md) . Le système envoie CBN \_ SELENDOK lorsque l’utilisateur sélectionne un élément de liste, ou sélectionne un élément, puis ferme la liste. Cela indique que l’utilisateur a terminé et que la sélection doit être traitée. CBN \_ SELENDCANCEL est envoyé lorsque l’utilisateur sélectionne un élément, mais sélectionne un autre contrôle, appuie sur ÉCHAP pendant que la liste déroulante est ouverte ou ferme la boîte de dialogue. Cela indique que la sélection de l’utilisateur doit être ignorée. CBN \_ SELENDOK est envoyé avant chaque message [CBN \_ selChange](cbn-selchange.md) .

Dans une zone de liste modifiable simple, le système envoie le code de notification [CBN \_ DBLCLK](cbn-dblclk.md) lorsque l’utilisateur double-clique sur un élément de liste. Dans une zone de liste déroulante ou une liste déroulante, un seul clic masque la liste. il n’est donc pas possible de double-cliquer sur un élément.

### <a name="drop-down-lists"></a>Listes déroulantes

Certains messages et notifications s’appliquent uniquement aux zones de liste déroulante contenant des listes déroulantes. Quand une liste déroulante est ouverte ou fermée, la fenêtre parente d’une zone de liste déroulante reçoit une notification sous la forme d’un message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) . Si la liste est ouverte, le mot de poids fort de *wParam* est [CBN \_ DROPDOWN](cbn-dropdown.md). Si la liste est fermée, il s’agit de [CBN \_ gros plan](cbn-closeup.md).

Une application peut ouvrir la liste d’une zone de liste déroulante ou d’une zone de liste déroulante à l’aide du message [**CB \_ SHOWDROPDOWN**](cb-showdropdown.md) . Il peut déterminer si la liste est ouverte à l’aide du message [**CB \_ GETDROPPEDSTATE**](cb-getdroppedstate.md) et peut déterminer les coordonnées d’une liste déroulante à l’aide du message [**CB \_ GETDROPPEDCONTROLRECT**](cb-getdroppedcontrolrect.md) . Une application peut également augmenter la largeur d’une liste déroulante à l’aide du message [**CB \_ SETDROPPEDWIDTH**](cb-setdroppedwidth.md) .

### <a name="list-contents"></a>Lister le contenu

Lorsqu’une application crée une zone de liste déroulante, elle Initialise généralement la zone de liste déroulante en ajoutant un ou plusieurs éléments à la liste. Plus tard, une application peut ajouter ou supprimer des éléments de liste, réinitialiser la liste ou récupérer des informations d’élément à partir de celle-ci.

Une application ajoute des éléments de liste à une zone de liste déroulante en lui envoyant le message [**CB \_ ADDSTRING**](cb-addstring.md) . L’élément spécifié est ajouté à la fin de la liste ou, dans une zone de liste déroulante triée, dans sa position triée correcte en fonction de la chaîne de l’élément. Dans une zone de liste modifiable non triée, une application peut utiliser le message [**CB \_ INSERTSTRING**](cb-insertstring.md) pour insérer un élément à une position spécifique. Une fois ajouté, un élément de liste est identifié par sa position.

En utilisant le message [**CB \_ FindString**](cb-findstring.md) ou [**CB \_ FindExactString**](cb-findstringexact.md) , une application peut déterminer la position d’un élément de liste. **CB \_ FINDSTRING** recherche un élément dont la chaîne commence par la chaîne spécifiée. **CB \_ FINDEXACTSTRING** recherche un élément dont la chaîne correspond exactement à la chaîne. Aucun des messages n’est sensible à la casse.

Une application peut supprimer un élément de liste à l’aide du message [**CB \_ DELETESTRING**](cb-deletestring.md) . Si une application doit réinitialiser la liste de la zone de liste déroulante, elle peut tout d’abord effacer tout son contenu à l’aide du message [**CB \_ RESETCONTENT**](cb-resetcontent.md) . Lors de l’ajout de plusieurs éléments à la liste après l’affichage d’une zone de liste déroulante, une application peut effacer l’indicateur de redessin pour empêcher que la zone de liste modifiable ne soit redessinée après l’ajout de chaque élément. Pour plus d’informations sur le redessin, consultez la description du message [**WM \_ SETREDRAW**](/windows/desktop/gdi/wm-setredraw) .

Pour récupérer la chaîne associée à un élément de liste, une application peut utiliser le message [**CB \_ GETLBTEXT**](cb-getlbtext.md) . La chaîne de l’élément est copiée dans la mémoire tampon spécifiée par l’application. Pour vous assurer que la mémoire tampon est suffisamment grande pour recevoir la chaîne, l’application peut d’abord utiliser le message [**CB \_ GETLBTEXTLEN**](cb-getlbtextlen.md) pour déterminer la longueur de la chaîne. Pour obtenir le nombre d’éléments de liste dans une zone de liste déroulante, une application peut utiliser le message [**CB \_ GETCOUNT**](cb-getcount.md) .

## <a name="edit-control-selection-fields"></a>Modifier les champs de sélection du contrôle

Une application peut récupérer ou définir le contenu du champ de sélection et peut déterminer ou définir la sélection de modification. L’application peut également limiter la quantité de texte qu’un utilisateur peut taper dans le champ de sélection. Lorsque le contenu du champ de sélection change, le système envoie des messages de notification à la procédure de la fenêtre parente ou de la boîte de dialogue.

Pour récupérer le contenu du champ de sélection, une application peut envoyer le message [**WM \_ GETTEXT**](/windows/desktop/winmsg/wm-gettext) à la zone de liste déroulante. Pour définir le contenu du champ de sélection d’une zone de liste modifiable simple ou d’une zone de liste déroulante, une application peut envoyer le message [**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext) à la zone de liste déroulante.

La sélection de modification correspond à la plage de texte sélectionné, le cas échéant, dans le champ de sélection d’une zone de liste modifiable simple ou déroulante. Une application peut déterminer les positions des caractères de début et de fin de la sélection actuelle à l’aide du message [**CB \_ GETEDITSEL**](cb-geteditsel.md) . Il peut également sélectionner des caractères dans la sélection de modification à l’aide du message [**CB \_ SETEDITSEL**](cb-seteditsel.md) .

Initialement, la quantité de texte que l’utilisateur peut taper dans le champ de sélection est limitée par la taille du champ de sélection. Toutefois, si la zone de liste déroulante a le style [**CBS \_ AUTOHSCROLL**](combo-box-styles.md) , le texte peut continuer au-delà de la taille du champ de sélection. Une application peut utiliser le message [**CB \_ LIMITTEXT**](cb-limittext.md) pour limiter la quantité de texte qu’un utilisateur peut taper dans le champ de sélection, que le contrôle ait le style **CBS \_ AUTOHSCROLL** ou non.

Lorsque l’utilisateur modifie le contenu du champ de sélection, la procédure de la fenêtre parente ou de la boîte de dialogue reçoit des messages de notification. Le code de notification [CBN \_ EDITUPDATE](cbn-editupdate.md) est envoyé en premier, ce qui indique que le texte dans le champ de sélection a été modifié. Une fois le texte modifié affiché, le système envoie [CBN \_ EDITCHANGE](cbn-editchange.md). Lorsque le contenu du champ de sélection change à la suite de la sélection d’un élément de liste, ces messages ne sont pas envoyés.

## <a name="owner-drawn-combo-boxes"></a>Zones de liste déroulante Owner-Drawn

Une application peut créer une zone de liste déroulante owner-drawn pour assumer la responsabilité de la peinture des éléments de liste. La fenêtre parente d’une zone de liste déroulante owner-drawn (son propriétaire) reçoit des messages [**WM \_ DRAWITEM**](wm-drawitem.md) lorsqu’une partie de la zone de liste déroulante doit être peinte. Une zone de liste déroulante owner-drawn peut répertorier des informations autres que des chaînes de texte, ou en plus de celles-ci. Les zones de liste déroulante owner-drawn peuvent être de n’importe quel type. Toutefois, le contrôle d’édition dans une zone de liste modifiable simple ou déroulante ne peut afficher que du texte, tandis que le propriétaire peint le champ de sélection dans une zone de liste déroulante.

Le propriétaire d’une zone de liste déroulante owner-drawn doit traiter le message [**WM \_ DRAWITEM**](wm-drawitem.md) . Ce message est envoyé chaque fois qu’une partie de la zone de liste déroulante doit être redessinée. Le propriétaire peut avoir besoin de traiter d’autres messages, selon les styles spécifiés pour la zone de liste déroulante.

Une application peut créer une zone de liste déroulante owner-drawn en spécifiant le style [**CBS \_ OWNERDRAWFIXED**](combo-box-styles.md) ou [**CBS \_ OWNERDRAWVARIABLE**](combo-box-styles.md) . Si tous les éléments de liste de la zone de liste déroulante sont de la même hauteur, tels que des chaînes ou des icônes, une application peut utiliser le style **CBS \_ OWNERDRAWFIXED** . Si les éléments de liste sont de hauteur variable, comme les bitmaps de taille différente, une application peut utiliser le style **CBS \_ OWNERDRAWVARIABLE** .

Le propriétaire d’une zone de liste déroulante owner-drawn peut traiter un message [**WM \_ MEASUREITEM**](wm-measureitem.md) pour spécifier les dimensions des éléments de liste dans la zone de liste déroulante. Si l’application crée la zone de liste déroulante en utilisant le style [**CBS \_ OWNERDRAWFIXED**](combo-box-styles.md) , le système envoie le message **WM \_ MEASUREITEM** une seule fois. Les dimensions spécifiées par le propriétaire sont utilisées pour tous les éléments de liste. Si le style [**CBS \_ OWNERDRAWVARIABLE**](combo-box-styles.md) est utilisé, le système envoie un message **WM \_ MEASUREITEM** pour chaque élément de liste ajouté à la zone de liste déroulante. Le propriétaire peut déterminer ou définir la hauteur d’un élément de liste à tout moment à l’aide des messages [**CB \_ GETITEMHEIGHT**](cb-getitemheight.md) et [**CB \_ SETITEMHEIGHT**](cb-setitemheight.md) , respectivement.

Si les informations affichées dans une zone de liste déroulante owner-drawn incluent du texte, une application peut effectuer le suivi du texte pour chaque élément de liste en spécifiant le style [**CBS \_ HASSTRINGS**](combo-box-styles.md) . Les zones de liste déroulante avec le style de [**\_ Tri CBS**](combo-box-styles.md) sont triées en fonction de ce texte. Si une zone de liste déroulante est triée et non le style **CBS \_ HASSTRINGS** , le propriétaire doit traiter le message [**WM \_ COMPAREITEM**](wm-compareitem.md) .

Dans une zone de liste déroulante owner-drawn, le propriétaire doit effectuer le suivi des éléments de liste contenant des informations autres que ou en plus du texte. Pour ce faire, une méthode pratique consiste à enregistrer le handle dans les informations en tant que données d’élément. Pour libérer des objets de données associés à des éléments dans une zone de liste déroulante, le propriétaire peut traiter le message [**WM \_ DELETEITEM**](wm-deleteitem.md) .

## <a name="subclassed-combo-boxes"></a>Zones de liste déroulante sous-classées

Le sous-classing est une procédure qui permet à une application d’intercepter et de traiter les messages envoyés ou publiés dans une fenêtre. En utilisant le sous-usinage, une application peut substituer son propre traitement à certains messages, tout en laissant la plupart du traitement des messages à la procédure de fenêtre définie par la classe.

Lorsque le système d’exploitation crée une fenêtre, il enregistre les informations qui le concernent dans une structure de données interne qui comprend un pointeur vers la procédure de fenêtre. Pour sous-classer une fenêtre, une application appelle la fonction [**SetClassLong**](/windows/desktop/api/winuser/nf-winuser-setclasslonga) pour remplacer le pointeur vers cette procédure par un pointeur vers une procédure de sous-classe définie par l’application. Par la suite, tous les messages dans la fenêtre sont envoyés à la procédure de sous-classe. Cette procédure utilise ensuite la fonction [**CallWindowProc**](/windows/desktop/api/winuser/nf-winuser-callwindowproca) pour transmettre des messages non traités à la procédure de fenêtre d’origine. Pour obtenir une description du traitement des messages effectué par la procédure de fenêtre de la classe COMBOBOX, consultez comportement de la [zone de liste déroulante par défaut](combo-box-features.md).

Lorsque la zone de liste déroulante est à l’extérieur d’une boîte de dialogue, une application ne peut pas traiter les touches TAB, entrée et ÉCHAP, sauf si elle utilise une procédure de sous-classe. Lorsqu’une zone de liste modifiable simple ou déroulante reçoit le focus d’entrée, elle définit immédiatement le focus sur son contrôle d’édition enfant. Par conséquent, une application doit sous-définir le contrôle d’édition pour intercepter l’entrée au clavier pour une zone de liste modifiable simple ou déroulante. Pour obtenir un exemple, consultez [sous-classement d’une zone de liste déroulante](using-combo-boxes.md).

Si une procédure de sous-classe traite le message [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) , elle doit utiliser la fonction [**BeginPaint**](/windows/desktop/api/winuser/nf-winuser-beginpaint) pour préparer la peinture. Avant d’appeler la fonction [**EndPaint**](/windows/desktop/api/winuser/nf-winuser-endpaint) , elle passe le handle de contexte de périphérique (DC) comme paramètre *wParam* pour la procédure de fenêtre. Si **EndPaint** est appelé en premier, la procédure de la fenêtre de classe ne dessine pas, car **EndPaint** valide la fenêtre entière.

Une technique en rapport avec le sous-classing est la superclassement. Une superclasse ressemble à toute autre classe, sauf que sa procédure de fenêtre n’appelle pas [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) pour gérer les messages non traités. Au lieu de cela, il transmet des messages non traités à la procédure de fenêtre pour la classe de fenêtre parente. Suivez les instructions des [procédures de fenêtre](/windows/desktop/winmsg/window-procedures) pour éviter les problèmes qui peuvent se produire avec le sous-classing et le surclassement.

 

 