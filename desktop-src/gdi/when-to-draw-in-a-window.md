---
description: 'Une application se dessine dans une fenêtre à plusieurs moments : lors de la création d’une fenêtre, lors de la modification de la taille de la fenêtre, lors du déplacement de la fenêtre depuis une autre fenêtre, lors de la réduction ou de l’agrandissement de la fenêtre, lors de l’affichage des données d’un fichier ouvert, lors du défilement, de la modification ou de la sélection d’une partie des'
ms.assetid: 4b5d6842-5707-4884-a55a-e09e342cea46
title: Quand dessiner dans une fenêtre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 832f219ad15fa919715b0f6892b73686237e1c3681e298106db3cefc4a8c3ec0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119468089"
---
# <a name="when-to-draw-in-a-window"></a>Quand dessiner dans une fenêtre

Une application se dessine dans une fenêtre à plusieurs moments : lors de la création d’une fenêtre, lors de la modification de la taille de la fenêtre, lors du déplacement de la fenêtre depuis une autre fenêtre, lors de la réduction ou de l’agrandissement de la fenêtre, lors de l’affichage des données d’un fichier ouvert, lors du défilement, de la modification ou de la sélection d’une partie des

Le système gère des actions telles que le déplacement et le redimensionnement d’une fenêtre. Si une action affecte le contenu de la fenêtre, le système marque la partie affectée de la fenêtre comme prête pour la mise à jour et, lors de la prochaine occasion, envoie un message de [**\_ peinture WM**](wm-paint.md) à la procédure de fenêtre de la fenêtre. Le message est un signal à l’application pour déterminer ce qui doit être mis à jour et pour effectuer le dessin nécessaire.

Certaines actions sont gérées par l’application, telles que l’affichage des fichiers ouverts et la sélection des données affichées. Pour ces actions, une application peut marquer pour mettre à jour la partie de la fenêtre affectée par l’action, ce qui entraîne l’envoi d’un message de [**\_ peinture WM**](wm-paint.md) à la prochaine occasion. Si une action requiert un retour immédiat, l’application peut dessiner pendant que l’action a lieu, sans attendre la **\_ peinture WM**. Par exemple, une application classique met en surbrillance la zone sélectionnée par l’utilisateur au lieu d’attendre le prochain message de **\_ peinture WM** pour mettre à jour la zone.

Dans tous les cas, une application peut dessiner dans une fenêtre dès sa création. Pour dessiner dans la fenêtre, l’application doit d’abord récupérer un handle vers un contexte de périphérique d’affichage pour la fenêtre. Dans l’idéal, une application effectue la plupart de ses opérations de dessin pendant le traitement des messages [**WM \_ Paint**](wm-paint.md) . Dans ce cas, l’application récupère un contexte de périphérique d’affichage en appelant la fonction [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) . Si une application est dessinée à tout moment, par exemple à partir de [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) ou pendant le traitement des messages du clavier ou de la souris, elle appelle la fonction [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) ou [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) pour récupérer le DC d’affichage.

 

 
