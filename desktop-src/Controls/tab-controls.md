---
title: À propos des contrôles Tab
description: Un contrôle tab équivaut aux intercalaires dans un classeur ou aux étiquettes dans une armoire de classement. En utilisant un contrôle tab, une application peut définir plusieurs pages pour la même zone d’une fenêtre ou d’une boîte de dialogue.
ms.assetid: 55ed2863-7f8d-43ce-a0f9-6f6d41e3f947
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c45ac7caa05c73e1dcf22a8e6f0eb4d031ca079
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104102421"
---
# <a name="about-tab-controls"></a>À propos des contrôles Tab

Un contrôle tab équivaut aux intercalaires dans un classeur ou aux étiquettes dans une armoire de classement. En utilisant un contrôle tab, une application peut définir plusieurs pages pour la même zone d’une fenêtre ou d’une boîte de dialogue. Chaque page se compose d’un certain type d’informations ou d’un groupe de contrôles que l’application affiche lorsque l’utilisateur sélectionne l’onglet correspondant.

La capture d’écran suivante montre un contrôle onglet simple qui contient des onglets pour les jours de la semaine. L’onglet Tuesday a été sélectionné.

![capture d’écran d’une feuille de propriétés avec cinq onglets, un pour chaque jour de la semaine](images/tab-simple.png)

Cette rubrique comprend les sections suivantes.

-   [Création de contrôles onglet](#creating-tab-controls)
-   [Styles du contrôle onglet](#tab-control-styles)
-   [Onglets et attributs de tabulation](#tabs-and-tab-attributes)
-   [Zone d’affichage](#display-area)
-   [Sélection de l’onglet](#tab-selection)
-   [Listes d’images du contrôle onglet](#tab-control-image-lists)
-   [Taille et position des tabulations](#tab-size-and-position)
-   [Onglets owner-drawn](#owner-drawn-tabs)
-   [Info-bulles des contrôles onglet](#tab-control-tooltips)
-   [Traitement par défaut des messages de contrôle d’onglet](#default-tab-control-message-processing)

## <a name="creating-tab-controls"></a>Création de contrôles onglet

Vous pouvez créer un contrôle onglet en appelant la fonction [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , en spécifiant la classe de fenêtre du [**\_ TABCONTROL de WC**](common-control-window-classes.md) . Cette classe de fenêtre est inscrite lors du chargement de la DLL de contrôles communs. Pour vous assurer que la DLL est chargée, utilisez la fonction [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) .

Dans Microsoft Visual Studio, vous pouvez créer un contrôle onglet à l’aide de la boîte à outils.

Vous envoyez des messages à un contrôle onglet pour ajouter des onglets et, sinon, affecter l’apparence et le comportement du contrôle. Chaque message a une macro correspondante que vous pouvez utiliser au lieu d’envoyer le message explicitement. Vous ne pouvez pas désactiver un onglet individuel dans un contrôle Tab. Toutefois, vous pouvez désactiver un contrôle onglet dans une feuille de propriétés en désactivant la page correspondante.

## <a name="tab-control-styles"></a>Styles du contrôle onglet

Vous pouvez appliquer certaines caractéristiques aux contrôles d’onglet en spécifiant des styles de contrôle d’onglet lorsque le contrôle est créé. Par exemple, vous pouvez spécifier l’alignement et l’apparence générale des onglets dans un contrôle Tab.

Vous pouvez faire en sorte que les onglets ressemblent à des boutons en spécifiant le style des [**\_ boutons TCS**](tab-control-styles.md) . Les onglets dans ce type de contrôle Tab doivent servir la même fonction que les contrôles Button ; autrement dit, le fait de cliquer sur un onglet doit exécuter une commande au lieu d’afficher une page. Étant donné que la zone d’affichage d’un contrôle onglet de bouton n’est généralement pas utilisée, aucune bordure n’est dessinée autour de celle-ci.

Vous pouvez faire en sorte qu’un onglet reçoive le focus d’entrée lorsque vous cliquez dessus en spécifiant le style [**\_ FOCUSONBUTTONDOWN TCS**](tab-control-styles.md) . Ce style est généralement utilisé uniquement avec le style de [**\_ boutons TCS**](tab-control-styles.md) . Vous pouvez spécifier qu’un onglet ne reçoit pas le focus d’entrée lorsque vous cliquez dessus à l’aide du style [**\_ FOCUSNEVER TCS**](tab-control-styles.md) .

Par défaut, un contrôle onglet n’affiche qu’une seule ligne d’onglets. Si tous les onglets ne peuvent pas être affichés à la fois, le contrôle onglet affiche un contrôle up-up afin que l’utilisateur puisse faire défiler des onglets supplémentaires dans l’affichage. Vous pouvez faire en sorte qu’un contrôle onglet affiche plusieurs lignes d’onglets, si nécessaire, en spécifiant le style [**\_ multiligne TCS**](tab-control-styles.md) . Avec ce style, tous les onglets peuvent être affichés à la fois. Les onglets sont alignés à gauche dans chaque ligne, sauf si vous spécifiez le style [**\_ RIGHTJUSTIFY TCS**](tab-control-styles.md) . Dans ce cas, la largeur de chaque onglet est augmentée afin que chaque ligne d’onglets remplisse toute la largeur du contrôle onglet.

Un contrôle onglet redimensionne automatiquement chaque onglet pour l’adapter à son icône, le cas échéant, et son étiquette. Pour attribuer la même largeur à tous les onglets, vous pouvez spécifier le style de la valeur de [**TCS \_**](tab-control-styles.md) . Le contrôle redimensionne tous les onglets pour qu’ils correspondent à l’étiquette la plus large, ou vous pouvez affecter une largeur et une hauteur spécifiques à l’aide du message [**\_ SETITEMSIZE TCM**](tcm-setitemsize.md) . Dans chaque onglet, le contrôle Centre l’icône et l’étiquette, en plaçant l’icône à gauche de l’étiquette. Vous pouvez forcer l’icône à gauche, en laissant l’étiquette centrée, en spécifiant le style [**\_ FORCEICONLEFT TCS**](tab-control-styles.md) . Vous pouvez aligner à gauche l’icône et l’étiquette à l’aide du style [**\_ FORCELABELLEFT TCS**](tab-control-styles.md) . Vous ne pouvez pas utiliser le style de la fonction **TCS \_** avec le style [**\_ RIGHTJUSTIFY TCS**](tab-control-styles.md) .

Vous pouvez spécifier que la fenêtre parente dessine les onglets dans le contrôle à l’aide du style [**\_ OWNERDRAWFIXED TCS**](tab-control-styles.md) . Pour plus d’informations, consultez les [onglets owner-drawn](#owner-drawn-tabs).

Vous pouvez spécifier qu’un contrôle onglet crée un contrôle ToolTip à l’aide du [**style \_ info-bulles TCS**](tab-control-styles.md) . Pour plus d’informations à ce sujet, consultez [info-bulles des contrôles onglet](#tab-control-tooltips).

## <a name="tabs-and-tab-attributes"></a>Onglets et attributs de tabulation

Chaque onglet d’un contrôle onglet se compose d’une icône, d’une étiquette et de données définies par l’application. Ces informations sont spécifiées par une structure [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) . Vous pouvez ajouter des onglets à un contrôle onglet, récupérer le nombre d’onglets, récupérer et définir le contenu d’un onglet, et supprimer des onglets. Les onglets sont identifiés par leur index de base zéro.

Pour ajouter des onglets à un contrôle onglet, utilisez le message [**TCM \_ INSERTITEM**](tcm-insertitem.md) , en spécifiant la position de l’élément et l’adresse d’une structure [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) . Vous pouvez récupérer et définir le contenu d’un onglet existant à l’aide des messages [**TCM \_ GETITEM**](tcm-getitem.md) et [**TCM \_ SETITEM**](tcm-setitem.md) . Pour chaque onglet, vous pouvez spécifier une icône, une étiquette ou les deux. Vous pouvez également spécifier les données définies par l’application à associer à l’onglet.

Vous pouvez récupérer le nombre actuel d’onglets à l’aide du message [**\_ GETITEMCOUNT TCM**](tcm-getitemcount.md) , supprimer un onglet à l’aide du message [**TCM \_ DELETEITEM**](tcm-deleteitem.md) et supprimer tous les onglets d’un contrôle onglet à l’aide du message [**TCM \_ DELETEALLITEMS**](tcm-deleteallitems.md) .

Vous pouvez associer des données définies par l’application à chaque onglet. Par exemple, vous pouvez enregistrer des informations sur chaque page avec son onglet correspondant. Par défaut, un contrôle onglet alloue quatre octets supplémentaires par onglet pour les données définies par l’application. Vous pouvez modifier le nombre d’octets supplémentaires par onglet à l’aide du message [**TCM \_ SETITEMEXTRA**](tcm-setitemextra.md) . Vous pouvez utiliser ce message uniquement lorsque le contrôle onglet est vide.

Les données définies par l’application sont spécifiées par le membre **lParam** de la structure [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) . Si vous utilisez plus de 4 octets de données définies par l’application, vous devez définir votre propre structure et l’utiliser à la place de **TCITEM**. Vous pouvez récupérer et définir des données définies par l’application de la même façon que vous récupérez et définissez d’autres informations sur un onglet, en utilisant les messages [**TCM \_ GETITEM**](tcm-getitem.md) et [**TCM \_ SETITEM**](tcm-setitem.md) .

Le premier membre de votre structure doit être une structure [**TCITEMHEADER**](/windows/win32/api/commctrl/ns-commctrl-tcitemheadera) , et les membres restants doivent spécifier des données définies par l’application. **TCITEMHEADER** est identique à [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema), sauf qu’il n’a pas le membre **lParam** . La différence entre la taille de votre structure et la taille de **TCITEMHEADER** doit être égale au nombre d’octets supplémentaires par tabulation.

## <a name="display-area"></a>Zone d’affichage

La zone d’affichage d’un contrôle onglet est la zone dans laquelle une application affiche la page actuelle. En règle générale, une application crée une fenêtre enfant ou une boîte de dialogue, en définissant la taille et la position de la fenêtre en fonction de la zone d’affichage. Étant donné le rectangle de fenêtre pour un contrôle onglet, vous pouvez calculer le rectangle englobant de la zone d’affichage à l’aide du message [**TCM \_ ADJUSTRECT**](tcm-adjustrect.md) .

Parfois, la zone d’affichage doit être une taille particulière, par exemple, la taille d’une boîte de dialogue enfant non modale. À partir du rectangle englobant pour la zone d’affichage, vous pouvez utiliser [**TCM \_ ADJUSTRECT**](tcm-adjustrect.md) pour calculer le rectangle de fenêtre correspondant pour le contrôle Tab.

## <a name="tab-selection"></a>Sélection de l’onglet

Quand l’utilisateur sélectionne un onglet, un contrôle onglet envoie les codes de notification de sa fenêtre parente sous la forme de messages de notification [**WM \_**](wm-notify.md) . Le code de notification [TCN \_ SELCHANGING](tcn-selchanging.md) est envoyé avant la modification de la sélection et le code de notification [TCN \_ selChange](tcn-selchange.md) est envoyé après la modification de la sélection.

Vous pouvez traiter [TCN \_ SELCHANGING](tcn-selchanging.md) pour enregistrer l’état de la page sortante. Vous pouvez retourner **true** pour empêcher la modification de la sélection. Par exemple, il se peut que vous ne souhaitiez pas quitter une boîte de dialogue enfant dans laquelle un contrôle a un paramètre non valide.

Vous devez traiter [TCN \_ selChange](tcn-selchange.md) pour afficher la page entrante dans la zone d’affichage. Cela peut simplement entraîner la modification des informations affichées dans une fenêtre enfant. Plus souvent, chaque page se compose d’une fenêtre enfant ou d’une boîte de dialogue. Dans ce cas, une application peut traiter cette notification en détruisant ou en masquant la fenêtre ou la boîte de dialogue enfant sortante et en créant ou en indiquant la fenêtre ou la boîte de dialogue enfant entrante.

Vous pouvez récupérer et définir la sélection actuelle à l’aide des messages [**TCM \_ GETCURSEL**](tcm-getcursel.md) et [**TCM \_ SETCURSEL**](tcm-setcursel.md) .

## <a name="tab-control-image-lists"></a>Listes d’images du contrôle onglet

Chaque onglet peut être associé à une icône, qui est spécifiée par un index dans la liste d’images du contrôle onglet. Lorsqu’un contrôle onglet est créé, il n’est associé à aucune liste d’images. Une application peut créer une liste d’images à l’aide de la fonction [**ImageList \_ Create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) , puis l’assigner à un contrôle onglet à l’aide du message [**\_ SETIMAGELIST TCM**](tcm-setimagelist.md) .

Vous pouvez ajouter des images à la liste d’images d’un contrôle onglet exactement comme vous le feriez pour n’importe quelle autre liste d’images. Toutefois, une application doit supprimer les images à l’aide du message [**TCM \_ REMOVEIMAGE**](tcm-removeimage.md) au lieu de la fonction [**ImageList \_ Remove**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_remove) . Ce message garantit que chaque onglet reste associé à la même image qu’avant.

La destruction d’un contrôle Tab ne détruit pas une liste d’images qui lui est associée. Vous devez détruire la liste d’images séparément. Cela est utile si vous souhaitez assigner la même liste d’images à plusieurs contrôles onglet.

Pour récupérer le handle de la liste d’images actuellement associée à un contrôle onglet, vous pouvez utiliser le message [**TCM \_ GETIMAGELIST**](tcm-getimagelist.md) .

## <a name="tab-size-and-position"></a>Taille et position des tabulations

Chaque onglet dans un contrôle onglet a une taille et une position. Vous pouvez définir la taille des onglets, récupérer le rectangle englobant d’un onglet ou déterminer l’onglet situé à une position spécifiée.

Pour les contrôles d’onglets à largeur fixe et owner-drawn, vous pouvez définir la largeur et la hauteur exactes des onglets à l’aide du message [**\_ SETITEMSIZE TCM**](tcm-setitemsize.md) . Dans d’autres contrôles onglet, la taille de chaque onglet est calculée en fonction de l’icône et de l’étiquette de l’onglet. Le contrôle onglet comprend de l’espace pour une bordure et une marge supplémentaire. Vous pouvez définir l’épaisseur de la marge en utilisant le message [**TCM \_ SETPADDING**](tcm-setpadding.md) .

Vous pouvez déterminer le rectangle englobant actuel d’un onglet à l’aide du message [**TCM \_ GETITEMRECT**](tcm-getitemrect.md) . Vous pouvez déterminer l’onglet, le cas échéant, à un emplacement spécifié à l’aide du message [**TCM \_ HITTEST**](tcm-hittest.md) .

Dans un contrôle onglet avec le [**style \_ multiligne TCS**](tab-control-styles.md) , vous pouvez déterminer le nombre actuel de lignes d’onglets à l’aide du message de [**\_ GETROWCOUNT de TCM**](tcm-getrowcount.md) .

## <a name="owner-drawn-tabs"></a>Onglets Owner-Drawn

Si un contrôle onglet a le [**style \_ OWNERDRAWFIXED TCS**](tab-control-styles.md) , la fenêtre parente doit peindre les onglets en traitant le message [**WM \_ DRAWITEM**](wm-drawitem.md) . Le contrôle onglet envoie ce message chaque fois qu’un onglet doit être peint. Le paramètre *lParam* spécifie l’adresse d’une structure [**drawitemstruct,**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) , qui contient l’index de l’onglet, son rectangle englobant et le contexte de périphérique (DC) dans lequel dessiner.

Par défaut, le membre **ItemData** de [**drawitemstruct,**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) contient la valeur du membre **lParam** de la structure [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) . Toutefois, si vous modifiez la quantité de données définies par l’application par onglet, **ItemData** contient l’adresse des données à la place. Vous pouvez modifier la quantité de données définies par l’application par onglet à l’aide du message [**TCM \_ SETITEMEXTRA**](tcm-setitemextra.md) .

Pour spécifier la taille des éléments dans un contrôle onglet, la fenêtre parente doit traiter le message [**WM \_ MEASUREITEM**](wm-measureitem.md) . Étant donné que tous les onglets d’un contrôle onglet owner-drawn ont la même taille, ce message n’est envoyé qu’une seule fois. Il n’existe aucun style de contrôle onglet pour les onglets owner-drawn de taille variable. Vous pouvez également définir la largeur et la hauteur des onglets à l’aide du message [**TCM \_ SETITEMSIZE**](tcm-setitemsize.md) .

## <a name="tab-control-tooltips"></a>Info-bulles des contrôles onglet

Vous pouvez utiliser un contrôle ToolTip pour fournir une brève description de chaque onglet dans un contrôle Tab. Un contrôle onglet avec le style [**\_ info-bulles TCS**](tab-control-styles.md) crée un contrôle ToolTip lorsqu’il est créé et détruit le contrôle ToolTip lorsqu’il est détruit. Vous pouvez également créer un contrôle ToolTip et l’assigner à un contrôle onglet.

Si vous utilisez un contrôle ToolTip avec un contrôle onglet, la fenêtre parente doit traiter le code de notification [ttn \_ GETDISPINFO](ttn-getdispinfo.md) pour fournir une description de chaque onglet à la demande.

Pour utiliser le même contrôle ToolTip avec plusieurs contrôles Tab, créez vous-même le contrôle ToolTip et attribuez-le au contrôle onglet à l’aide du message [**\_ SETTOOLTIPS TCM**](tcm-settooltips.md) . Vous pouvez récupérer le handle du contrôle ToolTip actuel d’un contrôle onglet à l’aide du message [**\_ GETTOOLTIPS TCM**](tcm-gettooltips.md) . Si vous créez votre propre contrôle ToolTip, vous ne devez pas utiliser le style [**\_ info-bulles TCS**](tab-control-styles.md) .

## <a name="default-tab-control-message-processing"></a>Traitement par défaut des messages de contrôle d’onglet

Cette section décrit le traitement des messages effectué par un contrôle onglet. Les messages spécifiques aux contrôles onglet sont abordés dans d’autres sections de cette documentation.



| Message                                                  | Traitement effectué                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_CAPTURECHANGED WM**](/windows/desktop/inputdev/wm-capturechanged) | Ne fait rien si le contrôle onglet a relâché la capture de la souris. Si une autre fenêtre a capturé la souris et qu’un bouton est maintenu enfoncé, la commande libère le bouton.                                                                                                                                                                                                                                                                                                                |
| [**création de WM \_**](/windows/desktop/winmsg/wm-create)                 | Alloue et Initialise une structure de données interne. Le contrôle crée un contrôle ToolTip si le [**style \_ info-bulles TCS**](tab-control-styles.md) est spécifié.                                                                                                                                                                                                                                                                                                    |
| [**\_destructeur WM**](/windows/desktop/winmsg/wm-destroy)               | Libère les ressources allouées pendant le traitement de [**\_ Create WM**](/windows/desktop/winmsg/wm-create) .                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**\_GETDLGCODE WM**](/windows/desktop/dlgbox/wm-getdlgcode)         | Retourne une combinaison des valeurs DLGC \_ WANTARROWS et DLGC \_ WANTCHARS.                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**WM \_ GETFONT**](/windows/desktop/winmsg/wm-getfont)               | Retourne le handle de la police utilisée pour les étiquettes.                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**WM- \_ touche**](/windows/desktop/inputdev/wm-keydown)               | Traite les touches de direction et modifie la sélection, le cas échéant.                                                                                                                                                                                                                                                                                                                                                                                                                |
| [**\_KILLFOCUS WM**](/windows/desktop/inputdev/wm-killfocus)           | Invalide l’onglet qui a le focus afin qu’il soit repeint pour refléter un État sans focus.                                                                                                                                                                                                                                                                                                                                                                                      |
| [**\_LBUTTONDOWN WM**](/windows/desktop/inputdev/wm-lbuttondown)       | Transfère le message au contrôle ToolTip, le cas échéant, et modifie la sélection si l’utilisateur clique sur un onglet. Si l’utilisateur clique sur un bouton, le contrôle redessine le bouton pour obtenir une apparence enfoncée et capture la souris. Si l’utilisateur clique sur un onglet ou un bouton et que le style [**\_ FOCUSONBUTTONDOWN TCS**](tab-control-styles.md) est spécifié, le contrôle définit le focus sur lui-même.                                                     |
| [**\_LBUTTONUP WM**](/windows/desktop/inputdev/wm-lbuttonup)           | Relâche la souris si un bouton a été enfoncé. Si le curseur se trouve sur le bouton et est maintenu enfoncé, le contrôle modifie la sélection en conséquence et redessine le bouton.                                                                                                                                                                                                                                                                                                         |
| [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove)           | Transfère le message au contrôle ToolTip, le cas échéant. Si le style des [**\_ boutons TCS**](tab-control-styles.md) est spécifié et que le bouton de la souris est maintenu enfoncé après un clic, le contrôle peut également redessiner le bouton affecté pour lui attribuer une apparence en relief ou en 3D.                                                                                                                                                                                            |
| [**\_notification WM**](wm-notify.md)                          | Transfère les codes de notification envoyés par le contrôle ToolTip.                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**\_peinture WM**](/windows/desktop/gdi/wm-paint)                            | Dessine une bordure autour de la zone d’affichage (sauf si le style des [**\_ boutons TCS**](tab-control-styles.md) est spécifié) et peint tous les onglets qui croisent le rectangle non valide. Pour chaque onglet, il dessine le corps de l’onglet (ou envoie un message [**WM \_ DRAWITEM**](wm-drawitem.md) à la fenêtre parente), puis dessine une bordure autour de l’onglet. Si le paramètre *wParam* est non null, le contrôle suppose que la valeur est un HDC et peint à l’aide de ce contexte de périphérique. |
| [**\_RBUTTONDOWN WM**](/windows/desktop/inputdev/wm-rbuttondown)       | Envoie un code de notification [ \_ RCLICK nm](nm-rclick-tab.md) à la fenêtre parente.                                                                                                                                                                                                                                                                                                                                                                                                   |
| [**WM \_ SetFocus**](/windows/desktop/inputdev/wm-setfocus)             | Invalide l’onglet qui a le focus afin qu’il soit repeint pour refléter un État focus.                                                                                                                                                                                                                                                                                                                                                                                    |
| [**\_SetFont WM**](/windows/desktop/winmsg/wm-setfont)               | Définit la police utilisée pour les étiquettes.                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**\_SETREDRAW WM**](/windows/desktop/gdi/wm-setredraw)                    | Définit l’état d’un indicateur interne qui détermine si le contrôle est repeint lorsque des éléments sont insérés et supprimés, lorsque la police est modifiée, et ainsi de suite.                                                                                                                                                                                                                                                                                                                      |
| [**taille du WM \_**](/windows/desktop/winmsg/wm-size)                     | Recalcule les positions des onglets et peut invalider une partie du contrôle onglet pour forcer le redessin de certains ou de tous les onglets.                                                                                                                                                                                                                                                                                                                                                             |



 

 

 