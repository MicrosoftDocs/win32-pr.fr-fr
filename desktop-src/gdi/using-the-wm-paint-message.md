---
description: Vous pouvez utiliser le \_ message WM Paint pour effectuer les dessins nécessaires à l’affichage des informations.
ms.assetid: cc56745f-95d0-4607-a206-1e7ed7109bf0
title: Utilisation du message WM_PAINT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1969d5aae7e64ad74d8070c7515daa6e9e782135ce0af54b49c7faab07f5d34
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119037447"
---
# <a name="using-the-wm_paint-message"></a>Utilisation du \_ message WM Paint

Vous pouvez utiliser le message [**WM \_ Paint**](wm-paint.md) pour effectuer les dessins nécessaires à l’affichage des informations. Étant donné que le système envoie des \_ messages de peinture WM à votre application lorsque celle-ci doit être mise à jour ou lorsque vous demandez explicitement une mise à jour, vous pouvez consolider le code pour le dessin dans la procédure de fenêtre de votre application. Vous pouvez ensuite utiliser ce code chaque fois que votre application doit dessiner des informations nouvelles ou existantes.

Les sections suivantes présentent différentes façons d’utiliser le \_ message de peinture WM pour dessiner dans une fenêtre :

-   [Dessin dans la zone cliente](drawing-in-the-client-area.md)
-   [Redessin de la zone cliente entière](redrawing-the-entire-client-area.md)
-   [Redessiner dans la région de mise à jour](redrawing-in-the-update-region.md)
-   [Invalidation de la zone cliente](invalidating-the-client-area.md)
-   [Dessin d’une fenêtre réduite](drawing-a-minimized-window.md)
-   [Dessin d’un arrière-plan de fenêtre personnalisé](drawing-a-custom-window-background.md)

 

 



