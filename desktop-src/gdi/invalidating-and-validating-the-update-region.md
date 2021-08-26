---
description: Une application invalide une partie d’une fenêtre et définit la région de mise à jour à l’aide de la fonction InvalidateRect ou InvalidateRgn.
ms.assetid: ec8abb77-47bc-4198-9daf-f2ccb0864ccc
title: Invalidation et validation de la région de mise à jour
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6813d88674ef0339cfd3501b561e5a7c95fa5b41f0c7f212e625f9846f5beb5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119944169"
---
# <a name="invalidating-and-validating-the-update-region"></a>Invalidation et validation de la région de mise à jour

Une application invalide une partie d’une fenêtre et définit la région de mise à jour à l’aide de la fonction [**InvalidateRect**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect) ou [**InvalidateRgn**](/windows/desktop/api/Winuser/nf-winuser-invalidatergn) . Ces fonctions ajoutent le rectangle ou la région spécifié (dans les coordonnées clientes) à la zone de mise à jour, en combinant le rectangle ou la région avec tout ce que le système ou l’application a pu ajouter précédemment à la région de mise à jour.

Les fonctions [**InvalidateRect**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect) et [**InvalidateRgn**](/windows/desktop/api/Winuser/nf-winuser-invalidatergn) ne génèrent pas de messages de [**\_ peinture WM**](wm-paint.md) . Au lieu de cela, le système accumule les modifications apportées par ces fonctions et ses propres modifications lorsqu’une fenêtre traite d’autres messages dans sa file d’attente de messages. En cumulant les modifications, une fenêtre traite toutes les modifications à la fois au lieu de mettre à jour les bits et les éléments une étape à la fois.

Les fonctions [**ValidateRect**](/windows/desktop/api/Winuser/nf-winuser-validaterect) et [**ValidateRgn**](/windows/desktop/api/Winuser/nf-winuser-validatergn) valident une partie de la fenêtre en supprimant un rectangle ou une région spécifiés de la région de mise à jour. Ces fonctions sont généralement utilisées lorsque la fenêtre a mis à jour une partie spécifique de l’écran dans la région de mise à jour avant de recevoir le message de [**\_ peinture WM**](wm-paint.md) .

 

 



