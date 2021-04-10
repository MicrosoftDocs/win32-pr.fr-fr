---
title: Utilisation du contrôle du lecteur Windows Media avec Microsoft Visual Studio
description: Utilisation du contrôle du lecteur Windows Media avec Microsoft Visual Studio
ms.assetid: e007876e-f215-4976-8a70-018fedc0e67d
keywords:
- Lecteur Windows Media, incorporer un contrôle ActiveX
- Modèle objet du lecteur Windows Media, incorporer un contrôle ActiveX
- modèle objet, incorporer un contrôle ActiveX
- Windows Media Player Mobile, incorporer un contrôle ActiveX
- Contrôle ActiveX du lecteur Windows Media, incorporation
- Windows Media Player Mobile, contrôle ActiveX, incorporation
- Contrôle ActiveX, incorporation
- Lecteur Windows Media,. NET Framework
- Windows Media Player Object Model, .NET Framework
- modèle objet, .NET Framework
- Windows Media Player Mobile, .NET Framework
- Contrôle ActiveX du lecteur Windows Media, .NET Framework
- Contrôle ActiveX mobile du lecteur Windows Media, .NET Framework
- Contrôle ActiveX, .NET Framework
- Contrôle ActiveX du lecteur Windows Media, Visual Studio
- Contrôle ActiveX Windows Media Player Mobile, Visual Studio
- Contrôle ActiveX, Visual Studio
- .NET Framework, incorporation de programme Visual Studio
- incorporation, programmes Visual Studio
- Visual Studio, incorporation de programmes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44b01fecd6acdfd5ccc9a7d823740ef3915bf9c6
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/21/2019
ms.locfileid: "104029913"
---
# <a name="using-the-windows-media-player-control-with-microsoft-visual-studio"></a><span data-ttu-id="bef03-123">Utilisation du contrôle du lecteur Windows Media avec Microsoft Visual Studio</span><span class="sxs-lookup"><span data-stu-id="bef03-123">Using the Windows Media Player Control with Microsoft Visual Studio</span></span>

<span data-ttu-id="bef03-124">Vous pouvez ajouter le contrôle ActiveX Windows Media Player 9 ou une version ultérieure à une application .NET Framework par le biais de la boîte à outils de Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="bef03-124">You can add the Windows Media Player 9 Series or later ActiveX control to a .NET Framework application through the Toolbox in Visual Studio.</span></span>

## <a name="adding-the-windows-media-player-control"></a><span data-ttu-id="bef03-125">Ajout du contrôle du lecteur Windows Media</span><span class="sxs-lookup"><span data-stu-id="bef03-125">Adding the Windows Media Player Control</span></span>

<span data-ttu-id="bef03-126">Avant de créer un nouveau projet, assurez-vous que la dernière version du lecteur Windows Media et du kit de développement logiciel (SDK) Windows Media Player est installée sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="bef03-126">Before creating a new project, make sure that the latest version of Windows Media Player and the Windows Media Player SDK is installed on your computer.</span></span>

<span data-ttu-id="bef03-127">Démarrez Visual Studio, puis créez un nouveau projet.</span><span class="sxs-lookup"><span data-stu-id="bef03-127">Start Visual Studio, then create a new project.</span></span>

<span data-ttu-id="bef03-128">Dans Visual Studio, ouvrez la boîte à outils.</span><span class="sxs-lookup"><span data-stu-id="bef03-128">In Visual Studio, open the Toolbox.</span></span>

<span data-ttu-id="bef03-129">Si le lecteur Windows Media n’apparaît pas dans la partie **composants** de la boîte à outils, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="bef03-129">If Windows Media Player does not appear in the **Components** portion of the Toolbox, do the following:</span></span>

1.  <span data-ttu-id="bef03-130">Cliquez avec le bouton droit dans la boîte à outils, puis sélectionnez **choisir les éléments**.</span><span class="sxs-lookup"><span data-stu-id="bef03-130">Right-click within the Toolbox, and then select **Choose Items**.</span></span> <span data-ttu-id="bef03-131">La boîte de dialogue Personnaliser la boîte **à outils** s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="bef03-131">This opens the **Customize Toolbox** dialog box.</span></span>
2.  <span data-ttu-id="bef03-132">Sous l’onglet **composants com** , sélectionnez lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="bef03-132">On the **COM Components** tab, select Windows Media Player.</span></span>

    <span data-ttu-id="bef03-133">Si le lecteur Windows Media n’apparaît pas dans la liste, cliquez sur **Parcourir**, puis ouvrez Wmp.dll, qui doit se trouver dans le \\ dossier Windows system32.</span><span class="sxs-lookup"><span data-stu-id="bef03-133">If Windows Media Player does not appear in the list, click **Browse**, and then open Wmp.dll, which should be in the Windows\\System32 folder.</span></span>

3.  <span data-ttu-id="bef03-134">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="bef03-134">Click **OK**.</span></span> <span data-ttu-id="bef03-135">Le contrôle du lecteur Windows Media est placé dans l’onglet Boîte à outils actif.</span><span class="sxs-lookup"><span data-stu-id="bef03-135">The Windows Media Player control will be placed on the current Toolbox tab.</span></span>

<span data-ttu-id="bef03-136">Vous pouvez maintenant sélectionner Windows Media Player dans la boîte à outils et l’ajouter à un formulaire.</span><span class="sxs-lookup"><span data-stu-id="bef03-136">You can now select Windows Media Player in the Toolbox and add it to a form.</span></span>

<span data-ttu-id="bef03-137">Visual Studio donne au contrôle du lecteur Windows Media un nom par défaut tel que « axWindowsMediaPlayer1 ».</span><span class="sxs-lookup"><span data-stu-id="bef03-137">Visual Studio gives the Windows Media Player control a default name such as "axWindowsMediaPlayer1".</span></span> <span data-ttu-id="bef03-138">Vous pouvez choisir un nom plus facile à mémoriser, tel que « Player ».</span><span class="sxs-lookup"><span data-stu-id="bef03-138">You may want to change the name to something more easily remembered, such as "Player".</span></span>

<span data-ttu-id="bef03-139">L’ajout du contrôle du lecteur Windows Media à partir de la boîte à outils ajoute également des références à deux bibliothèques créées par Visual Studio, AxWMPLib et WMPLib.</span><span class="sxs-lookup"><span data-stu-id="bef03-139">Adding the Windows Media Player control from the Toolbox also adds references to two libraries created by Visual Studio, AxWMPLib and WMPLib.</span></span> <span data-ttu-id="bef03-140">Vous pouvez les trouver dans le Explorateur de solutions sous **références**.</span><span class="sxs-lookup"><span data-stu-id="bef03-140">You can find them in the Solution Explorer under **References**.</span></span>

<span data-ttu-id="bef03-141">Pour faciliter l’utilisation des objets dans l’espace de noms Player, vous devez inclure l’espace de noms dans les directives using ou Imports de vos fichiers, comme suit :</span><span class="sxs-lookup"><span data-stu-id="bef03-141">To make using the objects in the Player namespace easier, you should include the namespace in the using or imports directives of your files, as follows:</span></span>


```Csharp
using WMPLib;
```




```VB
imports WMPLib

```



<span data-ttu-id="bef03-142">La directive garantit que vous pouvez faire référence aux objets **Player** sans qualifier complètement leurs noms.</span><span class="sxs-lookup"><span data-stu-id="bef03-142">The directive ensures that you can refer to **Player** objects without fully qualifying their names.</span></span>

> [!Note]  
> <span data-ttu-id="bef03-143">Le contrôle du lecteur Windows Media est un objet **AxWindowsMediaPlayer** de l’espace de noms **AxWMPLib** .</span><span class="sxs-lookup"><span data-stu-id="bef03-143">The Windows Media Player control is an **AxWindowsMediaPlayer** object from the **AxWMPLib** namespace.</span></span> <span data-ttu-id="bef03-144">Toutefois, la classe **AxWindowsMediaPlayer** utilise des types de données, des interfaces et d’autres éléments de l’espace de noms **wmplib** .</span><span class="sxs-lookup"><span data-stu-id="bef03-144">However, the **AxWindowsMediaPlayer** class uses data types, interfaces, and other elements from the **WMPLib** namespace.</span></span>

 

## <a name="configuring-visibility-of-the-control"></a><span data-ttu-id="bef03-145">Configuration de la visibilité du contrôle</span><span class="sxs-lookup"><span data-stu-id="bef03-145">Configuring Visibility of the Control</span></span>

<span data-ttu-id="bef03-146">Lorsque vous ajoutez pour la première fois le contrôle du lecteur Windows Media à un formulaire, il est visible.</span><span class="sxs-lookup"><span data-stu-id="bef03-146">When you first add the Windows Media Player control to a form, it will be visible.</span></span> <span data-ttu-id="bef03-147">Si vous ne souhaitez pas utiliser l’image visible du lecteur dans votre application, masquez le lecteur par défaut en définissant l’une des propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="bef03-147">If you do not want to use the visible image of the Player in your application, hide the default Player by setting any one of the following properties:</span></span>



| <span data-ttu-id="bef03-148">Propriété</span><span class="sxs-lookup"><span data-stu-id="bef03-148">Property</span></span>        | <span data-ttu-id="bef03-149">Valeur</span><span class="sxs-lookup"><span data-stu-id="bef03-149">Value</span></span>                                                 |
|-----------------|-------------------------------------------------------|
| <span data-ttu-id="bef03-150">**uiMode**</span><span class="sxs-lookup"><span data-stu-id="bef03-150">**uiMode**</span></span>      | <span data-ttu-id="bef03-151">« invisible » (consultez [Player. UIMODE](player-uimode.md).)</span><span class="sxs-lookup"><span data-stu-id="bef03-151">"invisible" (See [Player.uiMode](player-uimode.md).)</span></span> |
| <span data-ttu-id="bef03-152">**Visible**</span><span class="sxs-lookup"><span data-stu-id="bef03-152">**Visible**</span></span>     | <span data-ttu-id="bef03-153">"false"</span><span class="sxs-lookup"><span data-stu-id="bef03-153">"false"</span></span>                                               |
| <span data-ttu-id="bef03-154">**Size. Width**</span><span class="sxs-lookup"><span data-stu-id="bef03-154">**Size.Width**</span></span>  | <span data-ttu-id="bef03-155">0</span><span class="sxs-lookup"><span data-stu-id="bef03-155">0</span></span>                                                     |
| <span data-ttu-id="bef03-156">**Size. Height**</span><span class="sxs-lookup"><span data-stu-id="bef03-156">**Size.Height**</span></span> | <span data-ttu-id="bef03-157">0</span><span class="sxs-lookup"><span data-stu-id="bef03-157">0</span></span>                                                     |



 

<span data-ttu-id="bef03-158">Vous pouvez définir ces propriétés dans le code ou dans la fenêtre **Propriétés** lorsque le contrôle du lecteur Windows Media est sélectionné dans le concepteur de formulaires.</span><span class="sxs-lookup"><span data-stu-id="bef03-158">You can set these properties either in code or in the **Properties** window when the Windows Media Player control is selected in the form designer.</span></span>

## <a name="object-model-compatibility-of-the-control"></a><span data-ttu-id="bef03-159">Compatibilité du modèle objet du contrôle</span><span class="sxs-lookup"><span data-stu-id="bef03-159">Object Model Compatibility of the Control</span></span>

<span data-ttu-id="bef03-160">Le modèle objet pour le contrôle du lecteur Windows Media est fondamentalement le même dans le .NET Framework que dans le code et le script non managés.</span><span class="sxs-lookup"><span data-stu-id="bef03-160">The object model for the Windows Media Player control is basically the same in the .NET Framework as in unmanaged code and script.</span></span> <span data-ttu-id="bef03-161">Toutefois, il existe des différences dans la façon dont les éléments sont exposés :</span><span class="sxs-lookup"><span data-stu-id="bef03-161">However, there are differences in how elements are exposed:</span></span>

-   <span data-ttu-id="bef03-162">La plupart des objets sont exposés sous le nom de leur interface COM sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="bef03-162">Most objects are exposed under the name of their underlying COM interface.</span></span> <span data-ttu-id="bef03-163">Par exemple, l’objet **playlist** est exposé en tant que **IWMPPlaylist**.</span><span class="sxs-lookup"><span data-stu-id="bef03-163">For example, the **Playlist** object is exposed as **IWMPPlaylist**.</span></span>
-   <span data-ttu-id="bef03-164">Certaines interfaces ont des versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="bef03-164">Some interfaces have later versions.</span></span> <span data-ttu-id="bef03-165">Par exemple, **IWMPMedia** a reçu des fonctionnalités supplémentaires dans **IWMPMedia2** et **IWMPMedia3**.</span><span class="sxs-lookup"><span data-stu-id="bef03-165">For example, **IWMPMedia** was given additional functionality in **IWMPMedia2** and **IWMPMedia3**.</span></span> <span data-ttu-id="bef03-166">Si vous déclarez un objet en tant que **IWMPMedia**, vous avez généralement accès aux fonctionnalités de toutes les versions de l’interface.</span><span class="sxs-lookup"><span data-stu-id="bef03-166">If you declare an object as **IWMPMedia**, you usually have access to the functionality of all versions of the interface.</span></span> <span data-ttu-id="bef03-167">Toutefois, IntelliSense® ne reconnaît pas les méthodes ou les propriétés des interfaces ultérieures, et l’éditeur Visual Basic .NET ne corrige pas automatiquement la casse.</span><span class="sxs-lookup"><span data-stu-id="bef03-167">However, IntelliSense® will not recognize the methods or properties of the later-version interfaces, and the Visual Basic .NET editor will not automatically correct capitalization.</span></span> <span data-ttu-id="bef03-168">Pour tirer le meilleur parti d’IntelliSense et d’autres fonctionnalités de Visual Studio, déclarez l’objet à l’aide de la version la plus récente de l’interface, par exemple **IWMPMedia3**.</span><span class="sxs-lookup"><span data-stu-id="bef03-168">To get the full benefit of IntelliSense and other features of Visual Studio, declare the object by using the latest version of the interface, such as **IWMPMedia3**.</span></span>
-   <span data-ttu-id="bef03-169">Il n’existe pas de propriétés indexées (C#) ou de propriétés par défaut (Visual Basic .NET).</span><span class="sxs-lookup"><span data-stu-id="bef03-169">There are no indexed properties (C#) or default properties (Visual Basic .NET).</span></span> <span data-ttu-id="bef03-170">Par exemple, pour récupérer un **élément playlist. Item**, vous devez appeler la méthode d’accesseur **\_ Item IWMPlaylist. Get** en C# ou récupérer la propriété **IWMPlayist. Item** dans Visual Basic .net.</span><span class="sxs-lookup"><span data-stu-id="bef03-170">For example, to retrieve a **Playlist.item**, you must call the **IWMPlaylist.get\_Item** accessor method in C# or retrieve the **IWMPlayist.Item** property in Visual Basic .NET.</span></span>
-   <span data-ttu-id="bef03-171">En raison d’un conflit de noms entre la propriété **contrôles** du lecteur Windows Media et la propriété **contrôles** exposée par chaque contrôle, la version Player de cette propriété est appelée **CtlControls** dans le contexte du contrôle ActiveX.</span><span class="sxs-lookup"><span data-stu-id="bef03-171">Because of a naming conflict between the Windows Media Player **Controls** property and the **Controls** property exposed by every control, the Player version of this property is called **CtlControls** in the context of the ActiveX control.</span></span> <span data-ttu-id="bef03-172">(Toutefois, ce n’est pas le cas lorsque vous créez le joueur par programmation plutôt qu’en tant que contrôle ActiveX.)</span><span class="sxs-lookup"><span data-stu-id="bef03-172">(However, this is not the case when you create the Player programmatically rather than as an ActiveX control.)</span></span>

<span data-ttu-id="bef03-173">Utilisez l’Explorateur d’objets de Visual Studio pour rechercher les noms d’API corrects pour les méthodes et les objets dans les espaces de noms **AxWMPLib** et **wmplib** .</span><span class="sxs-lookup"><span data-stu-id="bef03-173">Use the Object Browser in Visual Studio to locate the correct API names for methods and objects in the **AxWMPLib** and **WMPLib** namespaces.</span></span>

## <a name="distributing-your-application"></a><span data-ttu-id="bef03-174">Distribution de votre application</span><span class="sxs-lookup"><span data-stu-id="bef03-174">Distributing Your Application</span></span>

<span data-ttu-id="bef03-175">Lorsque vous distribuez votre application, veillez à installer AxInterop.WMPLib.dll et Interop.WMPLib.dll dans le dossier de l’application.</span><span class="sxs-lookup"><span data-stu-id="bef03-175">When you distribute your application, be sure to install AxInterop.WMPLib.dll and Interop.WMPLib.dll in the application folder.</span></span> <span data-ttu-id="bef03-176">Vous devrez également vous assurer que la version requise du lecteur Windows Media est installée sur l’ordinateur de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="bef03-176">You will also need to make sure that the required Windows Media Player version is installed on the user's computer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bef03-177">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bef03-177">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bef03-178">**Création du contrôle du lecteur Windows Media par programmation**</span><span class="sxs-lookup"><span data-stu-id="bef03-178">**Creating the Windows Media Player Control Programmatically**</span></span>](creating-the-windows-media-player-control-programmatically.md)
</dt> <dt>

[<span data-ttu-id="bef03-179">**Incorporation du contrôle du lecteur Windows Media dans une solution C#**</span><span class="sxs-lookup"><span data-stu-id="bef03-179">**Embedding the Windows Media Player Control in a C# Solution**</span></span>](embedding-the-windows-media-player-control-in-a-c--solution.md)
</dt> <dt>

[<span data-ttu-id="bef03-180">**Intégration du contrôle du lecteur Windows Media dans une solution Visual Basic .NET**</span><span class="sxs-lookup"><span data-stu-id="bef03-180">**Embedding the Windows Media Player Control in a Visual Basic .NET Solution**</span></span>](embedding-the-windows-media-player-control-in-a-visual-basic--net-solution.md)
</dt> </dl>

 

 




