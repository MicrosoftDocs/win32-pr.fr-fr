---
description: Une application effectue un test de positionnement sur les régions pour déterminer les coordonnées de la position actuelle du curseur.
ms.assetid: 861a2558-0967-43f6-be3f-580992da05ff
title: Régions de test de positionnement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe136c3ba9ab4babfc1150ae4c3eee878cb42327
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202035"
---
# <a name="hit-testing-regions"></a><span data-ttu-id="18eca-103">Régions de test de positionnement</span><span class="sxs-lookup"><span data-stu-id="18eca-103">Hit Testing Regions</span></span>

<span data-ttu-id="18eca-104">Une application effectue un test de positionnement sur les régions pour déterminer les coordonnées de la position actuelle du curseur.</span><span class="sxs-lookup"><span data-stu-id="18eca-104">An application performs hit testing on regions to determine the coordinates of the current cursor position.</span></span> <span data-ttu-id="18eca-105">Il transmet ensuite ces coordonnées, ainsi qu’un handle identifiant la région à la fonction [**PtInRegion**](/windows/desktop/api/Wingdi/nf-wingdi-ptinregion) .</span><span class="sxs-lookup"><span data-stu-id="18eca-105">Then it passes these coordinates as well as a handle identifying the region to the [**PtInRegion**](/windows/desktop/api/Wingdi/nf-wingdi-ptinregion) function.</span></span> <span data-ttu-id="18eca-106">Les coordonnées du curseur peuvent être récupérées en traitant les différents messages de la souris, tels que [**WM \_ LBUTTONDOWN**](../inputdev/wm-lbuttondown.md) , [**WM \_ LBUTTONUP**](../inputdev/wm-lbuttonup.md) , [**WM \_ RBUTTONDOWN**](../inputdev/wm-rbuttondown.md) et [**WM \_ RBUTTONUP**](../inputdev/wm-rbuttonup.md).</span><span class="sxs-lookup"><span data-stu-id="18eca-106">The cursor coordinates can be retrieved by processing the various mouse messages, such as [**WM\_LBUTTONDOWN**](../inputdev/wm-lbuttondown.md) , [**WM\_LBUTTONUP**](../inputdev/wm-lbuttonup.md) , [**WM\_RBUTTONDOWN**](../inputdev/wm-rbuttondown.md) , and [**WM\_RBUTTONUP**](../inputdev/wm-rbuttonup.md).</span></span> <span data-ttu-id="18eca-107">La valeur de retour pour PtInRegion indique si la position du curseur se trouve dans la région donnée.</span><span class="sxs-lookup"><span data-stu-id="18eca-107">The return value for PtInRegion indicates whether the cursor position is within the given region.</span></span>

 

 
