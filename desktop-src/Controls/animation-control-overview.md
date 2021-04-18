---
title: À propos des contrôles d’animation
description: Un contrôle d’animation est une fenêtre qui affiche un clip Audio-Video entrelacé (AVI). Un clip AVI est une série de frames bitmap tels qu’un film. Les contrôles d’animation peuvent uniquement afficher des clips AVI qui ne contiennent pas de données audio.
ms.assetid: 6be69d1a-5b2c-41d5-b6d7-e86ddac2cb0d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1625828e5f4febce7314da365c9db93ce3a07136
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "106509280"
---
# <a name="about-animation-controls"></a>À propos des contrôles d’animation

Un *contrôle d’animation* est une fenêtre qui affiche un clip Audio-Video entrelacé (AVI). Un clip AVI est une série de frames bitmap tels qu’un film. Les contrôles d’animation peuvent uniquement afficher des clips AVI qui ne contiennent pas de données audio.

Une utilisation courante d’un contrôle d’animation consiste à indiquer l’activité du système au cours d’une opération de longue durée. Cela est possible, car le thread d’opération continue de s’exécuter pendant que le clip AVI est affiché. Par exemple, la boîte de dialogue Rechercher de l’Explorateur Windows affiche une loupe mobile lorsque le système recherche un fichier.

> [!Note]  
> Si vous utilisez ComCtl32.dll version 6, le thread n’est pas pris en charge ; Assurez-vous que votre application ne bloque pas l’interface utilisateur, sinon l’animation ne se produira pas.

 

Un contrôle d’animation peut afficher un clip AVI provenant d’un fichier AVI non compressé ou d’un fichier AVI compressé à l’aide de l’encodage d’exécution (BI \_ RLE8). Vous pouvez ajouter le clip AVI à votre application en tant que ressource AVI, ou le clip peut accompagner votre application sous la forme d’un fichier AVI distinct.

> [!Note]  
> Le fichier AVI, ou ressource, ne doit pas avoir de canal sonore. Les fonctionnalités du contrôle d’animation sont très limitées et peuvent faire l’objet de modifications. Si vous avez besoin d’un contrôle pour fournir des fonctionnalités de lecture et d’enregistrement multimédias pour votre application, vous pouvez utiliser le contrôle MCIWnd. Pour plus d’informations, consultez [classe de fenêtre MCIWnd](/windows/desktop/Multimedia/mciwnd-window-class).

 

Cette section décrit les rubriques suivantes.

-   [Création d’un contrôle d’animation](#animation-control-creation)
-   [À propos des messages de contrôle d’animation](#about-animation-control-messages)
-   [Traitement des messages par défaut](#default-message-processing)

## <a name="animation-control-creation"></a>Création d’un contrôle d’animation

Un contrôle d’animation appartient à la classe de fenêtre [**animer la \_ classe**](common-control-window-classes.md) . Vous créez un contrôle d’animation à l’aide de la fonction [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) ou [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) ou de la macro [**Animate \_ Create**](/windows/desktop/api/Commctrl/nf-commctrl-animate_create) . La macro positionne le contrôle d’animation dans l’angle supérieur gauche de la fenêtre parente et, si le style de [**\_ Centre ACS**](animation-control-styles.md) n’est pas spécifié, définit la largeur et la hauteur du contrôle en fonction des dimensions d’un cadre dans le clip avi. Si **le \_ Centre ACS** est spécifié, l' **animation \_ créer** affecte la valeur zéro à la largeur et à la hauteur du contrôle. Vous pouvez utiliser la fonction [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) pour définir la position et la taille du contrôle.

Si vous créez un contrôle d’animation dans une boîte de dialogue ou à partir d’une ressource de boîte de dialogue, le contrôle est détruit automatiquement lorsque l’utilisateur ferme la boîte de dialogue. Si vous créez un contrôle d’animation dans une fenêtre, vous devez détruire explicitement le contrôle.

## <a name="about-animation-control-messages"></a>À propos des messages de contrôle d’animation

Une application envoie des messages à un contrôle d’animation pour ouvrir, lire, arrêter et fermer le clip AVI correspondant. Chaque message comporte une ou plusieurs macros que vous pouvez utiliser au lieu d’envoyer le message explicitement.

Après la création d’un contrôle d’animation, une application envoie le message [**ACM \_ Open**](acm-open.md) pour ouvrir un clip AVI et le charger en mémoire. Le message spécifie le chemin d’accès d’un fichier AVI ou le nom d’une ressource AVI. Le système charge la ressource AVI à partir du module qui a créé le contrôle d’animation.

Si le contrôle d’animation a le style d' [**\_ exécution automatique**](animation-control-styles.md) des services ACS, le contrôle commence la lecture du clip AVI immédiatement après l’ouverture du fichier AVI ou de la ressource avi. Dans le cas contraire, une application peut utiliser le message de [**\_ lecture ACM**](acm-play.md) pour démarrer le clip avi. Une application peut arrêter le clip à tout moment en envoyant le message d' [**\_ arrêt ACM**](acm-stop.md) . La dernière image lue reste affichée lorsque le contrôle termine la lecture du clip AVI ou lorsque l' **\_ arrêt ACM** est envoyé.

Un contrôle d’animation peut envoyer deux codes de notification à sa fenêtre parente : [ACN \_ Start](acn-start.md) et [ACN \_ Stop](acn-stop.md). La plupart des applications ne gèrent aucune notification.

Pour fermer le fichier AVI ou la ressource AVI et le supprimer de la mémoire, une application peut utiliser la macro [**Animate \_ Close**](/windows/desktop/api/Commctrl/nf-commctrl-animate_close) , qui envoie l' [**ACM \_ Open**](acm-open.md) avec le nom de fichier ou le nom de la ressource ayant la valeur **null**.

## <a name="default-message-processing"></a>Traitement des messages par défaut

Cette section décrit les messages de fenêtre gérés par la procédure de fenêtre pour la classe de fenêtre [**animer la \_ classe**](common-control-window-classes.md) .



| Message                                    | Traitement effectué                                                                                                                                                                                                                                                                        |
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_Fermer WM**](/windows/desktop/winmsg/wm-close)           | Libère le fichier AVI ou la ressource AVI associée au contrôle animation.                                                                                                                                                                                                                   |
| [**\_destructeur WM**](/windows/desktop/winmsg/wm-destroy)       | Libère le fichier AVI ou la ressource AVI, libère une structure de données interne, puis appelle la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) .                                                                                                                                                |
| [**\_ERASEBKGND WM**](/windows/desktop/winmsg/wm-erasebkgnd) | Efface l’arrière-plan de la fenêtre à l’aide de la couleur d’arrière-plan actuelle pour les contrôles statiques.                                                                                                                                                                                                        |
| [**\_NCCREATE WM**](/windows/desktop/winmsg/wm-nccreate)     | Alloue et Initialise une structure de données interne, puis appelle [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).                                                                                                                                                                              |
| [**\_NCHITTEST WM**](/windows/desktop/inputdev/wm-nchittest) | Retourne la valeur du test de positionnement HTTRANSPARENT.                                                                                                                                                                                                                                                   |
| [**\_peinture WM**](/windows/desktop/gdi/wm-paint)              | Dessine un frame AVI dans le contrôle d’animation.                                                                                                                                                                                                                                                |
| [**taille du WM \_**](/windows/desktop/winmsg/wm-size)             | Vérifie si le contrôle a le style de [**\_ Centre ACS**](animation-control-styles.md) . Si le contrôle ne le fait pas, il appelle [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca). Dans le cas contraire, il Centre l’animation dans le contrôle, invalide le contrôle, puis appelle **DefWindowProc**. |



 

 

 