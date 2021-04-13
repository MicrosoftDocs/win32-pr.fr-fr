---
title: Utilisation de l’Assistant de plug-in avec Visual Studio
description: Utilisation de l’Assistant de plug-in avec Visual Studio
ms.assetid: 5d5521b7-5cbc-4259-92b1-a7250853fa2e
keywords:
- Plug-ins du lecteur Windows Media, Visual Studio
- plug-ins, Visual Studio
- génération de plug-ins, Visual Studio
- Assistant de plug-in Windows Media Player, Visual Studio
- Visual Studio, Assistant de plug-in du lecteur Windows Media
- Assistant de plug-in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c7f7db9bdc2a99a42f60c2faf38605e50e7dd3e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310397"
---
# <a name="using-the-plug-in-wizard-with-visual-studio"></a><span data-ttu-id="a4d72-109">Utilisation de l’Assistant de plug-in avec Visual Studio</span><span class="sxs-lookup"><span data-stu-id="a4d72-109">Using the Plug-in Wizard with Visual Studio</span></span>

<span data-ttu-id="a4d72-110">Après avoir installé les composants nécessaires, vous pouvez créer rapidement un plug-in qui servira de point de départ.</span><span class="sxs-lookup"><span data-stu-id="a4d72-110">After you have installed the necessary components, you can quickly create a plug-in that will serve as a starting point.</span></span> <span data-ttu-id="a4d72-111">Les étapes suivantes vous guideront.</span><span class="sxs-lookup"><span data-stu-id="a4d72-111">The following steps will guide you.</span></span>

1.  <span data-ttu-id="a4d72-112">Démarrez Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="a4d72-112">Start Microsoft Visual Studio.</span></span>
2.  <span data-ttu-id="a4d72-113">Dans le menu **fichier** , pointez sur **nouveau** , puis cliquez sur **projet**.</span><span class="sxs-lookup"><span data-stu-id="a4d72-113">From the **File** menu, point to **New** and then click **Project**.</span></span>
3.  <span data-ttu-id="a4d72-114">Dans **types de projets**, sélectionnez **Visual C++ projets**.</span><span class="sxs-lookup"><span data-stu-id="a4d72-114">In **Project Types**, select **Visual C++ Projects**.</span></span>
4.  <span data-ttu-id="a4d72-115">Dans **modèles**, sélectionnez **Assistant plug-in du lecteur Windows Media**.</span><span class="sxs-lookup"><span data-stu-id="a4d72-115">In **Templates**, select **Windows Media Player Plug-in Wizard**.</span></span>
5.  <span data-ttu-id="a4d72-116">Entrez un nom pour votre projet.</span><span class="sxs-lookup"><span data-stu-id="a4d72-116">Enter a name for your project.</span></span>
6.  <span data-ttu-id="a4d72-117">Entrez un emplacement pour votre projet.</span><span class="sxs-lookup"><span data-stu-id="a4d72-117">Enter a location for your project.</span></span> <span data-ttu-id="a4d72-118">Il s’agit du dossier dans lequel vos fichiers projet seront copiés.</span><span class="sxs-lookup"><span data-stu-id="a4d72-118">This is the folder to which your project files will be copied.</span></span>
7.  <span data-ttu-id="a4d72-119">Cliquez sur **OK** pour démarrer l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="a4d72-119">Click **OK** to start the wizard.</span></span>
8.  <span data-ttu-id="a4d72-120">Sélectionnez le type de plug-in que vous souhaitez créer.</span><span class="sxs-lookup"><span data-stu-id="a4d72-120">Select the type of plug-in you want to create.</span></span>
9.  <span data-ttu-id="a4d72-121">Complétez les boîtes de dialogue restantes dans l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="a4d72-121">Complete any remaining dialog boxes in the wizard.</span></span>
10. <span data-ttu-id="a4d72-122">Utilisez l’environnement de développement Visual Studio pour générer votre projet.</span><span class="sxs-lookup"><span data-stu-id="a4d72-122">Use the Visual Studio development environment to build your project.</span></span>
    > [!Note]  
    > <span data-ttu-id="a4d72-123">Dans Windows Vista et versions ultérieures, le projet ne sera pas généré avec succès, sauf si vous exécutez Visual Studio avec un jeton d’accès administrateur complet.</span><span class="sxs-lookup"><span data-stu-id="a4d72-123">In Windows Vista and later, the project will not build successfully unless you run Visual Studio with a full administrator access token.</span></span> <span data-ttu-id="a4d72-124">Cliquez avec le bouton droit sur le nom ou l’icône Visual Studio, puis cliquez sur **exécuter en tant qu’administrateur**.</span><span class="sxs-lookup"><span data-stu-id="a4d72-124">Right-click the Visual Studio name or icon, and click **Run as administrator**.</span></span>

     

<span data-ttu-id="a4d72-125">Avant de tenter de générer le projet, veillez à configurer votre environnement de développement de façon à ce qu’il pointe vers les dossiers nommés include et lib où vous avez installé le SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="a4d72-125">Before attempting to build the project, be sure to configure your development environment to point to the folders named Include and Lib where you installed the Windows SDK.</span></span> <span data-ttu-id="a4d72-126">Le compilateur et l’éditeur de liens auront besoin d’accéder à certains des fichiers de ces dossiers.</span><span class="sxs-lookup"><span data-stu-id="a4d72-126">Your compiler and linker will need access to some of the files in these folders.</span></span>

<span data-ttu-id="a4d72-127">Si vous avez exécuté l’utilitaire d’inscription Visual Studio fourni avec le SDK Windows, votre environnement de développement a probablement déjà été configuré pour pointer vers les dossiers include et lib SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="a4d72-127">If you ran the Visual Studio Registration utility that comes with the Windows SDK, your development environment has probably already been configured to point to the Windows SDK Include and Lib folders.</span></span> <span data-ttu-id="a4d72-128">Dans le cas contraire, vous devez configurer manuellement votre environnement de développement.</span><span class="sxs-lookup"><span data-stu-id="a4d72-128">Otherwise, you must manually configure your development environment.</span></span>

<span data-ttu-id="a4d72-129">Pour configurer manuellement Visual Studio, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="a4d72-129">To manually configure Visual Studio, use the following steps.</span></span>

1.  <span data-ttu-id="a4d72-130">Dans le menu **Outils** , cliquez sur **Options**.</span><span class="sxs-lookup"><span data-stu-id="a4d72-130">On the **Tools** menu, click **Options**.</span></span>
2.  <span data-ttu-id="a4d72-131">Cliquez sur **projets et solutions**, puis sur **Répertoires VC + +**.</span><span class="sxs-lookup"><span data-stu-id="a4d72-131">Click **Projects and Solutions**, and then click **VC++ Directories**.</span></span>
3.  <span data-ttu-id="a4d72-132">Sous **afficher les répertoires pour**, cliquez sur **inclure** les fichiers ou les **fichiers de bibliothèque**.</span><span class="sxs-lookup"><span data-stu-id="a4d72-132">Under **Show directories for**, click **Include files** or **Library files**.</span></span>
4.  <span data-ttu-id="a4d72-133">Ajoutez les répertoires pour les fichiers requis.</span><span class="sxs-lookup"><span data-stu-id="a4d72-133">Add the directories for the required files.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a4d72-134">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a4d72-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a4d72-135">Génération d’un plug-in</span><span class="sxs-lookup"><span data-stu-id="a4d72-135">Building a Plug-in</span></span>](building-a-plug-in.md)
</dt> </dl>

 

 




