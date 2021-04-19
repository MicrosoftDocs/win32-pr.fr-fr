---
title: Compilation de l’exemple de projet
description: Compilation de l’exemple de projet
ms.assetid: c605042e-ec45-44c7-afca-42a874882eab
keywords:
- Windows Media Player Online stores, compilation d’exemples de projets
- magasins en ligne, compilation d’exemples de projets
- types 2 magasins en ligne, compilation d’exemples de projets
- Magasins en ligne du lecteur Windows Media, exemples de projets
- magasins en ligne, exemples de projets
- types 2 magasins en ligne, exemples de projets
- Windows Media Player Online stores, Assistant projet
- magasins en ligne, Assistant projet
- type 2 magasins en ligne, Assistant projet
- plug-ins, Assistant projet
- Plug-ins du lecteur Windows Media, Assistant projet
- compilation d’exemples de projets
- exemples, type 2 magasins en ligne
- Assistant projet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1ea2382e5852965b246f1ef303e5e70d160cb22
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106545731"
---
# <a name="compiling-the-sample-project"></a><span data-ttu-id="d4b71-117">Compilation de l’exemple de projet</span><span class="sxs-lookup"><span data-stu-id="d4b71-117">Compiling the Sample Project</span></span>

<span data-ttu-id="d4b71-118">L’Assistant génère tous les fichiers dont vous avez besoin pour compiler l’exemple de projet. il n’est donc pas nécessaire de modifier les paramètres de projet par défaut.</span><span class="sxs-lookup"><span data-stu-id="d4b71-118">The wizard generates all the files you need to compile the sample project, so you shouldn't need to change the default project settings.</span></span> <span data-ttu-id="d4b71-119">Dans Visual Studio, dans le menu **générer** , cliquez sur **générer la solution** pour générer et inscrire le composant com.</span><span class="sxs-lookup"><span data-stu-id="d4b71-119">In Visual Studio, from the **Build** menu, click **Build Solution** to build and register the COM component.</span></span> <span data-ttu-id="d4b71-120">Par défaut, la configuration de débogage est active.</span><span class="sxs-lookup"><span data-stu-id="d4b71-120">By default, the Debug configuration is active.</span></span>

> [!Note]  
> <span data-ttu-id="d4b71-121">Dans Windows Vista et versions ultérieures, le projet ne sera pas généré avec succès, sauf si vous exécutez Visual Studio avec un jeton d’accès administrateur complet.</span><span class="sxs-lookup"><span data-stu-id="d4b71-121">In Windows Vista and later, the project will not build successfully unless you run Visual Studio with a full administrator access token.</span></span> <span data-ttu-id="d4b71-122">Cliquez avec le bouton droit sur le nom ou l’icône Visual Studio, puis cliquez sur **exécuter en tant qu’administrateur**.</span><span class="sxs-lookup"><span data-stu-id="d4b71-122">Right-click the Visual Studio name or icon, and click **Run as administrator**.</span></span>

 

<span data-ttu-id="d4b71-123">Avant de tenter de générer le projet, veillez à configurer votre environnement de développement de façon à ce qu’il pointe vers les dossiers nommés include et lib où vous avez installé le SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="d4b71-123">Before attempting to build the project, be sure to configure your development environment to point to the folders named Include and Lib where you installed the Windows SDK.</span></span> <span data-ttu-id="d4b71-124">Le compilateur et l’éditeur de liens auront besoin d’accéder à certains des fichiers de ces dossiers.</span><span class="sxs-lookup"><span data-stu-id="d4b71-124">Your compiler and linker will need access to some of the files in these folders.</span></span>

<span data-ttu-id="d4b71-125">Si vous avez exécuté l’utilitaire d’inscription Visual Studio fourni avec le kit de développement logiciel (SDK) Windows Vista, votre environnement de développement a probablement déjà été configuré pour pointer vers les dossiers include et lib de SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="d4b71-125">If you ran the Visual Studio Registration utility that comes with the Windows Vista SDK, your development environment has probably already been configured to point to the Windows SDK Include and Lib folders.</span></span> <span data-ttu-id="d4b71-126">Dans le cas contraire, vous devez configurer manuellement votre environnement de développement.</span><span class="sxs-lookup"><span data-stu-id="d4b71-126">Otherwise, you must manually configure your development environment.</span></span>

<span data-ttu-id="d4b71-127">Pour configurer manuellement Visual Studio, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="d4b71-127">To manually configure Visual Studio, use the following steps.</span></span>

1.  <span data-ttu-id="d4b71-128">Dans le menu **Outils** , cliquez sur **Options**.</span><span class="sxs-lookup"><span data-stu-id="d4b71-128">On the **Tools** menu, click **Options**.</span></span>
2.  <span data-ttu-id="d4b71-129">Cliquez sur **projets et solutions**, puis sur **Répertoires VC + +**.</span><span class="sxs-lookup"><span data-stu-id="d4b71-129">Click **Projects and Solutions**, and then click **VC++ Directories**.</span></span>
3.  <span data-ttu-id="d4b71-130">Sous **afficher les répertoires pour**, cliquez sur **inclure** les fichiers ou les **fichiers de bibliothèque**.</span><span class="sxs-lookup"><span data-stu-id="d4b71-130">Under **Show directories for**, click **Include files** or **Library files**.</span></span>
4.  <span data-ttu-id="d4b71-131">Ajoutez les répertoires pour les fichiers requis.</span><span class="sxs-lookup"><span data-stu-id="d4b71-131">Add the directories for the required files.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d4b71-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d4b71-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d4b71-133">Création du plug-in pour un magasin de type 2 en ligne</span><span class="sxs-lookup"><span data-stu-id="d4b71-133">Building the Plug-in for a Type 2 Online Store</span></span>](building-the-plug-in-for-a-type-2-online-store.md)
</dt> </dl>

 

 




