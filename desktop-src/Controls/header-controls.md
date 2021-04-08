---
title: À propos des contrôles Header
description: Un contrôle header est une fenêtre qui est généralement positionnée au-dessus de colonnes de texte ou de nombres. Elle contient un titre pour chaque colonne et peut être divisée en plusieurs parties.
ms.assetid: b464fb9a-e342-4209-ba6f-15b5388f3914
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6d9beaa9dc3bd8eb94d749ec271902a480b853e
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730404"
---
# <a name="about-header-controls"></a>À propos des contrôles Header

Un contrôle header est une fenêtre qui est généralement positionnée au-dessus de colonnes de texte ou de nombres. Elle contient un titre pour chaque colonne et peut être divisée en plusieurs parties. L’utilisateur peut faire glisser les séparateurs qui séparent les parties pour définir la largeur de chaque colonne. L’illustration suivante montre un contrôle header qui contient des colonnes étiquetées qui fournissent des informations détaillées sur les fichiers d’un répertoire.

![capture d’écran d’une boîte de dialogue avec un contrôle d’en-tête à trois colonnes](images/header.png)

Vous pouvez créer un contrôle header à l’aide de la fonction [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , en spécifiant la classe de fenêtre d' [**\_ en-tête WC**](common-control-window-classes.md) et les [styles de contrôle d’en-tête](header-control-styles.md)appropriés. Cette classe de fenêtre est inscrite lors du chargement de la DLL de contrôles communs. Pour vous assurer que cette DLL est chargée, utilisez la fonction [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) . Après avoir créé un contrôle header, vous pouvez le diviser en parties, définir le texte de chaque partie et contrôler l’apparence de la fenêtre à l’aide de messages de fenêtre d’en-tête.

Un contrôle header peut être créé en tant que fenêtre enfant d’un autre contrôle, tel qu’une zone de liste. Toutefois, le contrôle parent n’est pas informé du contrôle header et n’autorise pas l’espace occupé par l’en-tête, avec pour résultat que les éléments de liste apparaîtront derrière l’en-tête. Si vous souhaitez utiliser un contrôle header dans une zone de liste ou un autre contrôle, le contrôle parent doit être owner-drawn afin que tous les éléments s’affichent dans la position correcte.

Les contrôles d’affichage de liste ont déjà des contrôles Header. Au lieu de créer un contrôle d’en-tête pour un contrôle List-View, vous utilisez [**LVM \_ GETHEADER**](lvm-getheader.md) ou [**ListView \_ GETHEADER**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getheader) pour récupérer le contrôle existant.

-   [Taille et position de contrôle d’en-tête](#header-control-size-and-position)
-   [Éléments](#items)
-   [Contrôles Header owner-drawn](#owner-drawn-header-controls)
-   [Filtres de contrôle d’en-tête](#header-control-filters)
-   [Traitement par défaut des messages de contrôle d’en-tête](#default-header-control-message-processing)

## <a name="header-control-size-and-position"></a>Taille et position de contrôle d’en-tête

En général, vous devez définir la taille et la position d’un contrôle d’en-tête pour qu’il s’ajuste aux limites d’un rectangle particulier, par exemple la zone cliente d’une fenêtre. À l’aide du message de [**\_ disposition HDM**](hdm-layout.md) , vous pouvez récupérer les valeurs de taille et de position appropriées à partir du contrôle header.

Lors de l’envoi de la [**\_ disposition HDM**](hdm-layout.md), vous spécifiez l’adresse d’une structure [**HDLAYOUT**](/windows/win32/api/commctrl/ns-commctrl-hdlayout) qui contient les coordonnées du rectangle que le contrôle header doit occuper et fournit un pointeur vers une structure [**WINDOWPOS**](/windows/win32/api/winuser/ns-winuser-windowpos) . Le contrôle remplit la structure **WINDOWPOS** avec les valeurs de taille et de position appropriées pour positionner le contrôle le long du bord supérieur du rectangle spécifié. La valeur de hauteur est la somme des hauteurs des bordures horizontales du contrôle et de la hauteur moyenne des caractères de la police actuellement sélectionnée dans le contexte de périphérique du contrôle.

Si vous souhaitez utiliser la [**\_ disposition HDM**](hdm-layout.md) pour définir la taille initiale et la position d’un contrôle header, définissez l’état de visibilité initial du contrôle afin qu’il soit masqué. Après avoir envoyé la **\_ disposition HDM** pour récupérer les valeurs de taille et de position, vous pouvez utiliser la fonction [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) pour définir la nouvelle taille, la position et l’état de visibilité.

## <a name="items"></a>Éléments

Un contrôle header contient généralement plusieurs éléments d’en-tête qui définissent les colonnes du contrôle. Vous ajoutez un élément à un contrôle header en envoyant le message [**HDM \_ INSERTITEM**](hdm-insertitem.md) au contrôle. Le message comprend l’adresse d’une structure [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) . Cette structure définit les propriétés de l’élément d’en-tête, qui peut inclure une chaîne, une image bitmap, une taille initiale et une valeur **lParam** définie par l’application.

Le membre **fmt** de la structure [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) d’un élément peut inclure la **\_ chaîne HDF** ou l’indicateur de **\_ bitmap HDF** pour indiquer si le contrôle affiche la chaîne ou l’image bitmap de l’élément. Si vous souhaitez afficher à la fois une chaîne et une bitmap, créez un élément owner-drawn en définissant le membre **fmt** de façon à inclure l’indicateur **\_ OwnerDraw HDF** . La structure **HDITEM** spécifie également les indicateurs de mise en forme qui indiquent au contrôle s’il faut centrer, aligner à gauche ou aligner à droite la chaîne ou l’image bitmap dans le rectangle de l’élément.

[**HDM \_ INSERTITEM**](hdm-insertitem.md) retourne l’index de l’élément qui vient d’être ajouté. Vous pouvez utiliser l’index dans d’autres messages pour définir des propriétés ou récupérer des informations sur l’élément. Vous pouvez supprimer un élément à l’aide du message [**HDM \_ DELETEITEM**](hdm-deleteitem.md) , en spécifiant l’index de l’élément à supprimer.

Vous pouvez utiliser le message [**HDM \_ SETITEM**](hdm-setitem.md) pour définir les propriétés d’un élément d’en-tête existant et le message [**HDM \_ GETITEM**](hdm-getitem.md) pour récupérer les propriétés actuelles d’un élément. Pour récupérer le nombre d’éléments dans un contrôle header, utilisez le message [**HDM \_ GETITEMCOUNT**](hdm-getitemcount.md) .

## <a name="owner-drawn-header-controls"></a>Contrôles d’en-tête Owner-Drawn

Vous pouvez définir des éléments individuels d’un contrôle header en tant qu’éléments owner-drawn. L’utilisation de cette technique vous donne plus de contrôle que vous ne le feriez avec l’apparence d’un élément d’en-tête.

Vous pouvez utiliser le message [**HDM \_ INSERTITEM**](hdm-insertitem.md) pour insérer un nouvel élément owner-drawn dans un contrôle header ou le message [**HDM \_ SETITEM**](hdm-setitem.md) pour remplacer un élément existant par un élément owner-drawn. Les deux messages incluent l’adresse d’une structure [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) , qui doit avoir le membre **fmt** défini sur la valeur **\_ OwnerDraw HDF** .

Lorsqu’un contrôle header doit dessiner un élément owner-drawn, il envoie le message [**WM \_ DRAWITEM**](wm-drawitem.md) à la fenêtre parente. Le paramètre *wParam* du message est l’identificateur de fenêtre enfant du contrôle header et le paramètre *lParam* est l’adresse d’une structure [**drawitemstruct,**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) . La fenêtre parente utilise les informations de la structure pour dessiner l’élément. Pour un élément owner-drawn dans un contrôle header, la structure **drawitemstruct,** contient les informations suivantes.



| Membre         | Description                                                                                                                                            |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CtlType**    | [**ODT \_**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) Type de contrôle owner-drawn de l’en-tête.                                                                                        |
| **CtlID**      | Identificateur de la fenêtre enfant du contrôle header.                                                                                                         |
| **itemID**     | Index de l’élément à dessiner.                                                                                                                         |
| **itemAction** | [**Oda \_ DRAWENTIRE**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) Drawing-indicateur d’action.                                                                                         |
| **itemState**  | [**ODS \_ Dessin sélectionné**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) -indicateur d’action si le curseur se trouve sur l’élément et que le bouton de la souris est enfoncé. Dans le cas contraire, ce membre est égal à zéro. |
| **hwndItem**   | Handle du contrôle d’en-tête.                                                                                                                          |
| **hDC**        | Handle vers le contexte de périphérique du contrôle header.                                                                                                    |
| **rcItem**     | Coordonnées de l’élément d’en-tête à dessiner. Les coordonnées sont relatives au coin supérieur gauche du contrôle header.                               |
| **DonnéesÉlément**   | Valeur 32 bits définie par l’application et associée à l’élément.                                                                                             |



 

## <a name="header-control-filters"></a>Filtres de contrôle d’en-tête

En spécifiant le style de fenêtre [**HDS \_ FILTERBAR**](header-control-styles.md) pour un contrôle d’en-tête, vous pouvez activer le positionnement des zones d’édition de filtre sous les en-têtes de colonne. Un bouton de filtre s’affiche à côté de la zone d’édition. Vous pouvez implémenter le filtrage en répondant aux codes de notification [HDN \_ BEGINFILTEREDIT](hdn-beginfilteredit.md), [HDN \_ ENDFILTEREDIT](hdn-endfilteredit.md), [HDN \_ FILTERBTNCLICK](hdn-filterbtnclick.md)ou [HDN \_ ](hdn-filterchange.md) FILTERCHANGE.

Par défaut, la zone d’édition contient une invite demandant à l’utilisateur d’entrer du texte. Vous pouvez restaurer la zone d’édition à cet État par défaut en utilisant l' [**en-tête \_ ClearFilter**](/windows/desktop/api/Commctrl/nf-commctrl-header_clearfilter) ou l' [**en-tête \_ ClearAllFilters**](/windows/desktop/api/Commctrl/nf-commctrl-header_clearallfilters).

L’exemple de code suivant montre comment récupérer le contrôle header d’un contrôle List View et comment ajouter une barre de filtre.


```
// hList is the HWND of the list-view control.
HWND hHeader = ListView_GetHeader(hList);
LONG_PTR styles = GetWindowLongPtr(hHeader, GWL_STYLE);
SetWindowLongPtr(g_hHeader, GWL_STYLE, styles | HDS_FILTERBAR);
```



## <a name="default-header-control-message-processing"></a>Traitement par défaut des messages de contrôle d’en-tête

Cette section décrit les messages de fenêtre gérés par la procédure de fenêtre pour la classe de fenêtre d' [**\_ en-tête WC**](common-control-window-classes.md) .



| Message                                            | Traitement effectué                                                                                                                                                                                                                                                                                          |
|----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**création de WM \_**](/windows/desktop/winmsg/wm-create)                 | Initialise le contrôle header.                                                                                                                                                                                                                                                                               |
| [**\_destructeur WM**](/windows/desktop/winmsg/wm-destroy)               | Réinitialise le contrôle header.                                                                                                                                                                                                                                                                             |
| [**\_ERASEBKGND WM**](/windows/desktop/winmsg/wm-erasebkgnd)         | Remplit l’arrière-plan du contrôle d’en-tête à l’aide de la couleur d’arrière-plan actuelle du contrôle.                                                                                                                                                                                                                      |
| [**\_GETDLGCODE WM**](/windows/desktop/dlgbox/wm-getdlgcode)         | Retourne une combinaison des valeurs [**DLGC \_ WANTTAB**](/windows/desktop/dlgbox/wm-getdlgcode) et [**DLGC \_ WANTARROWS**](/windows/desktop/dlgbox/wm-getdlgcode) .                                                                                                                     |
| [**WM \_ GETFONT**](/windows/desktop/winmsg/wm-getfont)               | Retourne le handle de la police actuelle, qui est utilisé par le contrôle header pour dessiner son texte.                                                                                                                                                                                                                 |
| [**\_LBUTTONDBLCLK WM**](/windows/desktop/inputdev/wm-lbuttondblclk) | Capture l’entrée de la souris. Si le curseur de la souris se trouve sur un séparateur, le contrôle envoie le code de notification [HDN \_ BEGINTRACK](hdn-begintrack.md) et commence à faire glisser le séparateur. Si le curseur se trouve sur un élément, l’élément est affiché dans un état appuyé.                                                            |
| [**\_LBUTTONDOWN WM**](/windows/desktop/inputdev/wm-lbuttondown)     | Identique au message [**WM \_ LBUTTONDBLCLK**](/windows/desktop/inputdev/wm-lbuttondblclk) .                                                                                                                                                                                                                                       |
| [**\_LBUTTONUP WM**](/windows/desktop/inputdev/wm-lbuttonup)         | Libère la capture de la souris. Si le contrôle effectuait le suivi du mouvement de la souris, il envoie le code de notification [HDN \_ ENDTRACK](hdn-endtrack.md) et redessine le contrôle d’en-tête. Sinon, le contrôle envoie le code de notification [HDN \_ ITEMCLICK](hdn-itemclick.md) et redessine l’élément d’en-tête sur lequel l’utilisateur a cliqué. |
| [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove)         | Si un séparateur est glissé, le contrôle envoie le code de notification de [ \_ piste HDN](hdn-track.md) et affiche l’élément à la nouvelle position. Si le bouton gauche de la souris est enfoncé et que le curseur se trouve sur un élément, l’élément est affiché dans un état appuyé.                                                      |
| [**\_NCCREATE WM**](/windows/desktop/winmsg/wm-nccreate)             | Alloue et Initialise une structure de données interne.                                                                                                                                                                                                                                                         |
| [**\_NCDESTROY WM**](/windows/desktop/winmsg/wm-ncdestroy)           | Libère les ressources allouées par le contrôle header après que le contrôle header n’a pas été initialisé.                                                                                                                                                                                                                |
| [**\_peinture WM**](/windows/desktop/gdi/wm-paint)                      | Peint la région non valide du contrôle header. Si le paramètre *wParam* est non null, le contrôle suppose que la valeur est un HDC et peint à l’aide de ce contexte de périphérique.                                                                                                                                    |
| [**\_SETCURSOR WM**](/windows/desktop/menurc/wm-setcursor)           | Définit la forme du curseur, selon que le curseur se trouve sur un séparateur ou dans un élément d’en-tête.                                                                                                                                                                                                                   |
| [**\_SetFont WM**](/windows/desktop/winmsg/wm-setfont)               | Sélectionne un nouveau handle de police dans le contexte de périphérique pour le contrôle d’en-tête.                                                                                                                                                                                                                                     |



 

 

 