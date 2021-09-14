---
title: À propos des zones de liste
description: Cette section décrit les fonctionnalités de la zone de liste.
ms.assetid: 359bb363-5b97-4e0c-bdc4-bfa6a6504a76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 674712226a79960e44ab99ed8e59c88b27984efb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126999397"
---
# <a name="about-list-boxes"></a>À propos des zones de liste

Un contrôle de zone de liste contient une liste simple à partir de laquelle l’utilisateur peut généralement sélectionner un ou plusieurs éléments. Les zones de liste offrent une flexibilité limitée par rapport aux contrôles d' [affichage de liste](list-view-control-reference.md) .

Les éléments de zone de liste peuvent être représentés par des chaînes de texte, des bitmaps, ou les deux. Si la zone de liste n’est pas assez grande pour afficher tous les éléments de la zone de liste en même temps, la zone de liste fournit une barre de défilement. L’utilisateur fait défiler les éléments de la zone de liste et applique ou supprime l’état de la sélection, si nécessaire. La sélection d’un élément de zone de liste modifie son apparence, généralement en remplaçant les couleurs de texte et d’arrière-plan par celles spécifiées par les métriques du système d’exploitation approprié. Lorsque l’utilisateur sélectionne ou désélectionne un élément, le système envoie un message de notification à la fenêtre parente de la zone de liste.

Pour une application ANSI, le système convertit le texte d’une zone de liste en Unicode à l’aide de la page de codes **CP \_ ACP** . Cela peut entraîner des problèmes. par exemple, les caractères romains accentués dans une zone de liste non Unicode dans Windows, la version japonaise sera tronquée. Pour résoudre ce problème, compilez l’application en Unicode ou utilisez une zone de liste owner-drawn.

Cette section aborde les sujets suivants :

-   [Création d’une zone de liste](#creating-a-list-box)
-   [Types et styles de zone de liste](#list-box-types-and-styles)
-   [Fonctions de zone de liste](#list-box-functions)
-   [Messages de notification à partir de zones de liste](#notification-messages-from-list-boxes)
-   [Messages dans les zones de liste](#notification-messages-from-list-boxes)
-   [Traitement par défaut des messages de fenêtre](#default-window-message-processing)
-   [Zones de liste owner-drawn](#owner-drawn-list-boxes)
-   [Faire glisser les zones de liste](#drag-list-boxes)
    -   [Création de zones de liste de glissement](#creating-drag-list-boxes)
    -   [Faire glisser des messages de zone de liste](#drag-list-box-messages)
    -   [Faire glisser les codes de notification de zone de liste](#drag-list-box-notification-codes)

## <a name="creating-a-list-box"></a>Création d’une zone de liste

le moyen le plus simple de créer une zone de liste dans une boîte de dialogue consiste à la faire glisser de la boîte à outils dans Microsoft Visual Studio vers votre ressource de boîte de dialogue. Pour créer une zone de liste dynamiquement ou pour créer une zone de liste dans une fenêtre autre qu’une boîte de dialogue, utilisez la fonction [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , en spécifiant la classe de fenêtre de la zone de liste de [**WC \_**](common-control-window-classes.md) et les styles de zone de [liste](list-box-styles.md)appropriés.

## <a name="list-box-types-and-styles"></a>Types et styles de zone de liste

Il existe deux types de zones de liste : une sélection unique (valeur par défaut) et une sélection multiple. Dans une zone de liste à sélection unique, l’utilisateur ne peut sélectionner qu’un seul élément à la fois. Dans une zone de liste à sélection multiple, l’utilisateur peut sélectionner plusieurs éléments à la fois. Pour créer une zone de liste à sélection multiple, spécifiez le style de [**\_ MULTIPLESEL kg**](list-box-styles.md) ou [**\_ EXTENDEDSEL**](list-box-styles.md) .

L’apparence et le fonctionnement d’une zone de liste sont contrôlés par les [styles de zone de liste](list-box-styles.md) et les styles de fenêtre. Ces styles indiquent si la liste est triée, réorganisée en plusieurs colonnes, dessinées par l’application, et ainsi de suite. Les dimensions et les styles d’une zone de liste sont généralement définis dans un modèle de boîte de dialogue qui est inclus dans les ressources d’une application.

> [!Note]  
> Pour utiliser les styles visuels avec ces contrôles, une application doit inclure un manifeste et doit appeler [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) au début du programme. Pour plus d’informations sur les styles visuels, consultez [styles visuels](themes-overview.md). Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).

 

## <a name="list-box-functions"></a>Fonctions de zone de liste

La fonction [**DlgDirList**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista) remplace le contenu d’une zone de liste par les noms de lecteurs, de répertoires et de fichiers qui correspondent à un ensemble de critères spécifié. La fonction [**DlgDirSelectEx**](/windows/desktop/api/Winuser/nf-winuser-dlgdirselectexa) récupère la sélection actuelle dans une zone de liste initialisée par **DlgDirList**. Ces fonctions permettent à l’utilisateur de sélectionner un lecteur, un répertoire ou un fichier à partir d’une zone de liste sans taper l’emplacement et le nom du fichier.

En outre, la fonction [**GetListBoxInfo**](/windows/desktop/api/Winuser/nf-winuser-getlistboxinfo) retourne le nombre d’éléments par colonne dans une zone de liste spécifiée.

## <a name="notification-messages-from-list-boxes"></a>Messages de notification à partir de zones de liste

Lorsqu’un événement se produit dans une zone de liste, la zone de liste envoie un code de notification, sous la forme d’un message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) , à la procédure de la boîte de dialogue de la fenêtre propriétaire. Les codes de notification de zone de liste sont envoyés lorsqu’un utilisateur sélectionne, double-clique ou annule un élément de zone de liste ; Lorsque la zone de liste reçoit ou perd le focus clavier ; et lorsque le système ne peut pas allouer suffisamment de mémoire pour une demande de zone de liste. Un message de **\_ commande WM** contient l’identificateur de zone de liste dans le mot de poids faible du paramètre *wParam* et le code de notification dans le mot de poids fort. Le paramètre *lParam* contient le handle de fenêtre de contrôle.

Une procédure de boîte de dialogue n’est pas requise pour traiter ces messages ; la procédure de fenêtre par défaut les traite.

Une application doit surveiller et traiter les codes de notification de la zone de liste suivante.



| Code de notification                   | Description                                                      |
|-------------------------------------|------------------------------------------------------------------|
| [LBN \_ DBLCLK](lbn-dblclk.md)       | L’utilisateur double-clique sur un élément dans la zone de liste.                  |
| [LBN \_ ERRSPACE](lbn-errspace.md)   | La zone de liste ne peut pas allouer suffisamment de mémoire pour traiter une demande. |
| [LBN \_ KILLFOCUS](lbn-killfocus.md) | La zone de liste perd le focus clavier.                           |
| [LBN \_ SELCANCEL](lbn-selcancel.md) | L’utilisateur annule la sélection d’un élément dans la zone de liste.       |
| [LBN \_ selChange](lbn-selchange.md) | La sélection dans une zone de liste va être modifiée.                  |
| [LBN \_ SetFocus](lbn-setfocus.md)   | La zone de liste reçoit le focus clavier.                        |



 

## <a name="messages-to-list-boxes"></a>Messages dans les zones de liste

Une procédure de boîte de dialogue peut envoyer des messages à une zone de liste pour ajouter, supprimer, examiner et modifier des éléments de zone de liste. Par exemple, une procédure de boîte de dialogue peut envoyer un message [**lb \_ ADDSTRING**](lb-addstring.md) à une zone de liste pour ajouter un élément et un message [**lb \_ GETSEL**](lb-getsel.md) pour déterminer si l’élément est sélectionné. D’autres messages définissent et récupèrent des informations sur la taille, l’apparence et le comportement de la zone de liste. Par exemple, le message [**lb \_ SETHORIZONTALEXTENT**](lb-sethorizontalextent.md) définit la largeur de défilement d’une zone de liste. Une procédure de boîte de dialogue peut envoyer n’importe quel message à une zone de liste à l’aide de la fonction [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) ou [**SendDlgItemMessage**](/windows/desktop/api/winuser/nf-winuser-senddlgitemmessagea) .

Un élément de zone de liste est souvent référencé par son *index*, un entier qui représente la position de l’élément dans la zone de liste. L’index du premier élément d’une zone de liste est 0, l’index du deuxième élément est 1, et ainsi de suite.

Le tableau suivant décrit comment la procédure prédéfinie de la zone de liste répond aux messages de zone de liste.



| Message                                                   | response                                                                                                                                                                                                                         |
|-----------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_ADDFILE lb**](lb-addfile.md)                         | Insère un fichier dans une zone de liste de répertoires qui est remplie par la fonction [**DlgDirList**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista) et récupère l’index de la zone de liste de l’élément inséré.                                                                  |
| [**LB \_ ADDSTRING**](lb-addstring.md)                     | Ajoute une chaîne à une zone de liste et retourne son index.                                                                                                                                                                               |
| [**\_DELETESTRING lb**](lb-deletestring.md)               | Supprime une chaîne d’une zone de liste et retourne le nombre de chaînes qui restent dans la liste.                                                                                                                                      |
| [**direction \_ lb**](lb-dir.md)                                 | Ajoute une liste de noms de fichiers à une zone de liste et retourne l’index du dernier nom de fichier ajouté.                                                                                                                                       |
| [**\_FindString lb**](lb-findstring.md)                   | Retourne l’index de la première chaîne dans la zone de liste qui commence par une chaîne spécifiée.                                                                                                                                       |
| [**\_FINDEXACTSTRING lb**](lb-findstringexact.md)         | Retourne l’index de la chaîne dans la zone de liste qui est égale à une chaîne spécifiée.                                                                                                                                             |
| [**\_GETANCHORINDEX lb**](lb-getanchorindex.md)           | Retourne l’index de l’élément que la souris a sélectionné en dernier.                                                                                                                                                                      |
| [**\_GETCARETINDEX lb**](lb-getcaretindex.md)             | Retourne l’index de l’élément qui a le rectangle de focus.                                                                                                                                                                      |
| [**LB \_ GETCOUNT**](lb-getcount.md)                       | Retourne le nombre d’éléments dans la zone de liste.                                                                                                                                                                                     |
| [**\_GETCURSEL lb**](lb-getcursel.md)                     | Retourne l’index de l’élément actuellement sélectionné.                                                                                                                                                                                |
| [**\_GETHORIZONTALEXTENT lb**](lb-gethorizontalextent.md) | Retourne la largeur de défilement, en pixels, d’une zone de liste.                                                                                                                                                                          |
| [**\_GETITEMDATA lb**](lb-getitemdata.md)                 | Retourne la valeur associée à l’élément spécifié.                                                                                                                                                                    |
| [**\_GETITEMHEIGHT lb**](lb-getitemheight.md)             | Retourne la hauteur, en pixels, d’un élément dans une zone de liste.                                                                                                                                                                         |
| [**\_GETITEMRECT lb**](lb-getitemrect.md)                 | Récupère les coordonnées clientes de l’élément de zone de liste spécifié.                                                                                                                                                                 |
| [**\_GETLOCALE lb**](lb-getlocale.md)                     | Récupère les paramètres régionaux de la zone de liste. Le mot de poids fort contient le code de pays/région et le mot de poids faible contient l’identificateur de langue.                                                                              |
| [**\_GETSEL lb**](lb-getsel.md)                           | Retourne l’état de sélection d’un élément de zone de liste.                                                                                                                                                                                  |
| [**\_GETSELCOUNT lb**](lb-getselcount.md)                 | Retourne le nombre d’éléments sélectionnés dans une zone de liste à sélection multiple.                                                                                                                                                           |
| [**\_GETSELITEMS lb**](lb-getselitems.md)                 | Crée un tableau des index de tous les éléments sélectionnés dans une zone de liste à sélection multiple et retourne le nombre total d’éléments sélectionnés.                                                                                           |
| [**LB, \_ GETTEXT**](lb-gettext.md)                         | Récupère la chaîne associée à un élément spécifié et la longueur de la chaîne.                                                                                                                                              |
| [**\_GETTEXTLEN lb**](lb-gettextlen.md)                   | Retourne la longueur, en caractères, de la chaîne associée à un élément spécifié.                                                                                                                                               |
| [**\_GETTOPINDEX lb**](lb-gettopindex.md)                 | Retourne l’index du premier élément visible dans une zone de liste.                                                                                                                                                                       |
| [**LB \_ INITSTORAGE**](lb-initstorage.md)                 | Alloue de la mémoire pour le nombre spécifié d’éléments et leurs chaînes associées.                                                                                                                                                 |
| [**\_INSERTSTRING lb**](lb-insertstring.md)               | Insère une chaîne à un index spécifié dans une zone de liste.                                                                                                                                                                             |
| [**\_ITEMFROMPOINT lb**](lb-itemfrompoint.md)             | Récupère l’index de base zéro de l’élément le plus proche du point spécifié dans une zone de liste.                                                                                                                                            |
| [**\_RESETCONTENT lb**](lb-resetcontent.md)               | Supprime tous les éléments d’une zone de liste.                                                                                                                                                                                               |
| [**\_SELECTSTRING lb**](lb-selectstring.md)               | Sélectionne la première chaîne trouvée qui correspond à un préfixe spécifié.                                                                                                                                                               |
| [**\_SELITEMRANGE lb**](lb-selitemrange.md)               | Sélectionne une plage d’éléments spécifiée dans une zone de liste.                                                                                                                                                                                |
| [**\_SELITEMRANGEEX lb**](lb-selitemrangeex.md)           | Sélectionne une plage d’éléments spécifiée si l’index du premier élément de la plage est inférieur à l’index du dernier élément de la plage. Annule la sélection dans la plage si l’index du premier élément est supérieur au dernier. |
| [**\_SETANCHORINDEX lb**](lb-setanchorindex.md)           | Définit l’élément sur lequel la souris a sélectionné la dernière fois pour un élément spécifié.                                                                                                                                                                  |
| [**\_SETCARETINDEX lb**](lb-setcaretindex.md)             | Définit le rectangle de focus sur un élément de zone de liste spécifié.                                                                                                                                                                           |
| [**\_SETCOLUMNWIDTH lb**](lb-setcolumnwidth.md)           | Définit la largeur, en pixels, de toutes les colonnes dans une zone de liste.                                                                                                                                                                         |
| [**\_SETCOUNT lb**](lb-setcount.md)                       | Définit le nombre d’éléments dans une zone de liste.                                                                                                                                                                                          |
| [**\_SETCURSEL lb**](lb-setcursel.md)                     | Sélectionne un élément de zone de liste spécifié.                                                                                                                                                                                               |
| [**\_SETHORIZONTALEXTENT lb**](lb-sethorizontalextent.md) | Définit la largeur de défilement, en pixels, d’une zone de liste.                                                                                                                                                                             |
| [**\_SETITEMDATA lb**](lb-setitemdata.md)                 | Associe une valeur à un élément de zone de liste.                                                                                                                                                                                         |
| [**\_SETITEMHEIGHT lb**](lb-setitemheight.md)             | Définit la hauteur, en pixels, d’un ou de tous les éléments d’une zone de liste.                                                                                                                                                                   |
| [**LB \_ SETLOCALE**](lb-setlocale.md)                     | Définit les paramètres régionaux d’une zone de liste et retourne l’identificateur de paramètres régionaux précédent.                                                                                                                                                        |
| [**\_SETSEL lb**](lb-setsel.md)                           | Sélectionne un élément dans une zone de liste à sélection multiple.                                                                                                                                                                                |
| [**\_SETTABSTOPS lb**](lb-settabstops.md)                 | Définit les taquets de tabulation à ceux spécifiés dans un tableau spécifié.                                                                                                                                                                      |
| [**\_SETTOPINDEX lb**](lb-settopindex.md)                 | Fait défiler la zone de liste pour que l’élément spécifié se trouve en haut de la plage visible.                                                                                                                                                   |



 

## <a name="default-window-message-processing"></a>Traitement par défaut des messages de fenêtre

La procédure de fenêtre pour la classe de fenêtre de zone de liste prédéfinie effectue le traitement par défaut pour tous les messages qui ne sont pas traités par la zone de liste. Lorsque la procédure de la zone de liste retourne la **valeur false** pour un message, la procédure de fenêtre prédéfinie vérifie le message et exécute les actions par défaut, comme indiqué dans le tableau suivant.



| Message                                            | Action par défaut                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_caractère WM**](/windows/desktop/inputdev/wm-char)                   | Déplace la sélection vers le premier élément qui commence par le caractère tapé par l’utilisateur. Si la zone de liste a le style L [**BS \_ OwnerDraw**](button-styles.md) , aucune action ne se produit. Plusieurs caractères tapés dans un intervalle bref sont traités comme un groupe et le premier élément qui commence par cette série de caractères est sélectionné.<br/> |
| [**création de WM \_**](/windows/desktop/winmsg/wm-create)                 | Crée une zone de liste vide.                                                                                                                                                                                                                                                                                                                                               |
| [**\_destructeur WM**](/windows/desktop/winmsg/wm-destroy)               | Détruit la zone de liste et libère toutes les ressources qu’elle utilise.                                                                                                                                                                                                                                                                                                              |
|                                                    | Transmet le message à la procédure de boîte de dialogue ou au processus de fenêtre parente.                                                                                                                                                                                                                                                                                                 |
| [**\_activer WM**](/windows/desktop/winmsg/wm-enable)                 | Si le contrôle est visible, invalide le rectangle afin que les chaînes puissent être peintes en gris.                                                                                                                                                                                                                                                                                 |
| [**\_ERASEBKGND WM**](/windows/desktop/winmsg/wm-erasebkgnd)         | Efface l’arrière-plan d’une zone de liste. Si la zone de liste a le style g [**BS \_ OwnerDraw**](button-styles.md) , l’arrière-plan n’est pas effacé.                                                                                                                                                                                                                   |
| [**\_GETDLGCODE WM**](/windows/desktop/dlgbox/wm-getdlgcode)         | Retourne DLGC \_ WANTARROWS \| DLGC \_ WANTCHARS, ce qui indique que la procédure de zone de liste par défaut traite les touches de direction et les messages [**WM \_ char**](/windows/desktop/inputdev/wm-char) .                                                                                                                                                                                                      |
| [**WM \_ GETFONT**](/windows/desktop/winmsg/wm-getfont)               | Retourne un handle vers la police actuelle de la zone de liste.                                                                                                                                                                                                                                                                                                                   |
| [**\_HSCROLL WM**](wm-hscroll.md)                  | Fait défiler la zone de liste horizontalement.                                                                                                                                                                                                                                                                                                                                       |
| [**WM- \_ touche**](/windows/desktop/inputdev/wm-keydown)             | Traite les touches virtuelles pour le défilement. La clé virtuelle est l’index de l’élément vers lequel placer le signe insertion. La sélection n’est pas modifiée.                                                                                                                                                                                                                                       |
| [**\_KILLFOCUS WM**](/windows/desktop/inputdev/wm-killfocus)         | Désactive le signe insertion et le détruit. Envoie un code de notification [LBN \_ KILLFOCUS](lbn-killfocus.md) au propriétaire de la zone de liste.                                                                                                                                                                                                                                        |
| [**\_LBUTTONDBLCLK WM**](/windows/desktop/inputdev/wm-lbuttondblclk) | Effectue le suivi de la souris dans la zone cliente de la zone de liste. Cela permet à l’utilisateur d’annuler une sélection si le bouton de la souris est relâché en dehors de la zone cliente de la zone de liste.                                                                                                                                                                                                              |
| [**\_LBUTTONDOWN WM**](/windows/desktop/inputdev/wm-lbuttondown)     | Effectue le suivi de la souris dans la zone cliente de la zone de liste. Cela permet à l’utilisateur d’annuler une sélection si le bouton de la souris est relâché en dehors de la zone cliente de la zone de liste.                                                                                                                                                                                                              |
| [**\_LBUTTONUP WM**](/windows/desktop/inputdev/wm-lbuttonup)         | Effectue le suivi de la souris dans la zone cliente de la zone de liste. Cela permet à l’utilisateur d’annuler une sélection si le bouton de la souris est relâché en dehors de la zone cliente de la zone de liste.                                                                                                                                                                                                              |
| [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove)         | Effectue le suivi de la souris dans la zone cliente de la zone de liste. Cela permet à l’utilisateur d’annuler une sélection si le bouton de la souris est relâché en dehors de la zone cliente de la zone de liste.                                                                                                                                                                                                              |
| [**\_peinture WM**](/windows/desktop/gdi/wm-paint)                      | Effectue une opération de peinture sous-classée à l’aide du handle de zone de liste vers le contexte de périphérique (DC).                                                                                                                                                                                                                                                                           |
| [**WM \_ SetFocus**](/windows/desktop/inputdev/wm-setfocus)           | Active le signe insertion et envoie un code de notification [LBN \_ SetFocus](lbn-setfocus.md) au propriétaire de la zone de liste.                                                                                                                                                                                                                                                        |
| [**\_SetFont WM**](/windows/desktop/winmsg/wm-setfont)               | Définit une nouvelle police pour la zone de liste.                                                                                                                                                                                                                                                                                                                                        |
| [**\_SETREDRAW WM**](/windows/desktop/gdi/wm-setredraw)              | Définit ou efface l’indicateur de redessin en fonction de la valeur de *wParam*.                                                                                                                                                                                                                                                                                                           |
| [**taille du WM \_**](/windows/desktop/winmsg/wm-size)                     | Redimensionne la zone de liste en un nombre entier d’éléments.                                                                                                                                                                                                                                                                                                                     |
| [**\_VSCROLL WM**](wm-vscroll.md)                  | Fait défiler la zone de liste verticalement.                                                                                                                                                                                                                                                                                                                                         |



 

La procédure de zone de liste prédéfinie transmet tous les autres messages à [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) pour le traitement par défaut.

## <a name="owner-drawn-list-boxes"></a>Zones de liste Owner-Drawn

Une application peut créer une zone de liste *owner-drawn* pour assumer la responsabilité de la peinture des éléments de liste. La fenêtre parente ou la boîte de dialogue d’une zone de liste owner-drawn (son *propriétaire*) reçoit des messages [**WM \_**](wm-drawitem.md) à l’arrêt lorsqu’une partie de la zone de liste doit être peinte. Une zone de liste owner-drawn peut répertorier des informations autres que des chaînes de texte, ou en plus de celles-ci.

Le propriétaire d’une zone de liste owner-drawn doit traiter le message [**WM \_ DRAWITEM**](wm-drawitem.md) . Ce message est envoyé chaque fois qu’une partie de la zone de liste doit être redessinée. Le propriétaire peut avoir besoin de traiter d’autres messages, selon les styles spécifiés pour la zone de liste.

Une application peut créer une zone de liste owner-drawn en spécifiant le [**style \_ OWNERDRAWVARIABLE**](list-box-styles.md) [**kg \_ OWNERDRAWFIXED**](list-box-styles.md) ou lbs. Si tous les éléments de liste de la zone de liste sont de la même hauteur, tels que des chaînes ou des icônes, une application peut utiliser le style **\_ OWNERDRAWFIXED** . Si les éléments de liste sont de hauteur variable (par exemple, des bitmaps de taille différente), une application peut utiliser le style **\_ OWNERDRAWVARIABLE** .

Le propriétaire d’une zone de liste owner-drawn peut traiter un message [**WM \_ MEASUREITEM**](wm-measureitem.md) pour spécifier les dimensions des éléments de liste. Si l’application crée la zone de liste à l’aide du style [**\_ OWNERDRAWFIXED lbs**](list-box-styles.md) , le système envoie le message **WM \_ MEASUREITEM** une seule fois. Les dimensions spécifiées par le propriétaire sont utilisées pour tous les éléments de liste. Si le style [**lbs \_ OWNERDRAWVARIABLE**](list-box-styles.md) est utilisé, le système envoie un message **WM \_ MEASUREITEM** pour chaque élément de liste ajouté à la zone de liste. Le propriétaire peut déterminer ou définir la hauteur d’un élément de liste à tout moment à l’aide des messages [**lb \_ GETITEMHEIGHT**](lb-getitemheight.md) et [**lb \_ SETITEMHEIGHT**](lb-setitemheight.md) , respectivement.

Si les informations affichées dans une zone de liste owner-drawn contiennent du texte, une application peut effectuer le suivi du texte pour chaque élément de liste en spécifiant le style [**\_ HASSTRINGS**](list-box-styles.md) . Les zones de liste avec le style de [**\_ Tri lbs**](list-box-styles.md) sont triées en fonction de ce texte. Si une zone de liste est triée, mais n’est pas du style **\_ HASSTRINGS** , le propriétaire doit traiter le message [**WM \_ COMPAREITEM**](wm-compareitem.md) .

Dans une zone de liste owner-drawn, le propriétaire doit effectuer le suivi des éléments de liste qui contiennent des informations autres que ou en plus du texte. Pour ce faire, une méthode pratique consiste à enregistrer le descripteur sur les informations en tant que données d’élément à l’aide du message [**lb \_ SETITEMDATA**](lb-setitemdata.md) . Pour libérer des objets de données associés à des éléments dans une zone de liste, le propriétaire peut traiter le message [**WM \_ DELETEITEM**](wm-deleteitem.md) .

Pour obtenir un exemple de zone de liste owner-drawn, consultez [comment créer une zone de liste de Owner-Drawn](create-an-owner-drawn-list-box.md).

## <a name="drag-list-boxes"></a>Faire glisser les zones de liste

Une zone de liste de glissement est un type spécial de zone de liste qui permet à l’utilisateur de faire glisser des éléments d’une position à une autre. Une application peut utiliser une zone de liste de glissement pour afficher des chaînes dans une séquence particulière et permettre à l’utilisateur de modifier la séquence en faisant glisser les éléments dans la position.

### <a name="creating-drag-list-boxes"></a>Création de zones de liste de glissement

Les zones de liste faisant glisser ont les mêmes styles de fenêtre et traitent les mêmes messages que les zones de liste standard. Pour créer une zone de liste de glissement, commencez par créer une zone de liste standard, puis appelez la fonction [**MakeDragList**](/windows/desktop/api/Commctrl/nf-commctrl-makedraglist) . Pour convertir une zone de liste dans une boîte de dialogue en zone de liste de glissement, vous pouvez appeler **MakeDragList** lors du \_ traitement du message WM INITDIALOG.

### <a name="drag-list-box-messages"></a>Faire glisser des messages de zone de liste

Une zone de liste de glissement notifie la fenêtre parente des événements de glissement en lui envoyant un message de liste de glissement. La fenêtre parente doit traiter le message de liste de glissement.

La zone de liste glisser inscrit ce message lorsque la fonction [**MakeDragList**](/windows/desktop/api/Commctrl/nf-commctrl-makedraglist) est appelée. Pour récupérer l’identificateur de message (valeur numérique) du message de liste de glissement, appelez la fonction [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) et spécifiez la valeur DRAGLISTMSGSTRING.

Le paramètre *wParam* du message de liste de glissement est l’identificateur de contrôle pour la zone de liste de glissement. Le paramètre *lParam* est l’adresse d’une structure [**DRAGLISTINFO**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo) , qui contient le code de notification pour l’événement de glissement et d’autres informations. La valeur de retour du message dépend de la notification.

### <a name="drag-list-box-notification-codes"></a>Faire glisser les codes de notification de zone de liste

Le code de notification de la liste de glissement, qui est identifié par le membre **uNotification** de la structure [**DRAGLISTINFO**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo) inclus dans le message de liste de glisser-déplacer, peut être [DL \_ BEGINDRAG](dl-begindrag.md), [DL \_](dl-dragging.md)draging, [DL \_ CANCELDRAG](dl-canceldrag.md)ou [DL \_ relâchée](dl-dropped.md).

Le code de notification [DL \_ BEGINDRAG](dl-begindrag.md) est envoyé lorsque le curseur se trouve sur un élément de liste et que l’utilisateur clique avec le bouton gauche de la souris. La fenêtre parente peut retourner la **valeur true** pour commencer l’opération glisser ou **false** pour interdire le glissement. De cette façon, la fenêtre parente peut activer le glissement pour certains éléments de la liste et la désactiver pour d’autres. Vous pouvez déterminer l’élément de liste qui se trouve à l’emplacement spécifié à l’aide de la fonction [**LBItemFromPt**](/windows/desktop/api/Commctrl/nf-commctrl-lbitemfrompt) .

Si le glissement est activé, la [LD \_ faisant glisser](dl-dragging.md) le code de notification est envoyée chaque fois que la souris est déplacée, ou à intervalles réguliers si la souris n’est pas déplacée. La fenêtre parente doit d’abord déterminer l’élément de liste sous le curseur en utilisant [**LBItemFromPt**](/windows/desktop/api/Commctrl/nf-commctrl-lbitemfrompt) , puis dessiner l’icône d’insertion à l’aide de la fonction [**DrawInsert**](/windows/desktop/api/Commctrl/nf-commctrl-drawinsert) . En spécifiant la **valeur true** pour le paramètre *bAutoScroll* de **LBItemFromPt**, vous pouvez faire défiler la zone de liste d’une ligne si le curseur se trouve au-dessus ou au-dessous de sa zone cliente. La valeur que vous retournez pour cette notification spécifie le type de curseur de la souris que la zone de liste glisser-déplacer doit définir.

Le code de notification [DL \_ CANCELDRAG](dl-canceldrag.md) est envoyé si l’utilisateur annule une opération glisser-déplacer en cliquant sur le bouton droit de la souris ou en appuyant sur la touche ÉCHAP. Le code de notification [ \_ supprimé DL](dl-dropped.md) est envoyé si l’utilisateur effectue une opération glisser-déplacer en relâchant le bouton gauche de la souris, même si le curseur ne se trouve pas sur un élément de liste. La zone de liste glisser libère la capture de la souris avant l’envoi de l’une ou l’autre notification. La valeur de retour de ces deux notifications est ignorée. Faire glisser la liste

 

