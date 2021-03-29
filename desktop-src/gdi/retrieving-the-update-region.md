---
description: Les fonctions GetUpdateRect et GetUpdateRgn récupèrent la région de mise à jour actuelle pour la fenêtre.
ms.assetid: c0729c4f-3b00-4ab9-91b2-4a2fecee8727
title: Récupération de la région de mise à jour
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8115f47a6c585d5b660d73bbf4fb3de21334b6c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202010"
---
# <a name="retrieving-the-update-region"></a><span data-ttu-id="36b72-103">Récupération de la région de mise à jour</span><span class="sxs-lookup"><span data-stu-id="36b72-103">Retrieving the Update Region</span></span>

<span data-ttu-id="36b72-104">Les fonctions [**GetUpdateRect**](/windows/desktop/api/Winuser/nf-winuser-getupdaterect) et [**GetUpdateRgn**](/windows/desktop/api/Winuser/nf-winuser-getupdatergn) récupèrent la région de mise à jour actuelle pour la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="36b72-104">The [**GetUpdateRect**](/windows/desktop/api/Winuser/nf-winuser-getupdaterect) and [**GetUpdateRgn**](/windows/desktop/api/Winuser/nf-winuser-getupdatergn) functions retrieve the current update region for the window.</span></span> <span data-ttu-id="36b72-105">GetUpdateRect récupère le plus petit rectangle (en coordonnées logiques) qui englobe la totalité de la région de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="36b72-105">GetUpdateRect retrieves the smallest rectangle (in logical coordinates) that encloses the entire update region.</span></span> <span data-ttu-id="36b72-106">GetUpdateRgn récupère la région de mise à jour elle-même.</span><span class="sxs-lookup"><span data-stu-id="36b72-106">GetUpdateRgn retrieves the update region itself.</span></span> <span data-ttu-id="36b72-107">Ces fonctions peuvent être utilisées pour calculer la taille actuelle de la région de mise à jour afin de déterminer où exécuter une opération de dessin.</span><span class="sxs-lookup"><span data-stu-id="36b72-107">These functions can be used to calculate the current size of the update region to determine where to carry out a drawing operation.</span></span>

<span data-ttu-id="36b72-108">[**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) récupère également les dimensions du plus petit rectangle qui englobe la région de mise à jour actuelle, en copiant les dimensions dans le membre **rcPaint** de la structure [**PAINTSTRUCT,**](/windows/win32/api/winuser/ns-winuser-paintstruct) .</span><span class="sxs-lookup"><span data-stu-id="36b72-108">[**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) also retrieves the dimensions of the smallest rectangle enclosing the current update region, copying the dimensions to the **rcPaint** member in the [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct) structure.</span></span> <span data-ttu-id="36b72-109">Étant donné que **BeginPaint** valide la région de mise à jour, tout appel à [**GetUpdateRect**](/windows/desktop/api/Winuser/nf-winuser-getupdaterect) et [**GetUpdateRgn**](/windows/desktop/api/Winuser/nf-winuser-getupdatergn) immédiatement après un appel à **BeginPaint** retourne une région de mise à jour vide.</span><span class="sxs-lookup"><span data-stu-id="36b72-109">Because **BeginPaint** validates the update region, any call to [**GetUpdateRect**](/windows/desktop/api/Winuser/nf-winuser-getupdaterect) and [**GetUpdateRgn**](/windows/desktop/api/Winuser/nf-winuser-getupdatergn) immediately after a call to **BeginPaint** returns an empty update region.</span></span>

 

 



