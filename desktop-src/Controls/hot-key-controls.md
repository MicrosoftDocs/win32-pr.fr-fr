---
title: À propos des contrôles de touche d’accès rapide
description: Un contrôle de touche d’accès rapide est une fenêtre qui permet à l’utilisateur d’entrer une combinaison de touches à utiliser comme touche d’accès rapide.
ms.assetid: 5f011459-4c30-45d4-9668-19f575b041ce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dec45d61df535025cff00fee6428f604aa670bf3
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730484"
---
# <a name="about-hot-key-controls"></a>À propos des contrôles de touche d’accès rapide

Un contrôle de touche d’accès rapide est une fenêtre qui permet à l’utilisateur d’entrer une combinaison de touches à utiliser comme touche d’accès rapide. Une touche d’accès rapide est une combinaison de touches sur laquelle l’utilisateur peut appuyer pour effectuer une action rapidement. Par exemple, un utilisateur peut créer une touche d’accès rapide qui active une fenêtre donnée et l’affiche en haut de l’ordre de plan. Le contrôle de touche d’accès rapide affiche les choix de l’utilisateur et s’assure que l’utilisateur sélectionne une combinaison de touches valide. La capture d’écran suivante montre comment un contrôle de touche d’accès rapide s’affiche dans une boîte de dialogue lorsque l’utilisateur appuie sur la touche Alt.

![capture d’écran d’une boîte de dialogue qui contient un contrôle de touche d’accès rapide](images/hotkey.png)

## <a name="using-hot-key-controls"></a>Utilisation des contrôles de touche d’accès rapide

Quand l’utilisateur entre une combinaison de touches à utiliser comme touche d’accès rapide, les noms des clés s’affichent dans le contrôle de touche d’accès rapide. Une combinaison de touches peut se composer d’une touche de modification (telle que CTRL, ALT ou Maj) et d’une clé associée (telle qu’une touche de caractère, une touche de direction, une touche de fonction, etc.).

Une fois que l’utilisateur a choisi une combinaison de touches, l’application récupère la combinaison de touches à partir du contrôle de touche d’accès rapide et l’utilise pour configurer une touche d’accès rapide dans le système. Les informations récupérées à partir du contrôle de touche d’accès rapide incluent un indicateur qui spécifie la touche de modification et le code de touche virtuelle de la clé qui l’accompagne.

L’application peut utiliser les informations fournies par un contrôle de touche d’accès rapide pour configurer une touche d’accès rapide globale ou une touche d’accès rapide spécifique à un thread. Une touche d’accès rapide globale est associée à une fenêtre particulière ; elle permet à l’utilisateur d’activer la fenêtre à partir de n’importe quelle partie du système. Une application définit une touche d’accès rapide globale à l’aide du message [**WM \_ SETHOTKEY**](/windows/desktop/inputdev/wm-sethotkey) . Chaque fois que l’utilisateur appuie sur une touche d’accès rapide globale, la fenêtre spécifiée dans **WM \_ SETHOTKEY** reçoit un message [**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) qui spécifie la valeur de la [**\_ touche**](/windows/desktop/inputdev/wm-sethotkey) d’accès rapide SC. Ce message active la fenêtre qui le reçoit. La touche d’accès rapide reste valide jusqu’à ce que l’application qui a appelé **WM \_ SETHOTKEY** se termine.

Une touche d’accès rapide spécifique à un thread génère un message de [**\_ raccourci WM**](/windows/desktop/inputdev/wm-hotkey) qui est publié au début d’un thread particulier afin qu’il soit supprimé par l’itération suivante de la boucle de message. Une application définit une touche d’accès rapide spécifique au thread à l’aide de la fonction [**RegisterHotKey**](/windows/desktop/api/winuser/nf-winuser-registerhotkey) .

### <a name="hot-key-control-messages"></a>Messages de contrôle de touche d’accès rapide

Après la création d’un contrôle de touche d’accès rapide, une application interagit avec elle à l’aide de trois messages : [**hkm \_ SETRULES**](hkm-setrules.md), [**hkm \_ SETHOTKEY**](hkm-sethotkey.md)et [**hkm \_ GETHOTKEY**](hkm-gethotkey.md).

Une application peut envoyer le message [**hkm \_ SETRULES**](hkm-setrules.md) pour spécifier un ensemble de combinaisons de touches Ctrl, Alt et Maj qui sont considérées comme des touches d’accès rapide non valides. Si l’application spécifie une combinaison de touches non valide, elle doit également spécifier une combinaison de modificateurs par défaut à utiliser lorsque l’utilisateur sélectionne la combinaison non valide. Lorsque l’utilisateur entre dans la combinaison non valide, le système effectue une opération OR logique sur la combinaison non valide et la combinaison par défaut. Le résultat est considéré comme une combinaison valide ; elle est convertie en une chaîne et affichée dans le contrôle.

Le message [**hkm \_ SETHOTKEY**](hkm-sethotkey.md) permet à une application de définir la combinaison de touches d’accès rapide pour un contrôle de touche d’accès rapide. Ce message est également généralement utilisé lors de la création du contrôle de touche d’accès rapide.

Les applications utilisent le message [**hkm \_ GETHOTKEY**](hkm-gethotkey.md) pour récupérer le code de touche virtuel et les indicateurs de modificateur de la touche d’accès rapide choisie par l’utilisateur.

### <a name="hot-key-control-notifications"></a>Notifications de contrôle de touche d’accès rapide

Le contrôle de touche d’accès rapide n’envoie aucun code de notification via le message [**WM \_ Notify**](wm-notify.md) . Toutefois, il enverra la notification en [ \_ modification](en-change.md) via le message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) lorsque l’utilisateur modifie le contenu du contrôle.

### <a name="default-hot-key-message-processing"></a>Traitement par défaut des messages de touche d’accès rapide

Cette section décrit les messages de fenêtre gérés par la procédure de fenêtre pour la classe de fenêtre de [**raccourci clavier \_**](common-control-window-classes.md) prédéfinie utilisée avec les contrôles de touche d’accès rapide.



|                                                |                                                                                                                                                                                                                                                                                                                                               |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Message**                                    | **Traitement effectué**                                                                                                                                                                                                                                                                                                                      |
| [**\_caractère WM**](/windows/desktop/inputdev/wm-char)               | Récupère le code de la touche virtuelle.                                                                                                                                                                                                                                                                                                               |
| [**création de WM \_**](/windows/desktop/winmsg/wm-create)             | Initialise le contrôle de touche d’accès rapide, efface toutes les règles de touche d’accès rapide et utilise la police système.                                                                                                                                                                                                                                                          |
| [**\_ERASEBKGND WM**](/windows/desktop/winmsg/wm-erasebkgnd)     | Masque le signe insertion, appelle la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) et affiche à nouveau le signe insertion.                                                                                                                                                                                                                                     |
| [**\_GETDLGCODE WM**](/windows/desktop/dlgbox/wm-getdlgcode)     | Retourne une combinaison des valeurs [**DLGC \_ WANTCHARS**](/windows/desktop/dlgbox/wm-getdlgcode) et [**DLGC \_ WANTARROWS**](/windows/desktop/dlgbox/wm-getdlgcode) .                                                                                                                                               |
| [**WM \_ GETFONT**](/windows/desktop/winmsg/wm-getfont)           | Récupère la police.                                                                                                                                                                                                                                                                                                                           |
| [**WM- \_ touche**](/windows/desktop/inputdev/wm-keydown)         | Appelle la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) si la touche est entrée, Tab, barre d’espace, SUPPR, Echap ou retour arrière. Si la touche est Maj, CTRL ou ALT, elle vérifie si la combinaison est valide et, si c’est le cas, définit la touche d’accès rapide à l’aide de la combinaison. Toutes les autres clés sont définies en tant que clés à chaud sans que leur validité soit vérifiée en premier. |
| [**WM \_ KEYUP**](/windows/desktop/inputdev/wm-keyup)             | Récupère le code de la touche virtuelle.                                                                                                                                                                                                                                                                                                               |
| [**\_KILLFOCUS WM**](/windows/desktop/inputdev/wm-killfocus)     | Détruit le signe insertion.                                                                                                                                                                                                                                                                                                                           |
| [**\_LBUTTONDOWN WM**](/windows/desktop/inputdev/wm-lbuttondown) | Définit le focus sur la fenêtre.                                                                                                                                                                                                                                                                                                                 |
| [**\_NCCREATE WM**](/windows/desktop/winmsg/wm-nccreate)         | Définit le style de fenêtre [**WS \_ ex \_ CLIENTEDGE**](/windows/desktop/winmsg/extended-window-styles) .                                                                                                                                                                                                                              |
| [**\_peinture WM**](/windows/desktop/gdi/wm-paint)                  | Peint le contrôle de touche d’accès rapide.                                                                                                                                                                                                                                                                                                                   |
| [**WM \_ SetFocus**](/windows/desktop/inputdev/wm-setfocus)       | Crée et affiche le signe insertion.                                                                                                                                                                                                                                                                                                                  |
| [**\_SetFont WM**](/windows/desktop/winmsg/wm-setfont)           | Définit la police.                                                                                                                                                                                                                                                                                                                                |
| [**\_SYSCHAR WM**](/windows/desktop/menurc/wm-syschar)           | Récupère le code de la touche virtuelle.                                                                                                                                                                                                                                                                                                               |
| [**\_SYSKEYDOWN WM**](/windows/desktop/inputdev/wm-syskeydown)   | Appelle la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) si la touche est entrée, Tab, barre d’espace, SUPPR, Echap ou retour arrière. Si la touche est Maj, CTRL ou ALT, elle vérifie si la combinaison est valide et, si c’est le cas, définit la touche d’accès rapide à l’aide de la combinaison. Toutes les autres clés sont définies en tant que clés à chaud sans que leur validité soit vérifiée en premier. |
| [**\_SYSKEYUP WM**](/windows/desktop/inputdev/wm-syskeyup)       | Récupère le code de la touche virtuelle.                                                                                                                                                                                                                                                                                                               |



 

 

 