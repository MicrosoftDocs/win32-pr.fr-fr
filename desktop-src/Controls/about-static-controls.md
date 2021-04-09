---
title: À propos des contrôles statiques
description: Cette rubrique explique comment les contrôles statiques sont utilisés.
ms.assetid: 155904e1-a963-496d-9b22-6e95ed0ebd47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 064c1814b4f4ed6283b2fe22af06aed107e2c4d2
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103941407"
---
# <a name="about-static-controls"></a>À propos des contrôles statiques

Les applications utilisent souvent des contrôles statiques pour étiqueter d’autres contrôles ou pour séparer un groupe de contrôles. Bien que les contrôles statiques soient des fenêtres enfants, ils ne peuvent pas être sélectionnés. Par conséquent, ils ne peuvent pas recevoir le focus clavier et ne peuvent pas avoir d’interface clavier. Un contrôle statique avec le style de \_ notification SS reçoit l’entrée de la souris, en avertissant la fenêtre parente quand l’utilisateur clique ou double-clique sur le contrôle. Les contrôles statiques appartiennent à la classe de fenêtre statique.

Bien que les contrôles statiques puissent être utilisés dans les fenêtres superposées, indépendantes et enfants, ils sont conçus pour être utilisés dans les boîtes de dialogue, où le système normalise leur comportement. En utilisant des contrôles statiques en dehors des boîtes de dialogue, un développeur augmente le risque que l’application se comporte de manière non standard. En général, un développeur utilise des contrôles statiques dans les boîtes de dialogue ou utilise le \_ style SS OwnerDraw pour créer des contrôles statiques personnalisés.

Les rubriques suivantes sont présentées dans cette section.

-   [Types de contrôles statiques](#static-control-types)
    -   [Contrôle statique Graphics simple](#simple-graphics-static-control)
    -   [Contrôle statique de texte](#text-static-control)
    -   [Contrôle image statique](#image-static-control)
    -   [Contrôle statique owner-drawn](#owner-drawn-static-control)
-   [Traitement des messages par défaut du contrôle statique](#static-control-default-message-processing)

## <a name="static-control-types"></a>Types de contrôles statiques

Il existe quatre types de contrôles statiques. Chaque type a un ou plusieurs [styles de contrôle statiques](static-control-styles.md).

-   [Contrôle statique Graphics simple](#simple-graphics-static-control)
-   [Contrôle statique de texte](#text-static-control)
-   [Contrôle image statique](#image-static-control)
-   [Contrôle statique owner-drawn](#owner-drawn-static-control)

### <a name="simple-graphics-static-control"></a>Contrôle statique Graphics simple

Un contrôle Graphical static simple affiche un frame ou un rectangle rempli. Un frame peut être dessiné dans plusieurs styles, y compris en noir, en gris ou blanc. En outre, un frame peut être dessiné avec un style gravé pour lui attribuer une apparence en trois dimensions. Les styles de frame incluent SS \_ BLACKFRAME, SS \_ GRAYFRAME, SS \_ WHITEFRAME, SS \_ ETCHEDHORZ, SS \_ ETCHEDVERT et SS \_ ETCHEDFRAME.

Un rectangle peut être rempli avec une couleur dans l’un des trois styles suivants : noir, gris ou blanc. Ces styles sont définis par les constantes SS \_ BLACKRECT, SS \_ GRAYRECT et SS \_ WHITERECT.

Les styles graphiques ne peuvent pas être combinés.

### <a name="text-static-control"></a>Contrôle statique de texte

Un contrôle statique de texte affiche le texte dans un rectangle dans l’un des cinq styles suivants :

-   aligné à gauche sans retour automatique à la ligne
-   aligné à gauche avec le retour automatique à la ligne
-   centrée
-   alignée à droite
-   simple

Ces styles sont définis par les constantes SS \_ LEFTNOWORDWRAP, SS \_ Left, SS \_ Center, SS \_ Right et SS \_ simple, respectivement. Le système réorganise le texte de ces contrôles de manière prédéfinie, à l’exception du texte « simple », qui n’est pas réorganisé.

Une application peut modifier le texte d’un contrôle statique de texte à tout moment à l’aide de la fonction [**SetWindowText**](/windows/desktop/api/winuser/nf-winuser-setwindowtexta) ou du message [**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext) .

Le système affiche autant de texte que possible dans le contrôle statique et découpe tout ce qui n’est pas adapté. Pour calculer une taille appropriée pour le contrôle, récupérez les métriques de police pour le texte. Pour plus d’informations sur les polices et les métriques de police, consultez [polices et texte](/windows/desktop/gdi/fonts-and-text).

Par défaut, le texte de la fenêtre pour un contrôle statique, comme pour d’autres contrôles, peut contenir une esperluette qui définit le caractère suivant comme touche de raccourci pour le contrôle (ou, dans le cas de la plupart des contrôles statiques, pour le contrôle qu’il étiquette, qui est le contrôle suivant dans l’ordre de tabulation). Si vous souhaitez afficher les caractères & dans le texte plutôt que de les utiliser pour définir des raccourcis, incluez le \_ style SS NoPrefix.

### <a name="image-static-control"></a>Contrôle image statique

Un contrôle statique d’image peut afficher des bitmaps, des icônes (y compris des icônes animées) ou des reformateurs améliorés. Le type de graphique qu’un contrôle statique particulier affiche dépend du style du contrôle : SS \_ bitmap, SS \_ Icon ou SS \_ ENHMETAFILE. Une application spécifie le style lorsqu’elle crée le contrôle et spécifie également un handle vers l’image bitmap, l’icône ou le métafichier à afficher pour le contrôle. Une fois le contrôle créé, une application peut associer un autre graphique au contrôle en lui envoyant un message [**STM \_ SETIMAGE**](stm-setimage.md) , en spécifiant un handle vers le nouvel objet graphique. Une application peut récupérer un handle vers l’objet graphique actuellement associé à un contrôle statique en lui envoyant un message [**STM \_ GETIMAGE**](stm-getimage.md) . Une application envoie des messages à un contrôle statique à l’aide de la fonction [**SendDlgItemMessage**](/windows/desktop/api/winuser/nf-winuser-senddlgitemmessagea) .

### <a name="owner-drawn-static-control"></a>Contrôle statique Owner-Drawn

En utilisant le \_ style SS OwnerDraw, une application peut assumer la responsabilité de la peinture d’un contrôle statique. La fenêtre parente d’un contrôle statique owner-drawn (son propriétaire) reçoit un message [**WM \_ DRAWITEM**](wm-drawitem.md) chaque fois que le contrôle statique doit être peint. Le message inclut un pointeur vers une structure [**drawitemstruct,**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) qui contient des informations que la fenêtre propriétaire utilise lors du dessin du contrôle.

## <a name="static-control-default-message-processing"></a>Traitement des messages par défaut du contrôle statique

La procédure de fenêtre pour la classe de fenêtre de contrôle statique prédéfinie effectue le traitement par défaut pour tous les messages que la procédure de contrôle statique ne traite pas. Lorsque le contrôle statique retourne la **valeur false** pour un message, la procédure de fenêtre prédéfinie vérifie les messages et effectue l’action par défaut décrite dans le tableau suivant. Dans le tableau, un contrôle de texte statique est un contrôle statique avec le style SS \_ LEFTNOWORDWRAP, SS \_ Left, SS \_ Center, SS \_ Right ou SS \_ simple.



| Message                                                | Action par défaut                                                                                                                              |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [**création de WM \_**](/windows/desktop/winmsg/wm-create)                     | Charge l’objet graphique et dimensionne la fenêtre à la taille de l’objet, pour les contrôles statiques graphiques. N’effectue aucune action pour d’autres contrôles statiques. |
| [**\_destructeur WM**](/windows/desktop/winmsg/wm-destroy)                   | Libère et détruit tout objet graphique pour les contrôles statiques graphiques. N’effectue aucune action pour d’autres contrôles statiques.                              |
| [**\_activer WM**](/windows/desktop/winmsg/wm-enable)                     | Repeint les contrôles statiques visibles.                                                                                                           |
| [**\_ERASEBKGND WM**](/windows/desktop/winmsg/wm-erasebkgnd)             | Retourne la **valeur true**, indiquant que le contrôle efface l’arrière-plan.                                                                             |
| [**\_GETDLGCODE WM**](/windows/desktop/dlgbox/wm-getdlgcode)             | Retourne DLGC \_ statique.                                                                                                                       |
| [**WM \_ GETFONT**](/windows/desktop/winmsg/wm-getfont)                   | Retourne un handle vers la police pour les contrôles statiques de texte.                                                                                      |
| [**WM \_ GETTEXT**](/windows/desktop/winmsg/wm-gettext)                   | Retourne le nombre de caractères copiés.                                                                                                    |
| [**\_GETTEXTLENGTH WM**](/windows/desktop/winmsg/wm-gettextlength)       | Retourne la longueur, en caractères, du texte d’un contrôle statique de texte.                                                                   |
| [**\_LBUTTONDBLCLK WM**](/windows/desktop/inputdev/wm-lbuttondblclk)     | Envoie à la fenêtre parente un code de notification [STN \_ DBLCLK](stn-dblclk.md) si le style de contrôle est SS \_ Notify.                              |
| [**\_LBUTTONDOWN WM**](/windows/desktop/inputdev/wm-lbuttondown)         | Envoie à la fenêtre parente un code de notification de [ \_ clic sur un STN](stn-clicked.md) si le style de contrôle est SS \_ Notify.                            |
| [**\_NCLBUTTONDBLCLK WM**](/windows/desktop/inputdev/wm-nclbuttondblclk) | Envoie à la fenêtre parente un code de notification [STN \_ DBLCLK](stn-dblclk.md) si le style de contrôle est SS \_ Notify.                              |
| [**\_NCLBUTTONDOWN WM**](/windows/desktop/inputdev/wm-nclbuttondown)     | Envoie à la fenêtre parente un code de notification de [ \_ clic sur un STN](stn-clicked.md) si le style de contrôle est SS \_ Notify.                            |
| [**\_NCHITTEST WM**](/windows/desktop/inputdev/wm-nchittest)             | Retourne HTCLIENT si le style de contrôle a la valeur SS \_ Notify ; sinon, retourne HTTRANSPARENT.                                                      |
| [**\_peinture WM**](/windows/desktop/gdi/wm-paint)                          | Repeint le contrôle.                                                                                                                       |
| [**\_SetFont WM**](/windows/desktop/winmsg/wm-setfont)                   | Définit la police et repeint les contrôles statiques de texte.                                                                                        |
| [**WM, \_ SETTEXT**](/windows/desktop/winmsg/wm-settext)                   | Définit le texte et repeint les contrôles statiques de texte.                                                                                        |



 

La procédure de fenêtre prédéfinie transmet tous les autres messages à [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) pour le traitement par défaut.

 

 