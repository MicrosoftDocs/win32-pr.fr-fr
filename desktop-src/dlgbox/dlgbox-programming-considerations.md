---
title: Considérations relatives à la programmation des boîtes de dialogue
description: Cette vue d’ensemble décrit quelques considérations relatives à la programmation concernant les boîtes de dialogue.
ms.assetid: 49024a0f-ea92-4d56-b063-8e5fcdbd884a
keywords:
- Windows Interface utilisateur, fenêtrage
- Windows Interface utilisateur, boîtes de dialogue
- fenêtrage, boîtes de dialogue
- boîtes de dialogue, à propos de
- procédures de boîte de dialogue
- boîtes de dialogue, procédures
- Message WM_INITDIALOG
- Message WM_COMMAND
- Message WM_PARENTNOTIFY
- messages de couleur de contrôle
- boîtes de dialogue, traitement des messages
- boîtes de dialogue, interface clavier
- boîtes de dialogue, mnémoniques
- boîtes de dialogue, personnalisées
- boîtes de dialogue personnalisées
- boîtes de dialogue, paramètres
ms.topic: article
ms.date: 08/25/2020
ms.openlocfilehash: 956f700841b0a3d76b7e071f0232382507394879a0253bc4cbcea533fdbb23bf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119456249"
---
# <a name="dialog-box-programming-considerations"></a>Considérations relatives à la programmation des boîtes de dialogue

Cette vue d’ensemble décrit quelques considérations relatives à la programmation concernant les boîtes de dialogue.

La vue d’ensemble comprend les rubriques suivantes.

-   [Procédures de boîte de dialogue](#dialog-box-procedures)
    -   [Message WM \_ INITDIALOG](wm-initdialog.md)
    -   [Message de \_ commande WM](/windows/desktop/menurc/wm-command)
    -   [Message WM \_ PARENTNOTIFY](/previous-versions/windows/desktop/inputmsg/wm-parentnotify)
    -   [Messages de couleur de contrôle](#control-color-messages)
    -   [Traitement du message par défaut de la boîte de dialogue](#dialog-box-default-message-processing)
-   [Interface clavier de la boîte de dialogue](#dialog-box-keyboard-interface)
    -   [Le \_ style WS TABSTOP](/windows/desktop/winmsg/window-styles)
    -   [Le \_ style de groupe WS](/windows/desktop/winmsg/window-styles)
    -   [Les mnémoniques](#mnemonics)
-   [Paramètres de la boîte de dialogue](#dialog-box-settings)
    -   [Cases d’option et cases à cocher](#radio-buttons-and-check-boxes)
    -   [Boîte de dialogue Modifier les contrôles](#dialog-box-edit-controls)
    -   [Zones de liste, zones de liste modifiable et listes de répertoires](#list-boxes-combo-boxes-and-directory-listings)
    -   [Messages de contrôle de boîte de dialogue](#dialog-box-control-messages)
-   [Boîtes de dialogue personnalisées](#custom-dialog-boxes)

## <a name="dialog-box-procedures"></a>Procédures de boîte de dialogue

Une procédure de boîte de dialogue est similaire à une procédure de fenêtre en ce que le système envoie des messages à la procédure lorsqu’elle contient des informations à fournir ou à des tâches à effectuer. Contrairement à une procédure de fenêtre, une procédure de boîte de dialogue n’appelle jamais la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) . Au lieu de cela, elle retourne **true** si elle traite un message ou **false** dans le cas contraire.

Chaque procédure de la boîte de dialogue se présente sous la forme suivante :

```cpp
BOOL CALLBACK DlgProc(HWND hwndDlg, UINT message, WPARAM wParam, LPARAM lParam) 
{ 
    switch (message) 
    { 
 
        // Place message cases here. 
 
        default: 
            return FALSE; 
    } 
}
```

Les paramètres de procédure remplissent le même objectif que dans une procédure de fenêtre, avec le paramètre *hwndDlg* qui reçoit le handle de fenêtre de la boîte de dialogue.

La plupart des procédures de boîte de dialogue traitent le message [**WM \_ INITDIALOG**](wm-initdialog.md) et les messages de [**\_ commande WM**](/windows/desktop/menurc/wm-command) envoyés par les contrôles, mais traitent uniquement les autres messages. Si une procédure de boîte de dialogue ne traite pas de message, elle doit retourner la **valeur false** pour indiquer au système de traiter les messages en interne. La seule exception à cette règle est le message **WM \_ INITDIALOG** . La procédure de la boîte de dialogue doit retourner **true** pour demander au système de traiter davantage le message **WM \_ INITDIALOG** . Dans tous les cas, la procédure ne doit pas appeler [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).

- [Message WM \_ INITDIALOG](#the-wm_initdialog-message)
- [Message de \_ commande WM](#the-wm_command-message)
- [Message WM \_ PARENTNOTIFY](#the-wm_parentnotify-message)
- [Messages de couleur de contrôle](#control-color-messages)
- [Traitement du message par défaut de la boîte de dialogue](#dialog-box-default-message-processing)

### <a name="the-wm_initdialog-message"></a>Message WM \_ INITDIALOG

Le système n’envoie pas de message [**WM \_ Create**](/windows/desktop/winmsg/wm-create) à la procédure de la boîte de dialogue. Au lieu de cela, il envoie un message [**WM \_ INITDIALOG**](wm-initdialog.md) lorsqu’il crée la boîte de dialogue et tous ses contrôles, mais avant d’afficher la boîte de dialogue. La procédure doit effectuer toute initialisation requise pour s’assurer que la boîte de dialogue affiche les paramètres actuels associés à la tâche. Par exemple, lorsqu’une boîte de dialogue contient un contrôle pour afficher le lecteur et le répertoire actifs, la procédure doit déterminer le lecteur et le répertoire en cours et définir cette valeur pour le contrôle.

La procédure peut initialiser des contrôles à l’aide de fonctions telles que [**SetDlgItemText**](/windows/desktop/api/Winuser/nf-winuser-setdlgitemtexta) et [**CheckDlgButton**](https://msdn.microsoft.com/library/Cc410649(v=MSDN.10).aspx). Étant donné que les contrôles sont Windows, la procédure peut également les manipuler à l’aide de fonctions de gestion de fenêtre telles que [**EnableWindow**](/windows/desktop/api/winuser/nf-winuser-enablewindow) et [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus). La procédure peut récupérer le handle de fenêtre d’un contrôle à l’aide de la fonction [**GetDlgItem**](/windows/desktop/api/Winuser/nf-winuser-getdlgitem) .

La procédure de boîte de dialogue peut modifier le contenu, l’État et la position de n’importe quel contrôle, si nécessaire. Par exemple, dans une boîte de dialogue qui contient une zone de liste de noms de fichiers et un bouton **ouvrir** , la procédure peut désactiver le bouton **ouvrir** jusqu’à ce que l’utilisateur sélectionne un fichier dans la liste. Dans cet exemple, le modèle de boîte de dialogue spécifie le style [**WS \_ Disabled**](/windows/desktop/winmsg/window-styles) pour le bouton **ouvrir** et le système désactive automatiquement le bouton lors de sa création. Lorsque la procédure de boîte de dialogue reçoit un message de notification de la zone de liste indiquant que l’utilisateur a sélectionné un fichier, la procédure appelle la fonction [**EnableWindow**](/windows/desktop/api/winuser/nf-winuser-enablewindow) pour activer le bouton **ouvrir** .

Pour afficher une icône personnalisée dans la barre de légende de la boîte de dialogue, votre gestionnaire [**WM \_ INITDIALOG**](wm-initdialog.md) peut envoyer le message [**WM \_ SETICON**](/windows/desktop/winmsg/wm-seticon) à la boîte de dialogue.

Si l’application crée la boîte de dialogue à l’aide de l’une des fonctions [**DialogBoxParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxparama), [**DialogBoxIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama), [**CreateDialogParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogparama)ou [**CreateDialogIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama), le paramètre *lParam* du message [**WM \_ INITDIALOG**](wm-initdialog.md) contient le paramètre supplémentaire transmis à la fonction. Les applications utilisent généralement ce paramètre supplémentaire pour passer un pointeur vers des informations d’initialisation supplémentaires à la procédure de boîte de dialogue, mais la procédure de la boîte de dialogue doit déterminer la signification du paramètre. Si l’application utilise une autre fonction pour créer la boîte de dialogue, le système définit le paramètre *lParam* sur la **valeur null**.

Avant de retourner le message [**WM \_ INITDIALOG**](wm-initdialog.md) , la procédure doit déterminer s’il doit définir le focus d’entrée sur un contrôle spécifié. Si la procédure de boîte de dialogue retourne la **valeur true**, le système définit automatiquement le focus d’entrée sur le contrôle dont le handle de fenêtre est dans le paramètre *wParam* . Si le contrôle qui reçoit le focus par défaut n’est pas approprié, il peut définir le focus sur le contrôle approprié à l’aide de la fonction [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) . Si la procédure définit le focus d’entrée, elle doit retourner **false** pour empêcher le système de définir le focus par défaut. Le contrôle recevant le focus d’entrée par défaut est toujours le premier contrôle spécifié dans le modèle qui est visible, et non désactivé, et possède le style [WS \_ TABSTOP](/windows/desktop/winmsg/window-styles) . Si aucun contrôle n’existe, le système définit le focus d’entrée par défaut sur le premier contrôle du modèle.

### <a name="the-wm_command-message"></a>Message de \_ commande WM

Un contrôle peut envoyer un message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) à la procédure de boîte de dialogue lorsque l’utilisateur effectue une action dans le contrôle. Ces messages, appelés messages de notification, informent la procédure de l’entrée utilisateur et lui permettent d’effectuer les réponses appropriées.

Tous les contrôles prédéfinis, à l’exception des contrôles statiques, envoient des messages de notification pour les actions utilisateur sélectionnées. Par exemple, un bouton de commande envoie le message de notification sur lequel l’utilisateur a [**\_ cliqué**](../controls/bn-clicked.md) chaque fois que l’utilisateur clique sur le bouton. Dans tous les cas, le mot de poids faible du paramètre *wParam* contient l’identificateur de contrôle, le mot de poids fort de *wParam* contient le code de notification et le paramètre *lParam* contient le handle de fenêtre de contrôle.

La procédure de la boîte de dialogue doit analyser et traiter les messages de notification. En particulier, la procédure doit traiter des messages ayant les identificateurs IDOK ou IDCANCEL ; ces messages représentent une demande de fermeture de la boîte de dialogue par l’utilisateur. La procédure doit fermer la boîte de dialogue à l’aide de la fonction [**EndDialog**](/windows/desktop/api/Winuser/nf-winuser-enddialog) pour les boîtes de dialogue modales et de la fonction [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) pour les boîtes de dialogue non modales.

Le système envoie également des messages de [**\_ commande WM**](/windows/desktop/menurc/wm-command) à la procédure de boîte de dialogue si la boîte de dialogue a un menu, tel que le menu **fenêtre** , et que l’utilisateur clique sur un élément de menu. En particulier, le système envoie un message de **\_ commande WM** avec le paramètre *wParam* défini sur **IDCANCEL** chaque fois que l’utilisateur clique sur **Fermer** dans le menu fenêtre de la boîte de dialogue. Le message est quasiment identique au message de notification envoyé par le bouton **Annuler** et doit être traité exactement de la même façon.

### <a name="the-wm_parentnotify-message"></a>Message WM \_ PARENTNOTIFY

Un contrôle envoie un message [**WM \_ PARENTNOTIFY**](/previous-versions/windows/desktop/inputmsg/wm-parentnotify) chaque fois que l’utilisateur appuie sur un bouton de la souris tout en pointant sur le contrôle. Certaines applications interprètent ce message comme un signal permettant d’effectuer une action liée au contrôle, par exemple l’affichage d’une ligne de texte décrivant l’objectif du contrôle.

Le système envoie également des messages [**WM \_ PARENTNOTIFY**](/previous-versions/windows/desktop/inputmsg/wm-parentnotify) lorsqu’il crée et détruit une fenêtre, mais pas pour les contrôles créés à partir d’un modèle de boîte de dialogue. Le système empêche ces messages en spécifiant le style **WS \_ ex \_ NOPARENTNOTIFY** lors de la création des contrôles. Une application ne peut pas substituer ce comportement par défaut, sauf si elle crée ses propres contrôles pour la boîte de dialogue.

### <a name="control-color-messages"></a>Messages Control-Color

Les contrôles et le système peuvent envoyer des messages de couleur de contrôle lorsqu’ils souhaitent que la procédure de boîte de dialogue dessine l’arrière-plan d’un contrôle ou d’une autre fenêtre à l’aide d’un pinceau et de couleurs spécifiques. Cela peut être utile lorsque les applications remplacent les couleurs par défaut utilisées dans les boîtes de dialogue et leurs contrôles. Voici les messages de couleur de contrôle qui ont remplacé le message **WM \_ CTLCOLOR** .

-   [**\_CTLCOLORBTN WM**](../controls/wm-ctlcolorbtn.md)
-   [**\_CTLCOLORDLG WM**](wm-ctlcolordlg.md)
-   [**\_CTLCOLOREDIT WM**](../controls/wm-ctlcoloredit.md)
-   [**\_CTLCOLORLISTBOX WM**](../controls/wm-ctlcolorlistbox.md)
-   [**\_CTLCOLORSCROLLBAR WM**](../controls/wm-ctlcolorscrollbar.md)
-   [**\_CTLCOLORSTATIC WM**](../controls/wm-ctlcolorstatic.md)

Un contrôle envoie un message de couleur de contrôle à la procédure de boîte de dialogue juste avant de peindre son propre arrière-plan. Le message permet à la procédure de spécifier le pinceau à utiliser et de définir les couleurs d’arrière-plan et de premier plan. La procédure spécifie un pinceau en retournant la poignée de pinceau. Pour définir les couleurs d’arrière-plan et de premier plan, la procédure utilise les fonctions [**SetBkColor**](/windows/desktop/api/wingdi/nf-wingdi-setbkcolor) et [**SetTextColor**](/windows/desktop/api/wingdi/nf-wingdi-settextcolor) avec le contexte de périphérique d’affichage du contrôle. Le message de couleur de contrôle passe un handle au contexte de périphérique d’affichage à la procédure dans le paramètre *wParam* du message.

Le système envoie un message [**WM \_ CTLCOLORDLG**](wm-ctlcolordlg.md) à la procédure de boîte de dialogue si la procédure ne traite pas le message [**WM \_ ERASEBKGND**](/windows/desktop/winmsg/wm-erasebkgnd) . La classe de boîte de dialogue prédéfinie n’ayant pas de pinceau d’arrière-plan de classe, ce message permet à la procédure de définir son propre arrière-plan sans avoir à inclure le code pour effectuer le travail.

Dans tous les cas, lorsqu’une procédure de boîte de dialogue ne traite pas un message de couleur de contrôle, le système utilise un pinceau avec la couleur de fenêtre par défaut pour peindre l’arrière-plan pour tous les contrôles et les fenêtres à l’exception des barres de défilement. Une application peut récupérer la couleur de fenêtre par défaut en passant la valeur de la **\_ fenêtre couleur** à la fonction [**GetSysColor**](/windows/desktop/api/winuser/nf-winuser-getsyscolor) . Pendant que l’arrière-plan est peint, la couleur de premier plan du contexte de périphérique d’affichage est définie sur la couleur de texte par défaut (**couleur \_ WINDOWTEXT**). Pour les barres de défilement, le système utilise un pinceau avec la couleur de barre de défilement par défaut (**\_ ScrollBar de couleur**). Dans ce cas, les couleurs d’arrière-plan et de premier plan du contexte de périphérique d’affichage sont définies sur blanc et noir, respectivement.

### <a name="dialog-box-default-message-processing"></a>Traitement du message par défaut de la boîte de dialogue

La procédure de fenêtre pour la classe de boîte de dialogue prédéfinie effectue le traitement par défaut pour tous les messages que la procédure de boîte de dialogue ne traite pas. Lorsque la procédure de la boîte de dialogue retourne la **valeur false** pour un message, la procédure de fenêtre prédéfinie vérifie les messages et effectue les actions par défaut suivantes :



| Message                                            | Action par défaut                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DM \_ GETDEFID**](dm-getdefid.md)                | Vous pouvez envoyer ce message à une boîte de dialogue. La boîte de dialogue retourne l’identificateur du contrôle du bouton de commande par défaut, si la boîte de dialogue en possède un ; Sinon, elle retourne zéro.                                                                                                                                                                                                                                                                                                                      |
| [**repositionnement DM \_**](dm-reposition.md)            | Vous pouvez envoyer ce message à une boîte de dialogue de niveau supérieur. La boîte de dialogue se repositionne pour s’ajuster à la zone du bureau.                                                                                                                                                                                                                                                                                                                                                                       |
| [**DM \_ SETDEFID**](dm-setdefid.md)                | Vous pouvez envoyer ce message à une boîte de dialogue. La boîte de dialogue définit le bouton de commande par défaut sur le contrôle spécifié par l’identificateur de contrôle dans le paramètre *wParam* .                                                                                                                                                                                                                                                                                                                             |
| [**activation de WM \_**](/windows/desktop/inputdev/wm-activate)           | Restaure le focus d’entrée sur le contrôle identifié par le handle précédemment enregistré si la boîte de dialogue est activée. Dans le cas contraire, la procédure enregistre le handle dans le contrôle ayant le focus d’entrée.                                                                                                                                                                                                                                                                                               |
| [**\_CHARTOITEM WM**](../controls/wm-chartoitem.md)         | Retourne zéro.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**\_Fermer WM**](/windows/desktop/winmsg/wm-close)                   | Publie le message de notification de l' [**\_ utilisateur**](../controls/bn-clicked.md) dans la boîte de dialogue, en spécifiant **IDCANCEL** comme identificateur de contrôle. Si la boîte de dialogue a un identificateur de contrôle IDCANCEL et que le contrôle est actuellement désactivé, la procédure émet un avertissement et ne publie pas le message.                                                                                                                                                                                              |
| [**\_COMPAREITEM WM**](../controls/wm-compareitem.md)       | Retourne zéro.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**\_ERASEBKGND WM**](/windows/desktop/winmsg/wm-erasebkgnd)         | Remplit la zone cliente de la boîte de dialogue à l’aide du pinceau retourné à partir du message [**WM \_ CTLCOLORDLG**](wm-ctlcolordlg.md) ou de la couleur de la fenêtre par défaut.                                                                                                                                                                                                                                                                                                                                 |
| [**WM \_ GETFONT**](/windows/desktop/winmsg/wm-getfont)               | Retourne un handle vers la police de la boîte de dialogue définie par l’application.                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**\_INITDIALOG WM**](wm-initdialog.md)            | Retourne zéro.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**\_LBUTTONDOWN WM**](/windows/desktop/inputdev/wm-lbuttondown)     | Envoie un [**message \_ SHOWDROPDOWN CB**](../controls/cb-showdropdown.md) à la zone de liste déroulante ayant le focus d’entrée, en dirigeant le contrôle pour masquer sa zone de liste déroulante. La procédure appelle [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) pour terminer l’action par défaut.                                                                                                                                                                                                                                      |
| [**\_NCDESTROY WM**](/windows/desktop/winmsg/wm-ncdestroy)           | Libère la mémoire globale allouée pour les contrôles d’édition dans la boîte de dialogue (s’applique aux boîtes de dialogue qui spécifient le style [**DS \_ LOCALEDIT**](dialog-box-styles.md) ) et libère toute police définie par l’application (s’applique aux boîtes de dialogue qui spécifient le style DS [**\_ SetFont**](dialog-box-styles.md) ou [**DS \_ SHELLFONT**](dialog-box-styles.md) ). La procédure appelle la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) pour terminer l’action par défaut. |
| [**\_NCLBUTTONDOWN WM**](/windows/desktop/inputdev/wm-nclbuttondown) | Envoie un [**message \_ SHOWDROPDOWN CB**](../controls/cb-showdropdown.md) à la zone de liste déroulante ayant le focus d’entrée, en dirigeant le contrôle pour masquer sa zone de liste déroulante. La procédure appelle [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) pour terminer l’action par défaut.                                                                                                                                                                                                                                      |
| [**\_NEXTDLGCTL WM**](wm-nextdlgctl.md)            | Définit le focus d’entrée sur le contrôle suivant ou précédent dans la boîte de dialogue, sur le contrôle identifié par le handle dans le paramètre *wParam* , ou sur le premier contrôle dans la boîte de dialogue qui est visible, et non désactivé, et qui a le style [**WS \_ TABSTOP**](/windows/desktop/winmsg/window-styles) . La procédure ignore ce message si la fenêtre active avec le focus d’entrée n’est pas un contrôle.                                                                                                                  |
| [**WM \_ SetFocus**](/windows/desktop/inputdev/wm-setfocus)           | Définit le focus d’entrée sur le contrôle identifié par un handle de fenêtre de contrôle précédemment enregistré. Si aucun descripteur de ce type n’existe, la procédure définit le focus d’entrée sur le premier contrôle du modèle de boîte de dialogue qui est visible, et non désactivé, et qui a le style [**WS \_ TABSTOP**](/windows/desktop/winmsg/window-styles) . Si aucun contrôle n’existe, la procédure définit le focus d’entrée sur le premier contrôle du modèle.                                                                                          |
| [**WM \_ ShowWindow**](/windows/desktop/winmsg/wm-showwindow)         | Enregistre un handle sur le contrôle ayant le focus d’entrée si la boîte de dialogue est masquée, puis appelle [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) pour terminer l’action par défaut.                                                                                                                                                                                                                                                                                                                     |
| [**\_SYSCOMMAND WM**](/windows/desktop/menurc/wm-syscommand)         | Enregistre un handle sur le contrôle ayant le focus d’entrée si la boîte de dialogue est réduite, puis appelle [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) pour terminer l’action par défaut.                                                                                                                                                                                                                                                                                                                  |
| [**\_VKEYTOITEM WM**](../controls/wm-vkeytoitem.md)         | Retourne zéro.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |

La procédure de fenêtre prédéfinie transmet tous les autres messages à [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) pour le traitement par défaut.

## <a name="dialog-box-keyboard-interface"></a>Interface clavier de la boîte de dialogue

Le système fournit une interface clavier spéciale pour les boîtes de dialogue qui exécutent un traitement spécial pour plusieurs clés. L’interface génère des messages qui correspondent à certains boutons dans la boîte de dialogue ou modifie le focus d’entrée d’un contrôle à un autre. Voici les clés utilisées dans cette interface et leurs actions respectives.


| Clé            | Action                                                                                                                                                                    |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ALT +*mnémonique* | Déplace le focus d’entrée vers le premier contrôle (avec le style [**WS \_ TABSTOP**](/windows/desktop/winmsg/window-styles) ) après le contrôle statique contenant le mnémonique spécifié.        |
| INACTIF           | Déplace le focus d’entrée vers le contrôle suivant dans le groupe.                                                                                                                   |
| ENTRÉE          | Envoie un message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) à la procédure de la boîte de dialogue. Le paramètre *wParam* est défini sur IDOK ou sur l’identificateur de contrôle du bouton de commande par défaut. |
| ÉCHAP            | Envoie un message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) à la procédure de la boîte de dialogue. Le paramètre *wParam* est défini sur IDCANCEL.                                              |
| LEFT           | Déplace le focus d’entrée vers le contrôle précédent dans le groupe.                                                                                                               |
| *mnémotechniques*     | Déplace le focus d’entrée vers le premier contrôle (avec le style [**WS \_ TABSTOP**](/windows/desktop/winmsg/window-styles) ) après le contrôle statique contenant le mnémonique spécifié.        |
| RIGHT          | Déplace le focus d’entrée vers le contrôle suivant dans le groupe.                                                                                                                   |
| Maj+Tab      | Déplace le focus d’entrée vers le contrôle précédent qui a le style [**WS \_ TABSTOP**](/windows/desktop/winmsg/window-styles) .                                                                |
| Tab            | Déplace le focus d’entrée vers le contrôle suivant qui a le style [**WS \_ TABSTOP**](/windows/desktop/winmsg/window-styles) .                                                                    |
| UP             | Déplace le focus d’entrée vers le contrôle précédent dans le groupe.                                                                                                               |

Le système fournit automatiquement l’interface clavier pour toutes les boîtes de dialogue modales. Elle ne fournit pas l’interface pour les boîtes de dialogue non modales, sauf si l’application appelle la fonction [**IsDialogMessage**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) pour filtrer les messages dans sa boucle de message principale. Cela signifie que l’application doit transmettre le message à **IsDialogMessage** immédiatement après avoir récupéré le message de la file d’attente de messages. La fonction traite les messages s’il s’agit de la boîte de dialogue et retourne une valeur différente de zéro pour indiquer que le message a été traité et ne doit pas être transmis à la fonction [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) ou [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) .

Étant donné que l’interface de clavier de la boîte de dialogue utilise des touches de direction pour se déplacer entre les contrôles d’une boîte de dialogue, une application ne peut pas utiliser ces clés pour faire défiler le contenu d’une boîte de dialogue modale ou d’une boîte de dialogue non modale pour laquelle [**IsDialogMessage**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) est appelé. Quand une boîte de dialogue comporte des barres de défilement, l’application doit fournir une autre interface clavier pour les barres de défilement. Notez que l’interface de la souris pour le défilement est disponible lorsque le système comprend une souris.

### <a name="the-ws_tabstop-style"></a>Le \_ style WS TABSTOP

Le style [**WS \_ TABSTOP**](/windows/desktop/winmsg/window-styles) spécifie les contrôles que l’utilisateur peut déplacer en appuyant sur la touche Tab ou sur les touches Maj + Tab.

Quand l’utilisateur appuie sur TAB ou sur MAJ + TAB, le système détermine d’abord si ces clés sont traitées par le contrôle qui a actuellement le focus d’entrée. Elle envoie au contrôle un message [**WM \_ GETDLGCODE**](wm-getdlgcode.md) et, si le contrôle retourne DLGC \_ WANTTAB, le système passe les clés au contrôle. Dans le cas contraire, le système utilise la fonction [**GetNextDlgTabItem**](/windows/desktop/api/Winuser/nf-winuser-getnextdlgtabitem) pour localiser le contrôle suivant qui est visible, et non désactivé, et qui a le style [**WS \_ TABSTOP**](/windows/desktop/winmsg/window-styles) . La recherche commence par le contrôle qui possède actuellement le focus d’entrée et continue dans l’ordre dans lequel les contrôles ont été créés, c’est-à-dire l’ordre dans lequel ils sont définis dans le modèle de boîte de dialogue. Lorsque le système localise un contrôle ayant les caractéristiques requises, le système y déplace le focus d’entrée.

Si la recherche du contrôle suivant avec le style [**WS \_ TABSTOP**](/windows/desktop/winmsg/window-styles) rencontre une fenêtre avec le style **WS \_ ex \_ CONTROLPARENT** , le système recherche de manière récursive les enfants de la fenêtre.

Une application peut également utiliser [**GetNextDlgTabItem**](/windows/desktop/api/Winuser/nf-winuser-getnextdlgtabitem) pour localiser des contrôles avec le style [**WS \_ TABSTOP**](/windows/desktop/winmsg/window-styles) . La fonction récupère le handle de fenêtre du contrôle suivant ou précédent avec le style **WS \_ TABSTOP** sans déplacer le focus d’entrée.

### <a name="the-ws_group-style"></a>Le \_ style de groupe WS

Par défaut, le système déplace le focus d’entrée vers le contrôle suivant ou précédent chaque fois que l’utilisateur appuie sur une touche de direction. Tant que le contrôle actuel avec le focus d’entrée ne traite pas ces clés et que le contrôle suivant ou précédent n’est pas un contrôle statique, le système continue de déplacer le focus d’entrée sur tous les contrôles dans la boîte de dialogue lorsque l’utilisateur continue à appuyer sur les touches de direction.

Une application peut utiliser le style de [**\_ groupe WS**](/windows/desktop/winmsg/window-styles) pour modifier ce comportement par défaut. Le style marque le début d’un groupe de contrôles. Si un contrôle du groupe a le focus d’entrée lorsque l’utilisateur commence à appuyer sur les touches de direction, le focus reste dans le groupe. En général, le premier contrôle d’un groupe doit avoir le style de **\_ groupe WS** et tous les autres contrôles du groupe ne doivent pas avoir ce style. Tous les contrôles du groupe doivent être contigus, c’est-à-dire qu’ils doivent avoir été créés consécutivement sans contrôles intermédiaires.

Quand l’utilisateur appuie sur une touche de direction, le système détermine d’abord si le contrôle actuel ayant le focus d’entrée traite les touches de direction. Le système envoie un message [**WM \_ GETDLGCODE**](wm-getdlgcode.md) au contrôle et si le contrôle retourne la valeur **\_ WANTARROWS DLGC** , passe la clé au contrôle. Dans le cas contraire, le système utilise la fonction [**GetNextDlgGroupItem**](/windows/desktop/api/Winuser/nf-winuser-getnextdlggroupitem) pour déterminer le contrôle suivant dans le groupe.

[**GetNextDlgGroupItem**](/windows/desktop/api/Winuser/nf-winuser-getnextdlggroupitem) recherche dans l’ordre (ou dans l’ordre inverse) les contrôles qui ont été créés. Si l’utilisateur appuie sur la touche droite ou enfoncée, **GetNextDlgGroupItem** retourne le contrôle suivant si ce contrôle n’a pas le style de [**\_ groupe WS**](/windows/desktop/winmsg/window-styles) . Dans le cas contraire, la fonction inverse l’ordre de la recherche et retourne le premier contrôle avec le style de **\_ groupe WS** . Si l’utilisateur appuie sur la touche gauche ou haut, la fonction retourne le contrôle précédent, sauf si le contrôle actuel a déjà le style de **\_ groupe WS** . Si le contrôle actuel a ce style, la fonction inverse l’ordre de la recherche, localise le premier contrôle ayant le style **de \_ groupe WS** et retourne le contrôle qui précède immédiatement le contrôle localisé.

Si la recherche du contrôle suivant dans le groupe rencontre une fenêtre avec le style **WS \_ ex \_ CONTROLPARENT** , le système recherche de manière récursive les enfants de la fenêtre.

Une fois que le système a le contrôle suivant ou précédent, il envoie un message [**WM \_ GETDLGCODE**](wm-getdlgcode.md) au contrôle pour déterminer le type de contrôle. Le système déplace ensuite le focus d’entrée pour contrôler s’il ne s’agit pas d’un contrôle statique. Si le contrôle est une case d’option automatique, le système lui envoie un message de [**\_ clic sur BM**](../controls/bm-click.md) . Une application peut également utiliser [**GetNextDlgGroupItem**](/windows/desktop/api/Winuser/nf-winuser-getnextdlggroupitem) pour localiser des contrôles dans un groupe.

En règle générale, le premier contrôle du groupe combine les styles [**WS \_ Group**](/windows/desktop/winmsg/window-styles) et [**WS \_ TABSTOP**](/windows/desktop/winmsg/window-styles) afin que l’utilisateur puisse se déplacer d’un groupe à un groupe à l’aide de la touche Tab. Si le groupe contient des cases d’option, l’application doit appliquer le style **WS \_ TABSTOP** uniquement au premier contrôle du groupe. Le système déplace automatiquement le style lorsque l’utilisateur passe d’un contrôle à l’autre dans le groupe. Cela garantit que le focus d’entrée sera toujours sur le contrôle le plus récemment sélectionné lorsque l’utilisateur se déplace vers le groupe à l’aide de la touche TAB.

### <a name="mnemonics"></a>Les mnémoniques

Un mnémonique est une lettre ou un chiffre sélectionné dans l’étiquette d’un bouton ou dans le texte d’un contrôle statique. Le système déplace le focus d’entrée vers le contrôle associé au mnémonique chaque fois que l’utilisateur appuie sur la touche qui correspond au mnémonique ou appuie sur cette touche et la touche ALT en combinaison. Les mnémoniques permettent à l’utilisateur de passer rapidement à un contrôle spécifié à l’aide du clavier.

Une application crée un mnémonique pour un contrôle en insérant la esperluette (&) juste avant la lettre ou le chiffre sélectionné dans l’étiquette ou le texte du contrôle. Dans la plupart des cas, la chaîne se terminant par un caractère null fournie avec le contrôle dans le modèle de boîte de dialogue contient l’esperluette. Toutefois, une application peut créer un mnémonique à tout moment en remplaçant l’étiquette ou le texte existant d’un contrôle à l’aide de la fonction [**SetDlgItemText**](/windows/desktop/api/Winuser/nf-winuser-setdlgitemtexta) . Un seul mnémonique peut être spécifié pour chaque contrôle. Bien qu’il soit recommandé, les mnémoniques dans une boîte de dialogue ne sont pas nécessairement uniques.

Quand l’utilisateur appuie sur une touche de lettre ou de chiffre, le système détermine d’abord si le contrôle actuel ayant le focus d’entrée traite la clé. Le système envoie un message [**WM \_ GETDLGCODE**](wm-getdlgcode.md) au contrôle et, si le contrôle retourne la valeur **DLGC \_ WANTALLKEYS** ou **DLG \_ WANTMESSAGE** , le système passe la clé au contrôle. Dans le cas contraire, il recherche un contrôle dont le mnémonique correspond à la lettre ou au chiffre spécifié. Elle poursuit la recherche jusqu’à ce qu’elle trouve un contrôle ou ait examiné tous les contrôles. Au cours de la recherche, elle ignore tous les contrôles statiques qui ont le style [**SS \_ NoPrefix**](../controls/static-control-styles.md) .

Si la recherche d’un contrôle avec un mnémonique correspondant rencontre une fenêtre avec le style **WS \_ ex \_ CONTROLPARENT** , le système recherche de manière récursive les enfants de la fenêtre.

Si le système localise un contrôle statique et que le contrôle n’est pas désactivé, le système déplace le focus d’entrée vers le premier contrôle après le contrôle statique qui est visible, et non désactivé, et qui a le style [**WS \_ TABSTOP**](/windows/desktop/winmsg/window-styles) . Si le système localise un autre contrôle qui a un mnémonique correspondant, il déplace le focus d’entrée vers ce contrôle. Si le contrôle est un bouton de commande par défaut, le système envoie un message de notification sur lequel l' [**\_ utilisateur a cliqué**](../controls/bn-clicked.md) dans la procédure de la boîte de dialogue. Si le contrôle est un autre style de bouton et qu’aucun autre contrôle dans la boîte de dialogue n’a le même mnémonique, le système envoie le message de [**\_ clic BM**](../controls/bm-click.md) au contrôle.

## <a name="dialog-box-settings"></a>Paramètres de la boîte de dialogue

Les paramètres de la boîte de dialogue sont les sélections et les valeurs actuelles pour les contrôles de la boîte de dialogue. La procédure de boîte de dialogue est chargée d’initialiser les contrôles à ces paramètres lors de la création de la boîte de dialogue. Il est également chargé de récupérer les paramètres actuels des contrôles avant de détruire la boîte de dialogue. Les méthodes utilisées pour initialiser et récupérer les paramètres dépendent du type de contrôle.

Pour plus d'informations, voir les rubriques suivantes :

-   [Cases d’option et cases à cocher](#radio-buttons-and-check-boxes)
-   [Boîte de dialogue Modifier les contrôles](#dialog-box-edit-controls)
-   [Zones de liste, zones de liste modifiable et listes de répertoires](#list-boxes-combo-boxes-and-directory-listings)
-   [Messages de contrôle de boîte de dialogue](#dialog-box-control-messages)

### <a name="radio-buttons-and-check-boxes"></a>Cases d’option et cases à cocher

Les boîtes de dialogue utilisent des cases d’option et des cases à cocher pour permettre à l’utilisateur de choisir parmi une liste d’options. Les cases d’option permettent à l’utilisateur de choisir parmi des options qui s’excluent mutuellement ; les cases à cocher permettent à l’utilisateur de choisir une combinaison d’options.

La procédure de boîte de dialogue peut définir l’état initial d’une case à cocher à l’aide de la fonction [**CheckDlgButton**](https://msdn.microsoft.com/library/Cc410649(v=MSDN.10).aspx) , qui active ou désactive la case à cocher. Pour les cases d’option d’un groupe de cases d’option mutuellement exclusives, la procédure de boîte de dialogue peut utiliser la fonction [**CheckRadioButton**](https://msdn.microsoft.com/library/Cc410654(v=MSDN.10).aspx) pour définir la case d’option appropriée et effacer automatiquement toute autre case d’option.

Avant qu’une boîte de dialogue ne se termine, la procédure de la boîte de dialogue peut vérifier l’état de chaque case d’option et case à cocher à l’aide de la fonction [**IsDlgButtonChecked**](https://msdn.microsoft.com/library/Cc364806(v=MSDN.10).aspx) , qui retourne l’état actuel du bouton. En général, une boîte de dialogue enregistre ces informations pour initialiser les boutons la prochaine fois qu’elle crée la boîte de dialogue.

### <a name="dialog-box-edit-controls"></a>Boîte de dialogue Modifier les contrôles

De nombreuses boîtes de dialogue possèdent des contrôles d’édition qui permettent à l’utilisateur d’entrer du texte comme entrée. La plupart des procédures de boîte de dialogue initialisent un contrôle d’édition lors du premier démarrage de la boîte de dialogue. Par exemple, la procédure de boîte de dialogue peut placer un nom de fichier proposé dans le contrôle que l’utilisateur peut ensuite sélectionner, modifier ou remplacer. La procédure de boîte de dialogue peut définir le texte dans un contrôle d’édition à l’aide de la fonction [**SetDlgItemText**](/windows/desktop/api/Winuser/nf-winuser-setdlgitemtexta) , qui copie le texte d’une mémoire tampon spécifiée dans le contrôle d’édition. Lorsque le contrôle d’édition reçoit le focus d’entrée, il sélectionne automatiquement le texte complet pour modification.

Étant donné que les contrôles d’édition ne retournent pas automatiquement leur texte dans la boîte de dialogue, la procédure de la boîte de dialogue doit récupérer le texte avant qu’il ne se termine. Il peut récupérer le texte à l’aide de la fonction [**GetDlgItemText**](/windows/desktop/api/Winuser/nf-winuser-getdlgitemtexta) , qui copie le texte du contrôle d’édition dans une mémoire tampon. La procédure de boîte de dialogue enregistre généralement ce texte pour initialiser le contrôle d’édition ultérieurement ou le transmet à la fenêtre parente pour traitement.

Certaines boîtes de dialogue utilisent des contrôles d’édition qui permettent à l’utilisateur d’entrer des nombres. La procédure de boîte de dialogue peut récupérer un nombre à partir d’un contrôle d’édition à l’aide de la fonction [**GetDlgItemInt**](/windows/desktop/api/Winuser/nf-winuser-getdlgitemint) , qui récupère le texte du contrôle d’édition et convertit le texte en valeur décimale. L’utilisateur tape le nombre en chiffres décimaux. Il peut être signé ou non signé. La procédure de boîte de dialogue peut afficher un entier à l’aide de la fonction [**SetDlgItemInt**](/windows/desktop/api/Winuser/nf-winuser-setdlgitemint) . **SetDlgItemInt** convertit un entier signé ou non signé en une chaîne de chiffres décimaux.

### <a name="list-boxes-combo-boxes-and-directory-listings"></a>Zones de liste, zones de liste modifiable et listes de répertoires

Certaines boîtes de dialogue affichent des listes de noms à partir desquels l’utilisateur peut sélectionner un ou plusieurs noms. Pour afficher une liste de noms de fichiers, par exemple, une boîte de dialogue utilise généralement une zone de liste et les fonctions [**DlgDirList**](https://msdn.microsoft.com/library/Cc410788(v=MSDN.10).aspx) et [**DlgDirSelectEx**](https://msdn.microsoft.com/library/Cc410769(v=MSDN.10).aspx) . La fonction **DlgDirList** remplit automatiquement une zone de liste avec les noms de fichiers dans le répertoire actif. La fonction **DlgDirSelect** récupère le nom de fichier sélectionné dans la zone de liste. Ensemble, ces deux fonctions offrent un moyen pratique pour une boîte de dialogue d’afficher une liste de répertoires afin que l’utilisateur puisse sélectionner un fichier sans avoir à taper son nom et son emplacement.

Une boîte de dialogue peut également utiliser une zone de liste déroulante pour afficher une liste de noms de fichiers. La fonction [**DlgDirListComboBox**](https://msdn.microsoft.com/library/Cc410798(v=MSDN.10).aspx) remplit automatiquement une partie zone de liste de la zone de liste déroulante avec les noms de fichiers dans le répertoire actif. La fonction [**DlgDirSelectComboBoxEx**](https://msdn.microsoft.com/library/Cc410768(v=MSDN.10).aspx) récupère un nom de fichier sélectionné à partir de la partie zone de liste.

### <a name="dialog-box-control-messages"></a>Messages de contrôle de boîte de dialogue

De nombreux contrôles reconnaissent des messages prédéfinis qui, lorsqu’ils sont reçus par des contrôles, les obligent à exécuter une action. Par exemple, le message [**BM \_ SETCHECK**](../controls/bm-setcheck.md) définit la vérification dans une case à cocher et le message [**em \_ GETSEL**](../controls/em-getsel.md) récupère la partie du texte du contrôle qui est actuellement sélectionné. Les messages de contrôle offrent à une procédure de dialogue un accès plus souple et plus flexible aux contrôles que les fonctions standard. ils sont donc souvent utilisés lorsque la boîte de dialogue nécessite des interactions complexes avec l’utilisateur.

Une procédure de boîte de dialogue peut envoyer un message à un contrôle en fournissant l’identificateur de contrôle et à l’aide de la fonction [**SendDlgItemMessage**](/windows/desktop/api/Winuser/nf-winuser-senddlgitemmessagea) , qui est identique à la fonction [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) , sauf qu’elle utilise un identificateur de contrôle au lieu d’un handle de fenêtre pour identifier le contrôle qui doit recevoir le message. Un message spécifié peut exiger que la procédure de dialogue envoie des paramètres avec le message et que le message puisse avoir des valeurs de retour correspondantes. L’opération et les exigences de chaque message de contrôle dépendent de l’objectif du message et du contrôle qui le traite.

pour plus d’informations sur les messages de contrôle, consultez [Windows des contrôles](../controls/window-controls.md).

## <a name="custom-dialog-boxes"></a>Boîtes de dialogue personnalisées

Une application peut créer des boîtes de dialogue personnalisées en utilisant une classe de fenêtre définie par l’application pour les boîtes de dialogue au lieu d’utiliser la classe de boîte de dialogue prédéfinie. Les applications utilisent généralement cette méthode lorsqu’une boîte de dialogue est la fenêtre principale, mais elle est également utile pour créer des boîtes de dialogue modales et non modales pour les applications qui ont des fenêtres qui se chevauchent standard.

La classe de fenêtre définie par l’application permet à l’application de définir une procédure de fenêtre pour la boîte de dialogue et de traiter les messages avant de les envoyer à la procédure de la boîte de dialogue. Il permet également à l’application de définir une icône de classe, un pinceau d’arrière-plan de classe et un menu de classe pour la boîte de dialogue. L’application doit inscrire la classe de fenêtre avant de tenter de créer une boîte de dialogue et doit fournir le modèle de boîte de dialogue avec la valeur Atom ou le nom de la classe de fenêtre.

De nombreuses applications créent une nouvelle classe de boîte de dialogue en extrayant d’abord les informations de classe pour la classe de boîte de dialogue prédéfinie et en la passant à la fonction [**GetClassinfo**](/windows/desktop/api/winuser/nf-winuser-getclassinfoa) , qui remplit une structure [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) avec les informations. L’application modifie les membres individuels de la structure, tels que le nom de la classe, le pinceau et l’icône, puis inscrit la nouvelle classe à l’aide de la fonction [**registerClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa) . Si une application remplit la structure **WNDCLASS** seule, elle doit définir le membre **CbWndExtra** sur le **DLGWINDOWEXTRA**, qui est le nombre d’octets supplémentaires requis par le système pour chaque boîte de dialogue. Si une application utilise également des octets supplémentaires pour chaque boîte de dialogue, ceux-ci doivent dépasser les octets supplémentaires requis par le système.

La procédure de fenêtre de la boîte de dialogue personnalisée a les mêmes paramètres et exigences que toute autre procédure de fenêtre. Contrairement à d’autres procédures de fenêtre, toutefois, la procédure de fenêtre pour cette boîte de dialogue doit appeler la fonction [**DefDlgProc**](/windows/desktop/api/Winuser/nf-winuser-defdlgprocw) à la place de la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) pour tous les messages qu’elle ne traite pas. **DefDlgProc** effectue le même traitement par défaut des messages que la procédure de fenêtre pour la boîte de dialogue prédéfinie, qui inclut l’appel de la procédure de boîte de dialogue.

Une application peut également créer des boîtes de dialogue personnalisées en sous-classant la procédure de fenêtre de la boîte de dialogue prédéfinie. La fonction [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) permet à une application de spécifier la procédure de fenêtre pour une fenêtre spécifiée. L’application peut également tenter d’effectuer une sous-classe à l’aide de la fonction [**SetClassLong**](/windows/desktop/api/winuser/nf-winuser-setclasslonga) , mais cela affecte toutes les boîtes de dialogue du système, pas seulement celles qui appartiennent à l’application.

Les applications qui créent des boîtes de dialogue personnalisées fournissent parfois une autre interface clavier pour les boîtes de dialogue. Pour les boîtes de dialogue non modales, cela peut signifier que l’application n’appelle pas la fonction [**IsDialogMessage**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) et traite à la place toutes les entrées au clavier dans la procédure de fenêtre personnalisée. Dans ce cas, l’application peut utiliser le message [**WM \_ NEXTDLGCTL**](wm-nextdlgctl.md) pour réduire le code nécessaire pour déplacer le focus d’entrée d’un contrôle à un autre. Ce message, lorsqu’il est passé à [**DefDlgProc**](/windows/desktop/api/Winuser/nf-winuser-defdlgprocw), déplace le focus d’entrée vers un contrôle spécifié et met à jour l’apparence des contrôles, tels que le déplacement de la bordure du bouton de commande par défaut ou la définition d’une case d’option automatique.
