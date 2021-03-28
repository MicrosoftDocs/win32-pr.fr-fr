---
description: Une fenêtre ou un menu qui se trouve sur plus d’un moniteur entraîne une interruption visuelle pour une visionneuse. Pour réduire ce problème, le système affiche des menus et des fenêtres agrandies et agrandies sur une seule analyse. Le tableau suivant montre comment l’analyse est choisie.
ms.assetid: 9316c8dd-c9b7-49e2-a987-5949a87b0cfc
title: Positionnement des objets sur plusieurs moniteurs d’affichage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77149291737482fa0f3e7fe19ee4f350ee6521d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972567"
---
# <a name="positioning-objects-on-multiple-display-monitors"></a>Positionnement des objets sur plusieurs moniteurs d’affichage

Une fenêtre ou un menu qui se trouve sur plus d’un moniteur entraîne une interruption visuelle pour une visionneuse. Pour réduire ce problème, le système affiche des menus et des fenêtres agrandies et agrandies sur une seule analyse. Le tableau suivant montre comment l’analyse est choisie.



| Object         | Emplacement                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| window         | [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa)(ex) affiche une fenêtre sur le moniteur qui contient la plus grande partie de la fenêtre. Agrandit sur le moniteur qui contient la plus grande partie de la fenêtre avant qu’elle ne soit réduite.<br/> La combinaison de touches ALT-TAB affiche une fenêtre sur le moniteur qui contient la fenêtre actuellement active.<br/>                                                                                                                                          |
| fenêtre propriétaire   | sur le même moniteur que son propriétaire.                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| sous-menu        | Apparaît sur le moniteur qui contient la plus grande partie de l’élément de menu correspondant.                                                                                                                                                                                                                                                                                                                                                                                                          |
| menu contextuel   | Apparaît sur le moniteur où le clic droit s’est produit.                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| liste déroulante | Apparaît sur le moniteur qui contient le rectangle de la zone de liste déroulante.                                                                                                                                                                                                                                                                                                                                                                                                                           |
| boîte de dialogue     | Apparaît sur le moniteur de la fenêtre qui le possède. S’il est défini avec \_ le style DS CENTERMOUSE, il apparaît sur l’écran avec la souris.<br/> S’il n’a pas de propriétaire et que la fenêtre active et la boîte de dialogue se trouvent dans la même application, la boîte de dialogue s’affiche sur l’analyse de la fenêtre actuellement active.<br/> Si la boîte de dialogue n’a pas de propriétaire et que la fenêtre active n’est pas dans la même application que la boîte de dialogue, la boîte de dialogue s’affiche sur l’écran principal.<br/> |
| boîte de message    | Apparaît sur le moniteur de la fenêtre qui le possède.                                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

Si une fenêtre passe à deux moniteurs et que l’un des moniteurs est repositionné, le système positionne la fenêtre sur le moniteur qui contient la plus grande partie de la fenêtre d’origine.

Une application doit également placer des objets. Par exemple, il peut être nécessaire de créer une fenêtre sur le même moniteur qu’une autre fenêtre.

**Pour positionner un objet sur un système à plusieurs écrans**

1.  Déterminez l’analyse appropriée.
2.  Obtient les coordonnées du moniteur.
3.  Placez l’objet à l’aide des coordonnées.

En règle générale, vous allez positionner un objet sur le moniteur principal ou sur un moniteur sur lequel un objet est déjà présent. Pour identifier le moniteur d’un point, d’un rectangle ou d’une fenêtre donnés, utilisez [**MonitorFromPoint**](/windows/desktop/api/Winuser/nf-winuser-monitorfrompoint), [**MonitorFromRect**](/windows/desktop/api/Winuser/nf-winuser-monitorfromrect)et [**MonitorFromWindow**](/windows/desktop/api/Winuser/nf-winuser-monitorfromwindow).

Pour obtenir les coordonnées du moniteur, utilisez [**GetMonitorInfo**](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa), qui fournit à la fois la zone de travail et l’ensemble du rectangle d’analyse. Notez que les SM \_ CXSCREEN et SM \_ CYSCREEN font toujours référence à l’analyse principale, pas nécessairement à l’analyse qui affiche votre application. Évitez également le SM \_ xxVIRTUALSCREEN car il Centre votre fenêtre sur l’écran virtuel, et non sur une analyse.

Pour centrer les boîtes de dialogue dans la zone de travail d’une fenêtre, utilisez le \_ style de centre DS. Pour centrer la boîte de dialogue dans une fenêtre d’application, utilisez [**GetWindowRect**](/windows/win32/api/winuser/nf-winuser-getwindowrect). Windows restreint automatiquement les menus et les boîtes de dialogue à une analyse. Toutefois, il peut y avoir un problème pour les menus personnalisés, les zones déroulantes personnalisées, les palettes d’outils personnalisées et la position de l’application enregistrée.

Pour obtenir un exemple de la façon de positionner les objets correctement, consultez [positionnement des objets sur plusieurs configurations d’affichage](positioning-objects-on-a-multiple-display-setup.md).

L’utilisation \_ de SM CXSCREEN et SM \_ CYSCREEN pour déterminer l’emplacement d’une barre d’outils de bureau d’application (également appelée *appbar*) limite le appbar à l’analyse principale. Pour permettre à un appbar de se trouver sur n’importe quel bord d’une analyse, utilisez les mesures système appropriées pour calculer les bords des moniteurs. En outre, utilisez les macros **obten \_ X \_ lParam** et **obten \_ Y \_ lParam** pour extraire les coordonnées ; sinon, le signe des coordonnées peut être erroné. Ces macros sont incluses dans Windowsx. h.

La taille d’une fenêtre plein écran doit changer à mesure qu’elle se déplace entre les moniteurs avec des résolutions différentes. Pour ce faire, l’application doit vérifier la fenêtre dans laquelle elle se trouve, à l’aide de [**MonitorFromWindow**](/windows/desktop/api/Winuser/nf-winuser-monitorfromwindow) ou de [**MonitorFromPoint**](/windows/desktop/api/Winuser/nf-winuser-monitorfrompoint) , puis utiliser [**GetMonitorInfo**](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa) pour connaître la taille de l’analyse. Vous pouvez également utiliser **HMONITOR** à partir de la fonction DirectX **DirectDrawEnumerateEx** . Utilisez ensuite [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos) pour positionner et dimensionner la fenêtre pour couvrir l’analyse.

Une fenêtre agrandie ne couvre pas une barre des tâches qui a la propriété « Always on Top ». Toutefois, une fenêtre plein écran couvre la barre des tâches, par exemple dans les diaporamas et les jeux Microsoft PowerPoint.

Pour enregistrer et restaurer ultérieurement la position d’une fenêtre lorsqu’une application se ferme, utilisez les fonctions [**GetWindowPlacement**](/windows/win32/api/winuser/nf-winuser-getwindowplacement) et [**SetWindowPlacement**](/windows/win32/api/winuser/nf-winuser-setwindowplacement) . Toutefois, vérifiez que la position est toujours valide avant de l’utiliser, car l’analyse a pu être déplacée ou supprimée du système. L’application affiche la fenêtre sur l’écran principal si le **HMONITOR** d’une fenêtre n’est pas valide.

Le système tente de démarrer une application sur le moniteur qui contient son raccourci. Ainsi, l’une des façons de positionner une application consiste à avoir son raccourci sur un moniteur souhaité.

Si vous utilisez [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) ou [**ShellExecuteEx**](/windows/win32/api/shellapi/nf-shellapi-shellexecuteexa) , fournissez un *HWND* pour que le système ouvre toutes les nouvelles fenêtres sur le même moniteur que l’application appelante.

Notez que les valeurs de la structure [**minmaxinfo,**](/windows/win32/api/winuser/ns-winuser-minmaxinfo) sont légèrement modifiées pour un système avec plusieurs moniteurs.

 

 
