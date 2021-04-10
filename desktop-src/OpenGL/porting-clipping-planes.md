---
title: Portage des plans de découpage
description: OpenGL implémente les plans de découpage de la même façon que l’IRIS GL. En outre, dans OpenGL, vous pouvez interroger des plans de découpage. Le tableau suivant répertorie les fonctions d’IRIS dans le plan de découpage du GL et leurs fonctions OpenGL équivalentes.
ms.assetid: bfca59c3-b7ef-4545-8b8d-022ea782569b
keywords:
- Portage de l’IRIS dans le GL, plans de découpage
- Portage à partir de IRIS GL, plans de découpage
- portage vers OpenGL à partir de IRIS GL, plans de découpage
- Portage OpenGL à partir de IRIS GL, plans de découpage
- plans de découpage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3b531b39daf6670a3a99d9a4cbcf55158ea2d4f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675254"
---
# <a name="porting-clipping-planes"></a><span data-ttu-id="2c6ad-110">Portage des plans de découpage</span><span class="sxs-lookup"><span data-stu-id="2c6ad-110">Porting Clipping Planes</span></span>

<span data-ttu-id="2c6ad-111">OpenGL implémente les plans de découpage de la même façon que l’IRIS GL.</span><span class="sxs-lookup"><span data-stu-id="2c6ad-111">OpenGL implements clipping planes similarly to IRIS GL.</span></span> <span data-ttu-id="2c6ad-112">En outre, dans OpenGL, vous pouvez interroger des plans de découpage.</span><span class="sxs-lookup"><span data-stu-id="2c6ad-112">In addition, in OpenGL you can query clipping planes.</span></span> <span data-ttu-id="2c6ad-113">Le tableau suivant répertorie les fonctions d’IRIS dans le plan de découpage du GL et leurs fonctions OpenGL équivalentes.</span><span class="sxs-lookup"><span data-stu-id="2c6ad-113">The following table lists IRIS GL clipping plane functions and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="2c6ad-114">Fonction IRIS GL</span><span class="sxs-lookup"><span data-stu-id="2c6ad-114">IRIS GL function</span></span>                          | <span data-ttu-id="2c6ad-115">Fonction OpenGL</span><span class="sxs-lookup"><span data-stu-id="2c6ad-115">OpenGL function</span></span>                                                                               | <span data-ttu-id="2c6ad-116">Signification</span><span class="sxs-lookup"><span data-stu-id="2c6ad-116">Meaning</span></span>                                  |
|-------------------------------------------|-----------------------------------------------------------------------------------------------|------------------------------------------|
| <span data-ttu-id="2c6ad-117">**clipplane** (i, **CP \_ on**, params)</span><span class="sxs-lookup"><span data-stu-id="2c6ad-117">**clipplane** (i, **CP\_ON**, params)</span></span>     | <span data-ttu-id="2c6ad-118">[**glEnable**](glenable.md) ( \_ plan de coupe GL \_ )</span><span class="sxs-lookup"><span data-stu-id="2c6ad-118">[**glEnable**](glenable.md) ( GL\_CLIP\_PLANEi )</span></span>                                             | <span data-ttu-id="2c6ad-119">Active le découpage sur le plan i.</span><span class="sxs-lookup"><span data-stu-id="2c6ad-119">Enables clipping on plane i.</span></span>             |
| <span data-ttu-id="2c6ad-120">**clipplane**(i, **CP \_ define**, plan)</span><span class="sxs-lookup"><span data-stu-id="2c6ad-120">**clipplane**( i, **CP\_DEFINE**, plane )</span></span> | <span data-ttu-id="2c6ad-121">[**glClipPlane**](glclipplane.md) ( \_ plan de coupe GL \_ , plan)</span><span class="sxs-lookup"><span data-stu-id="2c6ad-121">[**glClipPlane**](glclipplane.md) ( GL\_CLIP\_PLANEi, plane )</span></span>                                | <span data-ttu-id="2c6ad-122">Définit le plan de découpage.</span><span class="sxs-lookup"><span data-stu-id="2c6ad-122">Defines clipping plane.</span></span>                  |
|                                           | [<span data-ttu-id="2c6ad-123">**glGetClipPlane**</span><span class="sxs-lookup"><span data-stu-id="2c6ad-123">**glGetClipPlane**</span></span>](glgetclipplane.md)                                                      | <span data-ttu-id="2c6ad-124">Retourne l’équation du plan de découpage.</span><span class="sxs-lookup"><span data-stu-id="2c6ad-124">Returns clipping plane equation.</span></span>         |
|                                           | <span data-ttu-id="2c6ad-125">[**glIsEnabled**](glisenabled.md) ( \_ plan de coupe GL \_ )</span><span class="sxs-lookup"><span data-stu-id="2c6ad-125">[**glIsEnabled**](glisenabled.md) ( GL\_CLIP\_PLANEi )</span></span>                                       | <span data-ttu-id="2c6ad-126">Retourne la valeur true si le plan de découpage est activé.</span><span class="sxs-lookup"><span data-stu-id="2c6ad-126">Returns true if clip plane i is enabled.</span></span> |
| <span data-ttu-id="2c6ad-127">**scrmask**</span><span class="sxs-lookup"><span data-stu-id="2c6ad-127">**scrmask**</span></span>                               | [<span data-ttu-id="2c6ad-128">**glScissor**</span><span class="sxs-lookup"><span data-stu-id="2c6ad-128">**glScissor**</span></span>](glscissor.md)                                                                | <span data-ttu-id="2c6ad-129">Définit la zone de ciseaux.</span><span class="sxs-lookup"><span data-stu-id="2c6ad-129">Defines the scissor box.</span></span>                 |
| <span data-ttu-id="2c6ad-130">**getscrmask**</span><span class="sxs-lookup"><span data-stu-id="2c6ad-130">**getscrmask**</span></span>                            | <span data-ttu-id="2c6ad-131">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) (zone de ciseaux de GL \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="2c6ad-131">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( GL\_SCISSOR\_BOX )</span></span> | <span data-ttu-id="2c6ad-132">Retourne la zone de la ciseaux actuelle.</span><span class="sxs-lookup"><span data-stu-id="2c6ad-132">Returns the current scissor box.</span></span>         |



 

<span data-ttu-id="2c6ad-133">Pour activer le test de ciseaux, appelez **glEnable** à l’aide de \_ \_ la zone de ciseaux du GL comme paramètre.</span><span class="sxs-lookup"><span data-stu-id="2c6ad-133">To turn on the scissor test, call **glEnable** using GL\_SCISSOR\_BOX as the parameter.</span></span>

<span data-ttu-id="2c6ad-134">??</span><span class="sxs-lookup"><span data-stu-id="2c6ad-134">??</span></span>

 

 




