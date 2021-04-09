---
title: À propos des contrôles Up-Down
description: Un contrôle up-up est une paire de boutons fléchés sur lesquels l’utilisateur peut cliquer pour incrémenter ou décrémenter une valeur, telle qu’une position de défilement ou un nombre affiché dans un contrôle auxiliaire (appelé fenêtre associée).
ms.assetid: ae2c0283-9cad-40d1-b8a6-a90484a95f56
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cc8dad15a8254b138cae4175cc16b1ef3111745
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730581"
---
# <a name="about-up-down-controls"></a>À propos des contrôles Up-Down

Un contrôle up-up est une paire de boutons fléchés sur lesquels l’utilisateur peut cliquer pour incrémenter ou décrémenter une valeur, telle qu’une position de défilement ou un nombre affiché dans un contrôle auxiliaire (appelé fenêtre associée).

Pour l’utilisateur, un contrôle up-out et sa fenêtre associée se présentent souvent comme un seul contrôle. Vous pouvez spécifier qu’un contrôle up-up se positionne automatiquement en regard de sa fenêtre associée et qu’il définit automatiquement la légende de la fenêtre associée à sa position actuelle. Par exemple, vous pouvez utiliser un contrôle up-up avec un contrôle d’édition pour inviter l’utilisateur à entrer des données numériques. L’illustration suivante montre un contrôle up-up avec un contrôle d’édition comme fenêtre associée, une combinaison parfois appelée contrôle Spinner.

![capture d’écran montrant un contrôle rectangulaire concis avec des flèches vers le haut et vers le bas sur le bord droit](images/updown.jpg)

Les rubriques suivantes sont présentées dans cette section.

-   [Styles de contrôle up-up](#up-down-control-styles)
-   [Position et accélération](#position-and-acceleration)
-   [Up-Down par défaut contrôle le traitement des messages](#default-up-down-controls-message-processing)

## <a name="up-down-control-styles"></a>Styles de contrôle Up-Down

À l’aide des styles de fenêtre, vous pouvez manipuler les caractéristiques d’un contrôle up-up, par exemple comment il se positionne par rapport à la fenêtre associée, s’il définit le texte de la fenêtre associée et s’il traite les touches haut et bas.

Un contrôle up-up avec le style d’un type d’inscription d’un niveau d’inscription ou d' [**uds \_**](up-down-control-styles.md) s’aligne sur le bord gauche ou droit [**de la fenêtre \_**](up-down-control-styles.md) associée. La largeur de la fenêtre associée est réduite pour s’adapter à la largeur du contrôle up-up.

Un contrôle up-up avec le style [**uds \_ SETBUDDYINT**](up-down-control-styles.md) définit la légende de la fenêtre associée à chaque fois que la position actuelle change. Le contrôle insère un séparateur des milliers entre les trois chiffres d’une chaîne décimale, à moins que le style « [**uds \_ nomilles**](up-down-control-styles.md) » soit spécifié. Si la fenêtre associée est une zone de liste, un contrôle up-up définit sa sélection actuelle au lieu de sa légende.

Vous pouvez spécifier le style [**uds \_ ARROWKEYS**](up-down-control-styles.md) pour fournir une interface de clavier pour un contrôle up-up. Si ce style est spécifié, le contrôle traite les touches de direction haut et bas. Le contrôle sous-classe également la fenêtre associée afin qu’il puisse traiter ces clés lorsque la fenêtre associée a le focus.

Si vous utilisez un contrôle up-up pour le défilement horizontal, vous pouvez spécifier le [**style \_ d’UDS**](up-down-control-styles.md) . Ce style amène les flèches du contrôle up-up à pointer vers la gauche et vers la droite, et non vers le haut et vers le bas.

Par défaut, la position actuelle ne change pas si l’utilisateur tente de l’incrémenter ou de la décrémenter au-delà de la valeur maximale ou minimale. Vous pouvez modifier ce comportement en utilisant le style d' [**\_ habillage uds**](up-down-control-styles.md) , afin que la position « habille » à l’extrême opposée. Par exemple, l’incrémentation au-delà de la limite supérieure ramène la position à la limite inférieure.

## <a name="position-and-acceleration"></a>Position et accélération

Après la création d’un contrôle up-out, vous pouvez modifier la position actuelle, la position minimale et la position maximale du contrôle en envoyant des messages. Vous pouvez également modifier la base de base utilisée pour afficher la position actuelle dans la fenêtre associée et la vitesse à laquelle la position actuelle change lorsque l’utilisateur clique sur la flèche haut ou bas.

Pour récupérer la position actuelle d’un contrôle up-up, utilisez le message [**UDM \_ GETPOS**](udm-getpos.md) . Pour un contrôle up-up avec une fenêtre associée, la position actuelle est le nombre dans la légende de la fenêtre associée. Étant donné que la légende peut avoir changé (par exemple, l’utilisateur a peut-être modifié le texte d’un contrôle d’édition), le contrôle up-out récupère la légende actuelle et met à jour sa position actuelle en conséquence.

La légende de la fenêtre associée peut être une chaîne décimale ou hexadécimale, en fonction de la base de base (autrement dit, de base 10 ou 16) du contrôle up-up. Vous pouvez définir la base de base à l’aide du message [**UDM \_ SETBASE**](udm-setbase.md) et récupérer la base de base à l’aide du message [**UDM \_ getBase (**](udm-getbase.md) .

Le message [**UDM \_ SetPos**](udm-setpos.md) définit la position actuelle d’une fenêtre associée. Notez qu’à la différence d’une barre de défilement, un contrôle up-up modifie automatiquement sa position actuelle lorsqu’un utilisateur clique sur les flèches vers le haut et vers le bas. Une application, par conséquent, n’a pas besoin de définir la position actuelle lors du traitement du message [**WM \_ VSCROLL**](wm-vscroll.md) ou [**WM \_ HSCROLL**](wm-hscroll.md) .

Vous pouvez modifier les positions minimale et maximale d’un contrôle up-up en utilisant le message [**UDM \_ SetRange**](udm-setrange.md) . La position maximale peut être inférieure à la valeur minimale et, dans ce cas, un clic sur le bouton fléché vers le haut réduit la position actuelle. En d’autres termes, le fait de remonter vers la position maximale. Pour récupérer les positions minimale et maximale d’un contrôle up-up, utilisez le message [**UDM \_ GETRANGE**](udm-getrange.md) .

Vous pouvez contrôler la fréquence à laquelle la position change lorsque l’utilisateur maintient le bouton fléché enfoncé en définissant l’accélération du contrôle up-up. L’accélération est définie par un tableau de structures [**UDACCEL**](/windows/desktop/api/Commctrl/ns-commctrl-udaccel) . Chaque structure spécifie un intervalle de temps et le nombre d’unités d’incrémentation ou de décrémentation à la fin de cet intervalle. Pour définir l’accélération, utilisez le message [**UDM \_ SETACCEL**](udm-setaccel.md) . Pour récupérer les informations d’accélération, utilisez le message [**UDM \_ GETACCEL**](udm-getaccel.md) .

## <a name="default-up-down-controls-message-processing"></a>Up-Down par défaut contrôle le traitement des messages

Cette section décrit les messages Windows standard traités par un contrôle up-out.



| Message                                        | Traitement effectué                                                                                                                                                                                         |
|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**création de WM \_**](/windows/desktop/winmsg/wm-create)             | Alloue et Initialise une structure de données privée et enregistre son adresse sous forme de données de fenêtre.                                                                                                                     |
| [**\_destructeur WM**](/windows/desktop/winmsg/wm-destroy)           | Libère les données allouées pendant le traitement de [**\_ Create WM**](/windows/desktop/winmsg/wm-create) .                                                                                                                                   |
| [**\_activer WM**](/windows/desktop/winmsg/wm-enable)             | Invalide la fenêtre.                                                                                                                                                                                      |
| [**WM- \_ touche**](/windows/desktop/inputdev/wm-keydown)         | Modifie la position actuelle dans le cas d’une flèche haut ou flèche bas.                                                                                                                                   |
| [**WM \_ KEYUP**](/windows/desktop/inputdev/wm-keyup)             | Termine la modification de la position.                                                                                                                                                                               |
| [**\_LBUTTONDOWN WM**](/windows/desktop/inputdev/wm-lbuttondown) | Capture la souris. Si la fenêtre associée est un contrôle d’édition ou une zone de liste, elle définit le focus sur la fenêtre associée. Si la souris se trouve au-dessus du bouton haut ou de la flèche vers le haut, elle commence à modifier la position et définit un minuteur. |
| [**\_LBUTTONUP WM**](/windows/desktop/inputdev/wm-lbuttonup)     | Termine la modification de la position et libère la capture de la souris si le contrôle up-up a capturé la souris. Si la fenêtre associée est un contrôle d’édition, elle sélectionne tout le texte du contrôle d’édition.             |
| [**\_peinture WM**](/windows/desktop/gdi/wm-paint)                  | Peint le contrôle up-up. Si le paramètre *wParam* est non null, le contrôle suppose que la valeur est un **HDC** et peint à l’aide de ce contexte de périphérique.                                                    |
| [**\_minuteur WM**](/windows/desktop/winmsg/wm-timer)               | Modifie la position actuelle si la souris est maintenue sur un bouton et qu’un intervalle suffisant s’est écoulé.                                                                                            |



 

 

 