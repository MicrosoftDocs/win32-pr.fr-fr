---
title: Installation de l’Assistant de plug-in de boutique en ligne
description: Installation de l’Assistant de plug-in de boutique en ligne
ms.assetid: 75f7c279-4800-4146-8198-1dc76472237d
keywords:
- Windows Media Player Online stores, plug-ins
- magasins en ligne, plug-ins
- types 1 magasins en ligne, plug-ins
- Windows Media Player Online stores, Assistant plug-in
- magasins en ligne, Assistant de plug-in
- tapez 1 magasins en ligne, Assistant de plug-in
- Windows Media Player Online stores, Assistant Installation du plug-in
- magasins en ligne, Assistant Installation du plug-in
- type 1 magasins en ligne, Assistant Installation du plug-in
- plug-ins, Windows Media Player Online stores
- plug-ins, magasins en ligne
- plug-ins, type 1 magasins en ligne
- plug-ins, installation de l’Assistant de plug-in
- plug-ins, Assistant de plug-in
- Plug-ins du lecteur Windows Media, type 1 magasins en ligne
- Plug-ins du lecteur Windows Media, magasins en ligne
- Plug-ins du lecteur Windows Media, magasins en ligne Windows Media Player
- Plug-ins du lecteur Windows Media, Assistant Installation du plug-in
- Plug-ins du lecteur Windows Media, Assistant plug-in
- Assistant Installation du plug-in
- Assistant de plug-in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13d236c2160c5783f909430e6b49ef2e6361de22
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029325"
---
# <a name="installing-the-online-store-plug-in-wizard"></a><span data-ttu-id="5ca50-124">Installation de l’Assistant de plug-in de boutique en ligne</span><span class="sxs-lookup"><span data-stu-id="5ca50-124">Installing the Online Store Plug-in Wizard</span></span>

<span data-ttu-id="5ca50-125">Pour configurer votre environnement de développement afin de créer des plug-ins de magasin en ligne de type 1, vous devez installer les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="5ca50-125">To set up your development environment for creating type 1 online store plug-ins, you must install the following items:</span></span>

-   <span data-ttu-id="5ca50-126">Microsoft Visual Studio 2005 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="5ca50-126">Microsoft Visual Studio 2005 or later</span></span>
-   <span data-ttu-id="5ca50-127">Lecteur Windows Media 11 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="5ca50-127">Windows Media Player 11 or later</span></span>
-   <span data-ttu-id="5ca50-128">SDK Windows, qui comprend le kit de développement logiciel (SDK) du lecteur Windows Media</span><span class="sxs-lookup"><span data-stu-id="5ca50-128">Windows SDK, which includes the Windows Media Player SDK</span></span>
-   <span data-ttu-id="5ca50-129">Assistant de plug-in de magasin en ligne</span><span class="sxs-lookup"><span data-stu-id="5ca50-129">Online store plug-in wizard</span></span>

## <a name="installing-the-wizard"></a><span data-ttu-id="5ca50-130">Installation de l’Assistant</span><span class="sxs-lookup"><span data-stu-id="5ca50-130">Installing the Wizard</span></span>

<span data-ttu-id="5ca50-131">Utilisez les étapes suivantes pour installer l’Assistant de plug-in du magasin en ligne dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="5ca50-131">Use the following steps to install the online store plug-in wizard in Visual Studio.</span></span>

1.  <span data-ttu-id="5ca50-132">Localisez le dossier dans lequel vous avez installé le SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="5ca50-132">Locate the folder where you installed the Windows SDK.</span></span> <span data-ttu-id="5ca50-133">Développez le dossier pour afficher ses sous-dossiers, puis accédez à exemples d' \\ \\ \\ assistants multimédia WMP \\ .</span><span class="sxs-lookup"><span data-stu-id="5ca50-133">Expand the folder to view its subfolders, and navigate to Samples\\Multimedia\\WMP\\wizards\\services.</span></span>
2.  <span data-ttu-id="5ca50-134">Recherchez les trois fichiers suivants :</span><span class="sxs-lookup"><span data-stu-id="5ca50-134">Locate the following three files:</span></span>
    -   <span data-ttu-id="5ca50-135">wmpservices. vsz</span><span class="sxs-lookup"><span data-stu-id="5ca50-135">wmpservices.vsz</span></span>
    -   <span data-ttu-id="5ca50-136">wmpservices. vsdir</span><span class="sxs-lookup"><span data-stu-id="5ca50-136">wmpservices.vsdir</span></span>
    -   <span data-ttu-id="5ca50-137">wmpservices. ico</span><span class="sxs-lookup"><span data-stu-id="5ca50-137">wmpservices.ico</span></span>
3.  <span data-ttu-id="5ca50-138">À l’aide d’un éditeur de texte tel que le bloc-notes, modifiez le fichier wmpservices. vsz.</span><span class="sxs-lookup"><span data-stu-id="5ca50-138">Using a text editor such as Notepad, edit the wmpservices.vsz file.</span></span>

    <span data-ttu-id="5ca50-139">Recherchez la ligne suivante :</span><span class="sxs-lookup"><span data-stu-id="5ca50-139">Locate the following line:</span></span>

    ```
    Wizard=VsWizard.<VsWizardEngine version goes here>
    ```

    

    <span data-ttu-id="5ca50-140">Modifiez l' `<VsWizardEngine version goes here>` une des valeurs suivantes, en fonction de la version de Visual Studio que vous avez installée.</span><span class="sxs-lookup"><span data-stu-id="5ca50-140">Change `<VsWizardEngine version goes here>` to one of the following values, depending on which version of Visual Studio you have installed.</span></span>

    

    | <span data-ttu-id="5ca50-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="5ca50-141">Value</span></span>              | <span data-ttu-id="5ca50-142">Version de Visual Studio</span><span class="sxs-lookup"><span data-stu-id="5ca50-142">Visual Studio version</span></span> |
    |--------------------|-----------------------|
    | <span data-ttu-id="5ca50-143">VsWizardEngine. 8.0</span><span class="sxs-lookup"><span data-stu-id="5ca50-143">VsWizardEngine.8.0</span></span> | <span data-ttu-id="5ca50-144">Visual Studio 2005</span><span class="sxs-lookup"><span data-stu-id="5ca50-144">Visual Studio 2005</span></span>    |
    | <span data-ttu-id="5ca50-145">VsWizardEngine. 9.0</span><span class="sxs-lookup"><span data-stu-id="5ca50-145">VsWizardEngine.9.0</span></span> | <span data-ttu-id="5ca50-146">Visual Studio 2008</span><span class="sxs-lookup"><span data-stu-id="5ca50-146">Visual Studio 2008</span></span>    |

    

     

    <span data-ttu-id="5ca50-147">Recherchez la ligne suivante :</span><span class="sxs-lookup"><span data-stu-id="5ca50-147">Locate the following line:</span></span>

    ```
    Param="ABSOLUTE_PATH = <path to wmpservices directory goes here>"
    ```

    

    <span data-ttu-id="5ca50-148">Accédez au `<path to wmpservices directory goes here>` chemin d’accès où se trouvent les fichiers de l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="5ca50-148">Change `<path to wmpservices directory goes here>` to the path where the wizard files are located.</span></span>

    <span data-ttu-id="5ca50-149">Par exemple, supposons que vous disposez de Visual Studio 2008 et que vos fichiers d’Assistant se trouvent ici : C : \\ Program Files \\ Microsoft SDK \\ Windows \\ v 7.0 \\ exemples \\ multimédia \\ WMP \\ assistants \\ services.</span><span class="sxs-lookup"><span data-stu-id="5ca50-149">For example, suppose you have Visual Studio 2008, and your wizard files are here: C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\WMP\\wizards\\services.</span></span> <span data-ttu-id="5ca50-150">Votre fichier wmpservices. vsz ressemble alors à ceci :</span><span class="sxs-lookup"><span data-stu-id="5ca50-150">Then your wmpservices.vsz file would look like this:</span></span>

    ```
    VSWIZARD 7.0
    Wizard=VsWizard.VsWizardEngine.9.0

    Param="WIZARD_NAME = wmpservices"
    Param="ABSOLUTE_PATH = C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\Multimedia\WMP\wizards\services"
    Param="FALLBACK_LCID = 1033"
    ```

    

4.  <span data-ttu-id="5ca50-151">Localisez le dossier dans lequel vous avez installé Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="5ca50-151">Locate the folder where you installed Visual Studio.</span></span> <span data-ttu-id="5ca50-152">Développez le dossier pour afficher ses sous-dossiers et recherchez un dossier nommé VCProjects.</span><span class="sxs-lookup"><span data-stu-id="5ca50-152">Expand the folder to view its subfolders, and locate a folder named vcprojects.</span></span>
5.  <span data-ttu-id="5ca50-153">Copiez les trois fichiers listés à l’étape 2 dans le dossier VCProjects.</span><span class="sxs-lookup"><span data-stu-id="5ca50-153">Copy the three files listed in step 2 to the vcprojects folder.</span></span> <span data-ttu-id="5ca50-154">L’Assistant est maintenant installé.</span><span class="sxs-lookup"><span data-stu-id="5ca50-154">The wizard is now installed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5ca50-155">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5ca50-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ca50-156">Création du plug-in pour un magasin de type 1 en ligne</span><span class="sxs-lookup"><span data-stu-id="5ca50-156">Building the Plug-in for a Type 1 Online Store</span></span>](building-the-plug-in-for-a-type-1-online-store.md)
</dt> </dl>

 

 




