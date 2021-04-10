---
title: Portage de fonctions qui obtiennent des matrices et des transformations
description: Le tableau suivant répertorie les fonctions d’IRIS GL qui obtiennent l’état des matrices et des transformations et leurs équivalents OpenGL.
ms.assetid: 53546bc0-ce1d-47e0-ab5e-5d6789c6db2a
keywords:
- Portage de l’IRIS dans le GL, matrices
- Portage à partir de IRIS GL, matrices
- portage vers OpenGL à partir de IRIS GL, matrices
- Portage OpenGL à partir de IRIS GL, matrices
- matrices
- Portage de l’IRIS dans le GL, transformations
- Portage à partir de IRIS GL, transformations
- portage vers OpenGL à partir de IRIS GL, transformations
- Portage OpenGL depuis IRIS GL, transformations
- transformations
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93b32ab017e81c9875666785786b29d9c94c7fd1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940070"
---
# <a name="porting-functions-that-get-matrices-and-transformations"></a><span data-ttu-id="f9803-113">Portage de fonctions qui obtiennent des matrices et des transformations</span><span class="sxs-lookup"><span data-stu-id="f9803-113">Porting Functions that Get Matrices and Transformations</span></span>

<span data-ttu-id="f9803-114">Le tableau suivant répertorie les fonctions d’IRIS GL qui obtiennent l’état des matrices et des transformations et leurs équivalents OpenGL.</span><span class="sxs-lookup"><span data-stu-id="f9803-114">The following table lists the IRIS GL functions that get the state of matrices and transformations and their OpenGL equivalents.</span></span>



| <span data-ttu-id="f9803-115">Requête Matrix GL IRIS</span><span class="sxs-lookup"><span data-stu-id="f9803-115">IRIS GL matrix query</span></span>                  | <span data-ttu-id="f9803-116">Requête de matrice glGet OpenGL</span><span class="sxs-lookup"><span data-stu-id="f9803-116">OpenGL glGet matrix query</span></span>         | <span data-ttu-id="f9803-117">Signification</span><span class="sxs-lookup"><span data-stu-id="f9803-117">Meaning</span></span>                                                         |
|---------------------------------------|-----------------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="f9803-118">**getmmode**</span><span class="sxs-lookup"><span data-stu-id="f9803-118">**getmmode**</span></span>                          | <span data-ttu-id="f9803-119">\_mode de matrice du GL \_</span><span class="sxs-lookup"><span data-stu-id="f9803-119">GL\_MATRIX\_MODE</span></span>                  | <span data-ttu-id="f9803-120">Retourne le mode matrice actuel.</span><span class="sxs-lookup"><span data-stu-id="f9803-120">Returns the current matrix mode.</span></span>                                |
| <span data-ttu-id="f9803-121">**getmatrix** en mode **MVIEWING**</span><span class="sxs-lookup"><span data-stu-id="f9803-121">**getmatrix** in **MVIEWING** mode</span></span>    | <span data-ttu-id="f9803-122">\_matrice MODELVIEW \_ GL</span><span class="sxs-lookup"><span data-stu-id="f9803-122">GL\_MODELVIEW\_MATRIX</span></span>             | <span data-ttu-id="f9803-123">Retourne une copie de la matrice de vue de modèle actuelle.</span><span class="sxs-lookup"><span data-stu-id="f9803-123">Returns a copy of the current model-view matrix.</span></span>                |
| <span data-ttu-id="f9803-124">**getmatrix** en mode **MPROJECTION**</span><span class="sxs-lookup"><span data-stu-id="f9803-124">**getmatrix** in **MPROJECTION** mode</span></span> | <span data-ttu-id="f9803-125">\_matrice de projection GL \_</span><span class="sxs-lookup"><span data-stu-id="f9803-125">GL\_PROJECTION\_MATRIX</span></span>            | <span data-ttu-id="f9803-126">Retourne une copie de la matrice de projection actuelle.</span><span class="sxs-lookup"><span data-stu-id="f9803-126">Returns a copy of the current projection matrix.</span></span>                |
| <span data-ttu-id="f9803-127">**getmatrix** en mode **MTEXTURE**</span><span class="sxs-lookup"><span data-stu-id="f9803-127">**getmatrix** in **MTEXTURE** mode</span></span>    | <span data-ttu-id="f9803-128">\_matrice de texture GL \_</span><span class="sxs-lookup"><span data-stu-id="f9803-128">GL\_TEXTURE\_MATRIX</span></span>               | <span data-ttu-id="f9803-129">Retourne une copie de la matrice de texture actuelle.</span><span class="sxs-lookup"><span data-stu-id="f9803-129">Returns a copy of the current texture matrix.</span></span>                   |
| <span data-ttu-id="f9803-130">Non applicable.</span><span class="sxs-lookup"><span data-stu-id="f9803-130">Not applicable.</span></span>                       | <span data-ttu-id="f9803-131">\_profondeur de \_ la \_ pile \_ MODELVIEW GL Max</span><span class="sxs-lookup"><span data-stu-id="f9803-131">GL\_MAX\_MODELVIEW\_STACK\_DEPTH</span></span>  | <span data-ttu-id="f9803-132">Retourne la profondeur maximale prise en charge de la pile de matrices de vue de modèle.</span><span class="sxs-lookup"><span data-stu-id="f9803-132">Returns maximum supported depth of the model-view matrix stack.</span></span> |
| <span data-ttu-id="f9803-133">Non applicable.</span><span class="sxs-lookup"><span data-stu-id="f9803-133">Not applicable.</span></span>                       | <span data-ttu-id="f9803-134">profondeur de la \_ \_ pile de projection Max \_ GL \_</span><span class="sxs-lookup"><span data-stu-id="f9803-134">GL\_MAX\_PROJECTION\_STACK\_DEPTH</span></span> | <span data-ttu-id="f9803-135">Retourne la profondeur maximale prise en charge de la pile de la matrice de projection.</span><span class="sxs-lookup"><span data-stu-id="f9803-135">Returns maximum supported depth of the projection matrix stack.</span></span> |
| <span data-ttu-id="f9803-136">Non applicable.</span><span class="sxs-lookup"><span data-stu-id="f9803-136">Not applicable.</span></span>                       | <span data-ttu-id="f9803-137">profondeur de la \_ \_ pile de texture Max \_ . GL \_</span><span class="sxs-lookup"><span data-stu-id="f9803-137">GL\_MAX\_TEXTURE\_STACK\_DEPTH</span></span>    | <span data-ttu-id="f9803-138">Retourne la profondeur maximale prise en charge de la pile de matrices de texture.</span><span class="sxs-lookup"><span data-stu-id="f9803-138">Returns maximum supported depth of the texture matrix stack.</span></span>    |
| <span data-ttu-id="f9803-139">Non applicable.</span><span class="sxs-lookup"><span data-stu-id="f9803-139">Not applicable.</span></span>                       | <span data-ttu-id="f9803-140">profondeur de la \_ pile MODELVIEW GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="f9803-140">GL\_MODELVIEW\_STACK\_DEPTH</span></span>       | <span data-ttu-id="f9803-141">Retourne le nombre de matrices sur la pile de la vue de modèle.</span><span class="sxs-lookup"><span data-stu-id="f9803-141">Returns number of matrices on the model view stack.</span></span>             |
| <span data-ttu-id="f9803-142">Non applicable.</span><span class="sxs-lookup"><span data-stu-id="f9803-142">Not applicable.</span></span>                       | <span data-ttu-id="f9803-143">profondeur de la \_ pile de projection GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="f9803-143">GL\_PROJECTION\_STACK\_DEPTH</span></span>      | <span data-ttu-id="f9803-144">Retourne le nombre de matrices sur la pile de projection.</span><span class="sxs-lookup"><span data-stu-id="f9803-144">Returns number of matrices on the projection stack.</span></span>             |
| <span data-ttu-id="f9803-145">Non applicable.</span><span class="sxs-lookup"><span data-stu-id="f9803-145">Not applicable.</span></span>                       | <span data-ttu-id="f9803-146">profondeur de la \_ pile de textures GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="f9803-146">GL\_TEXTURE\_STACK\_DEPTH</span></span>         | <span data-ttu-id="f9803-147">Retourne le nombre de matrices sur la pile de texture.</span><span class="sxs-lookup"><span data-stu-id="f9803-147">Returns number of matrices on the texture stack.</span></span>                |



 

<span data-ttu-id="f9803-148">??</span><span class="sxs-lookup"><span data-stu-id="f9803-148">??</span></span>

 

 




