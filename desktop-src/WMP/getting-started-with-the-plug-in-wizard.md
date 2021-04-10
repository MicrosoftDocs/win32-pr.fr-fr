---
title: Prise en main à l’aide de l’Assistant de plug-in
description: Prise en main à l’aide de l’Assistant de plug-in
ms.assetid: 77fc1b0c-20f5-434d-9142-f112489a7f08
keywords:
- Plug-ins du lecteur Windows Media, Assistant Installation du plug-in
- plug-ins, installation de l’Assistant de plug-in
- génération de plug-ins, installation de l’Assistant de plug-in
- Assistant de plug-in du lecteur Windows Media, installation
- Assistant Installation du plug-in
- Assistant de plug-in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a4feb9cfa60c120bfc5bb675ea8a8078b95ad14
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940172"
---
# <a name="getting-started-with-the-plug-in-wizard"></a><span data-ttu-id="ea564-109">Prise en main à l’aide de l’Assistant de plug-in</span><span class="sxs-lookup"><span data-stu-id="ea564-109">Getting Started with the Plug-in Wizard</span></span>

<span data-ttu-id="ea564-110">Pour configurer votre environnement de développement pour la création de plug-ins du lecteur Windows Media, vous devez installer les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="ea564-110">To set up your development environment for creating Windows Media Player plug-ins, you must install the following items:</span></span>

-   <span data-ttu-id="ea564-111">Microsoft Visual Studio .NET 2003 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="ea564-111">Microsoft Visual Studio .NET 2003 or later</span></span>
-   <span data-ttu-id="ea564-112">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="ea564-112">Windows Media Player 9 Series or later</span></span>
-   <span data-ttu-id="ea564-113">SDK Windows, qui comprend le kit de développement logiciel (SDK) du lecteur Windows Media</span><span class="sxs-lookup"><span data-stu-id="ea564-113">Windows SDK, which includes the Windows Media Player SDK</span></span>
-   <span data-ttu-id="ea564-114">Assistant de plug-in du lecteur Windows Media</span><span class="sxs-lookup"><span data-stu-id="ea564-114">Windows Media Player Plug-in Wizard</span></span>

## <a name="installing-the-wizard"></a><span data-ttu-id="ea564-115">Installation de l’Assistant</span><span class="sxs-lookup"><span data-stu-id="ea564-115">Installing the Wizard</span></span>

<span data-ttu-id="ea564-116">Procédez comme suit pour installer l’Assistant de plug-in du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="ea564-116">Perform the following steps to install the Windows Media Player Plug-in Wizard.</span></span>

1.  <span data-ttu-id="ea564-117">Localisez le dossier dans lequel vous avez installé le SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="ea564-117">Locate the folder where you installed the Windows SDK.</span></span> <span data-ttu-id="ea564-118">Développez le dossier pour afficher ses sous-dossiers, puis accédez à exemples d' \\ \\ \\ assistants multimédia WMP \\ wmpwiz.</span><span class="sxs-lookup"><span data-stu-id="ea564-118">Expand the folder to view its subfolders, and navigate to Samples\\Multimedia\\WMP\\wizards\\wmpwiz.</span></span>
2.  <span data-ttu-id="ea564-119">Recherchez les trois fichiers suivants :</span><span class="sxs-lookup"><span data-stu-id="ea564-119">Locate the following three files:</span></span>
    -   <span data-ttu-id="ea564-120">wmpwiz. vsz</span><span class="sxs-lookup"><span data-stu-id="ea564-120">wmpwiz.vsz</span></span>
    -   <span data-ttu-id="ea564-121">wmpwiz. vsdir</span><span class="sxs-lookup"><span data-stu-id="ea564-121">wmpwiz.vsdir</span></span>
    -   <span data-ttu-id="ea564-122">wmpwiz. ico</span><span class="sxs-lookup"><span data-stu-id="ea564-122">wmpwiz.ico</span></span>
3.  <span data-ttu-id="ea564-123">À l’aide d’un éditeur de texte, tel que le bloc-notes, modifiez le fichier wmpwiz. vsz.</span><span class="sxs-lookup"><span data-stu-id="ea564-123">Using a text editor, such as Notepad, edit the wmpwiz.vsz file.</span></span>

    <span data-ttu-id="ea564-124">Recherchez la ligne suivante :</span><span class="sxs-lookup"><span data-stu-id="ea564-124">Locate the following line:</span></span>

    ```
    Wizard=VsWizard.<VsWizardEngine version goes here>
    ```

    

    <span data-ttu-id="ea564-125">Modifiez l' `<VsWizardEngine version goes here>` une des valeurs suivantes, en fonction de la version de Visual Studio que vous avez installée.</span><span class="sxs-lookup"><span data-stu-id="ea564-125">Change `<VsWizardEngine version goes here>` to one of the following values, depending on which version of Visual Studio you have installed.</span></span>

    

    | <span data-ttu-id="ea564-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="ea564-126">Value</span></span>              | <span data-ttu-id="ea564-127">Version de Visual Studio</span><span class="sxs-lookup"><span data-stu-id="ea564-127">Visual Studio version</span></span>   |
    |--------------------|-------------------------|
    | <span data-ttu-id="ea564-128">VsWizardEngine. 7.1</span><span class="sxs-lookup"><span data-stu-id="ea564-128">VsWizardEngine.7.1</span></span> | <span data-ttu-id="ea564-129">Visual Studio .NET 2003</span><span class="sxs-lookup"><span data-stu-id="ea564-129">Visual Studio .NET 2003</span></span> |
    | <span data-ttu-id="ea564-130">VsWizardEngine. 8.0</span><span class="sxs-lookup"><span data-stu-id="ea564-130">VsWizardEngine.8.0</span></span> | <span data-ttu-id="ea564-131">Visual Studio 2005</span><span class="sxs-lookup"><span data-stu-id="ea564-131">Visual Studio 2005</span></span>      |
    | <span data-ttu-id="ea564-132">VsWizardEngine. 9.0</span><span class="sxs-lookup"><span data-stu-id="ea564-132">VsWizardEngine.9.0</span></span> | <span data-ttu-id="ea564-133">Visual Studio 2008</span><span class="sxs-lookup"><span data-stu-id="ea564-133">Visual Studio 2008</span></span>      |

    

     

    <span data-ttu-id="ea564-134">Recherchez la ligne suivante :</span><span class="sxs-lookup"><span data-stu-id="ea564-134">Locate the following line:</span></span>

    ```
    Param="ABSOLUTE_PATH = <path to wmpwiz directory goes here>"
    ```

    

    <span data-ttu-id="ea564-135">Accédez au `<path to wmpwiz directory goes here>` chemin d’accès où se trouvent les fichiers de l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="ea564-135">Change `<path to wmpwiz directory goes here>` to the path where the wizard files are located.</span></span>

    <span data-ttu-id="ea564-136">Supposons, par exemple, que vous disposiez de Visual Studio 2008, et que vos fichiers d’Assistant se trouvent ici : C : \\ Program Files \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ Multimedia \\ WMP \\ assistants \\ wmpwiz.</span><span class="sxs-lookup"><span data-stu-id="ea564-136">For example, suppose you have Visual Studio 2008, and your wizard files are here: C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\WMP\\wizards\\wmpwiz.</span></span> <span data-ttu-id="ea564-137">Votre fichier wmpwiz. vsz ressemble alors à ceci :</span><span class="sxs-lookup"><span data-stu-id="ea564-137">Then your wmpwiz.vsz file would look like this:</span></span>

    ```
    VSWIZARD 7.0
    Wizard=VsWizard.VsWizardEngine.9.0

    Param="WIZARD_NAME = Windows Media Player Plug-in Wizard"
    Param="ABSOLUTE_PATH = C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\Multimedia\WMP\wizards\wmpwiz"
    Param="FALLBACK_LCID = 1033"
    ```

    

4.  <span data-ttu-id="ea564-138">Localisez le dossier dans lequel vous avez installé Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="ea564-138">Locate the folder where you installed Visual Studio.</span></span> <span data-ttu-id="ea564-139">Développez le dossier pour afficher ses sous-dossiers et recherchez un dossier nommé VCProjects.</span><span class="sxs-lookup"><span data-stu-id="ea564-139">Expand the folder to view its subfolders, and locate a folder named vcprojects.</span></span>
5.  <span data-ttu-id="ea564-140">Copiez les trois fichiers listés à l’étape 2 dans le dossier VCProjects.</span><span class="sxs-lookup"><span data-stu-id="ea564-140">Copy the three files listed in step 2 to the vcprojects folder.</span></span> <span data-ttu-id="ea564-141">L’Assistant est maintenant installé.</span><span class="sxs-lookup"><span data-stu-id="ea564-141">The wizard is now installed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ea564-142">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ea564-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ea564-143">Génération d’un plug-in</span><span class="sxs-lookup"><span data-stu-id="ea564-143">Building a Plug-in</span></span>](building-a-plug-in.md)
</dt> <dt>

[<span data-ttu-id="ea564-144">Utilisation de l’Assistant de plug-in avec Visual Studio</span><span class="sxs-lookup"><span data-stu-id="ea564-144">Using the Plug-in Wizard with Visual Studio</span></span>](using-the-plug-in-wizard-with-visual-studio.md)
</dt> </dl>

 

 




