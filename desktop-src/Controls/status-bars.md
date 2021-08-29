---
title: barres d’état (contrôles de Windows)
description: Une barre d’État est une fenêtre horizontale au bas d’une fenêtre parente dans laquelle une application peut afficher différents types d’informations d’État.
ms.assetid: vs|controls|~\controls\status\status.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc75802c7aa478a8bc02cf67bb8474a4535239261f3b398f564a9ad25a15f96d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119816322"
---
# <a name="status-bars-windows-controls"></a>barres d’état (contrôles de Windows)

Une *barre d’État* est une fenêtre horizontale au bas d’une fenêtre parente dans laquelle une application peut afficher différents types d’informations d’État. La barre d’État peut être divisée en parties pour afficher plusieurs types d’informations. la capture d’écran suivante montre la barre d’état dans l’application Microsoft Windows Paint. Dans ce cas, la barre d’état contient le texte « pour obtenir de l’aide, cliquez sur rubriques d’aide dans le menu aide ». La barre d’État est la zone en bas de la fenêtre qui contient le texte d’aide et des informations de coordonnées.

![capture d’écran de l’application Paint, avec une barre d’État qui contient des indications sur l’aide en ligne](images/sb-paint.png)

Cette section comprend les rubriques suivantes.

-   [Types et styles](#types-and-styles)
-   [Taille et hauteur](#size-and-height)
-   [Barres d’État à plusieurs parties](#multiple-part-status-bars)
-   [Opérations sur le texte de la barre d’État](#status-bar-text-operations)
-   [Barres d’État owner-drawn](#owner-drawn-status-bars)
-   [Barres d’état de mode simple](#simple-mode-status-bars)
-   [Traitement du message de la barre d’État par défaut](#default-status-bar-message-processing)

## <a name="types-and-styles"></a>Types et styles

La position par défaut d’une barre d’État se trouve en bas de la fenêtre parente, mais vous pouvez spécifier le style [**CCS \_ Top**](common-control-styles.md) pour qu’il apparaisse en haut de la zone cliente de la fenêtre parente.

Vous pouvez spécifier le style [**SBARS \_ SIZEGRIP**](status-bar-styles.md) pour inclure une poignée de dimensionnement à l’extrémité droite de la barre d’État.

> [!Note]  
> Il n’est pas recommandé de combiner les styles de [**\_ SIZEGRIP**](status-bar-styles.md) [**CCS \_ Top**](common-control-styles.md) et SBARS, car la poignée de redimensionnement résultante n’est pas fonctionnelle.

 

## <a name="size-and-height"></a>Taille et hauteur

La procédure de fenêtre pour la barre d’État définit automatiquement la taille initiale et la position de la fenêtre, en ignorant les valeurs spécifiées dans la fonction [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) . La largeur est la même que celle de la zone cliente de la fenêtre parente. La hauteur est basée sur les métriques de la police actuellement sélectionnée dans le contexte de périphérique de la barre d’État et sur la largeur des bordures de la fenêtre.

La procédure de fenêtre ajuste automatiquement la taille de la barre d’état chaque fois qu’elle reçoit un message de [**\_ taille WM**](/windows/desktop/winmsg/wm-size) . En règle générale, lorsque la taille de la fenêtre parente change, le parent envoie un message de **\_ taille WM** à la barre d’État.

Une application peut définir la hauteur minimale de la zone de dessin d’une barre d’État en envoyant la fenêtre un message [**SB \_ SETMINHEIGHT**](sb-setminheight.md) , en spécifiant la hauteur minimale, en pixels. La zone de dessin n’inclut pas les bordures de la fenêtre. Une hauteur minimale est utile pour dessiner dans une barre d’État owner-drawn. Pour plus d’informations, consultez [barres d’État owner-drawn](#owner-drawn-status-bars) plus loin dans ce chapitre.

Vous récupérez les largeurs des bordures d’une barre d’État en envoyant la fenêtre à un message [**SB \_ GETBORDERS**](sb-getborders.md) . Le message comprend l’adresse d’un tableau de trois éléments qui reçoit les largeurs.

## <a name="multiple-part-status-bars"></a>Barres d’État Multiple-Part

Une barre d’État peut avoir de nombreuses parties différentes, chacune affichant une ligne de texte différente. Vous divisez une barre d’État en parties en envoyant la fenêtre un message [**SB \_ SETPARTS**](sb-setparts.md) , en spécifiant le nombre de parties à créer et l’adresse d’un tableau d’entiers. Le tableau contient un élément pour chaque partie, et chaque élément spécifie la coordonnée cliente du bord droit d’un composant.

Une barre d’État peut avoir un maximum de 256 parties, bien que les applications en utilisent généralement beaucoup moins. Vous récupérez le nombre de parties dans une barre d’État, ainsi que la coordonnée du bord droit de chaque partie, en envoyant la fenêtre à un message [**SB \_ GETPARTS**](sb-getparts.md) .

## <a name="status-bar-text-operations"></a>Opérations sur le texte de la barre d’État

Vous définissez le texte de n’importe quelle partie d’une barre d’État en envoyant le message [**SB \_ SETTEXT**](sb-settext.md) , en spécifiant l’index de base zéro d’une partie, l’adresse de la chaîne à dessiner dans la partie et la technique de dessin de la chaîne. La technique de dessin détermine si le texte a une bordure et, le cas contraire, le style de la bordure. Elle détermine également si la fenêtre parente est responsable du dessin du texte. Pour plus d’informations, consultez la section [barre d’État owner-drawn Status](#owner-drawn-status-bars) ci-dessous.

Par défaut, le texte est aligné à gauche dans la partie spécifiée d’une barre d’État. Vous pouvez incorporer des caractères de tabulation ( \\ t) dans le texte pour le centrer ou l’aligner à droite. Le texte à droite d’un seul caractère de tabulation est centré et le texte à droite d’un deuxième onglet est aligné à droite.

Pour récupérer du texte à partir d’une barre d’État, utilisez les messages [**SB \_ GETTEXTLENGTH**](sb-gettextlength.md) et [**SB \_ GETTEXT**](sb-gettext.md) .

Si votre application utilise une barre d’État qui n’a qu’une seule partie, vous pouvez utiliser les messages [**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext), [**WM \_ GETTEXT**](/windows/desktop/winmsg/wm-gettext)et [**WM \_ GETTEXTLENGTH**](/windows/desktop/winmsg/wm-gettextlength) pour effectuer des opérations de texte. Ces messages traitent uniquement la partie dont l’index est égal à zéro, ce qui vous permet de traiter la barre d’État comme un contrôle de texte statique.

Pour afficher une ligne d’État sans créer de barre d’État, utilisez la fonction [**DrawStatusText**](/windows/desktop/api/Commctrl/nf-commctrl-drawstatustexta) . La fonction utilise les mêmes techniques pour dessiner l’état que la procédure de fenêtre pour la barre d’État, mais elle ne définit pas automatiquement la taille et la position des informations d’État. Lors de l’appel de la fonction, vous devez spécifier la taille et la position des informations d’État, ainsi que le contexte de périphérique de la fenêtre dans laquelle le dessiner.

## <a name="owner-drawn-status-bars"></a>Barres d’État Owner-Drawn

Vous pouvez définir des parties individuelles d’une barre d’État pour qu’elles soient des parties owner-drawn. L’utilisation de cette technique vous donne plus de contrôle que vous ne le feriez autrement sur l’apparence de la partie de la fenêtre. Par exemple, vous pouvez afficher une image bitmap plutôt que du texte ou dessiner du texte à l’aide d’une police différente.

Pour définir une partie de la fenêtre comme owner-drawn, envoyez le message [**SB \_ SETTEXT**](sb-settext.md) à la barre d’État, en spécifiant la partie et la \_ technique de dessin OwnerDraw SBT. Quand SBT \_ OwnerDraw est spécifié, le paramètre *lParam* est une valeur 32 bits définie par l’application que l’application peut utiliser lors du dessin de la partie. Par exemple, vous pouvez spécifier un handle de police, un descripteur de bitmap, une adresse de chaîne, et ainsi de suite.

Quand une barre d’État doit dessiner un élément owner-drawn, elle envoie le message [**WM \_ DRAWITEM**](wm-drawitem.md) à la fenêtre parente. Le paramètre *wParam* du message est l’identificateur de fenêtre enfant de la barre d’État, et le paramètre *lParam* est l’adresse d’une structure [**drawitemstruct,**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) . La fenêtre parente utilise les informations de la structure pour dessiner le composant. Pour une partie owner-drawn d’une barre d’État, **drawitemstruct,** contient les informations suivantes.



| Membre         | Description                                                                                                            |
|----------------|------------------------------------------------------------------------------------------------------------------------|
| **CtlType**    | Non défini n’utilisez pas.                                                                                                 |
| **CtlID**      | Identificateur de fenêtre enfant de la barre d’État.                                                                             |
| **itemID**     | Index de base zéro du composant à dessiner.                                                                              |
| **itemAction** | Non défini n’utilisez pas.                                                                                                 |
| **itemState**  | Non défini n’utilisez pas.                                                                                                 |
| **hwndItem**   | Handle de la barre d’État.                                                                                              |
| **hDC**        | Handle vers le contexte de périphérique de la barre d’État.                                                                        |
| **rcItem**     | Coordonnées de la partie de la fenêtre à dessiner. Les coordonnées sont exprimées par rapport à l’angle supérieur gauche de la barre d’État.   |
| **DonnéesÉlément**   | Valeur 32 bits définie par l’application, spécifiée dans le paramètre *lParam* du message [**SB \_ SETTEXT**](sb-settext.md) . |



 

## <a name="simple-mode-status-bars"></a>Barres d’état de mode simple

Vous placez une barre d’État en « mode simple » en lui envoyant un message [**SB \_ simple**](sb-simple.md) . Une barre d’état de mode simple n’affiche qu’une seule partie. Lorsque le texte de la fenêtre est défini, la fenêtre est invalidée, mais elle n’est pas redessinée jusqu’à [**la \_ peinture WM**](/windows/desktop/gdi/wm-paint)suivante. En attendant, le message réduit le scintillement de l’écran en réduisant le nombre de rafraîchissements de la fenêtre. Une barre d’état de mode simple est utile pour afficher le texte d’aide pour les éléments de menu pendant que l’utilisateur fait défiler le menu.

La chaîne affichée par une barre d’État en mode simple est conservée séparément des chaînes qu’elle affiche en mode non simple. Cela signifie que vous pouvez placer la fenêtre en mode simple, définir son texte et revenir en mode non simple sans modifier le texte en mode non simple.

Lors de la définition du texte d’une barre d’état de mode simple, vous pouvez spécifier n’importe quelle technique de dessin, à l’exception de SBT \_ OwnerDraw. Une barre d’état de mode simple ne prend pas en charge le dessin owner-drawn.

## <a name="default-status-bar-message-processing"></a>Traitement du message de la barre d’État par défaut

Cette section décrit les messages traités par la procédure de fenêtre pour la classe [**STATUSCLASSNAME**](common-control-window-classes.md) prédéfinie.



| Message               | Traitement par défaut                                                                                                                                                                                                                                                       |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **création de WM \_**        | Initialise la barre d’État.                                                                                                                                                                                                                                              |
| **\_destructeur WM**       | Libère les ressources allouées pour la barre d’État.                                                                                                                                                                                                                            |
| **WM \_ GETFONT**       | Retourne le handle de la police actuelle dans laquelle la barre d’État dessine le texte.                                                                                                                                                                                         |
| **WM \_ GETTEXT**       | Copie le texte de la première partie d’une barre d’État dans une mémoire tampon. Elle retourne une valeur 32 bits qui spécifie la longueur, en caractères, du texte et de la technique utilisée pour dessiner le texte.                                                                                |
| **\_GETTEXTLENGTH WM** | Retourne une valeur 32 bits qui spécifie la longueur, en caractères, du texte de la première partie d’une barre d’État et de la technique utilisée pour dessiner le texte.                                                                                                                  |
| **\_NCHITTEST WM**     | Retourne la valeur HTBOTTOMRIGHT si le curseur de la souris se trouve dans la poignée de redimensionnement, ce qui amène le système à afficher le curseur de dimensionnement. Si le curseur de la souris ne se trouve pas dans la poignée de redimensionnement, la barre d’état transmet ce message à la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) . |
| **\_peinture WM**         | Peint la région non valide de la barre d’État. Si le paramètre *wParam* est non **null**, le contrôle suppose que la valeur est un HDC et peint à l’aide de ce contexte de périphérique.                                                                                               |
| **\_SetFont WM**       | Sélectionne la poignée de police dans le contexte de périphérique pour la barre d’État.                                                                                                                                                                                                      |
| **WM, \_ SETTEXT**       | Copie le texte spécifié dans la première partie d’une barre d’État, à l’aide de l’opération de dessin par défaut (spécifiée comme zéro). Elle retourne **true** en cas de réussite, ou **false** dans le cas contraire.                                                                                       |
| **taille du WM \_**          | Redimensionne la barre d’État en fonction de la largeur actuelle de la zone cliente de la fenêtre parente et de la hauteur de la police actuelle de la barre d’État.                                                                                                                               |



 

 

 
