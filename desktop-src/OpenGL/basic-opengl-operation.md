---
title: Opération OpenGL de base
description: Opération OpenGL de base
ms.assetid: ad4c9321-a9e3-40c5-af80-0ad6a8b9f380
keywords:
- OpenGL, opérations de base
- OpenGL, traitement des données
- OpenGL, étapes de traitement
- OpenGL, afficher les listes
- afficher les listes OpenGL
- OpenGL, évaluateurs
- évaluateurs OpenGL
- OpenGL, opérations par vertex
- opérations par vertex OpenGL
- OpenGL, assembly primitif
- assembly primitif OpenGL
- OpenGL, pixellisation
- pixellisation OpenGL
- OpenGL, opérations par fragment
- opérations par fragment OpenGL
- framebuffers, opérations de base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77f6b9fb8c8ca4efb05d9050e0de3da807b213e7
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "103953320"
---
# <a name="basic-opengl-operation"></a><span data-ttu-id="5e751-119">Opération OpenGL de base</span><span class="sxs-lookup"><span data-stu-id="5e751-119">Basic OpenGL Operation</span></span>

<span data-ttu-id="5e751-120">Le diagramme suivant illustre comment OpenGL traite les données.</span><span class="sxs-lookup"><span data-stu-id="5e751-120">The following diagram illustrates how OpenGL processes data.</span></span> <span data-ttu-id="5e751-121">Comme illustré, les commandes entrent à partir de la gauche et passent par un pipeline de traitement.</span><span class="sxs-lookup"><span data-stu-id="5e751-121">As shown, commands enter from the left and proceed through a processing pipeline.</span></span> <span data-ttu-id="5e751-122">Certaines commandes spécifient des objets géométriques à dessiner, tandis que d’autres contrôlent la façon dont les objets sont traités au cours des différentes étapes de traitement.</span><span class="sxs-lookup"><span data-stu-id="5e751-122">Some commands specify geometric objects to be drawn, and others control how the objects are handled during various processing stages.</span></span>

![Diagramme montrant les étapes du pipeline de traitement des données OpenGL.](images/basic01.png)

<span data-ttu-id="5e751-124">Les étapes de traitement de l’opération OpenGL de base sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="5e751-124">The processing stages in basic OpenGL operation are as follows:</span></span>

-   <span data-ttu-id="5e751-125">**Afficher la liste** Plutôt que de faire en sorte que toutes les commandes passent immédiatement par le pipeline, vous pouvez choisir de les accumuler dans une liste d’affichage pour les traiter ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="5e751-125">**Display list** Rather than having all commands proceed immediately through the pipeline, you can choose to accumulate some of them in a display list for processing later.</span></span>
-   <span data-ttu-id="5e751-126">**Évaluateur** L’étape de traitement de l’évaluateur offre un moyen efficace de calculer la géométrie des courbes et des surfaces en évaluant les commandes polynomiaux des valeurs d’entrée.</span><span class="sxs-lookup"><span data-stu-id="5e751-126">**Evaluator** The evaluator stage of processing provides an efficient way to approximate curve and surface geometry by evaluating polynomial commands of input values.</span></span>
-   <span data-ttu-id="5e751-127">**Opérations par vertex et assembly primitif** OpenGL traite les primitivespoints géométriques, les segments de ligne et les polygonsall qui sont décrits par des vertex.</span><span class="sxs-lookup"><span data-stu-id="5e751-127">**Per-vertex operations and primitive assembly** OpenGL processes geometric primitivespoints, line segments, and polygonsall of which are described by vertices.</span></span> <span data-ttu-id="5e751-128">Les vertex sont transformés et allumés, et les primitives sont ajustées à la fenêtre d’affichage en vue de la pixellisation.</span><span class="sxs-lookup"><span data-stu-id="5e751-128">Vertices are transformed and lit, and primitives are clipped to the viewport in preparation for rasterization.</span></span>
-   <span data-ttu-id="5e751-129">**Pixellisation** L’étape de pixellisation produit une série d’adresses de tampons de trames et de valeurs associées à l’aide d’une description à deux dimensions d’un point, d’un segment de ligne ou d’un polygone.</span><span class="sxs-lookup"><span data-stu-id="5e751-129">**Rasterization** The rasterization stage produces a series of frame-buffer addresses and associated values using a two-dimensional description of a point, line segment, or polygon.</span></span> <span data-ttu-id="5e751-130">Chaque fragment produit est introduit dans la dernière étape, opérations par fragment.</span><span class="sxs-lookup"><span data-stu-id="5e751-130">Each fragment so produced is fed into the last stage, per-fragment operations.</span></span>
-   <span data-ttu-id="5e751-131">**Opérations par fragment** Il s’agit des opérations finales effectuées sur les données avant qu’elles ne soient stockées sous la forme de pixels dans le trame.</span><span class="sxs-lookup"><span data-stu-id="5e751-131">**Per-fragment operations** These are the final operations performed on the data before it is stored as pixels in the framebuffer.</span></span>

    <span data-ttu-id="5e751-132">Les opérations par fragment incluent les mises à jour conditionnelles du trame en fonction des valeurs z entrantes et précédemment stockées (pour la mise en mémoire tampon z) et de la fusion des couleurs de pixels entrantes avec des couleurs stockées, ainsi que du masquage et d’autres opérations logiques sur les valeurs de pixel.</span><span class="sxs-lookup"><span data-stu-id="5e751-132">Per-fragment operations include conditional updates to the framebuffer based on incoming and previously stored z values (for z buffering) and blending of incoming pixel colors with stored colors, as well as masking and other logical operations on pixel values.</span></span>

<span data-ttu-id="5e751-133">Les données peuvent être entrées sous la forme de pixels plutôt que de vertex.</span><span class="sxs-lookup"><span data-stu-id="5e751-133">Data can be input in the form of pixels rather than vertices.</span></span> <span data-ttu-id="5e751-134">Les données sous la forme de pixels, telles que peuvent décrire une image à utiliser dans le mappage de texture, ignore la première étape de traitement décrite ci-dessus et est traitée en tant que pixels, dans l’étape des opérations de pixel.</span><span class="sxs-lookup"><span data-stu-id="5e751-134">Data in the form of pixels, such as might describe an image for use in texture mapping, skips the first stage of processing described above and instead is processed as pixels, in the pixel operations stage.</span></span> <span data-ttu-id="5e751-135">Opérations de pixel suivantes, les données de pixels sont :</span><span class="sxs-lookup"><span data-stu-id="5e751-135">Following pixel operations, the pixel data is either:</span></span>

-   <span data-ttu-id="5e751-136">Stocké en tant que mémoire de texture pour une utilisation à l’étape de pixellisation.</span><span class="sxs-lookup"><span data-stu-id="5e751-136">Stored as texture memory, for use in the rasterization stage.</span></span>
-   <span data-ttu-id="5e751-137">Pixellisé, avec les fragments résultants fusionnés dans le trame comme s’ils étaient générés à partir de données géométriques.</span><span class="sxs-lookup"><span data-stu-id="5e751-137">Rasterized, with the resulting fragments merged into the framebuffer just as if they were generated from geometric data.</span></span>

 

 




