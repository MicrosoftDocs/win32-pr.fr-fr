---
title: Utilisation du contrôle du lecteur Windows Media avec Visual Basic
description: Utilisation du contrôle du lecteur Windows Media avec Visual Basic
ms.assetid: 83e5440b-096b-42e1-9038-d779895d9519
keywords:
- Lecteur Windows Media, incorporer un contrôle ActiveX
- Modèle objet du lecteur Windows Media, incorporer un contrôle ActiveX
- modèle objet, incorporer un contrôle ActiveX
- Windows Media Player Mobile, incorporer un contrôle ActiveX
- Contrôle ActiveX du lecteur Windows Media, incorporation
- Windows Media Player Mobile, contrôle ActiveX, incorporation
- Contrôle ActiveX, incorporation
- Lecteur Windows Media, Visual Basic
- Windows Media Player Object Model, Visual Basic
- modèle objet, Visual Basic
- Windows Media Player Mobile, Visual Basic
- Contrôle ActiveX du lecteur Windows Media, Visual Basic
- Contrôle ActiveX Windows Media Player Mobile, Visual Basic
- Contrôle ActiveX, Visual Basic
- Incorporation de programmes basés sur Visual Basic
- incorporation, programmes basés sur des Visual Basic
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8f2ddd78fe5a254f5bf699fbd2557f1e8700c73
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310458"
---
# <a name="using-the-windows-media-player-control-with-visual-basic"></a><span data-ttu-id="2e036-119">Utilisation du contrôle du lecteur Windows Media avec Visual Basic</span><span class="sxs-lookup"><span data-stu-id="2e036-119">Using the Windows Media Player Control with Visual Basic</span></span>

<span data-ttu-id="2e036-120">Cette section décrit comment utiliser le contrôle ActiveX du lecteur Windows Media série 9 ou une version ultérieure dans les applications créées avec Microsoft Visual Basic 6,0.</span><span class="sxs-lookup"><span data-stu-id="2e036-120">This section describes how to use the Windows Media Player 9 Series or later ActiveX control in applications created with Microsoft Visual Basic 6.0.</span></span>

## <a name="getting-started"></a><span data-ttu-id="2e036-121">Mise en route</span><span class="sxs-lookup"><span data-stu-id="2e036-121">Getting Started</span></span>

<span data-ttu-id="2e036-122">Pour ajouter le contrôle du lecteur Windows Media à la boîte à outils, commencez par sélectionner **composants** dans le menu **projet** .</span><span class="sxs-lookup"><span data-stu-id="2e036-122">To add the Windows Media Player control to the toolbox, first select **Components** from the **Project** menu.</span></span> <span data-ttu-id="2e036-123">Dans la boîte de dialogue composants, activez la case à cocher en regard de « lecteur Windows Media ».</span><span class="sxs-lookup"><span data-stu-id="2e036-123">In the Components dialog box, select the check box next to "Windows Media Player".</span></span> <span data-ttu-id="2e036-124">En bas de la boîte de dialogue, vérifiez que le fichier sélectionné est wmp.dll.</span><span class="sxs-lookup"><span data-stu-id="2e036-124">At the bottom of the dialog box, confirm that the selected file is wmp.dll.</span></span> <span data-ttu-id="2e036-125">Après avoir fermé la boîte de dialogue, vous pouvez placer une instance du contrôle du lecteur Windows Media sur votre formulaire de la façon habituelle.</span><span class="sxs-lookup"><span data-stu-id="2e036-125">After closing the dialog box, you can place an instance of the Windows Media Player control on your form in the usual ways.</span></span>

<span data-ttu-id="2e036-126">Vous pouvez définir de nombreuses propriétés de contrôle à l’aide de l’Fenêtre Propriétés.</span><span class="sxs-lookup"><span data-stu-id="2e036-126">You can set many control properties using the Properties window.</span></span> <span data-ttu-id="2e036-127">Pour définir certaines propriétés, vous devez utiliser la boîte de dialogue Propriétés du lecteur Windows Media, que vous ouvrez à l’aide de l’élément « (personnalisé) » dans le Fenêtre Propriétés.</span><span class="sxs-lookup"><span data-stu-id="2e036-127">To set some properties you must use the Windows Media Player Properties dialog box, which you open using the "(Custom)" item in the Properties window.</span></span>

## <a name="object-references"></a><span data-ttu-id="2e036-128">Références d'objet</span><span class="sxs-lookup"><span data-stu-id="2e036-128">Object References</span></span>

<span data-ttu-id="2e036-129">Vous utilisez certaines propriétés de contrôle de lecteur pour récupérer des références à des objets particuliers.</span><span class="sxs-lookup"><span data-stu-id="2e036-129">You use certain Player control properties to get references to particular objects.</span></span> <span data-ttu-id="2e036-130">Par exemple, la propriété **cdromCollection** retourne une référence à un objet **cdromCollection** .</span><span class="sxs-lookup"><span data-stu-id="2e036-130">For example, the **cdromCollection** property returns a reference to a **CdromCollection** object.</span></span> <span data-ttu-id="2e036-131">Vous devez assigner une telle référence à une variable que vous avez déclarée en tant qu’interface correspondante.</span><span class="sxs-lookup"><span data-stu-id="2e036-131">You must assign such a reference to a variable that you declared as the corresponding interface.</span></span> <span data-ttu-id="2e036-132">Dans le cas de la propriété **cdromCollection** , par exemple, vous affectez sa valeur de retour à une variable de type **IWMPCdromCollection**.</span><span class="sxs-lookup"><span data-stu-id="2e036-132">In the case of the **cdromCollection** property, for example, you assign its return value to a variable of type **IWMPCdromCollection**.</span></span>

<span data-ttu-id="2e036-133">Lisez la rubrique [interfaces](interfaces.md) dans la [Référence du modèle objet pour C++](object-model-reference-for-c.md) afin d’identifier les objets qui implémentent plusieurs interfaces.</span><span class="sxs-lookup"><span data-stu-id="2e036-133">Read the [Interfaces](interfaces.md) topic in the [Object Model Reference for C++](object-model-reference-for-c.md) to identify which objects implement multiple interfaces.</span></span> <span data-ttu-id="2e036-134">Dans ce cas, vous devez déclarer une variable objet en tant qu’interface avec un numéro le plus élevé documenté dans ce kit de développement logiciel (SDK) pour accéder à toutes les propriétés et méthodes de cet objet.</span><span class="sxs-lookup"><span data-stu-id="2e036-134">In those cases, you must declare an object variable as the highest-numbered interface documented in this SDK to have access to all of the properties and methods of that object.</span></span> <span data-ttu-id="2e036-135">Par exemple, vous devez affecter la valeur de la propriété **currentMedia** du contrôle du lecteur Windows Media à une variable déclarée comme **IWMPMedia3** pour vous assurer que vous avez accès aux méthodes **getAttributeCountByType** et **getItemInfoByType** .</span><span class="sxs-lookup"><span data-stu-id="2e036-135">For example, you should assign the value of the Windows Media Player control **currentMedia** property to a variable declared as **IWMPMedia3** to assure that you have access to the **getAttributeCountByType** and **getItemInfoByType** methods.</span></span>

> [!Note]  
> <span data-ttu-id="2e036-136">L’objet **WindowsMediaPlayer** implémente toutes les propriétés et méthodes des interfaces **IWMPCore**, **IWMPCore2**, **IWMPCore3**, **IWMPPlayer**, **IWMPPlayer2**, **IWMPPlayer3** et **IWMPPlayer4** .</span><span class="sxs-lookup"><span data-stu-id="2e036-136">The **WindowsMediaPlayer** object implements all of the properties and methods of the **IWMPCore**, **IWMPCore2**, **IWMPCore3**, **IWMPPlayer**, **IWMPPlayer2**, **IWMPPlayer3**, and **IWMPPlayer4** interfaces.</span></span> <span data-ttu-id="2e036-137">Vous n’avez pas besoin de déclarer des variables distinctes pour l’une de ces interfaces.</span><span class="sxs-lookup"><span data-stu-id="2e036-137">You do not need to declare separate variables for any of these interfaces.</span></span> <span data-ttu-id="2e036-138">Vous pouvez accéder à l’ensemble de ses membres à l’aide du nom que vous avez attribué à votre instance **WindowsMediaPlayer** .</span><span class="sxs-lookup"><span data-stu-id="2e036-138">You can access all of their members using the name you assigned to your **WindowsMediaPlayer** instance.</span></span>

 

<span data-ttu-id="2e036-139">Dans l’Explorateur d’objets Visual Basic, vous verrez de nombreuses interfaces destinées à une utilisation privée par le contrôle du lecteur Windows Media, y compris certains qui prennent en charge les développeurs d’apparences.</span><span class="sxs-lookup"><span data-stu-id="2e036-139">In the Visual Basic Object Browser you will see many interfaces that are intended for private use by the Windows Media Player control, including some that support skin developers.</span></span> <span data-ttu-id="2e036-140">Vous devez utiliser uniquement les objets, les propriétés, les méthodes et les événements documentés dans ce kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="2e036-140">You should use only the objects, properties, methods, and events that are documented in this SDK.</span></span>

## <a name="additional-tips"></a><span data-ttu-id="2e036-141">Conseils supplémentaires</span><span class="sxs-lookup"><span data-stu-id="2e036-141">Additional Tips</span></span>

-   <span data-ttu-id="2e036-142">La documentation de référence montre la syntaxe JScript.</span><span class="sxs-lookup"><span data-stu-id="2e036-142">The reference documentation shows JScript syntax.</span></span> <span data-ttu-id="2e036-143">En JScript, les arguments passés aux méthodes sont toujours placés entre parenthèses.</span><span class="sxs-lookup"><span data-stu-id="2e036-143">In JScript, arguments passed to methods are always enclosed in parentheses.</span></span> <span data-ttu-id="2e036-144">Dans Visual Basic 6,0, les arguments passés aux méthodes qui ne retournent pas de valeur ne doivent pas être placés entre parenthèses.</span><span class="sxs-lookup"><span data-stu-id="2e036-144">In Visual Basic 6.0, arguments passed to methods that do not return a value must not be enclosed in parentheses.</span></span>
-   <span data-ttu-id="2e036-145">Certaines propriétés ou méthodes peuvent ne pas s’afficher dans la fonctionnalité de saisie semi-automatique de code dans le Visual Basic éditeur de code.</span><span class="sxs-lookup"><span data-stu-id="2e036-145">Some properties or methods may not appear in the Auto List code-completion feature in the Visual Basic code editor.</span></span> <span data-ttu-id="2e036-146">Vous pouvez toujours utiliser ces membres en tapant leurs noms exactement tels qu’ils apparaissent dans cette documentation.</span><span class="sxs-lookup"><span data-stu-id="2e036-146">You can still use those members by typing their names exactly as they appear in this documentation.</span></span>
-   <span data-ttu-id="2e036-147">Gérez l’apparence visuelle du contrôle à l’aide de la propriété **UIMODE** .</span><span class="sxs-lookup"><span data-stu-id="2e036-147">Manage the visual appearance of the control using the **uimode** property.</span></span> <span data-ttu-id="2e036-148">Vous pouvez le faire de deux manières.</span><span class="sxs-lookup"><span data-stu-id="2e036-148">You can do so in two ways.</span></span> <span data-ttu-id="2e036-149">Vous pouvez utiliser la liste déroulante **Sélectionner un mode** dans la boîte de dialogue Propriétés du lecteur Windows Media, ou vous pouvez taper la valeur correcte dans la fenêtre Propriétés.</span><span class="sxs-lookup"><span data-stu-id="2e036-149">You can use the **Select a mode** drop-down list in the Windows Media Player Properties dialog box, or you can type the correct value in the Properties window.</span></span>

    <span data-ttu-id="2e036-150">En particulier, n’utilisez pas la propriété **visible** pour masquer le contrôle. Affectez plutôt la valeur « invisible » à la propriété **UIMODE** .</span><span class="sxs-lookup"><span data-stu-id="2e036-150">In particular, do not use the **visible** property to hide the control; instead, assign the value "invisible" to the **uimode** property.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2e036-151">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2e036-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2e036-152">**Guide de contrôle du lecteur**</span><span class="sxs-lookup"><span data-stu-id="2e036-152">**Player Control Guide**</span></span>](player-control-guide.md)
</dt> </dl>

 

 




