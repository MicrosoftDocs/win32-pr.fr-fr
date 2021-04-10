---
title: Installation de l’Assistant projet
description: Installation de l’Assistant projet
ms.assetid: bb27e5f0-d49e-46e5-a15f-be1a0a752c1c
keywords:
- Windows Media Player Online stores, plug-ins
- magasins en ligne, plug-ins
- tapez 2 magasins en ligne, plug-ins
- Windows Media Player Online stores, Assistant plug-in
- magasins en ligne, Assistant de plug-in
- type 2 magasins en ligne, Assistant de plug-in
- Windows Media Player Online stores, Assistant projet
- magasins en ligne, Assistant projet
- type 2 magasins en ligne, Assistant projet
- Windows Media Player Online stores, Assistant Installation du plug-in
- magasins en ligne, Assistant Installation du plug-in
- type 2 magasins en ligne, Assistant Installation du plug-in
- Windows Media Player Online stores, Assistant Installation de projet
- magasins en ligne, Assistant Installation de projet
- type 2 magasins en ligne, Assistant Installation de projet
- plug-ins, Windows Media Player Online stores
- plug-ins, magasins en ligne
- plug-ins, type 2 magasins en ligne
- plug-ins, installation de l’Assistant de plug-in
- plug-ins, Assistant de plug-in
- plug-ins, installation de l’Assistant projet
- plug-ins, Assistant projet
- Plug-ins du lecteur Windows Media, type 2 magasins en ligne
- Plug-ins du lecteur Windows Media, magasins en ligne
- Plug-ins du lecteur Windows Media, magasins en ligne Windows Media Player
- Plug-ins du lecteur Windows Media, Assistant Installation du plug-in
- Plug-ins du lecteur Windows Media, Assistant plug-in
- Plug-ins du lecteur Windows Media, Assistant Installation du projet
- Plug-ins du lecteur Windows Media, Assistant projet
- Assistant Installation du plug-in
- Assistant de plug-in
- Assistant Installation de projet
- Assistant projet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc37754a028d73114b1b425dcbc80e268559355d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674193"
---
# <a name="installing-the-project-wizard"></a><span data-ttu-id="633b3-136">Installation de l’Assistant projet</span><span class="sxs-lookup"><span data-stu-id="633b3-136">Installing the Project Wizard</span></span>

<span data-ttu-id="633b3-137">Pour configurer votre environnement de développement afin de créer des plug-ins de magasin en ligne de type 2, vous devez installer les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="633b3-137">To set up your development environment for creating type 2 online store plug-ins, you must install the following items:</span></span>

-   <span data-ttu-id="633b3-138">Microsoft Visual Studio .NET 2003 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="633b3-138">Microsoft Visual Studio .NET 2003 or later</span></span>
-   <span data-ttu-id="633b3-139">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="633b3-139">Windows Media Player 9 Series or later</span></span>
-   <span data-ttu-id="633b3-140">SDK Windows, qui comprend le kit de développement logiciel (SDK) du lecteur Windows Media</span><span class="sxs-lookup"><span data-stu-id="633b3-140">Windows SDK, which includes the Windows Media Player SDK</span></span>
-   <span data-ttu-id="633b3-141">Assistant de plug-in de magasin en ligne</span><span class="sxs-lookup"><span data-stu-id="633b3-141">Online store plug-in wizard</span></span>

## <a name="installing-the-wizard"></a><span data-ttu-id="633b3-142">Installation de l’Assistant</span><span class="sxs-lookup"><span data-stu-id="633b3-142">Installing the Wizard</span></span>

<span data-ttu-id="633b3-143">Utilisez les étapes suivantes pour installer l’Assistant de plug-in du magasin en ligne dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="633b3-143">Use the following steps to install the online store plug-in wizard in Visual Studio.</span></span>

1.  <span data-ttu-id="633b3-144">Localisez le dossier dans lequel vous avez installé le SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="633b3-144">Locate the folder where you installed the Windows SDK.</span></span> <span data-ttu-id="633b3-145">Développez le dossier pour afficher ses sous-dossiers, puis accédez à exemples d' \\ \\ \\ assistants multimédia WMP \\ .</span><span class="sxs-lookup"><span data-stu-id="633b3-145">Expand the folder to view its subfolders, and navigate to Samples\\Multimedia\\WMP\\wizards\\services.</span></span>
2.  <span data-ttu-id="633b3-146">Recherchez les trois fichiers suivants :</span><span class="sxs-lookup"><span data-stu-id="633b3-146">Locate the following three files:</span></span>
    -   <span data-ttu-id="633b3-147">wmpservices. vsz</span><span class="sxs-lookup"><span data-stu-id="633b3-147">wmpservices.vsz</span></span>
    -   <span data-ttu-id="633b3-148">wmpservices. vsdir</span><span class="sxs-lookup"><span data-stu-id="633b3-148">wmpservices.vsdir</span></span>
    -   <span data-ttu-id="633b3-149">wmpservices. ico</span><span class="sxs-lookup"><span data-stu-id="633b3-149">wmpservices.ico</span></span>
3.  <span data-ttu-id="633b3-150">À l’aide d’un éditeur de texte tel que le bloc-notes, modifiez le fichier wmpservices. vsz.</span><span class="sxs-lookup"><span data-stu-id="633b3-150">Using a text editor such as Notepad, edit the wmpservices.vsz file.</span></span>

    <span data-ttu-id="633b3-151">Recherchez la ligne suivante :</span><span class="sxs-lookup"><span data-stu-id="633b3-151">Locate the following line:</span></span>

    ```
    Wizard=VsWizard.<VsWizardEngine version goes here>
    ```

    

    <span data-ttu-id="633b3-152">Modifiez l' `<VsWizardEngine version goes here>` une des valeurs suivantes, en fonction de la version de Visual Studio que vous avez installée.</span><span class="sxs-lookup"><span data-stu-id="633b3-152">Change `<VsWizardEngine version goes here>` to one of the following values, depending on which version of Visual Studio you have installed.</span></span>

    

    | <span data-ttu-id="633b3-153">Valeur</span><span class="sxs-lookup"><span data-stu-id="633b3-153">Value</span></span>              | <span data-ttu-id="633b3-154">Version de Visual Studio</span><span class="sxs-lookup"><span data-stu-id="633b3-154">Visual Studio version</span></span>   |
    |--------------------|-------------------------|
    | <span data-ttu-id="633b3-155">VsWizardEngine. 7.1</span><span class="sxs-lookup"><span data-stu-id="633b3-155">VsWizardEngine.7.1</span></span> | <span data-ttu-id="633b3-156">Visual Studio .NET 2003</span><span class="sxs-lookup"><span data-stu-id="633b3-156">Visual Studio .NET 2003</span></span> |
    | <span data-ttu-id="633b3-157">VsWizardEngine. 8.0</span><span class="sxs-lookup"><span data-stu-id="633b3-157">VsWizardEngine.8.0</span></span> | <span data-ttu-id="633b3-158">Visual Studio 2005</span><span class="sxs-lookup"><span data-stu-id="633b3-158">Visual Studio 2005</span></span>      |
    | <span data-ttu-id="633b3-159">VsWizardEngine. 9.0</span><span class="sxs-lookup"><span data-stu-id="633b3-159">VsWizardEngine.9.0</span></span> | <span data-ttu-id="633b3-160">Visual Studio 2008</span><span class="sxs-lookup"><span data-stu-id="633b3-160">Visual Studio 2008</span></span>      |

    

     

    <span data-ttu-id="633b3-161">Recherchez la ligne suivante :</span><span class="sxs-lookup"><span data-stu-id="633b3-161">Locate the following line:</span></span>

    ```
    Param="ABSOLUTE_PATH = <path to wmpservices directory goes here>"
    ```

    

    <span data-ttu-id="633b3-162">Accédez au `<path to wmpservices directory goes here>` chemin d’accès où se trouvent les fichiers de l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="633b3-162">Change `<path to wmpservices directory goes here>` to the path where the wizard files are located.</span></span>

    <span data-ttu-id="633b3-163">Par exemple, supposons que vous disposez de Visual Studio 2008 et que vos fichiers d’Assistant se trouvent ici : C : \\ Program Files \\ Microsoft SDK \\ Windows \\ v 7.0 \\ exemples \\ multimédia \\ WMP \\ assistants \\ services.</span><span class="sxs-lookup"><span data-stu-id="633b3-163">For example, suppose you have Visual Studio 2008, and your wizard files are here: C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\WMP\\wizards\\services.</span></span> <span data-ttu-id="633b3-164">Votre fichier wmpservices. vsz ressemble alors à ceci :</span><span class="sxs-lookup"><span data-stu-id="633b3-164">Then your wmpservices.vsz file would look like this:</span></span>

    ```
    VSWIZARD 7.0
    Wizard=VsWizard.VsWizardEngine.9.0

    Param="WIZARD_NAME = wmpservices"
    Param="ABSOLUTE_PATH = C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\Multimedia\WMP\wizards\services"
    Param="FALLBACK_LCID = 1033"
    ```

    

4.  <span data-ttu-id="633b3-165">Localisez le dossier dans lequel vous avez installé Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="633b3-165">Locate the folder where you installed Visual Studio.</span></span> <span data-ttu-id="633b3-166">Développez le dossier pour afficher ses sous-dossiers et recherchez un dossier nommé VCProjects.</span><span class="sxs-lookup"><span data-stu-id="633b3-166">Expand the folder to view its subfolders, and locate a folder named vcprojects.</span></span>
5.  <span data-ttu-id="633b3-167">Copiez les trois fichiers listés à l’étape 2 dans le dossier VCProjects.</span><span class="sxs-lookup"><span data-stu-id="633b3-167">Copy the three files listed in step 2 to the vcprojects folder.</span></span> <span data-ttu-id="633b3-168">L’Assistant est maintenant installé.</span><span class="sxs-lookup"><span data-stu-id="633b3-168">The wizard is now installed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="633b3-169">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="633b3-169">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="633b3-170">**Création du plug-in pour un magasin de type 2 en ligne**</span><span class="sxs-lookup"><span data-stu-id="633b3-170">**Building the Plug-in for a Type 2 Online Store**</span></span>](building-the-plug-in-for-a-type-2-online-store.md)
</dt> </dl>

 

 




