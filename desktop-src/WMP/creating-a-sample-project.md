---
title: Création d’un exemple de projet
description: Création d’un exemple de projet
ms.assetid: 9cbbd1a7-88e7-4947-8dca-e06e364102f7
keywords:
- Windows Media Player Online stores, création d’exemples de projets
- magasins en ligne, créer des exemples de projets
- type 2 magasins en ligne, création d’exemples de projets
- Magasins en ligne du lecteur Windows Media, exemples de projets
- magasins en ligne, exemples de projets
- types 2 magasins en ligne, exemples de projets
- Windows Media Player Online stores, Assistant projet
- magasins en ligne, Assistant projet
- type 2 magasins en ligne, Assistant projet
- plug-ins, Assistant projet
- Plug-ins du lecteur Windows Media, Assistant projet
- création d’exemples de projets
- exemples, type 2 magasins en ligne
- Assistant projet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4756cc7ae8d27c2a790a7ac96af638eea72d861
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/21/2020
ms.locfileid: "104101325"
---
# <a name="creating-a-sample-project"></a><span data-ttu-id="c885b-117">Création d’un exemple de projet</span><span class="sxs-lookup"><span data-stu-id="c885b-117">Creating a Sample Project</span></span>

<span data-ttu-id="c885b-118">Pour créer un projet à l’aide de l’Assistant projet, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="c885b-118">To create a new project using the project wizard, follow these steps:</span></span>

1.  <span data-ttu-id="c885b-119">Ouvrez Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="c885b-119">Open Microsoft Visual Studio.</span></span>
2.  <span data-ttu-id="c885b-120">Dans le menu **Fichier**, pointez sur **Nouveau**, puis cliquez sur **Projet**.</span><span class="sxs-lookup"><span data-stu-id="c885b-120">From the **File** menu, point to **New**, and then click **Project**.</span></span>
3.  <span data-ttu-id="c885b-121">Dans la zone de liste **types de projets** , choisissez **Visual C++ projets**.</span><span class="sxs-lookup"><span data-stu-id="c885b-121">In the **Project Types** list box, choose **Visual C++ Projects**.</span></span>
4.  <span data-ttu-id="c885b-122">Dans la zone de liste **modèles** , choisissez **Windows Media Player assistant magasins en ligne**.</span><span class="sxs-lookup"><span data-stu-id="c885b-122">In the **Templates** list box, choose **Windows Media Player Online Stores Wizard**.</span></span>
5.  <span data-ttu-id="c885b-123">Tapez un nom et un emplacement pour votre projet.</span><span class="sxs-lookup"><span data-stu-id="c885b-123">Type a name and location for your project.</span></span>
6.  <span data-ttu-id="c885b-124">Cliquez sur **OK** pour démarrer l’Assistant projet.</span><span class="sxs-lookup"><span data-stu-id="c885b-124">Click **OK** to start the project wizard.</span></span>
7.  <span data-ttu-id="c885b-125">Sélectionnez **type 2 (intégration de base)**, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="c885b-125">Select **Type 2 (Basic integration)**, and click **Next**.</span></span>
8.  <span data-ttu-id="c885b-126">Tapez le nom convivial et l’ID du serveur de distribution de contenu pour votre service.</span><span class="sxs-lookup"><span data-stu-id="c885b-126">Type the friendly name and content distributor ID for your service.</span></span> <span data-ttu-id="c885b-127">Tapez l’URL de la page Web qui supprime le service de l’ordinateur de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c885b-127">Type the URL for the webpage that removes the service from the user's computer.</span></span>
    > [!Note]  
    > <span data-ttu-id="c885b-128">La valeur que vous fournissez pour l’ID de serveur de distribution de contenu ne doit pas contenir d’espaces.</span><span class="sxs-lookup"><span data-stu-id="c885b-128">The value you provide for the content distributor ID must not contain spaces.</span></span> <span data-ttu-id="c885b-129">L’Assistant supprime tous les espaces de la chaîne que vous fournissez.</span><span class="sxs-lookup"><span data-stu-id="c885b-129">The wizard removes any spaces from the string you provide.</span></span>

     

9.  <span data-ttu-id="c885b-130">Cliquez sur **Terminer** pour créer le projet.</span><span class="sxs-lookup"><span data-stu-id="c885b-130">Click **Finish** to create the project.</span></span>

<span data-ttu-id="c885b-131">L’Assistant génère automatiquement un nouveau projet C++ qui crée un plug-in de magasin en ligne de type 2 qui implémente les interfaces **IWMPSubscriptionService** et **IWMPSubscriptionService2** .</span><span class="sxs-lookup"><span data-stu-id="c885b-131">The wizard automatically generates a new C++ project that creates a type 2 online store plug-in that implements the **IWMPSubscriptionService** and **IWMPSubscriptionService2** interfaces.</span></span> <span data-ttu-id="c885b-132">Chaque fois que vous exécutez l’Assistant, il crée le même projet, mais le composant qui est créé lorsque vous compilez le projet a un ID de classe unique.</span><span class="sxs-lookup"><span data-stu-id="c885b-132">Each time you run the wizard it creates the same project, but the component that is created when you compile the project has a unique class ID.</span></span> <span data-ttu-id="c885b-133">Le nom du projet, le nom convivial et l’ID du serveur de distribution de contenu peuvent également être différents en fonction des valeurs que vous avez fournies lors de l’exécution de l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="c885b-133">The project name, the friendly name, and content distributor ID may also be different depending on the values you provided when you ran the wizard.</span></span> <span data-ttu-id="c885b-134">L’exemple de projet inscrit le composant à l’aide d’un nom de clé qui correspond à la valeur que vous avez fournie pour le nom convivial.</span><span class="sxs-lookup"><span data-stu-id="c885b-134">The sample project registers the component by using a key name that matches the value you supplied for the friendly name.</span></span>

<span data-ttu-id="c885b-135">L’exemple utilise du code Active Template Library (ATL) pour fournir des implémentations COM.</span><span class="sxs-lookup"><span data-stu-id="c885b-135">The sample uses Active Template Library (ATL) code to provide COM implementations.</span></span>

<span data-ttu-id="c885b-136">L’Assistant crée les fichiers suivants pour vous :</span><span class="sxs-lookup"><span data-stu-id="c885b-136">The wizard creates the following files for you:</span></span>

-   <span data-ttu-id="c885b-137">*NomProjet* dll. cpp.</span><span class="sxs-lookup"><span data-stu-id="c885b-137">*ProjectName* dll.cpp.</span></span> <span data-ttu-id="c885b-138">Implémente les exportations de la bibliothèque de liens dynamiques (DLL), telles que la fonction de point d’entrée DLL principale.</span><span class="sxs-lookup"><span data-stu-id="c885b-138">Implements the Dynamic Link Library (DLL) exports such as the main DLL entry point function.</span></span> <span data-ttu-id="c885b-139">Contient également le mappage d’objet ATL et la déclaration de module.</span><span class="sxs-lookup"><span data-stu-id="c885b-139">Also contains the ATL object map and module declaration.</span></span>
-   <span data-ttu-id="c885b-140">*NomProjet*. cpp.</span><span class="sxs-lookup"><span data-stu-id="c885b-140">*ProjectName*.cpp.</span></span> <span data-ttu-id="c885b-141">Contient des implémentations par défaut pour les méthodes des interfaces IWMPSubscriptionService et IWMPSubscriptionService2.</span><span class="sxs-lookup"><span data-stu-id="c885b-141">Contains default implementations for the methods of the IWMPSubscriptionService and IWMPSubscriptionService2 interfaces.</span></span> <span data-ttu-id="c885b-142">Contient également le code permettant de définir les boîtes de dialogue que l’exemple ouvre lorsque les méthodes sont appelées par le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="c885b-142">Also contains code to define the dialog boxes that the sample opens when methods are called by Windows Media Player.</span></span>
-   <span data-ttu-id="c885b-143">*NomProjet*. def. Déclare les exportations de DLL.</span><span class="sxs-lookup"><span data-stu-id="c885b-143">*ProjectName*.def. Declares the DLL exports.</span></span>
-   <span data-ttu-id="c885b-144">StdAfx. cpp.</span><span class="sxs-lookup"><span data-stu-id="c885b-144">StdAfx.cpp.</span></span> <span data-ttu-id="c885b-145">Comprend des en-têtes standard.</span><span class="sxs-lookup"><span data-stu-id="c885b-145">Includes standard headers.</span></span>
-   <span data-ttu-id="c885b-146">WMP. h.</span><span class="sxs-lookup"><span data-stu-id="c885b-146">wmp.h.</span></span> <span data-ttu-id="c885b-147">Fichier d’en-tête du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="c885b-147">The Windows Media Player header file.</span></span>
-   <span data-ttu-id="c885b-148">wmpplug. h.</span><span class="sxs-lookup"><span data-stu-id="c885b-148">wmpplug.h.</span></span> <span data-ttu-id="c885b-149">Fichier d’en-tête du plug-in du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="c885b-149">The Windows Media Player plug-in header file.</span></span>
-   <span data-ttu-id="c885b-150">subscriptionservices. h.</span><span class="sxs-lookup"><span data-stu-id="c885b-150">subscriptionservices.h.</span></span> <span data-ttu-id="c885b-151">Fichier d’en-tête des magasins en ligne du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="c885b-151">The Windows Media Player online stores header file.</span></span>
-   <span data-ttu-id="c885b-152">Resource. h.</span><span class="sxs-lookup"><span data-stu-id="c885b-152">resource.h.</span></span> <span data-ttu-id="c885b-153">Contient les définitions de ressource.</span><span class="sxs-lookup"><span data-stu-id="c885b-153">Contains resource definitions.</span></span>
-   <span data-ttu-id="c885b-154">**NomProjet**. h.</span><span class="sxs-lookup"><span data-stu-id="c885b-154">**ProjectName**.h.</span></span> <span data-ttu-id="c885b-155">Contient les définitions de classe pour l’objet de magasin en ligne et les boîtes de dialogue.</span><span class="sxs-lookup"><span data-stu-id="c885b-155">Contains class definitions for the online store object and the dialog boxes.</span></span> <span data-ttu-id="c885b-156">Définit l’ID de classe de l’objet et la constante d’ID du serveur de distribution de contenu.</span><span class="sxs-lookup"><span data-stu-id="c885b-156">Defines the object's class ID and the content distributor ID constant.</span></span>
-   <span data-ttu-id="c885b-157">StdAfx. h.</span><span class="sxs-lookup"><span data-stu-id="c885b-157">StdAfx.h.</span></span> <span data-ttu-id="c885b-158">Contient les inclusions système standard.</span><span class="sxs-lookup"><span data-stu-id="c885b-158">Contains standard system includes.</span></span>
-   <span data-ttu-id="c885b-159">*NomProjet*. rc.</span><span class="sxs-lookup"><span data-stu-id="c885b-159">*ProjectName*.rc.</span></span> <span data-ttu-id="c885b-160">Fichier de script de ressources.</span><span class="sxs-lookup"><span data-stu-id="c885b-160">The resource script file.</span></span> <span data-ttu-id="c885b-161">Contient des définitions pour les ressources et les contrôles de boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="c885b-161">This contains definitions for the dialog box resources and controls.</span></span> <span data-ttu-id="c885b-162">Il s’agit également de l’emplacement de stockage de la table de chaînes.</span><span class="sxs-lookup"><span data-stu-id="c885b-162">This is also where the string table is stored.</span></span> <span data-ttu-id="c885b-163">La table de chaînes contient vos constantes de chaîne de nom de projet et de nom convivial.</span><span class="sxs-lookup"><span data-stu-id="c885b-163">The string table contains your project name and friendly name string constants.</span></span> <span data-ttu-id="c885b-164">En général, vous travaillez avec ce fichier dans l’éditeur de ressources de Visual Studio, et non pas en tant que texte brut.</span><span class="sxs-lookup"><span data-stu-id="c885b-164">Usually you work with this file in the Visual Studio resource editor, not as plain text.</span></span>
-   <span data-ttu-id="c885b-165">*NomProjet*. RGS.</span><span class="sxs-lookup"><span data-stu-id="c885b-165">*ProjectName*.rgs.</span></span> <span data-ttu-id="c885b-166">Fichier de script du Registre.</span><span class="sxs-lookup"><span data-stu-id="c885b-166">The registry script file.</span></span> <span data-ttu-id="c885b-167">Ce fichier contient les informations utilisées pour ajouter votre classe de composant au registre afin que le lecteur Windows Media puisse la localiser.</span><span class="sxs-lookup"><span data-stu-id="c885b-167">This file contains the information used to add your component class to the registry so Windows Media Player can locate it.</span></span> <span data-ttu-id="c885b-168">Vous pouvez modifier le nom de clé de votre service dans ce fichier.</span><span class="sxs-lookup"><span data-stu-id="c885b-168">You can change the key name for your service in this file.</span></span>

> [!Note]  
> <span data-ttu-id="c885b-169">Vous devez définir l’adresse de base de votre DLL sur 0x0F100000 pour éviter les conflits avec le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="c885b-169">You should set the base address for your DLL to 0x0F100000 to avoid conflicts with Windows Media Player.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="c885b-170">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c885b-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c885b-171">**Création du plug-in pour un magasin de type 2 en ligne**</span><span class="sxs-lookup"><span data-stu-id="c885b-171">**Building the Plug-in for a Type 2 Online Store**</span></span>](building-the-plug-in-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="c885b-172">**Interface IWMPSubscriptionService**</span><span class="sxs-lookup"><span data-stu-id="c885b-172">**IWMPSubscriptionService Interface**</span></span>](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice)
</dt> <dt>

[<span data-ttu-id="c885b-173">**Interface IWMPSubscriptionService2**</span><span class="sxs-lookup"><span data-stu-id="c885b-173">**IWMPSubscriptionService2 Interface**</span></span>](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice2)
</dt> </dl>

 

 




