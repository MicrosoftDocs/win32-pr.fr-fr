---
title: Points de Portage
description: OpenGL n’a aucune commande pour dessiner un point unique. Sinon, les fonctions de point de Portage sont simples. Le tableau suivant répertorie les fonctions d’IRIS dans le GL pour les points de dessin et leurs fonctions OpenGL équivalentes.
ms.assetid: 348c7767-321a-43c6-bc88-7dc00f426f50
keywords:
- Portage de l’IRIS dans le GL, points
- Portage à partir de IRIS GL, points
- portage vers OpenGL à partir de IRIS GL, points
- Portage OpenGL à partir de IRIS GL, points
- fonctions de dessin, points
- points
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 322413cd6a11a589884bce2628e229984c7936ed
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106509811"
---
# <a name="porting-points"></a><span data-ttu-id="c5a2f-111">Points de Portage</span><span class="sxs-lookup"><span data-stu-id="c5a2f-111">Porting Points</span></span>

<span data-ttu-id="c5a2f-112">OpenGL n’a aucune commande pour dessiner un point unique.</span><span class="sxs-lookup"><span data-stu-id="c5a2f-112">OpenGL has no command to draw a single point.</span></span> <span data-ttu-id="c5a2f-113">Sinon, les fonctions de point de Portage sont simples.</span><span class="sxs-lookup"><span data-stu-id="c5a2f-113">Otherwise, porting point functions is straightforward.</span></span> <span data-ttu-id="c5a2f-114">Le tableau suivant répertorie les fonctions d’IRIS dans le GL pour les points de dessin et leurs fonctions OpenGL équivalentes.</span><span class="sxs-lookup"><span data-stu-id="c5a2f-114">The following table lists IRIS GL functions for drawing points and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="c5a2f-115">Fonction IRIS GL</span><span class="sxs-lookup"><span data-stu-id="c5a2f-115">IRIS GL function</span></span>           | <span data-ttu-id="c5a2f-116">Fonction OpenGL</span><span class="sxs-lookup"><span data-stu-id="c5a2f-116">OpenGL function</span></span>                                                   | <span data-ttu-id="c5a2f-117">Signification</span><span class="sxs-lookup"><span data-stu-id="c5a2f-117">Meaning</span></span>                                                                                                                                              |
|----------------------------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5a2f-118">**PNT**</span><span class="sxs-lookup"><span data-stu-id="c5a2f-118">**pnt**</span></span>                    |                                                                   | <span data-ttu-id="c5a2f-119">Dessine un point unique.</span><span class="sxs-lookup"><span data-stu-id="c5a2f-119">Draws a single point.</span></span>                                                                                                                                |
| <span data-ttu-id="c5a2f-120">**bgnpoint**, **point de terminaison**</span><span class="sxs-lookup"><span data-stu-id="c5a2f-120">**bgnpoint**, **endpoint**</span></span> | <span data-ttu-id="c5a2f-121">[**glBegin**](glbegin.md) ( \_ points GL), [ **glEnd**](glend.md)</span><span class="sxs-lookup"><span data-stu-id="c5a2f-121">[**glBegin**](glbegin.md) ( GL\_POINTS ), [**glEnd**](glend.md)</span></span> | <span data-ttu-id="c5a2f-122">Interprète les vertex comme des points.</span><span class="sxs-lookup"><span data-stu-id="c5a2f-122">Interprets vertices as points.</span></span>                                                                                                                       |
| <span data-ttu-id="c5a2f-123">**pntsize**</span><span class="sxs-lookup"><span data-stu-id="c5a2f-123">**pntsize**</span></span>                | [<span data-ttu-id="c5a2f-124">**glPointSize**</span><span class="sxs-lookup"><span data-stu-id="c5a2f-124">**glPointSize**</span></span>](glpointsize.md)                                | <span data-ttu-id="c5a2f-125">Définit la taille du point en pixels.</span><span class="sxs-lookup"><span data-stu-id="c5a2f-125">Sets point size in pixels.</span></span>                                                                                                                           |
| <span data-ttu-id="c5a2f-126">**pntsmooth**</span><span class="sxs-lookup"><span data-stu-id="c5a2f-126">**pntsmooth**</span></span>              | <span data-ttu-id="c5a2f-127">[**glEnable**](glenable.md) ( \_ Smooth point GL \_ )</span><span class="sxs-lookup"><span data-stu-id="c5a2f-127">[**glEnable**](glenable.md) ( GL\_POINT\_SMOOTH )</span></span>                | <span data-ttu-id="c5a2f-128">Active l’anticrénelage de point.</span><span class="sxs-lookup"><span data-stu-id="c5a2f-128">Turns on point antialiasing.</span></span> <span data-ttu-id="c5a2f-129">(Pour plus d’informations sur l’anticrénelage des points, consultez [Portage de fonctions d’anticrénelage](porting-antialiasing-functions.md).)</span><span class="sxs-lookup"><span data-stu-id="c5a2f-129">(For more information on point antialiasing, see [Porting Antialiasing Functions](porting-antialiasing-functions.md).)</span></span> |



 

<span data-ttu-id="c5a2f-130">Pour plus d’informations sur les fonctions d’extraction associées, consultez [**glPointSize**](glpointsize.md).</span><span class="sxs-lookup"><span data-stu-id="c5a2f-130">For information about related get functions, see [**glPointSize**](glpointsize.md).</span></span>

<span data-ttu-id="c5a2f-131">??</span><span class="sxs-lookup"><span data-stu-id="c5a2f-131">??</span></span>

 

 




