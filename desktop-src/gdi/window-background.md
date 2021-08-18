---
description: L’arrière-plan de la fenêtre est la couleur ou le motif utilisé pour remplir la zone cliente avant le début du dessin d’une fenêtre.
ms.assetid: d0613f9b-e65b-4de2-887d-2b642d36b22d
title: Arrière-plan de fenêtre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 819f3bf333728909bdd0e374d41b7665f0517bcc17666b88c58f610e0127d942
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119848939"
---
# <a name="window-background"></a>Arrière-plan de fenêtre

L’arrière-plan de la fenêtre est la couleur ou le motif utilisé pour remplir la zone cliente avant le début du dessin d’une fenêtre. L’arrière-plan de la fenêtre couvre tout ce qui se trouvait à l’écran avant le déplacement de la fenêtre, en effaçant les images existantes et en empêchant la nouvelle sortie de l’application d’être mélangée à des informations non liées.

Le système peint l’arrière-plan d’une fenêtre ou donne à la fenêtre la possibilité de le faire en lui envoyant un message [**WM \_ ERASEBKGND**](../winmsg/wm-erasebkgnd.md) quand l’application appelle [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint). Si une application ne traite pas le message, mais la transmet à [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca), le système efface l’arrière-plan en le remplissant avec le modèle dans le pinceau d’arrière-plan spécifié par la classe de la fenêtre. Si le pinceau n’est pas valide ou si la classe n’a pas de pinceau d’arrière-plan, le système définit le membre **fErase** dans la structure [**PAINTSTRUCT,**](/windows/win32/api/winuser/ns-winuser-paintstruct) que **BeginPaint** retourne, mais n’effectue aucune autre action. L’application a ensuite une deuxième chance de dessiner l’arrière-plan de la fenêtre, si nécessaire.

S’il traite [**WM \_ ERASEBKGND**](../winmsg/wm-erasebkgnd.md), l’application doit utiliser le paramètre *wParam* du message pour dessiner l’arrière-plan. Ce paramètre contient un handle vers le contexte de périphérique d’affichage pour la fenêtre. Une fois l’arrière-plan dessiné, l’application doit retourner une valeur différente de zéro. Cela garantit que [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) ne définit pas par erreur le membre **fErase** de la structure [**PAINTSTRUCT,**](/windows/win32/api/winuser/ns-winuser-paintstruct) sur une valeur différente de zéro (ce qui indique que l’arrière-plan doit être effacé) lorsque l’application traite le message de [**\_ peinture WM**](wm-paint.md) suivant.

Une application peut définir un pinceau d’arrière-plan de classe en assignant une poignée de pinceau ou une valeur de couleur système au membre **hbrBackground** de la structure [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) lors de l’inscription de la classe avec la fonction [**registerClass**](/windows/win32/api/winuser/nf-winuser-registerclassa) . La fonction [**GetStockObject**](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject) ou [**CreateSolidBrush**](/windows/desktop/api/Wingdi/nf-wingdi-createsolidbrush) peut être utilisée pour créer une poignée de pinceau. Une valeur de couleur système peut être l’une des valeurs définies pour la fonction [**SetSysColors**](/windows/win32/api/winuser/nf-winuser-setsyscolors) . (La valeur doit être augmentée d’une unité avant d’être assignée au membre.)

Une application peut traiter le message [**WM \_ ERASEBKGND**](../winmsg/wm-erasebkgnd.md) même si un pinceau d’arrière-plan de classe est défini. C’est généralement le cas dans les applications qui permettent à l’utilisateur de modifier la couleur ou le motif d’arrière-plan d’une fenêtre spécifiée sans affecter les autres fenêtres de la classe. Dans ce cas, l’application ne doit pas passer le message à [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).

Il n’est pas nécessaire qu’une application aligne les pinceaux, car le système dessine le pinceau à l’aide de l’origine de la fenêtre comme point de référence. À partir de cela, l’utilisateur peut déplacer la fenêtre sans affecter l’alignement des pinceaux de motif.

 

 
