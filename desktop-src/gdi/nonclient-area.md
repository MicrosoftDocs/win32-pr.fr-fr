---
description: Le système envoie un \_ message WM NCPAINT à la fenêtre chaque fois qu’une partie de la zone non cliente de la fenêtre, telle que la barre de titre, la barre de menus ou le cadre de la fenêtre, doit être mise à jour.
ms.assetid: e4dc61f3-6a9f-4ed4-8685-62eb4ceb85f1
title: Zone non cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c51da31709f5bd9326cc0d05a9e37e2df78bfbb4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127415920"
---
# <a name="nonclient-area"></a>Zone non cliente

Le système envoie un message [**WM \_ NCPAINT**](wm-ncpaint.md) à la fenêtre chaque fois qu’une partie de la zone non cliente de la fenêtre, telle que la barre de titre, la barre de menus ou le cadre de la fenêtre, doit être mise à jour. Le système peut également envoyer d’autres messages pour indiquer à une fenêtre de mettre à jour une partie de sa zone cliente. par exemple, lorsqu’une fenêtre devient active ou inactive, elle envoie le message [**WM \_ NCACTIVATE**](../winmsg/wm-ncactivate.md) pour mettre à jour sa barre de titre. En général, le traitement de ces messages pour des fenêtres standard n’est pas recommandé, car l’application doit être en mesure de dessiner toutes les parties requises de la zone non cliente pour la fenêtre. Pour cette raison, la plupart des applications transmettent ces messages à [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) pour le traitement par défaut.

Une application qui crée des zones non clientes personnalisées pour ses fenêtres doit traiter ces messages. Dans ce cas, l’application doit utiliser un contexte de périphérique Windows pour effectuer le dessin dans la fenêtre. Le *contexte de périphérique Windows* permet à l’application de dessiner dans toutes les parties de la fenêtre, y compris la zone non cliente. Une application récupère un contexte de périphérique de fenêtre à l’aide de la fonction [**GetWindowDC**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc) ou [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) et, lorsque le dessin est terminé, doit libérer le contexte de périphérique de la fenêtre à l’aide de la fonction [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) .

Le système gère une région de mise à jour pour la zone non cliente. Quand une application reçoit un message [**WM \_ NCPAINT**](wm-ncpaint.md) , le paramètre *wParam* contient un handle vers une région définissant les dimensions de la région de mise à jour. L’application peut utiliser la poignée pour combiner la région de mise à jour avec la zone de découpage pour le contexte de périphérique Windows. Le système ne combine pas automatiquement la région de mise à jour lors de la récupération du contexte de périphérique Windows, à moins que l’application utilise [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) et spécifie à la fois le descripteur de région et l' \_ indicateur DCX INTERSECTRGN. Si l’application ne combine pas la région de mise à jour, seules les opérations de dessin qui s’étendent autrement en dehors de la fenêtre sont découpées. L’application n’est pas responsable de l’effacement de la région de mise à jour, qu’elle utilise ou non la région.

Si une application traite le message [**WM \_ NCACTIVATE**](../winmsg/wm-ncactivate.md) , une fois le traitement terminé, elle doit retourner la **valeur true** pour indiquer au système d’effectuer la modification de la fenêtre active. Si la fenêtre est réduite lorsque l’application reçoit le message **WM \_ NCACTIVATE** , elle doit transmettre le message à [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca). Dans ce cas, la fonction par défaut redessine l’étiquette de l’icône.

 

 
