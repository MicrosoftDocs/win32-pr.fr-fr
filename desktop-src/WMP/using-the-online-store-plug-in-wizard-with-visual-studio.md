---
title: Utilisation de l’Assistant de plug-in de boutique en ligne avec Visual Studio
description: Utilisation de l’Assistant de plug-in de boutique en ligne avec Visual Studio
ms.assetid: 0bf670cd-897d-4cd6-ae95-ae16b2dacc96
keywords:
- Windows Media Player Online stores, plug-ins
- magasins en ligne, plug-ins
- types 1 magasins en ligne, plug-ins
- Windows Media Player Online stores, Assistant plug-in
- magasins en ligne, Assistant de plug-in
- tapez 1 magasins en ligne, Assistant de plug-in
- Windows Media Player Online stores, Visual Studio
- magasins en ligne, Visual Studio
- types 1 magasins en ligne, Visual Studio
- plug-ins, Windows Media Player Online stores
- plug-ins, magasins en ligne
- plug-ins, type 1 magasins en ligne
- plug-ins, Visual Studio
- plug-ins, Assistant de plug-in
- Plug-ins du lecteur Windows Media, type 1 magasins en ligne
- Plug-ins du lecteur Windows Media, magasins en ligne
- Plug-ins du lecteur Windows Media, magasins en ligne Windows Media Player
- Plug-ins du lecteur Windows Media, Visual Studio
- Plug-ins du lecteur Windows Media, Assistant plug-in
- Visual Studio, Assistant Windows Media Player stores Online
- Assistant de plug-in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0c9aadbb9cef4b44cb421bf8a4737cc408c5220
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106508964"
---
# <a name="using-the-online-store-plug-in-wizard-with-visual-studio"></a><span data-ttu-id="545a2-124">Utilisation de l’Assistant de plug-in de boutique en ligne avec Visual Studio</span><span class="sxs-lookup"><span data-stu-id="545a2-124">Using the Online Store Plug-in Wizard with Visual Studio</span></span>

<span data-ttu-id="545a2-125">Après avoir installé les composants nécessaires, vous pouvez créer rapidement un plug-in qui servira de point de départ.</span><span class="sxs-lookup"><span data-stu-id="545a2-125">After you have installed the necessary components, you can quickly create a plug-in that will serve as a starting point.</span></span> <span data-ttu-id="545a2-126">Les étapes suivantes vous guident :</span><span class="sxs-lookup"><span data-stu-id="545a2-126">The following steps will guide you:</span></span>

1.  <span data-ttu-id="545a2-127">Démarrez Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="545a2-127">Start Microsoft Visual Studio.</span></span>
2.  <span data-ttu-id="545a2-128">Dans le menu **fichier** , pointez sur **nouveau** , puis cliquez sur **projet**.</span><span class="sxs-lookup"><span data-stu-id="545a2-128">From the **File** menu, point to **New** and then click **Project**.</span></span>
3.  <span data-ttu-id="545a2-129">Dans **types de projets**, cliquez sur **projets de Visual C++**.</span><span class="sxs-lookup"><span data-stu-id="545a2-129">In **Project Types**, click **Visual C++ Projects**.</span></span>
4.  <span data-ttu-id="545a2-130">Dans **modèles**, cliquez sur **Assistant magasins en ligne du lecteur Windows Media**.</span><span class="sxs-lookup"><span data-stu-id="545a2-130">In **Templates**, click **Windows Media Player Online Stores Wizard**.</span></span>
5.  <span data-ttu-id="545a2-131">Entrez un nom pour votre projet.</span><span class="sxs-lookup"><span data-stu-id="545a2-131">Enter a name for your project.</span></span>
6.  <span data-ttu-id="545a2-132">Entrez un emplacement pour votre projet.</span><span class="sxs-lookup"><span data-stu-id="545a2-132">Enter a location for your project.</span></span> <span data-ttu-id="545a2-133">Il s’agit du dossier dans lequel vos fichiers projet seront copiés.</span><span class="sxs-lookup"><span data-stu-id="545a2-133">This is the folder to which your project files will be copied.</span></span>
7.  <span data-ttu-id="545a2-134">Cliquez sur **OK** pour démarrer l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="545a2-134">Click **OK** to start the wizard.</span></span>
8.  <span data-ttu-id="545a2-135">Sélectionnez **type 1 (intégration profonde)**, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="545a2-135">Select **Type 1 (Deep integration)**, and click **Next**.</span></span>
9.  <span data-ttu-id="545a2-136">Entrez un nom convivial et un serveur de distribution de contenu.</span><span class="sxs-lookup"><span data-stu-id="545a2-136">Enter a friendly name and a content distributor.</span></span> <span data-ttu-id="545a2-137">Cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="545a2-137">Click **Finish**.</span></span>
10. <span data-ttu-id="545a2-138">Utilisez l’environnement de développement Visual Studio pour générer votre projet.</span><span class="sxs-lookup"><span data-stu-id="545a2-138">Use the Visual Studio development environment to build your project.</span></span>
    > [!Note]  
    > <span data-ttu-id="545a2-139">Dans Windows Vista et versions ultérieures, le projet ne sera pas généré avec succès, sauf si vous exécutez Visual Studio avec un jeton d’accès administrateur complet.</span><span class="sxs-lookup"><span data-stu-id="545a2-139">In Windows Vista and later, the project will not build successfully unless you run Visual Studio with a full administrator access token.</span></span> <span data-ttu-id="545a2-140">Cliquez avec le bouton droit sur le nom ou l’icône Visual Studio, puis cliquez sur **exécuter en tant qu’administrateur**.</span><span class="sxs-lookup"><span data-stu-id="545a2-140">Right-click the Visual Studio name or icon, and click **Run as administrator**.</span></span>

     

<span data-ttu-id="545a2-141">Avant de tenter de générer le projet, veillez à configurer votre environnement de développement de façon à ce qu’il pointe vers les dossiers nommés include et lib où vous avez installé le SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="545a2-141">Before attempting to build the project, be sure to configure your development environment to point to the folders named Include and Lib where you installed the Windows SDK.</span></span> <span data-ttu-id="545a2-142">Le compilateur et l’éditeur de liens auront besoin d’accéder à certains des fichiers de ces dossiers.</span><span class="sxs-lookup"><span data-stu-id="545a2-142">Your compiler and linker will need access to some of the files in these folders.</span></span>

<span data-ttu-id="545a2-143">Si vous avez exécuté l’utilitaire d’inscription Visual Studio fourni avec le SDK Windows, votre environnement de développement a probablement déjà été configuré pour pointer vers les dossiers include et lib SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="545a2-143">If you ran the Visual Studio Registration utility that comes with the Windows SDK, your development environment has probably already been configured to point to the Windows SDK Include and Lib folders.</span></span> <span data-ttu-id="545a2-144">Dans le cas contraire, vous devez configurer manuellement votre environnement de développement.</span><span class="sxs-lookup"><span data-stu-id="545a2-144">Otherwise, you must manually configure your development environment.</span></span>

<span data-ttu-id="545a2-145">Pour configurer manuellement Visual Studio, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="545a2-145">To manually configure Visual Studio, use the following steps.</span></span>

1.  <span data-ttu-id="545a2-146">Dans le menu **Outils** , cliquez sur options.</span><span class="sxs-lookup"><span data-stu-id="545a2-146">On the **Tools** menu, click Options.</span></span>
2.  <span data-ttu-id="545a2-147">Cliquez sur **projets et solutions**, puis sur **Répertoires VC + +**.</span><span class="sxs-lookup"><span data-stu-id="545a2-147">Click **Projects and Solutions**, and then click **VC++ Directories**.</span></span>
3.  <span data-ttu-id="545a2-148">Sous **afficher les répertoires pour**, cliquez sur **inclure** les fichiers ou les **fichiers de bibliothèque**.</span><span class="sxs-lookup"><span data-stu-id="545a2-148">Under **Show directories for**, click **Include files** or **Library files**.</span></span>
4.  <span data-ttu-id="545a2-149">Ajoutez les répertoires pour les fichiers requis.</span><span class="sxs-lookup"><span data-stu-id="545a2-149">Add the directories for the required files.</span></span>

## <a name="related-topics"></a><span data-ttu-id="545a2-150">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="545a2-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="545a2-151">Création du plug-in pour un magasin de type 1 en ligne</span><span class="sxs-lookup"><span data-stu-id="545a2-151">Building the Plug-in for a Type 1 Online Store</span></span>](building-the-plug-in-for-a-type-1-online-store.md)
</dt> </dl>

 

 




