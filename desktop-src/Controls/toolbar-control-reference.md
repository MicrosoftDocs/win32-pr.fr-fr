---
title: Barre d’outils
description: Cette section contient des informations sur les éléments de programmation utilisés avec les contrôles ToolBar.
ms.assetid: vs|controls|~\controls\toolbar\reflist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a22fd1b51ea1fab45061125654029951f4557472fab62847773e559647e12272
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118166497"
---
# <a name="toolbar"></a>Barre d’outils

Cette section contient des informations sur les éléments de programmation utilisés avec les contrôles ToolBar.

### <a name="overviews"></a>Vues d'ensemble



| Rubrique                                                   | Contenu                                                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [À propos des contrôles ToolBar](toolbar-controls-overview.md) | Une barre d’outils est un contrôle qui contient un ou plusieurs boutons. Chaque bouton, lorsque l’utilisateur clique sur un utilisateur, envoie un message de commande à la fenêtre parente. En règle générale, les boutons d’une barre d’outils correspondent aux éléments du menu de l’application, ce qui offre un moyen supplémentaire et plus direct à l’utilisateur d’accéder aux commandes d’une application.<br/> |
| [Utilisation des contrôles ToolBar](using-toolbar-controls.md)    | Cette rubrique contient des détails d’implémentation et un exemple de code pour l’utilisation de contrôles ToolBar dans vos applications.<br/>                                                                                                                                                                                                                  |



 

### <a name="functions"></a>Fonctions



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Rubrique</th>
<th>Contenu</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-createmappedbitmap"><strong>CreateMappedBitmap</strong></a></td>
<td>Crée une bitmap à utiliser dans une barre d’outils. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex"><strong>CreateToolbarEx</strong></a></td>
<td>Crée une fenêtre de barre d’outils et ajoute les boutons spécifiés à la barre d’outils.
<blockquote>
[!Note]<br />
Cette fonction est déconseillée, car elle ne prend pas en charge toutes les fonctionnalités des barres d’outils. Utilisez à la place <a href="/windows/desktop/api/winuser/nf-winuser-createwindowexa"><strong>CreateWindowEx</strong></a> . Pour obtenir des exemples, consultez <a href="using-toolbar-controls.md">utilisation de contrôles ToolBar</a>.
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

### <a name="messages"></a>Messages



| Rubrique                                                         | Contenu                                                                                                                                                                                                |
|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**TO \_ ADDBITMAP**](tb-addbitmap.md)                         | Ajoute une ou plusieurs images à la liste des images de bouton disponibles pour une barre d’outils. <br/>                                                                                                               |
| [**TO \_ ADDBUTTONS**](tb-addbuttons.md)                       | Ajoute un ou plusieurs boutons à une barre d’outils.<br/>                                                                                                                                                       |
| [**TO \_ ADDSTRING**](tb-addstring.md)                         | Ajoute une nouvelle chaîne au pool de chaînes de la barre d’outils.<br/>                                                                                                                                              |
| [**\_REdimensionnement automatique to**](tb-autosize.md)                           | Entraîne le redimensionnement d’une barre d’outils. <br/>                                                                                                                                                             |
| [**TO \_ BUTTONCOUNT**](tb-buttoncount.md)                     | Récupère le nombre de boutons actuellement dans la barre d’outils. <br/>                                                                                                                                  |
| [**TO \_ BUTTONSTRUCTSIZE**](tb-buttonstructsize.md)           | Spécifie la taille de la structure [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) . <br/>                                                                                                                           |
| [**TO \_ CHANGEBITMAP**](tb-changebitmap.md)                   | Modifie l’image bitmap d’un bouton dans une barre d’outils.<br/>                                                                                                                                                |
| [**TO \_ CHECKBUTTON**](tb-checkbutton.md)                     | Vérifie ou décoche un bouton donné dans une barre d’outils.<br/>                                                                                                                                              |
| [**TO \_ COMMANDTOINDEX**](tb-commandtoindex.md)               | Récupère l’index de base zéro pour le bouton associé à l’identificateur de commande spécifié. <br/>                                                                                             |
| [**\_personnalisation to**](tb-customize.md)                         | Affiche la boîte de dialogue **personnaliser la barre d’outils** .<br/>                                                                                                                                               |
| [**TO \_ DELETEBUTTON**](tb-deletebutton.md)                   | Supprime un bouton de la barre d’outils. <br/>                                                                                                                                                          |
| [**TO \_ ENABLEBUTTON**](tb-enablebutton.md)                   | Active ou désactive le bouton spécifié dans une barre d’outils.<br/>                                                                                                                                       |
| [**TO \_ GETANCHORHIGHLIGHT**](tb-getanchorhighlight.md)       | Récupère le paramètre de surbrillance d’ancrage d’une barre d’outils. <br/>                                                                                                                                       |
| [**TO \_ GETBITMAP**](tb-getbitmap.md)                         | Récupère l’index de l’image bitmap associée à un bouton dans une barre d’outils. <br/>                                                                                                                    |
| [**TO \_ GETBITMAPFLAGS**](tb-getbitmapflags.md)               | Récupère les indicateurs qui décrivent le type de bitmap à utiliser.<br/>                                                                                                                             |
| [**TO \_ GETBUTTON**](tb-getbutton.md)                         | Récupère des informations sur le bouton spécifié dans une barre d’outils.<br/>                                                                                                                               |
| [**TO \_ GETBUTTONINFO**](tb-getbuttoninfo.md)                 | Récupère des informations étendues pour un bouton dans une barre d’outils. <br/>                                                                                                                                   |
| [**TO \_ GETBUTTONSIZE**](tb-getbuttonsize.md)                 | Récupère la largeur et la hauteur actuelles des boutons de la barre d’outils, en pixels. <br/>                                                                                                                       |
| [**TO \_ GETBUTTONTEXT**](tb-getbuttontext.md)                 | Récupère le texte d’affichage d’un bouton dans une barre d’outils.<br/>                                                                                                                                         |
| [**TO \_ GETCOLORSCHEME**](tb-getcolorscheme.md)               | Récupère les informations de modèle de couleur à partir du contrôle ToolBar. <br/>                                                                                                                            |
| [**TO \_ GETDISABLEDIMAGELIST**](tb-getdisabledimagelist.md)   | Récupère la liste d’images utilisée par un contrôle de barre d’outils pour afficher les boutons inactifs. <br/>                                                                                                           |
| [**TO \_ GETEXTENDEDSTYLE**](tb-getextendedstyle.md)           | Récupère les styles étendus pour un contrôle ToolBar. <br/>                                                                                                                                        |
| [**TO \_ GETHOTIMAGELIST**](tb-gethotimagelist.md)             | Récupère la liste d’images utilisée par un contrôle de barre d’outils pour afficher les boutons actifs.<br/>                                                                                                                 |
| [**TO \_ GETHOTITEM**](tb-gethotitem.md)                       | Récupère l’index de l’élément réactif dans une barre d’outils. <br/>                                                                                                                                           |
| [**TO \_ GETIDEALSIZE**](tb-getidealsize.md)                   | Obtient la taille idéale de la barre d’outils.<br/>                                                                                                                                                          |
| [**TO \_ GETIMAGELIST**](tb-getimagelist.md)                   | Récupère la liste d’images utilisée par un contrôle de barre d’outils pour afficher les boutons dans leur état par défaut. Un contrôle ToolBar utilise cette liste d’images pour afficher les boutons lorsqu’ils ne sont pas à chaud ou désactivés.<br/> |
| [**TO \_ GETIMAGELISTCOUNT**](tb-getimagelistcount.md)         | Obtient le nombre de listes d’images associées à la barre d’outils.<br/>                                                                                                                                  |
| [**TO \_ GETINSERTMARK**](tb-getinsertmark.md)                 | Récupère la marque d’insertion actuelle pour la barre d’outils. <br/>                                                                                                                                       |
| [**TO \_ GETINSERTMARKCOLOR**](tb-getinsertmarkcolor.md)       | Récupère la couleur utilisée pour dessiner la marque d’insertion pour la barre d’outils. <br/>                                                                                                                        |
| [**TO \_ GETITEMDROPDOWNRECT**](tb-getitemdropdownrect.md)     | Obtient le rectangle englobant de la fenêtre déroulante pour un élément de barre d’outils avec une [**\_ liste déroulante BTNS**](toolbar-control-and-button-styles.md)style.<br/>                                  |
| [**TO \_ GETITEMRECT**](tb-getitemrect.md)                     | Récupère le rectangle englobant d’un bouton dans une barre d’outils. <br/>                                                                                                                                  |
| [**TO \_ GETMAXSIZE**](tb-getmaxsize.md)                       | Récupère la taille totale de tous les boutons et séparateurs visibles dans la barre d’outils. <br/>                                                                                                       |
| [**TO \_ GETMETRICS**](tb-getmetrics.md)                       | Récupère les métriques d’un contrôle ToolBar.<br/>                                                                                                                                                  |
| [**TO \_ GETOBJECT**](tb-getobject.md)                         | Récupère le [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) pour un contrôle ToolBar. <br/>                                                                                                                     |
| [**TO \_ GETPADDING**](tb-getpadding.md)                       | Récupère le remplissage pour un contrôle de barre d’outils. <br/>                                                                                                                                                |
| [**TO \_ GETPRESSEDIMAGELIST**](tb-getpressedimagelist.md)     | Obtient la liste d’images utilisée par un contrôle de barre d’outils pour afficher les boutons dans un état appuyé.<br/>                                                                                                       |
| [**TO \_ GETRECT**](tb-getrect.md)                             | Récupère le rectangle englobant d’un bouton de barre d’outils spécifié. <br/>                                                                                                                            |
| [**TO \_ GETROWS**](tb-getrows.md)                             | Récupère le nombre de lignes de boutons dans une barre d’outils avec le style [**\_ encapsulé TBSTYLE**](toolbar-control-and-button-styles.md) . <br/>                                        |
| [**TO \_ GETSTATE**](tb-getstate.md)                           | Récupère des informations sur l’état du bouton spécifié dans une barre d’outils, par exemple s’il est activé, appuyé ou activé. <br/>                                                             |
| [**TO \_ GETSTRING**](tb-getstring.md)                         | Récupère une chaîne à partir du pool de chaînes d’une barre d’outils.<br/>                                                                                                                                             |
| [**TO \_ GETSTYLE**](tb-getstyle.md)                           | Récupère les styles en cours d’utilisation pour un contrôle ToolBar. <br/>                                                                                                                                |
| [**TO \_ GETTEXTROWS**](tb-gettextrows.md)                     | Récupère le nombre maximal de lignes de texte qui peuvent être affichées sur un bouton de barre d’outils. <br/>                                                                                                        |
| [**TO \_ GETTOOLTIPS**](tb-gettooltips.md)                     | Récupère le handle du contrôle ToolTip, le cas échéant, associé à la barre d’outils. <br/>                                                                                                           |
| [**TO \_ GETUNICODEFORMAT**](tb-getunicodeformat.md)           | Récupère l’indicateur de format de caractère Unicode pour le contrôle. <br/>                                                                                                                                |
| [**TO \_ HASACCELERATOR**](tb-hasaccelerator.md)               | **Destiné à un usage interne ; non recommandé pour une utilisation dans les applications.**<br/> Récupère le nombre de boutons de la barre d’outils qui contiennent le caractère d’accélérateur spécifié. <br/>                      |
| [**TO \_ HIDEBUTTON**](tb-hidebutton.md)                       | Masque ou affiche le bouton spécifié dans une barre d’outils.<br/>                                                                                                                                            |
| [**TO \_ HITTEST**](tb-hittest.md)                             | Détermine où un point se trouve dans un contrôle de barre d’outils. <br/>                                                                                                                                         |
| [**TO \_ indéterminés**](tb-indeterminate.md)                 | Définit ou efface l’état indéterminé du bouton spécifié dans une barre d’outils.<br/>                                                                                                                 |
| [**TO \_ INSERTBUTTON**](tb-insertbutton.md)                   | Insère un bouton dans une barre d’outils.<br/>                                                                                                                                                               |
| [**TO \_ INSERTMARKHITTEST**](tb-insertmarkhittest.md)         | Récupère les informations sur les marques d’insertion pour un point dans une barre d’outils. <br/>                                                                                                                          |
| [**TO \_ ISBUTTONCHECKED**](tb-isbuttonchecked.md)             | Détermine si le bouton spécifié dans une barre d’outils est activé. <br/>                                                                                                                            |
| [**TO \_ ISBUTTONENABLED**](tb-isbuttonenabled.md)             | Détermine si le bouton spécifié dans une barre d’outils est activé. <br/>                                                                                                                            |
| [**TO \_ ISBUTTONHIDDEN**](tb-isbuttonhidden.md)               | Détermine si le bouton spécifié dans une barre d’outils est masqué. <br/>                                                                                                                             |
| [**TO \_ ISBUTTONHIGHLIGHTED**](tb-isbuttonhighlighted.md)     | Vérifie l’état de mise en surbrillance d’un bouton de barre d’outils. <br/>                                                                                                                                             |
| [**TO \_ ISBUTTONINDETERMINATE**](tb-isbuttonindeterminate.md) | Détermine si le bouton spécifié dans une barre d’outils est indéterminé. <br/>                                                                                                                      |
| [**TO \_ ISBUTTONPRESSED**](tb-isbuttonpressed.md)             | Détermine si le bouton spécifié dans une barre d’outils est enfoncé. <br/>                                                                                                                            |
| [**TO \_ LOADIMAGES**](tb-loadimages.md)                       | Charge les images de bouton définies par le système dans la liste d’images d’un contrôle ToolBar.<br/>                                                                                                                      |
| [**TO \_ MAPACCELERATOR**](tb-mapaccelerator.md)               | Détermine l’ID du bouton qui correspond au caractère d’accélérateur spécifié.<br/>                                                                                                     |
| [**TO \_ MARKBUTTON**](tb-markbutton.md)                       | Définit l’état de surbrillance d’un bouton donné dans un contrôle ToolBar.<br/>                                                                                                                             |
| [**TO \_ MOVEBUTTON**](tb-movebutton.md)                       | Déplace un bouton d’un index vers un autre. <br/>                                                                                                                                                   |
| [**TO \_ PRESSBUTTON**](tb-pressbutton.md)                     | Appuie sur le bouton spécifié ou le relâche dans une barre d’outils.<br/>                                                                                                                                       |
| [**TO \_ REPLACEBITMAP**](tb-replacebitmap.md)                 | Remplace une image bitmap existante par une nouvelle image bitmap.<br/>                                                                                                                                               |
| [**TO \_ SAVERESTORE**](tb-saverestore.md)                     | Envoyer ce message pour lancer l’enregistrement ou la restauration de l’état d’une barre d’outils.<br/>                                                                                                                           |
| [**TO \_ SETANCHORHIGHLIGHT**](tb-setanchorhighlight.md)       | Définit le paramètre de surbrillance d’ancrage pour une barre d’outils. <br/>                                                                                                                                            |
| [**TO \_ SETBITMAPSIZE**](tb-setbitmapsize.md)                 | Définit la taille des images bitmap à ajouter à une barre d’outils. <br/>                                                                                                                             |
| [**TO \_ SETBOUNDINGSIZE**](tb-setboundingsize.md)             | **Destiné à un usage interne ; non recommandé pour une utilisation dans les applications.**<br/> Définit la taille limite pour un contrôle de barre d’outils à plusieurs colonnes. <br/>                                               |
| [**TO \_ SETBUTTONINFO**](tb-setbuttoninfo.md)                 | Définit les informations d’un bouton existant dans une barre d’outils.<br/>                                                                                                                                    |
| [**TO \_ SETBUTTONSIZE**](tb-setbuttonsize.md)                 | Définit la taille des boutons sur une barre d’outils.<br/>                                                                                                                                                       |
| [**TO \_ SETBUTTONWIDTH**](tb-setbuttonwidth.md)               | Définit les largeurs minimale et maximale des boutons dans le contrôle ToolBar.<br/>                                                                                                                           |
| [**TO \_ SETCMDID**](tb-setcmdid.md)                           | Définit l’identificateur de commande d’un bouton de barre d’outils. <br/>                                                                                                                                            |
| [**TO \_ SETCOLORSCHEME**](tb-setcolorscheme.md)               | Définit les informations de jeu de couleurs pour le contrôle ToolBar. <br/>                                                                                                                                  |
| [**TO \_ SETDISABLEDIMAGELIST**](tb-setdisabledimagelist.md)   | Définit la liste d’images que le contrôle ToolBar utilisera pour afficher les boutons désactivés. <br/>                                                                                                          |
| [**TO \_ SETDRAWTEXTFLAGS**](tb-setdrawtextflags.md)           | Définit les indicateurs de dessin de texte pour la barre d’outils. <br/>                                                                                                                                                |
| [**TO \_ SETEXTENDEDSTYLE**](tb-setextendedstyle.md)           | Définit les styles étendus pour un contrôle de barre d’outils. <br/>                                                                                                                                             |
| [**TO \_ SETHOTIMAGELIST**](tb-sethotimagelist.md)             | Définit la liste d’images que le contrôle ToolBar utilisera pour afficher les boutons actifs.<br/>                                                                                                                |
| [**TO \_ SETHOTITEM**](tb-sethotitem.md)                       | Définit l’élément réactif dans une barre d’outils.<br/>                                                                                                                                                              |
| [**TO \_ SETHOTITEM2**](tb-sethotitem2.md)                     | Définit l’élément réactif dans une barre d’outils.<br/>                                                                                                                                                              |
| [**TO \_ SETIMAGELIST**](tb-setimagelist.md)                   | Définit la liste d’images utilisée par la barre d’outils pour afficher les boutons dont l’État par défaut est.<br/>                                                                                                |
| [**TO \_ SETINDENT**](tb-setindent.md)                         | Définit la mise en retrait du premier bouton dans un contrôle de barre d’outils. <br/>                                                                                                                             |
| [**TO \_ SETINSERTMARK**](tb-setinsertmark.md)                 | Définit la marque d’insertion actuelle pour la barre d’outils. <br/>                                                                                                                                            |
| [**TO \_ SETINSERTMARKCOLOR**](tb-setinsertmarkcolor.md)       | Définit la couleur utilisée pour dessiner la marque d’insertion pour la barre d’outils. <br/>                                                                                                                             |
| [**TO \_ SETLISTGAP**](tb-setlistgap.md)                       | Définit la distance entre les boutons de la barre d’outils dans une barre d’outils spécifique.<br/>                                                                                                                         |
| [**TO \_ SETMAXTEXTROWS**](tb-setmaxtextrows.md)               | Définit le nombre maximal de lignes de texte affichées sur un bouton de barre d’outils. <br/>                                                                                                                         |
| [**TO \_ SETMETRICS**](tb-setmetrics.md)                       | Définit les métriques d’un contrôle ToolBar.<br/>                                                                                                                                                       |
| [**TO \_ SETPADDING**](tb-setpadding.md)                       | Définit la marge intérieure d’un contrôle de barre d’outils.<br/>                                                                                                                                                      |
| [**TO \_ SetParent,**](tb-setparent.md)                         | Définit la fenêtre à laquelle le contrôle de barre d’outils envoie des codes de notification. <br/>                                                                                                                      |
| [**TO \_ SETPRESSEDIMAGELIST**](tb-setpressedimagelist.md)     | Définit la liste d’images utilisée par la barre d’outils pour afficher les boutons qui sont dans un état appuyé.<br/>                                                                                                    |
| [**TO \_ SETROWS**](tb-setrows.md)                             | Définit le nombre de lignes de boutons dans une barre d’outils.<br/>                                                                                                                                             |
| [**TO \_ SETSTATE**](tb-setstate.md)                           | Définit l’état du bouton spécifié dans une barre d’outils.<br/>                                                                                                                                        |
| [**TO \_ SETSTYLE**](tb-setstyle.md)                           | Définit le style d’un contrôle ToolBar. <br/>                                                                                                                                                       |
| [**TO \_ SETTOOLTIPS**](tb-settooltips.md)                     | Associe un contrôle ToolTip à une barre d’outils. <br/>                                                                                                                                                |
| [**TO \_ SETUNICODEFORMAT**](tb-setunicodeformat.md)           | Définit l’indicateur de format de caractère Unicode pour le contrôle. Ce message vous permet de modifier le jeu de caractères utilisé par le contrôle au moment de l’exécution plutôt que de devoir recréer le contrôle. <br/>    |
| [**TO \_ SETWINDOWTHEME**](tb-setwindowtheme.md)               | Définit le style visuel d’un contrôle de barre d’outils.<br/>                                                                                                                                                  |
| [**TO \_ TRANSLATEACCELERATOR**](tb-translateaccelerator.md)   | Transmet un message de clavier à la barre d’outils.<br/>                                                                                                                                                    |



 

### <a name="notifications"></a>Notifications



| Rubrique                                                            | Contenu                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [NM \_ caractère (barre d’outils)](nm-char-toolbar.md)                        | Envoyé par la barre d’outils lorsqu’il reçoit un message [**WM \_ char**](/windows/desktop/inputdev/wm-char) . Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .<br/>                                                                                                                                       |
| [NM \_ , clic (barre d’outils)](nm-click-toolbar.md)                      | Envoyé par un contrôle de barre d’outils lorsque l’utilisateur clique sur un élément avec le bouton gauche de la souris. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .<br/>                                                                                                                                     |
| [NM \_ CUSTOMDRAW (barre d’outils)](nm-customdraw-toolbar.md)            | Envoyé par la barre d’outils pour signaler à sa fenêtre parente les opérations de dessin. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .<br/>                                                                                                                                              |
| [NM \_ DBLCLK (barre d’outils)](nm-dblclk-toolbar.md)                    | Avertit la fenêtre parente d’un contrôle ToolBar que l’utilisateur a double-cliqué sur le bouton gauche de la souris dans le contrôle. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .<br/>                                                                                             |
| [\_Touche nm (barre d’outils)](nm-keydown-toolbar.md)                  | Envoyé par un contrôle lorsque le contrôle a le focus clavier et que l’utilisateur appuie sur une touche. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) . <br/>                                                                                                                                 |
| [\_LDOWN nm](nm-ldown-toolbar.md)                                | Avertit la fenêtre parente d’une barre d’outils que le bouton gauche de la souris a été enfoncé. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .<br/>                                                                                                                                        |
| [NM \_ RCLICK (barre d’outils)](nm-rclick-toolbar.md)                    | Envoyé par un contrôle ToolBar lorsque l’utilisateur clique sur la barre d’outils avec le bouton droit de la souris. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .<br/>                                                                                                                                |
| [NM \_ RDBLCLK (barre d’outils)](nm-rdblclk-toolbar.md)                  | Avertit la fenêtre parente d’un contrôle que l’utilisateur a double-cliqué sur le bouton droit de la souris dans le contrôle. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .<br/>                                                                                                         |
| [NM \_ RELEASEDCAPTURE (barre d’outils)](nm-releasedcapture-toolbar-.md) | Avertit une fenêtre parente d’un contrôle ToolBar que le contrôle libère la capture de la souris. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) . <br/>                                                                                                                               |
| [NM \_ TOOLTIPSCREATED (barre d’outils)](nm-tooltipscreated-toolbar-.md) | Avertit la fenêtre parente d’une barre d’outils que la barre d’outils a créé un contrôle ToolTip. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) . <br/>                                                                                                                                    |
| [TBN \_ BEGINADJUST](tbn-beginadjust.md)                          | Avertit la fenêtre parente d’une barre d’outils que l’utilisateur a commencé à personnaliser une barre d’outils. Ce code de message est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) . <br/>                                                                                                                                          |
| [TBN \_ BEGINDRAG](tbn-begindrag.md)                              | Avertit la fenêtre parente d’une barre d’outils que l’utilisateur a commencé à faire glisser un bouton dans une barre d’outils. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) . <br/>                                                                                                                            |
| [TBN \_ CUSTHELP](tbn-custhelp.md)                                | Avertit la fenêtre parente d’une barre d’outils que l’utilisateur a choisi le bouton aide dans la boîte de dialogue Personnaliser la barre d’outils. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .<br/>                                                                                                       |
| [TBN \_ DELETINGBUTTON](tbn-deletingbutton.md)                    | Envoyé par un contrôle de barre d’outils lorsqu’un bouton va être supprimé. <br/>                                                                                                                                                                                                                                                |
| [TBN \_ DRAGOUT](tbn-dragout.md)                                  | Envoyé par un contrôle de barre d’outils lorsque l’utilisateur clique sur un bouton, puis déplace le curseur en dehors du bouton. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) . <br/>                                                                                                                     |
| [TBN, \_ DRAGOVER](tbn-dragover.md)                                | Vérifie si un message [**\_ MARKBUTTON to**](tb-markbutton.md) doit être envoyé pour un bouton qui est glissé. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .<br/>                                                                                           |
| [\_liste déroulante TBN](tbn-dropdown.md)                                | Envoyé par un contrôle de barre d’outils lorsque l’utilisateur clique sur un bouton déroulant. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) . <br/>                                                                                                                                                     |
| [TBN \_ DUPACCELERATOR](tbn-dupaccelerator.md)                    | Détermine si une touche d’accès rapide peut être utilisée sur au moins deux barres d’outils actives. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .<br/>                                                                                                                                      |
| [TBN \_ ENDADJUST](tbn-endadjust.md)                              | Avertit la fenêtre parente d’une barre d’outils que l’utilisateur a arrêté de personnaliser une barre d’outils. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) . <br/>                                                                                                                                   |
| [TBN \_ ENDDRAG](tbn-enddrag.md)                                  | Avertit la fenêtre parente de la barre d’outils que l’utilisateur a cessé de faire glisser un bouton dans une barre d’outils. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) . <br/>                                                                                                                        |
| [TBN \_ GETBUTTONINFO](tbn-getbuttoninfo.md)                      | Récupère les informations de personnalisation de la barre d’outils et avertit la fenêtre parente de la barre d’outils de toute modification apportée à la barre d’outils. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) . <br/>                                                                                        |
| [TBN \_ GETDISPINFO](tbn-getdispinfo.md)                          | Récupère les informations d’affichage d’un élément de barre d’outils. Cette notification est envoyée sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .<br/>                                                                                                                                                                           |
| [TBN \_ GETINFOTIP](tbn-getinfotip.md)                            | Récupère les informations de l’info-bulle d’un élément de barre d’outils. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .<br/>                                                                                                                                                                      |
| [TBN \_ GETOBJECT](tbn-getobject.md)                              | Envoyé par un contrôle ToolBar qui utilise le style [**TBSTYLE \_ REGISTERDROP**](toolbar-control-and-button-styles.md) pour demander un objet cible de déplacement lorsque le pointeur passe sur l’un de ses boutons. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .<br/> |
| [TBN \_ HOTITEMCHANGE](tbn-hotitemchange.md)                      | Envoyé par un contrôle de barre d’outils lorsque l’élément réactif (en surbrillance) change. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) . <br/>                                                                                                                                                    |
| [TBN \_ INITCUSTOMIZE](tbn-initcustomize.md)                      | Avertit la fenêtre parente d’une barre d’outils que la personnalisation a commencé. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .<br/>                                                                                                                                                       |
| [TBN \_ MAPACCELERATOR](tbn-mapaccelerator.md)                    | Demande l’index du bouton dans la barre d’outils correspondant au caractère d’accélérateur spécifié. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .<br/>                                                                                                                  |
| [TBN \_ QUERYDELETE](tbn-querydelete.md)                          | Avertit la fenêtre parente de la barre d’outils qu’un bouton peut être supprimé d’une barre d’outils pendant que l’utilisateur personnalise la barre d’outils. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) . <br/>                                                                                        |
| [TBN \_ QUERYINSERT](tbn-queryinsert.md)                          | Avertit la fenêtre parente de la barre d’outils qu’un bouton peut être inséré à gauche du bouton spécifié pendant que l’utilisateur personnalise une barre d’outils. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .<br/>                                                                     |
| [\_réinitialisation TBN](tbn-reset.md)                                      | Avertit la fenêtre parente de la barre d’outils que l’utilisateur a réinitialisé le contenu de la boîte de dialogue Personnaliser la barre d’outils. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .<br/>                                                                                                          |
| [\_restauration TBN](tbn-restore.md)                                  | Avertit la fenêtre parente d’une barre d’outils qu’une barre d’outils est en cours de restauration. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .<br/>                                                                                                                                 |
| [TBN \_ Enregistrer](tbn-save.md)                                        | Avertit la fenêtre parente d’une barre d’outils qu’une barre d’outils est en cours d’enregistrement. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .<br/>                                                                                                                                    |
| [TBN \_ TOOLBARCHANGE](tbn-toolbarchange.md)                      | Avertit la fenêtre parente de la barre d’outils que l’utilisateur a personnalisé une barre d’outils. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) . <br/>                                                                                                                                          |
| [TBN \_ WRAPACCELERATOR](tbn-wrapaccelerator.md)                  | Demande l’index du bouton dans une ou plusieurs barres d’outils correspondant au caractère d’accélérateur spécifié. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .<br/>                                                                                                         |
| [TBN \_ WRAPHOTITEM](tbn-wraphotitem.md)                          | Avertit une application avec au moins deux barres d’outils que l’élément réactif est sur le point de changer. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .<br/>                                                                                                                                |



 

### <a name="structures"></a>Structures



| Rubrique                                      | Contenu                                                                                                                                                                                                                                                                |
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**COLORMAP**](/windows/desktop/api/Commctrl/ns-commctrl-colormap)               | Contient les informations utilisées par la fonction [**CreateMappedBitmap**](/windows/desktop/api/Commctrl/nf-commctrl-createmappedbitmap) pour mapper les couleurs de l’image bitmap. <br/>                                                                                                                                 |
| [**NMTBCUSTOMDRAW**](/windows/desktop/api/Commctrl/ns-commctrl-nmtbcustomdraw)   | Contient des informations spécifiques à un code de notification [ \_ CUSTOMDRAW nm](nm-customdraw-toolbar.md) envoyé par un contrôle ToolBar. <br/>                                                                                                                                |
| [**NMTBDISPINFO**](/windows/desktop/api/Commctrl/ns-commctrl-nmtbdispinfoa)       | Contient et reçoit les informations d’affichage d’un élément de barre d’outils. Cette structure est utilisée avec le code de notification [TBN \_ GETDISPINFO](tbn-getdispinfo.md) . <br/>                                                                                                    |
| [**NMTBGETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-nmtbgetinfotipa)   | Contient et reçoit des informations sur l’info-bulle pour un élément de barre d’outils. Cette structure est utilisée avec le code de notification [TBN \_ GETINFOTIP](tbn-getdispinfo.md) . <br/>                                                                                                     |
| [**NMTBHOTITEM**](/windows/win32/api/commctrl/ns-commctrl-nmtbhotitem)         | Contient des informations utilisées avec le code de notification [TBN \_ HOTITEMCHANGE](tbn-hotitemchange.md) . <br/>                                                                                                                                                           |
| [**NMTBRESTORE**](/windows/win32/api/commctrl/ns-commctrl-nmtbrestore)         | Permet aux applications d’extraire les informations qui ont été placées dans [**NMTBSAVE**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave) lors de l’enregistrement de l’état de la barre d’outils. Cette structure est transmise aux applications lorsqu’elles reçoivent un code de notification de [ \_ restauration TBN](tbn-restore.md) .<br/>             |
| [**NMTBSAVE**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave)               | Cette structure est transmise aux applications lorsqu’elles reçoivent un code de notification d' [ \_ enregistrement TBN](tbn-save.md) . Elle contient des informations sur le bouton en cours d’enregistrement. Les applications peuvent modifier les valeurs des membres pour enregistrer des informations supplémentaires. <br/> |
| [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara)             | Contient les informations utilisées pour traiter les codes de notification de la barre d’outils. Cette structure remplace la structure **TBNOTIFY** . <br/>                                                                                                                                      |
| [**TBADDBITMAP**](/windows/win32/api/commctrl/ns-commctrl-tbaddbitmap)         | Ajoute une bitmap qui contient des images de bouton à une barre d’outils.<br/>                                                                                                                                                                                                      |
| [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton)               | Contient des informations sur un bouton dans une barre d’outils.<br/>                                                                                                                                                                                                            |
| [**TBBUTTONINFO**](/windows/desktop/api/Commctrl/ns-commctrl-tbbuttoninfoa)       | Contient ou reçoit des informations pour un bouton spécifique dans une barre d’outils.<br/>                                                                                                                                                                                         |
| [**TBINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-tbinsertmark)       | Contient des informations sur la marque d’insertion dans un contrôle ToolBar. <br/>                                                                                                                                                                                            |
| [**TBMETRICS**](/windows/desktop/api/Commctrl/ns-commctrl-tbmetrics)             | Définit les métriques d’une barre d’outils utilisées pour réduire ou développer des éléments de barre d’outils.<br/>                                                                                                                                                                            |
| [**TBREPLACEBITMAP**](/windows/desktop/api/Commctrl/ns-commctrl-tbreplacebitmap) | Utilisé avec le [**message \_ REPLACEBITMAP to**](tb-replacebitmap.md) pour remplacer une image bitmap de barre d’outils par une autre.<br/>                                                                                                                                              |
| [**TBSAVEPARAMS**](/windows/win32/api/commctrl/ns-commctrl-tbsaveparamsa)       | Spécifie l’emplacement dans le registre où le message [**\_ SAVERESTORE to**](tb-saverestore.md) stocke et récupère les informations sur l’état d’une barre d’outils. <br/>                                                                                           |



 

### <a name="constants"></a>Constantes



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Rubrique</th>
<th>Contenu</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="toolbar-button-states.md">États des boutons de barre d’outils</a></td>
<td>Cette section répertorie les États qu’un bouton de barre d’outils peut avoir. <br/></td>
</tr>
<tr class="even">
<td><a href="toolbar-control-and-button-styles.md">Styles de contrôle et de bouton de barre d’outils</a></td>
<td>Les styles de fenêtre suivants sont spécifiques aux barres d’outils. Elles sont combinées avec d’autres styles de fenêtre lorsque la barre d’outils est créée.<br/> <strong>Remarque</strong> Pour les contrôles communs <a href="common-control-versions.md">version 6,00</a>, si un <a href="themes-overview.md">style visuel</a> est utilisé avec la barre d’outils, les boutons sont toujours transparents quel que soit le paramètre de style. Sinon, le comportement de transparence est normal, comme indiqué par l’utilisation de l' <a href="toolbar-control-and-button-styles.md"><strong>TBSTYLE_FLAT</strong></a> ou du style de <a href="toolbar-control-and-button-styles.md"><strong>TBSTYLE_TRANSPARENT</strong></a> .
<blockquote>
[!Note]<br />
Comctl32.dll version 6 n’est pas redistribuable, mais elle est incluse dans Windows ou version ultérieure. Pour utiliser Comctl32.dll version 6, spécifiez-la dans un manifeste. Pour plus d’informations sur les manifestes, consultez <a href="cookbook-overview.md">activation des styles visuels</a>.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><a href="toolbar-extended-styles.md">Styles étendus de la barre d’outils</a></td>
<td>Cette section répertorie les styles étendus pris en charge par les contrôles ToolBar.<br/></td>
</tr>
<tr class="even">
<td><a href="toolbar-standard-button-image-index-values.md">Valeurs d’index d’image du bouton standard de la barre d’outils</a></td>
<td>Cette section spécifie les valeurs d’index des images au sein de bitmaps standard.<br/></td>
</tr>
</tbody>
</table>



 

