---
title: Modification de la ressource de boîte de dialogue Echo
description: Modification de la ressource de boîte de dialogue Echo
ms.assetid: 2a371004-82a5-42fb-b19c-ea1928a122a1
keywords:
- Plug-ins du lecteur Windows Media, pages de propriétés de l’exemple Echo
- plug-ins, pages de propriétés d’exemple Echo
- plug-ins de traitement de signal numérique, pages de propriétés d’exemple Echo
- Plug-ins DSP, pages de propriétés d’exemple Echo
- Exemple de plug-in DSP Echo, pages de propriétés
- Echo DSP, exemple de plug-in, ressource de boîte de dialogue
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09caa800376a7962a11912bc582a091f0de52c16
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310645"
---
# <a name="modifying-the-echo-dialog-resource"></a><span data-ttu-id="6f7ca-109">Modification de la ressource de boîte de dialogue Echo</span><span class="sxs-lookup"><span data-stu-id="6f7ca-109">Modifying the Echo Dialog Resource</span></span>

<span data-ttu-id="6f7ca-110">Vous devez modifier la ressource de boîte de dialogue qui est l’interface utilisateur de l’objet de page de propriétés.</span><span class="sxs-lookup"><span data-stu-id="6f7ca-110">You need to change the dialog resource that is the user interface for the property page object.</span></span> <span data-ttu-id="6f7ca-111">Vous pouvez d’abord modifier la zone d’édition et l’étiquette existantes afin qu’elles soient utiles pour la propriété délai, puis ajouter une deuxième zone d’édition et une autre étiquette pour la propriété de combinaison humide.</span><span class="sxs-lookup"><span data-stu-id="6f7ca-111">You can first change the existing edit box and label to be useful for the delay time property and then add a second edit box and label for the wet mix property.</span></span>

<span data-ttu-id="6f7ca-112">Pour modifier la ressource de boîte de dialogue dans Visual C++ :</span><span class="sxs-lookup"><span data-stu-id="6f7ca-112">To edit the dialog resource in Visual C++:</span></span>

1.  <span data-ttu-id="6f7ca-113">Cliquez sur l’onglet **ResourceView** dans l’espace de travail projet.</span><span class="sxs-lookup"><span data-stu-id="6f7ca-113">Click the **ResourceView** tab in the Project Workspace.</span></span>
2.  <span data-ttu-id="6f7ca-114">Développez l’arborescence ressources en ouvrant le dossier de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="6f7ca-114">Expand the resources tree by opening the top level folder.</span></span>
3.  <span data-ttu-id="6f7ca-115">Ouvrez le dossier **boîte de dialogue** .</span><span class="sxs-lookup"><span data-stu-id="6f7ca-115">Open the **Dialog** folder.</span></span>
4.  <span data-ttu-id="6f7ca-116">Double-cliquez sur le nom de la ressource de boîte de dialogue, IDD \_ ECHOPROPPAGE.</span><span class="sxs-lookup"><span data-stu-id="6f7ca-116">Double-click the dialog resource name, IDD\_ECHOPROPPAGE.</span></span> <span data-ttu-id="6f7ca-117">L’éditeur de ressources s’affiche dans le volet droit.</span><span class="sxs-lookup"><span data-stu-id="6f7ca-117">The resource editor appears in the right pane.</span></span>

## <a name="changing-the-existing-resources"></a><span data-ttu-id="6f7ca-118">Modification des ressources existantes</span><span class="sxs-lookup"><span data-stu-id="6f7ca-118">Changing the Existing Resources</span></span>

<span data-ttu-id="6f7ca-119">Pour modifier les ressources de la page de propriétés existante pour la propriété Delay Time :</span><span class="sxs-lookup"><span data-stu-id="6f7ca-119">To change the existing property page resources for the delay time property:</span></span>

1.  <span data-ttu-id="6f7ca-120">Tout d’abord, modifiez le texte dans le contrôle de texte statique existant.</span><span class="sxs-lookup"><span data-stu-id="6f7ca-120">First, change the text in the existing static text control.</span></span> <span data-ttu-id="6f7ca-121">Cliquez avec le bouton droit sur le contrôle, puis choisissez **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="6f7ca-121">Right-click the control and then choose **Properties**.</span></span> <span data-ttu-id="6f7ca-122">Dans le champ **légende** , tapez la nouvelle légende :</span><span class="sxs-lookup"><span data-stu-id="6f7ca-122">In the **Caption** field, type the new caption:</span></span>
    ```C++
    Delay time (0 to 2000):
    
    ```

    

2.  <span data-ttu-id="6f7ca-123">Fermez la boîte de dialogue Propriétés du texte.</span><span class="sxs-lookup"><span data-stu-id="6f7ca-123">Close the Text Properties dialog box.</span></span>
3.  <span data-ttu-id="6f7ca-124">À présent, modifiez le nom du contrôle zone d’édition.</span><span class="sxs-lookup"><span data-stu-id="6f7ca-124">Now, change the name of the edit box control.</span></span> <span data-ttu-id="6f7ca-125">Pour ce faire, cliquez avec le bouton droit sur le contrôle, puis choisissez **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="6f7ca-125">To do this, right-click the control and then choose **Properties**.</span></span> <span data-ttu-id="6f7ca-126">Dans le champ **ID** , tapez un nouveau nom pour le contrôle :</span><span class="sxs-lookup"><span data-stu-id="6f7ca-126">In the **ID** field, type a new name for the control:</span></span>
    ```C++
    IDC_DELAYTIME
    
    ```

    

4.  <span data-ttu-id="6f7ca-127">Fermez la boîte de dialogue Modifier les propriétés.</span><span class="sxs-lookup"><span data-stu-id="6f7ca-127">Close the Edit Properties dialog box.</span></span>
5.  <span data-ttu-id="6f7ca-128">Enregistrez la ressource.</span><span class="sxs-lookup"><span data-stu-id="6f7ca-128">Save the resource.</span></span>
6.  <span data-ttu-id="6f7ca-129">Répondez **Oui** si vous êtes invité à recharger le fichier Resource. h.</span><span class="sxs-lookup"><span data-stu-id="6f7ca-129">Answer **Yes** if prompted to reload the file resource.h.</span></span>
7.  <span data-ttu-id="6f7ca-130">Cliquez sur l’onglet **fileview** dans l’espace de travail projet.</span><span class="sxs-lookup"><span data-stu-id="6f7ca-130">Click the **FileView** tab in the Project Workspace.</span></span> <span data-ttu-id="6f7ca-131">Ouvrez Resource. h</span><span class="sxs-lookup"><span data-stu-id="6f7ca-131">Open resource.h</span></span>
8.  <span data-ttu-id="6f7ca-132">Recherchez la \# ressource définir pour la zone d’édition du facteur d’échelle (IDC \_ SCALEFACTOR) et supprimez-la.</span><span class="sxs-lookup"><span data-stu-id="6f7ca-132">Locate the \#define for the scale factor edit box resource (IDC\_SCALEFACTOR) and delete it.</span></span> <span data-ttu-id="6f7ca-133">Il doit avoir le même numéro d’ID qu’IDC \_ DELAYTIME.</span><span class="sxs-lookup"><span data-stu-id="6f7ca-133">It should have the same id number as IDC\_DELAYTIME.</span></span>

## <a name="adding-the-new-resources"></a><span data-ttu-id="6f7ca-134">Ajout des nouvelles ressources</span><span class="sxs-lookup"><span data-stu-id="6f7ca-134">Adding the New Resources</span></span>

<span data-ttu-id="6f7ca-135">Pour ajouter les nouvelles ressources de la page de propriétés pour la propriété de combinaison humide :</span><span class="sxs-lookup"><span data-stu-id="6f7ca-135">To add the new property page resources for the wet mix property:</span></span>

1.  <span data-ttu-id="6f7ca-136">Cliquez sur l’onglet **ResourceView** dans l’espace de travail du projet pour le sélectionner.</span><span class="sxs-lookup"><span data-stu-id="6f7ca-136">Click the **ResourceView** tab in the Project Workspace to select it.</span></span>
2.  <span data-ttu-id="6f7ca-137">Double-cliquez sur le nom de la boîte de dialogue page de propriétés, IDD \_ ECHOPROPPAGE.</span><span class="sxs-lookup"><span data-stu-id="6f7ca-137">Double-click the name of the property page dialog box, IDD\_ECHOPROPPAGE.</span></span> <span data-ttu-id="6f7ca-138">L’éditeur de ressources s’affiche dans le volet droit.</span><span class="sxs-lookup"><span data-stu-id="6f7ca-138">The resource editor appears in the right pane.</span></span>
3.  <span data-ttu-id="6f7ca-139">Utilisez la boîte à outils pour ajouter un contrôle de texte statique et une zone d’édition à la page de propriétés.</span><span class="sxs-lookup"><span data-stu-id="6f7ca-139">Use the toolbox to add a static text control and an edit box to the property page.</span></span>
4.  <span data-ttu-id="6f7ca-140">Cliquez avec le bouton droit sur le contrôle texte statique et choisissez **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="6f7ca-140">Right-click the static text control and choose **Properties**.</span></span>
5.  <span data-ttu-id="6f7ca-141">Tapez un nouveau nom pour le contrôle de texte statique dans le champ **ID** :</span><span class="sxs-lookup"><span data-stu-id="6f7ca-141">Type a new name for the static text control in the **ID** field:</span></span>
    ```C++
    IDC_MIXLABEL
    
    ```

    

6.  <span data-ttu-id="6f7ca-142">Tapez une légende pour l’étiquette :</span><span class="sxs-lookup"><span data-stu-id="6f7ca-142">Type a caption for the label:</span></span>
    ```C++
    Effect level (%):
    
    ```

    

7.  <span data-ttu-id="6f7ca-143">Fermez la boîte de dialogue Propriétés du texte.</span><span class="sxs-lookup"><span data-stu-id="6f7ca-143">Close the Text Properties dialog box.</span></span>
8.  <span data-ttu-id="6f7ca-144">Cliquez avec le bouton droit sur la zone d’édition et choisissez **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="6f7ca-144">Right-click the edit box and choose **Properties**.</span></span>
9.  <span data-ttu-id="6f7ca-145">Tapez un nouveau nom pour la zone d’édition dans le champ **ID** :</span><span class="sxs-lookup"><span data-stu-id="6f7ca-145">Type a new name for the edit box in the **ID** field:</span></span>
    ```C++
    IDC_WETMIX
    
    ```

    

10. <span data-ttu-id="6f7ca-146">Fermez la boîte de dialogue Modifier les propriétés.</span><span class="sxs-lookup"><span data-stu-id="6f7ca-146">Close the Edit Properties dialog box.</span></span>

<span data-ttu-id="6f7ca-147">Lorsque vous enregistrez le projet, vous pouvez être invité à recharger Resource. h.</span><span class="sxs-lookup"><span data-stu-id="6f7ca-147">When you save the project, you may be prompted to reload resource.h.</span></span> <span data-ttu-id="6f7ca-148">Si cela se produit, cliquez sur **Oui** .</span><span class="sxs-lookup"><span data-stu-id="6f7ca-148">Click **Yes** if this happens.</span></span> <span data-ttu-id="6f7ca-149">L’éditeur de ressources de boîte de dialogue doit ajouter les noms de ressources et les numéros d’ID à Resource. h pour les éléments que vous avez ajoutés.</span><span class="sxs-lookup"><span data-stu-id="6f7ca-149">The dialog box resource editor should add the resource names and id numbers to resource.h for the items you added.</span></span> <span data-ttu-id="6f7ca-150">Si, pour une raison quelconque, cela ne se produit pas, vous devez ouvrir Resource. h et taper de nouvelles entrées pour l’étiquette et le contrôle de zone d’édition, et assigner à chacun un numéro d’identification unique.</span><span class="sxs-lookup"><span data-stu-id="6f7ca-150">If for some reason this doesn't happen, you must open resource.h and type new entries for the label and edit box control, and assign each a unique id number.</span></span>

## <a name="modifying-and-adding-the-string-resources"></a><span data-ttu-id="6f7ca-151">Modification et ajout des ressources de type chaîne</span><span class="sxs-lookup"><span data-stu-id="6f7ca-151">Modifying and Adding the String Resources</span></span>

<span data-ttu-id="6f7ca-152">L’exemple de code de l’Assistant de plug-in spécifie une ressource de type chaîne nommée IDS \_ SCALERANGEERROR qui contient un message à afficher lorsque l’entrée utilisateur est hors limites.</span><span class="sxs-lookup"><span data-stu-id="6f7ca-152">The plug-in wizard sample code specifies a string resource named IDS\_SCALERANGEERROR that contains a message to display when the user input is out of range.</span></span> <span data-ttu-id="6f7ca-153">Vous pouvez modifier cette ressource en fonction de vos besoins pour la valeur de délai en procédant comme suit dans Visual C++ :</span><span class="sxs-lookup"><span data-stu-id="6f7ca-153">You can modify this resource to suit your needs for the delay time value by following these steps in Visual C++:</span></span>

1.  <span data-ttu-id="6f7ca-154">Cliquez sur l’onglet **ResourceView** .</span><span class="sxs-lookup"><span data-stu-id="6f7ca-154">Click the **ResourceView** tab.</span></span>
2.  <span data-ttu-id="6f7ca-155">Ouvrez le dossier **table de chaînes** .</span><span class="sxs-lookup"><span data-stu-id="6f7ca-155">Open the **String Table** folder.</span></span>
3.  <span data-ttu-id="6f7ca-156">Double-cliquez sur l’icône de la **table de chaînes** pour ouvrir l’éditeur de ressources.</span><span class="sxs-lookup"><span data-stu-id="6f7ca-156">Double-click the **String Table** icon to open the resource editor.</span></span>
4.  <span data-ttu-id="6f7ca-157">Double-cliquez sur le nom de la ressource que vous souhaitez modifier, dans le cas présent, IDS \_ SCALERANGEERROR.</span><span class="sxs-lookup"><span data-stu-id="6f7ca-157">Double-click the name of the resource you want to edit, in this case, IDS\_SCALERANGEERROR.</span></span> <span data-ttu-id="6f7ca-158">La boîte de dialogue Propriétés de la chaîne s’affiche.</span><span class="sxs-lookup"><span data-stu-id="6f7ca-158">The String Properties dialog box appears.</span></span>
5.  <span data-ttu-id="6f7ca-159">Remplacez le nom dans le champ **ID** par IDS \_ DELAYRANGEERROR.</span><span class="sxs-lookup"><span data-stu-id="6f7ca-159">Change the name in the **ID** field to IDS\_DELAYRANGEERROR.</span></span>
6.  <span data-ttu-id="6f7ca-160">Modifiez le texte dans le champ **légende** :</span><span class="sxs-lookup"><span data-stu-id="6f7ca-160">Change the text in the **Caption** field:</span></span>
    ```C++
    You must enter a delay time between 0 and 2000 milliseconds.
    
    ```

    

7.  <span data-ttu-id="6f7ca-161">Fermez la boîte de dialogue Propriétés de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="6f7ca-161">Close the String Properties dialog box.</span></span>

<span data-ttu-id="6f7ca-162">Ensuite, ajoutez une nouvelle ressource de type chaîne pour le message d’erreur de propriété de combinaison humide.</span><span class="sxs-lookup"><span data-stu-id="6f7ca-162">Next, add a new string resource for the wet mix property error message.</span></span>

1.  <span data-ttu-id="6f7ca-163">Double-cliquez sur la ligne vide en bas de l’éditeur de ressources.</span><span class="sxs-lookup"><span data-stu-id="6f7ca-163">Double-click the empty line at the bottom of the resource editor.</span></span>
2.  <span data-ttu-id="6f7ca-164">Remplacez le nom dans le champ **ID** par IDS \_ MIXRANGEERROR.</span><span class="sxs-lookup"><span data-stu-id="6f7ca-164">Change the name in the **ID** field to IDS\_MIXRANGEERROR.</span></span>
3.  <span data-ttu-id="6f7ca-165">Ajoutez le texte suivant au champ **Caption** :</span><span class="sxs-lookup"><span data-stu-id="6f7ca-165">Add the following text to the **Caption** field:</span></span>
    ```C++
    You must enter an effect level between 0 and 100 percent.
    
    ```

    

4.  <span data-ttu-id="6f7ca-166">Fermez la boîte de dialogue Propriétés de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="6f7ca-166">Close the String Properties dialog box.</span></span>

<span data-ttu-id="6f7ca-167">Il existe deux autres valeurs que vous pouvez modifier dans la table de chaînes.</span><span class="sxs-lookup"><span data-stu-id="6f7ca-167">There are two other values you will want to change in the String Table.</span></span> <span data-ttu-id="6f7ca-168">ID \_ FRIENDLYNAME est le nom qui apparaît dans l’interface utilisateur du lecteur Windows Media pour identifier le plug-in.</span><span class="sxs-lookup"><span data-stu-id="6f7ca-168">IDS\_FRIENDLYNAME is the name that appears in the Windows Media Player user interface to identify the plug-in.</span></span> <span data-ttu-id="6f7ca-169">Description des ID \_ vous permet de donner à l’utilisateur des informations sur votre plug-in.</span><span class="sxs-lookup"><span data-stu-id="6f7ca-169">IDS\_DESCRIPTION lets you tell the user about your plug-in.</span></span> <span data-ttu-id="6f7ca-170">Ces deux chaînes sont passées en tant que paramètres à la fonction **IWMPMediaPluginRegistrar :: WMPRegisterPlayerPlugin** , qui est appelée dans la méthode DllRegisterServer dans Echodll. cpp.</span><span class="sxs-lookup"><span data-stu-id="6f7ca-170">Both of these strings are passed as parameters to the **IWMPMediaPluginRegistrar::WMPRegisterPlayerPlugin** function, which is called in the DllRegisterServer method in Echodll.cpp.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6f7ca-171">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6f7ca-171">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6f7ca-172">**Modification de la page de propriétés de l’exemple Echo**</span><span class="sxs-lookup"><span data-stu-id="6f7ca-172">**Modifying the Echo Sample Property Page**</span></span>](modifying-the-echo-sample-property-page.md)
</dt> </dl>

 

 




