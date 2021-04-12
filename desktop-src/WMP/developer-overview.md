---
title: Vue d’ensemble du développeur
description: Vue d’ensemble du développeur
ms.assetid: 72a330b4-5957-4159-b5e8-0c9a4491b589
keywords:
- Plug-ins du lecteur Windows Media, visualisations
- plug-ins, visualisations
- visualisations, vue d’ensemble du développeur
- visualisations personnalisées, vue d’ensemble du développeur
- visualisations, contrôles COM
- visualisations personnalisées, contrôles COM
- visualisations, entrée audio
- visualisations personnalisées, entrée audio
- visualisations, sortie graphique
- visualisations personnalisées, sortie graphique
- visualisations, outils de dessin
- visualisations personnalisées, outils de dessin
- visualisations, langage de programmation
- visualisations personnalisées, langage de programmation
- visualisations, Visual C++
- visualisations personnalisées, Visual C++
- visualisations, Assistant de plug-in
- visualisations personnalisées, Assistant de plug-in
- Assistant de plug-in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36ec8632bd5611e081a4a17d1b0390dc99a09703
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310598"
---
# <a name="developer-overview"></a><span data-ttu-id="0d1d1-122">Vue d’ensemble du développeur</span><span class="sxs-lookup"><span data-stu-id="0d1d1-122">Developer Overview</span></span>

<span data-ttu-id="0d1d1-123">Du point de vue du développeur, les visualisations sont des programmes logiciels qui prennent des données audio fournies par le lecteur Windows Media et convertissent ces données en graphiques qui seront les yeux de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0d1d1-123">From the developer's point of view, visualizations are software programs that take audio data provided by Windows Media Player and convert that data to graphics that will please the eye of the user.</span></span> <span data-ttu-id="0d1d1-124">Les sujets principaux qu’un développeur doit comprendre pour créer une nouvelle visualisation sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="0d1d1-124">The main subjects a developer needs to understand to create a new visualization are the following:</span></span>

## <a name="visualization-packaging"></a><span data-ttu-id="0d1d1-125">Empaquetage de visualisation</span><span class="sxs-lookup"><span data-stu-id="0d1d1-125">Visualization Packaging</span></span>

<span data-ttu-id="0d1d1-126">Les visualisations sont des contrôles COM utilisés par le lecteur Windows Media pour transformer les formes d’ondes audio en graphiques animés dans Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="0d1d1-126">Visualizations are COM controls that Windows Media Player uses to turn audio waveforms into animated graphics in Microsoft Windows.</span></span> <span data-ttu-id="0d1d1-127">Les contrôles COM sont empaquetés en tant que bibliothèques de liens dynamiques (dll) Microsoft Windows et doivent être inscrits dans le Registre Windows.</span><span class="sxs-lookup"><span data-stu-id="0d1d1-127">The COM controls are packaged as Microsoft Windows dynamic-link libraries (DLLs) and must be registered in the Windows registry.</span></span> <span data-ttu-id="0d1d1-128">Lors de l’exécution du lecteur Windows Media, les visualisations personnalisées enregistrées sont chargées et affichées conformément aux instructions de la peau utilisée par le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="0d1d1-128">When Windows Media Player runs, registered custom visualizations are loaded and viewed in accordance with the instructions of the skin that Windows Media Player is using.</span></span>

## <a name="audio-input"></a><span data-ttu-id="0d1d1-129">Entrée audio</span><span class="sxs-lookup"><span data-stu-id="0d1d1-129">Audio Input</span></span>

<span data-ttu-id="0d1d1-130">Le lecteur Windows Media fournit votre code avec des instantanés de données audio Frequency et Waveform à des intervalles chronométrés mesurés en fractions de seconde.</span><span class="sxs-lookup"><span data-stu-id="0d1d1-130">Windows Media Player provides your code with snapshots of audio frequency and waveform data at timed intervals measured in fractions of a second.</span></span> <span data-ttu-id="0d1d1-131">L’intervalle de capture instantanée est déterminé en interne par le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="0d1d1-131">The snapshot interval is internally determined by the Windows Media Player.</span></span>

## <a name="graphical-output"></a><span data-ttu-id="0d1d1-132">Sortie graphique</span><span class="sxs-lookup"><span data-stu-id="0d1d1-132">Graphical Output</span></span>

<span data-ttu-id="0d1d1-133">La sortie graphique de votre visualisation est un contexte de périphérique Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="0d1d1-133">The graphical output from your visualization is a Microsoft Windows device context.</span></span> <span data-ttu-id="0d1d1-134">Il s’agit d’une surface de dessin Windows standard que vous pouvez dessiner à chaque fois qu’un instantané audio est fourni.</span><span class="sxs-lookup"><span data-stu-id="0d1d1-134">This is a standard Windows drawing surface that you can draw upon every time an audio snapshot is provided.</span></span> <span data-ttu-id="0d1d1-135">Toutes les technologies Windows en arrière-plan sont prises en charge pour vous.</span><span class="sxs-lookup"><span data-stu-id="0d1d1-135">All of the background Windows technology is taken care of for you.</span></span> <span data-ttu-id="0d1d1-136">Il vous suffit de dessiner sur le contexte de l’appareil avec les données audio fournies.</span><span class="sxs-lookup"><span data-stu-id="0d1d1-136">You just have to draw on the device context with the audio data provided.</span></span>

## <a name="drawing-tools"></a><span data-ttu-id="0d1d1-137">Outils de dessin</span><span class="sxs-lookup"><span data-stu-id="0d1d1-137">Drawing Tools</span></span>

<span data-ttu-id="0d1d1-138">Vous pouvez dessiner sur le contexte de périphérique à l’aide de fonctions Microsoft Windows Graphics Device Interface (GDI) standard, en utilisant des stylets et des pinceaux pour créer des conceptions qui sont modifiées par les données audio fournies par le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="0d1d1-138">You can draw on the device context with standard Microsoft Windows Graphics Device Interface (GDI) functions, using pens and brushes to create designs that are modified by the audio data supplied to you by Windows Media Player.</span></span> <span data-ttu-id="0d1d1-139">GDI fournit un ensemble complet d’outils de dessin qui peuvent créer de nombreux genres d’effets visuels.</span><span class="sxs-lookup"><span data-stu-id="0d1d1-139">GDI provides a rich set of drawing tools that can create many kinds of visual effects.</span></span>

## <a name="programming-language"></a><span data-ttu-id="0d1d1-140">Langage de programmation</span><span class="sxs-lookup"><span data-stu-id="0d1d1-140">Programming Language</span></span>

<span data-ttu-id="0d1d1-141">Microsoft Visual C++ 6,0 et versions ultérieures est la seule langue prise en charge pour la création de visualisations personnalisées.</span><span class="sxs-lookup"><span data-stu-id="0d1d1-141">Microsoft Visual C++ 6.0 and higher is the only supported language for creating custom visualizations.</span></span>

## <a name="plug-in-wizard"></a><span data-ttu-id="0d1d1-142">Assistant de plug-in</span><span class="sxs-lookup"><span data-stu-id="0d1d1-142">Plug-in Wizard</span></span>

<span data-ttu-id="0d1d1-143">Le lecteur Windows Media fournit un Assistant COM que vous pouvez ajouter à Visual C++ qui générera le code sous-jacent requis pour votre visualisation.</span><span class="sxs-lookup"><span data-stu-id="0d1d1-143">Windows Media Player provides a COM wizard that you can add to Visual C++ that will generate the underlying code needed for your visualization.</span></span> <span data-ttu-id="0d1d1-144">Non seulement tous les fichiers sources sont fournis, mais un exemple d’apparence est généré pour faciliter le test de votre visualisation.</span><span class="sxs-lookup"><span data-stu-id="0d1d1-144">Not only are all source files provided, but a sample skin is generated to make it easy to test your visualization.</span></span> <span data-ttu-id="0d1d1-145">Le code généré crée une visualisation similaire aux barres, avec deux présélections.</span><span class="sxs-lookup"><span data-stu-id="0d1d1-145">The generated code creates a visualization similar to Bars, with two presets.</span></span> <span data-ttu-id="0d1d1-146">Vous pouvez ensuite modifier le code pour créer votre propre visualisation.</span><span class="sxs-lookup"><span data-stu-id="0d1d1-146">You can then modify the code to create your own visualization.</span></span> <span data-ttu-id="0d1d1-147">Un fichier de Registre est également généré pour inscrire votre visualisation afin que le lecteur Windows Media puisse la charger.</span><span class="sxs-lookup"><span data-stu-id="0d1d1-147">A registry file is also generated to register your visualization so that Windows Media Player can load it.</span></span>

<span data-ttu-id="0d1d1-148">La rubrique suivante décrit comment le code de visualisation traite les données audio :</span><span class="sxs-lookup"><span data-stu-id="0d1d1-148">The following topic describes how visualization code processes audio data:</span></span>

-   [<span data-ttu-id="0d1d1-149">Flow de contrôle</span><span class="sxs-lookup"><span data-stu-id="0d1d1-149">Flow of Control</span></span>](flow-of-control.md)

## <a name="related-topics"></a><span data-ttu-id="0d1d1-150">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0d1d1-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0d1d1-151">**À propos des visualisations personnalisées**</span><span class="sxs-lookup"><span data-stu-id="0d1d1-151">**About Custom Visualizations**</span></span>](about-custom-visualizations.md)
</dt> </dl>

 

 




