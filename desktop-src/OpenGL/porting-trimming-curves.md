---
title: Portage des courbes de suppression
description: Les courbes de suppression OpenGL sont très similaires aux courbes de rognage de l’IRIS. Le tableau suivant répertorie les fonctions IRIS GL permettant de définir des courbes de rognage et leurs fonctions OpenGL équivalentes.
ms.assetid: 9aeea9ca-5ecd-4be1-853d-45b1566b263b
keywords:
- Portage de l’IRIS dans le grand livre, découpage des courbes
- Portage à partir de IRIS GL, courbes de rognage
- portage vers OpenGL à partir de IRIS GL, courbes de rognage
- Portage OpenGL à partir de IRIS GL, courbes de rognage
- courbes de rognage
- courbes
- Portage de l’IRIS dans le GL, courbes
- Portage à partir de IRIS GL, courbes
- portage vers OpenGL à partir de IRIS GL, courbes
- Portage OpenGL à partir de IRIS GL, courbes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cc82822b2e0b9e66729f0cb1a0e939d2775999c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104197163"
---
# <a name="porting-trimming-curves"></a><span data-ttu-id="ddfce-114">Portage des courbes de suppression</span><span class="sxs-lookup"><span data-stu-id="ddfce-114">Porting Trimming Curves</span></span>

<span data-ttu-id="ddfce-115">Les courbes de suppression OpenGL sont très similaires aux courbes de rognage de l’IRIS.</span><span class="sxs-lookup"><span data-stu-id="ddfce-115">OpenGL trimming curves are very similar to IRIS GL trimming curves.</span></span> <span data-ttu-id="ddfce-116">Le tableau suivant répertorie les fonctions IRIS GL permettant de définir des courbes de rognage et leurs fonctions OpenGL équivalentes.</span><span class="sxs-lookup"><span data-stu-id="ddfce-116">The following table lists the IRIS GL functions for defining trimming curves and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="ddfce-117">Fonction IRIS GL</span><span class="sxs-lookup"><span data-stu-id="ddfce-117">IRIS GL function</span></span> | <span data-ttu-id="ddfce-118">Fonction OpenGL</span><span class="sxs-lookup"><span data-stu-id="ddfce-118">OpenGL function</span></span>                        | <span data-ttu-id="ddfce-119">Signification</span><span class="sxs-lookup"><span data-stu-id="ddfce-119">Meaning</span></span>                              |
|------------------|----------------------------------------|--------------------------------------|
| <span data-ttu-id="ddfce-120">**bgntrim**</span><span class="sxs-lookup"><span data-stu-id="ddfce-120">**bgntrim**</span></span>      | [<span data-ttu-id="ddfce-121">**gluBeginTrim**</span><span class="sxs-lookup"><span data-stu-id="ddfce-121">**gluBeginTrim**</span></span>](glubegintrim.md)   | <span data-ttu-id="ddfce-122">Commence la définition de la courbe de délimitation.</span><span class="sxs-lookup"><span data-stu-id="ddfce-122">Begins trimming-curve definition.</span></span>    |
| <span data-ttu-id="ddfce-123">**pwlcurve**</span><span class="sxs-lookup"><span data-stu-id="ddfce-123">**pwlcurve**</span></span>     | [<span data-ttu-id="ddfce-124">**gluPwlCurve**</span><span class="sxs-lookup"><span data-stu-id="ddfce-124">**gluPwlCurve**</span></span>](glupwlcurve.md)     | <span data-ttu-id="ddfce-125">Définit une courbe linéaire par morceaux.</span><span class="sxs-lookup"><span data-stu-id="ddfce-125">Defines a piecewise linear curve.</span></span>    |
| <span data-ttu-id="ddfce-126">**nurbscurve**</span><span class="sxs-lookup"><span data-stu-id="ddfce-126">**nurbscurve**</span></span>   | [<span data-ttu-id="ddfce-127">**gluNurbsCurve**</span><span class="sxs-lookup"><span data-stu-id="ddfce-127">**gluNurbsCurve**</span></span>](glunurbscurve.md) | <span data-ttu-id="ddfce-128">Spécifie les attributs de la courbe de rognage.</span><span class="sxs-lookup"><span data-stu-id="ddfce-128">Specifies trimming-curve attributes.</span></span> |
| <span data-ttu-id="ddfce-129">**endtrim**</span><span class="sxs-lookup"><span data-stu-id="ddfce-129">**endtrim**</span></span>      | [<span data-ttu-id="ddfce-130">**gluEndTrim**</span><span class="sxs-lookup"><span data-stu-id="ddfce-130">**gluEndTrim**</span></span>](gluendtrim.md)       | <span data-ttu-id="ddfce-131">Termine la définition de la courbe de rognage.</span><span class="sxs-lookup"><span data-stu-id="ddfce-131">Ends trimming-curve definition.</span></span>      |



 

<span data-ttu-id="ddfce-132">??</span><span class="sxs-lookup"><span data-stu-id="ddfce-132">??</span></span>

 

 




