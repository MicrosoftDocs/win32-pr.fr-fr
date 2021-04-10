---
title: Zone de liste
description: Cette section contient des informations sur les éléments de programmation utilisés avec les zones de liste. Une zone de liste est une fenêtre de contrôle qui contient une liste simple d’éléments à partir desquels l’utilisateur peut choisir.
ms.assetid: vs|controls|~\controls\listboxes\listboxes.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fda5e6bb2d1d4c3c4f23e506900257c1b2ce64b
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104102393"
---
# <a name="list-box"></a>Zone de liste

Cette section contient des informations sur les éléments de programmation utilisés avec les zones de liste. Une zone de liste est une fenêtre de contrôle qui contient une liste simple d’éléments à partir desquels l’utilisateur peut choisir. Pour obtenir des listes plus complexes, utilisez plutôt le [mode liste](list-view-control-reference.md) .

### <a name="overviews"></a>Vues d'ensemble



| Rubrique                                    | Contenu                                                              |
|------------------------------------------|-----------------------------------------------------------------------|
| [À propos des zones de liste](about-list-boxes.md) | Décrit les fonctionnalités de zone de liste.<br/>                               |
| [Utilisation des zones de liste](using-list-boxes.md) | Explique comment effectuer des tâches associées aux zones de liste. <br/> |



 

### <a name="functions"></a>Fonctions



| Rubrique                                    | Contenu                                                                                                                |
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [**DlgDirList**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista)         | Remplace le contenu d’une zone de liste par les noms des sous-répertoires et des fichiers d’un répertoire spécifié.<br/> |
| [**DlgDirSelectEx**](/windows/desktop/api/Winuser/nf-winuser-dlgdirselectexa) | Récupère la sélection actuelle à partir d’une zone de liste à sélection unique.<br/>                                            |
| [**DrawInsert**](/windows/desktop/api/Commctrl/nf-commctrl-drawinsert)         | Dessine l’icône d’insertion dans la fenêtre parente de la zone de liste de glissement spécifiée. <br/>                                  |
| [**GetListBoxInfo**](/windows/desktop/api/Winuser/nf-winuser-getlistboxinfo) | Récupère des informations sur la zone de liste spécifiée.<br/>                                                          |
| [**LBItemFromPt**](/windows/desktop/api/Commctrl/nf-commctrl-lbitemfrompt)     | Récupère l’index de l’élément au point spécifié dans une zone de liste. <br/>                                       |
| [**MakeDragList**](/windows/desktop/api/Commctrl/nf-commctrl-makedraglist)     | Remplace la zone de liste à sélection unique spécifiée par une zone de liste de glissement. <br/>                                         |



 

### <a name="messages"></a>Messages



| Rubrique                                                     | Contenu                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_ADDFILE lb**](lb-addfile.md)                         | Ajoute le nom de fichier spécifié à une zone de liste qui contient une liste de répertoires. <br/>                                                                                                                                                                                     |
| [**LB \_ ADDSTRING**](lb-addstring.md)                     | Ajoute une chaîne à une zone de liste. <br/>                                                                                                                                                                                                                                      |
| [**\_DELETESTRING lb**](lb-deletestring.md)               | Supprime une chaîne dans une zone de liste. <br/>                                                                                                                                                                                                                                   |
| [**direction \_ lb**](lb-dir.md)                                 | Ajoute des noms à la liste affichée par une zone de liste. <br/>                                                                                                                                                                                                                   |
| [**\_FindString lb**](lb-findstring.md)                   | Recherche la première chaîne dans une zone de liste qui commence par la chaîne spécifiée. <br/>                                                                                                                                                                                       |
| [**\_FINDEXACTSTRING lb**](lb-findstringexact.md)         | Recherche la première chaîne de zone de liste qui correspond exactement à la chaîne spécifiée, sauf que la recherche ne respecte pas la casse. <br/>                                                                                                                                          |
| [**\_GETANCHORINDEX lb**](lb-getanchorindex.md)           | Obtient l’index de l’élément d’ancrage qui est, l’élément à partir duquel une sélection multiple démarre. <br/>                                                                                                                                                                       |
| [**\_GETCARETINDEX lb**](lb-getcaretindex.md)             | Récupère l’index de l’élément qui a le rectangle de focus dans une zone de liste à sélection multiple. L’élément peut être ou non sélectionné. <br/>                                                                                                                               |
| [**LB \_ GETCOUNT**](lb-getcount.md)                       | Obtient le nombre d’éléments dans une zone de liste. <br/>                                                                                                                                                                                                                           |
| [**\_GETCURSEL lb**](lb-getcursel.md)                     | Obtient l’index de l’élément actuellement sélectionné, le cas échéant, dans une zone de liste à sélection unique. <br/>                                                                                                                                                                            |
| [**\_GETHORIZONTALEXTENT lb**](lb-gethorizontalextent.md) | Obtient la largeur, en pixels, qu’une zone de liste peut faire défiler horizontalement (la largeur avec défilement) si la zone de liste a une barre de défilement horizontale. <br/>                                                                                                                       |
| [**\_GETITEMDATA lb**](lb-getitemdata.md)                 | Obtient la valeur définie par l’application associée à l’élément de zone de liste spécifié. <br/>                                                                                                                                                                                   |
| [**\_GETITEMHEIGHT lb**](lb-getitemheight.md)             | Obtient la hauteur des éléments dans une zone de liste. <br/>                                                                                                                                                                                                                           |
| [**\_GETITEMRECT lb**](lb-getitemrect.md)                 | Obtient les dimensions du rectangle qui délimite un élément de zone de liste tel qu’il est actuellement affiché dans la zone de liste. <br/>                                                                                                                                                    |
| [**\_GETLISTBOXINFO lb**](lb-getlistboxinfo.md)           | Obtient le nombre d’éléments par colonne dans une zone de liste spécifiée. <br/>                                                                                                                                                                                                      |
| [**\_GETLOCALE lb**](lb-getlocale.md)                     | Obtient les paramètres régionaux actuels de la zone de liste. <br/>                                                                                                                                                                                                                          |
| [**\_GETSEL lb**](lb-getsel.md)                           | Obtient l’état de sélection d’un élément. <br/>                                                                                                                                                                                                                              |
| [**\_GETSELCOUNT lb**](lb-getselcount.md)                 | Obtient le nombre total d’éléments sélectionnés dans une zone de liste à sélection multiple. <br/>                                                                                                                                                                                         |
| [**\_GETSELITEMS lb**](lb-getselitems.md)                 | Remplit une mémoire tampon avec un tableau d’entiers qui spécifient les numéros d’élément des éléments sélectionnés dans une zone de liste à sélection multiple. <br/>                                                                                                                                        |
| [**LB, \_ GETTEXT**](lb-gettext.md)                         | Obtient une chaîne à partir d’une zone de liste. <br/>                                                                                                                                                                                                                                    |
| [**\_GETTEXTLEN lb**](lb-gettextlen.md)                   | Obtient la longueur d’une chaîne dans une zone de liste. <br/>                                                                                                                                                                                                                        |
| [**\_GETTOPINDEX lb**](lb-gettopindex.md)                 | Obtient l’index du premier élément visible dans une zone de liste. <br/>                                                                                                                                                                                                           |
| [**LB \_ INITSTORAGE**](lb-initstorage.md)                 | Alloue de la mémoire pour le stockage des éléments de zone de liste. Ce message est utilisé avant qu’une application ajoute un grand nombre d’éléments à une zone de liste.<br/>                                                                                                                                |
| [**\_INSERTSTRING lb**](lb-insertstring.md)               | Insère une chaîne ou des données d’élément dans une zone de liste. Contrairement au message [**lb \_ ADDSTRING**](lb-addstring.md) , le [**message \_ INSERTSTRING**](lb-insertstring.md) ne provoque pas le tri d’une liste avec le style de [**\_ Tri lbs**](list-box-styles.md) . <br/> |
| [**\_ITEMFROMPOINT lb**](lb-itemfrompoint.md)             | Obtient l’index de base zéro de l’élément le plus proche du point spécifié dans une zone de liste.<br/>                                                                                                                                                                                   |
| [**\_RESETCONTENT lb**](lb-resetcontent.md)               | Supprime tous les éléments d’une zone de liste. <br/>                                                                                                                                                                                                                                |
| [**\_SELECTSTRING lb**](lb-selectstring.md)               | Recherche un élément qui commence par les caractères d’une chaîne spécifiée dans une zone de liste. <br/>                                                                                                                                                                            |
| [**\_SELITEMRANGE lb**](lb-selitemrange.md)               | Sélectionne ou désélectionne un ou plusieurs éléments consécutifs dans une zone de liste à sélection multiple. <br/>                                                                                                                                                                              |
| [**\_SELITEMRANGEEX lb**](lb-selitemrangeex.md)           | Sélectionne un ou plusieurs éléments consécutifs dans une zone de liste à sélection multiple. <br/>                                                                                                                                                                                           |
| [**\_SETANCHORINDEX lb**](lb-setanchorindex.md)           | Définit l’élément d’ancrage qui est l’élément à partir duquel commence une sélection multiple. Une sélection multiple s’étend sur tous les éléments de l’élément d’ancrage à l’élément du signe insertion.<br/>                                                                                                        |
| [**\_SETCARETINDEX lb**](lb-setcaretindex.md)             | Définit le rectangle de focus sur l’élément à l’index spécifié dans une zone de liste à sélection multiple. Si l’élément n’est pas visible, il fait l’objet d’un défilement dans la vue. <br/>                                                                                                               |
| [**\_SETCOLUMNWIDTH lb**](lb-setcolumnwidth.md)           | Définit la largeur, en pixels, de toutes les colonnes dans une zone de liste à plusieurs colonnes. <br/>                                                                                                                                                                                          |
| [**\_SETCOUNT lb**](lb-setcount.md)                       | Définit le nombre d’éléments dans une zone de liste créée avec le style [**\_ NoData**](list-box-styles.md) et non créé avec le [**style \_ HASSTRINGS**](list-box-styles.md) . <br/>                                                          |
| [**\_SETCURSEL lb**](lb-setcursel.md)                     | Sélectionne une chaîne et la fait défiler en vue, si nécessaire. <br/>                                                                                                                                                                                                          |
| [**\_SETHORIZONTALEXTENT lb**](lb-sethorizontalextent.md) | Définit la largeur, en pixels, à laquelle une zone de liste peut faire défiler horizontalement (la largeur avec défilement). <br/>                                                                                                                                                               |
| [**\_SETITEMDATA lb**](lb-setitemdata.md)                 | Définit une valeur associée à l’élément spécifié dans une zone de liste. <br/>                                                                                                                                                                                            |
| [**\_SETITEMHEIGHT lb**](lb-setitemheight.md)             | Définit la hauteur, en pixels, des éléments d’une zone de liste. <br/>                                                                                                                                                                                                               |
| [**LB \_ SETLOCALE**](lb-setlocale.md)                     | Définit les paramètres régionaux actuels de la zone de liste. <br/>                                                                                                                                                                                                                          |
| [**\_SETSEL lb**](lb-setsel.md)                           | Sélectionne une chaîne dans une zone de liste à sélection multiple. <br/>                                                                                                                                                                                                                |
| [**\_SETTABSTOPS lb**](lb-settabstops.md)                 | Définit les positions des taquets de tabulation dans une zone de liste. <br/>                                                                                                                                                                                                                        |
| [**\_SETTOPINDEX lb**](lb-settopindex.md)                 | Garantit que l’élément spécifié dans une zone de liste est visible. <br/>                                                                                                                                                                                                         |



 

### <a name="notifications"></a>Notifications



| Rubrique                                             | Contenu                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [LBN \_ DBLCLK](lbn-dblclk.md)                     | Indique à l’application que l’utilisateur a double-cliqué sur un élément dans une zone de liste. <br/>                                                                                                                                                                                                                                         |
| [LBN \_ ERRSPACE](lbn-errspace.md)                 | Indique à l’application que la zone de liste ne peut pas allouer suffisamment de mémoire pour répondre à une demande spécifique. <br/>                                                                                                                                                                                                                     |
| [LBN \_ KILLFOCUS](lbn-killfocus.md)               | Indique à l’application que la zone de liste a perdu le focus clavier. <br/>                                                                                                                                                                                                                                                  |
| [LBN \_ SELCANCEL](lbn-selcancel.md)               | Indique à l’application que l’utilisateur a annulé la sélection dans une zone de liste. <br/>                                                                                                                                                                                                                                         |
| [LBN \_ selChange](lbn-selchange.md)               | Indique à l’application que la sélection dans une zone de liste a été modifiée. <br/>                                                                                                                                                                                                                                                   |
| [LBN \_ SetFocus](lbn-setfocus.md)                 | Indique à l’application que la zone de liste a reçu le focus clavier. <br/>                                                                                                                                                                                                                                              |
| [**\_CHARTOITEM WM**](wm-chartoitem.md)           | Envoyé par une zone de liste avec le style [**\_ WANTKEYBOARDINPUT lbs**](list-box-styles.md) à son propriétaire en réponse à un message [**WM \_ char**](/windows/desktop/inputdev/wm-char) . <br/>                                                                                                                                        |
| [**\_CTLCOLORLISTBOX WM**](wm-ctlcolorlistbox.md) | Envoyé à la fenêtre parente d’une zone de liste avant que le système ne dessine la zone de liste. En répondant à ce message, la fenêtre parente peut définir les couleurs de texte et d’arrière-plan de la zone de liste à l’aide du handle de contexte de périphérique d’affichage spécifié. <br/>                                                                              |
| [**WM \_ DELETEITEM**](wm-deleteitem.md)           | Envoyé au propriétaire d’une zone de liste ou d’une zone de liste déroulante lorsque la zone de liste ou la zone de liste déroulante est détruite ou lorsque des éléments sont supprimés par le message [**lb \_ DELETESTRING**](lb-deletestring.md), [**lb \_ RESETCONTENT**](lb-resetcontent.md), [**CB \_ DELETESTRING**](cb-deletestring.md)ou [**CB \_ RESETCONTENT**](cb-resetcontent.md) . <br/> |
| [**\_VKEYTOITEM WM**](wm-vkeytoitem.md)           | Envoyé par une zone de liste avec le style [**\_ WANTKEYBOARDINPUT lbs**](list-box-styles.md) à son propriétaire en réponse à un message « [**WM \_**](/windows/desktop/inputdev/wm-keydown) KeyOut ». <br/>                                                                                                                                  |
| [DL \_ BEGINDRAG](dl-begindrag.md)                 | Avertit la fenêtre parente de la zone de liste de glissement que l’utilisateur a cliqué avec le bouton gauche de la souris sur un élément. <br/>                                                                                                                                                                                                                   |
| [DL \_ CANCELDRAG](dl-canceldrag.md)               | Signale que l’utilisateur a annulé une opération glisser en cliquant sur le bouton droit de la souris ou en appuyant sur la touche ÉCHAP. <br/>                                                                                                                                                                                                          |
| [\_glisser-déplacer](dl-dragging.md)                   | Signale que l’utilisateur a déplacé la souris tout en faisant glisser un élément. <br/>                                                                                                                                                                                                                                                        |
| [DL \_ supprimé](dl-dropped.md)                     | Signale que l’utilisateur a terminé une opération glisser-déplacer en relâchant le bouton gauche de la souris. <br/>                                                                                                                                                                                                                                 |



 

### <a name="structures"></a>Structures



| Rubrique                                        | Contenu                                                                                                                                                               |
|----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DELETEITEMSTRUCT,**](/windows/win32/api/winuser/ns-winuser-deleteitemstruct) | Contient des informations sur un élément de zone de liste ou de zone de liste déroulante supprimé.<br/>                                                                                            |
| [**DRAGLISTINFO**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo)         | Contient des informations sur un événement de glissement. Le pointeur vers [**DRAGLISTINFO**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo) est passé en tant que paramètre *lParam* du message de liste de glissement. <br/> |



 

### <a name="constants"></a>Constantes



| Rubrique                                  | Contenu                                                                |
|----------------------------------------|-------------------------------------------------------------------------|
| [Styles de zone de liste](list-box-styles.md) | Décrit les styles de fenêtre qui définissent un contrôle de zone de liste. <br/> |



 

 

