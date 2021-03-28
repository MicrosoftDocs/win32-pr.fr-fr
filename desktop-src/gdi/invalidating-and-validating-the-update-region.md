---
description: Une application invalide une partie d’une fenêtre et définit la région de mise à jour à l’aide de la fonction InvalidateRect ou InvalidateRgn.
ms.assetid: ec8abb77-47bc-4198-9daf-f2ccb0864ccc
title: Invalidation et validation de la région de mise à jour
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ba895875f9ec1350b6eb28ccb8f1721df6999ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972662"
---
# <a name="invalidating-and-validating-the-update-region"></a><span data-ttu-id="5d913-103">Invalidation et validation de la région de mise à jour</span><span class="sxs-lookup"><span data-stu-id="5d913-103">Invalidating and Validating the Update Region</span></span>

<span data-ttu-id="5d913-104">Une application invalide une partie d’une fenêtre et définit la région de mise à jour à l’aide de la fonction [**InvalidateRect**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect) ou [**InvalidateRgn**](/windows/desktop/api/Winuser/nf-winuser-invalidatergn) .</span><span class="sxs-lookup"><span data-stu-id="5d913-104">An application invalidates a portion of a window and sets the update region by using the [**InvalidateRect**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect) or [**InvalidateRgn**](/windows/desktop/api/Winuser/nf-winuser-invalidatergn) function.</span></span> <span data-ttu-id="5d913-105">Ces fonctions ajoutent le rectangle ou la région spécifié (dans les coordonnées clientes) à la zone de mise à jour, en combinant le rectangle ou la région avec tout ce que le système ou l’application a pu ajouter précédemment à la région de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="5d913-105">These functions add the specified rectangle or region (in client coordinates) to the update region, combining the rectangle or region with anything the system or the application may have previously added to the update region.</span></span>

<span data-ttu-id="5d913-106">Les fonctions [**InvalidateRect**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect) et [**InvalidateRgn**](/windows/desktop/api/Winuser/nf-winuser-invalidatergn) ne génèrent pas de messages de [**\_ peinture WM**](wm-paint.md) .</span><span class="sxs-lookup"><span data-stu-id="5d913-106">The [**InvalidateRect**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect) and [**InvalidateRgn**](/windows/desktop/api/Winuser/nf-winuser-invalidatergn) functions do not generate [**WM\_PAINT**](wm-paint.md) messages.</span></span> <span data-ttu-id="5d913-107">Au lieu de cela, le système accumule les modifications apportées par ces fonctions et ses propres modifications lorsqu’une fenêtre traite d’autres messages dans sa file d’attente de messages.</span><span class="sxs-lookup"><span data-stu-id="5d913-107">Instead, the system accumulates the changes made by these functions and its own changes while a window processes other messages in its message queue.</span></span> <span data-ttu-id="5d913-108">En cumulant les modifications, une fenêtre traite toutes les modifications à la fois au lieu de mettre à jour les bits et les éléments une étape à la fois.</span><span class="sxs-lookup"><span data-stu-id="5d913-108">By accumulating changes, a window processes all changes at once instead of updating bits and pieces one step at a time.</span></span>

<span data-ttu-id="5d913-109">Les fonctions [**ValidateRect**](/windows/desktop/api/Winuser/nf-winuser-validaterect) et [**ValidateRgn**](/windows/desktop/api/Winuser/nf-winuser-validatergn) valident une partie de la fenêtre en supprimant un rectangle ou une région spécifiés de la région de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="5d913-109">The [**ValidateRect**](/windows/desktop/api/Winuser/nf-winuser-validaterect) and [**ValidateRgn**](/windows/desktop/api/Winuser/nf-winuser-validatergn) functions validate a portion of the window by removing a specified rectangle or region from the update region.</span></span> <span data-ttu-id="5d913-110">Ces fonctions sont généralement utilisées lorsque la fenêtre a mis à jour une partie spécifique de l’écran dans la région de mise à jour avant de recevoir le message de [**\_ peinture WM**](wm-paint.md) .</span><span class="sxs-lookup"><span data-stu-id="5d913-110">These functions are typically used when the window has updated a specific part of the screen in the update region before receiving the [**WM\_PAINT**](wm-paint.md) message.</span></span>

 

 



