---
description: Bien que les applications exécutent la plupart des opérations de dessin pendant le \_ traitement du message de peinture WM, il est parfois plus efficace pour une application de dessiner directement dans une fenêtre sans compter sur le \_ message WM Paint.
ms.assetid: 2d015879-58d2-4cbe-b1cc-445f2e8fd316
title: Dessin sans le message WM_PAINT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36ff9a18e923feceb33f961c9427852b2c2daddfcfc4e093809e24cd42f32869
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118250338"
---
# <a name="drawing-without-the-wm_paint-message"></a>Dessin sans le \_ message WM Paint

Bien que les applications exécutent la plupart des opérations de dessin pendant le traitement du message de [**\_ peinture WM**](wm-paint.md) , il est parfois plus efficace pour une application de dessiner directement dans une fenêtre sans compter sur le message **WM \_ Paint** . Cela peut être utile lorsque l’utilisateur a besoin d’un retour immédiat, par exemple lors de la sélection de texte et du déplacement ou du dimensionnement d’un objet. Dans ce cas, l’application se dessine généralement lors du traitement des messages du clavier ou de la souris.

Pour dessiner dans une fenêtre sans utiliser un message [**WM \_ Paint**](wm-paint.md) , l’application utilise la fonction [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) ou [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) pour récupérer un contexte de périphérique d’affichage pour la fenêtre. Avec le contexte de périphérique d’affichage, l’application peut dessiner dans la fenêtre et éviter toute intrusion dans d’autres fenêtres. Lorsque l’application a terminé le dessin, elle appelle la fonction [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) pour libérer le contexte de périphérique d’affichage en vue d’une utilisation par d’autres applications.

Quand vous dessinez sans utiliser un message [**WM \_ Paint**](wm-paint.md) , l’application n’invalide généralement pas la fenêtre. Au lieu de cela, il se dessine de manière à ce qu’il puisse facilement restaurer la fenêtre et supprimer le dessin. Par exemple, quand l’utilisateur sélectionne du texte ou un objet, l’application dessine généralement la sélection en inversant tout ce qui se trouve déjà dans la fenêtre. L’application peut supprimer la sélection et restaurer le contenu d’origine de la fenêtre en l’inverse simplement.

L’application est chargée de gérer attentivement les modifications apportées à la fenêtre. En particulier, si une application dessine une sélection et qu’un message de [**\_ peinture WM**](wm-paint.md) intermédiaire se produit, l’application doit s’assurer que tout dessin effectué pendant le message n’endommage pas la sélection. Pour éviter cela, de nombreuses applications suppriment la sélection, effectuent des opérations de dessin habituelles, puis restaurent la sélection lorsque le dessin est terminé.

 

 



