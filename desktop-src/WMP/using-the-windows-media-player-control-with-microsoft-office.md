---
title: Utilisation du contrôle du lecteur Windows Media avec Microsoft Office
description: Utilisation du contrôle du lecteur Windows Media avec Microsoft Office
ms.assetid: bc7b2623-8e6d-4af6-b4d0-8087c0159273
keywords:
- Lecteur Windows Media, incorporer un contrôle ActiveX
- Modèle objet du lecteur Windows Media, incorporer un contrôle ActiveX
- modèle objet, incorporer un contrôle ActiveX
- Windows Media Player Mobile, incorporer un contrôle ActiveX
- Contrôle ActiveX du lecteur Windows Media, incorporation
- Windows Media Player Mobile, contrôle ActiveX, incorporation
- Contrôle ActiveX, incorporation
- Windows Media Player, Office
- Windows Media Player Object Model, Office
- modèle objet, Office
- Windows Media Player Mobile, Office
- Contrôle ActiveX du lecteur Windows Media, Office
- Windows Media Player Mobile, contrôle ActiveX, Office
- Contrôle ActiveX, Office
- Incorporation de documents Office
- incorporation, documents Office
- Contrôle ActiveX du lecteur Windows Media, Excel
- Contrôle ActiveX Windows Media Player Mobile, Excel
- Contrôle ActiveX, Excel
- incorporation, feuilles de calcul Excel
- Incorporation dans une feuille de calcul Excel
- Contrôle ActiveX du lecteur Windows Media, PowerPoint
- Windows Media Player Mobile contrôle ActiveX, PowerPoint
- Contrôle ActiveX, PowerPoint
- incorporation, diaporamas PowerPoint
- Incorporation de diaporama PowerPoint
- Windows Media Player ActiveX (contrôle), Word
- Windows Media Player Mobile contrôle ActiveX, Word
- Contrôle ActiveX, Word
- Incorporation de documents Word
- incorporation, documents Word
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2504b46b4fb409dede108c41b43014c3aaeae5ec
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940024"
---
# <a name="using-the-windows-media-player-control-with-microsoft-office"></a><span data-ttu-id="b53a3-134">Utilisation du contrôle du lecteur Windows Media avec Microsoft Office</span><span class="sxs-lookup"><span data-stu-id="b53a3-134">Using the Windows Media Player Control with Microsoft Office</span></span>

<span data-ttu-id="b53a3-135">Cette section explique comment incorporer le contrôle ActiveX du lecteur Windows Media série 9 ou ultérieur dans différents documents créés à l’aide de Microsoft Office XP.</span><span class="sxs-lookup"><span data-stu-id="b53a3-135">This section describes how to embed the Windows Media Player 9 Series or later ActiveX control in various documents created using Microsoft Office XP.</span></span>

<span data-ttu-id="b53a3-136">Dans Microsoft Word, Excel et PowerPoint®, vous incorporez le contrôle en sélectionnant **objet** dans le menu **insertion** , puis en choisissant **lecteur Windows Media** dans la liste des types d’objets disponibles.</span><span class="sxs-lookup"><span data-stu-id="b53a3-136">In Microsoft Word, Excel, and PowerPoint®, you embed the control by selecting **Object** from the **Insert** menu, then choosing **Windows Media Player** from the list of available object types.</span></span> <span data-ttu-id="b53a3-137">Le contrôle du lecteur Windows Media apparaît dans le document à l’emplacement actuel.</span><span class="sxs-lookup"><span data-stu-id="b53a3-137">The Windows Media Player control appears in the document at the current location.</span></span> <span data-ttu-id="b53a3-138">Vous pouvez ensuite sélectionner le contrôle de mise en **forme** (mettre en **forme l’objet** dans Excel) dans le menu contextuel du contrôle pour ajuster la disposition, le style d’habillage du texte et d’autres options de mise en forme.</span><span class="sxs-lookup"><span data-stu-id="b53a3-138">You can then select **Format Control** ( **Format Object** in Excel) from the shortcut menu for the control to adjust the layout, text wrapping style, and other format options.</span></span> <span data-ttu-id="b53a3-139">Dans Word et Excel, vous devez être en mode création pour effectuer cette opération.</span><span class="sxs-lookup"><span data-stu-id="b53a3-139">In Word and Excel, you must be in design mode to do this.</span></span>

<span data-ttu-id="b53a3-140">Une fois que vous avez placé et mis en forme le contrôle, vous pouvez le configurer à l’aide de la boîte de dialogue **Propriétés** , accessible à partir de la boîte **à outils contrôle** ou du menu contextuel en mode création pour Word et Excel.</span><span class="sxs-lookup"><span data-stu-id="b53a3-140">Once you have positioned and formatted the control, you can configure it using the **Properties** dialog box, which is accessible from the **Control Toolbox** or from the shortcut menu in design mode for Word and Excel.</span></span> <span data-ttu-id="b53a3-141">Ici, vous pouvez spécifier des propriétés de contrôle du lecteur de base, telles que le nom du contrôle, l’URL d’un fichier multimédia numérique et le mode de l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b53a3-141">Here you can specify basic Player control properties such as the control name, the URL of a digital media file, and the user interface mode.</span></span> <span data-ttu-id="b53a3-142">Si vous affectez à la propriété **UIMODE** la valeur « None », tous les éléments du contrôle sont masqués à l’exception de la fenêtre vidéo ou de visualisation, ce qui vous permet d’ajouter vos propres boutons et d’écrire du code de script à l’aide de Visual Basic pour applications (VBA) pour gérer les clics de bouton et les événements de contrôle de joueur.</span><span class="sxs-lookup"><span data-stu-id="b53a3-142">Setting the **uiMode** property to "none" hides everything in the control except the video or visualization window, allowing you to add your own buttons and write script code using Visual Basic for Applications (VBA) to handle the button clicks and Player control events.</span></span>

<span data-ttu-id="b53a3-143">À partir de la boîte de dialogue **Propriétés** de base, vous pouvez également accéder à la boîte de dialogue **Propriétés du contrôle du lecteur Windows Media** plus sophistiqué en double-cliquant sur la ligne « (personnalisé) » ou en cliquant sur le bouton de sélection (« ... ») après avoir sélectionné cette ligne.</span><span class="sxs-lookup"><span data-stu-id="b53a3-143">From the basic **Properties** dialog box, you can also access the more sophisticated **Windows Media Player Control Properties** dialog box by double-clicking the "(Custom)" row or by clicking the ellipsis ("...") button after selecting that row.</span></span> <span data-ttu-id="b53a3-144">À partir de cette boîte de dialogue, vous pouvez modifier toutes les propriétés de contrôle de lecteur disponibles.</span><span class="sxs-lookup"><span data-stu-id="b53a3-144">From this dialog box, you can modify all available Player control properties.</span></span>

> [!Note]  
> <span data-ttu-id="b53a3-145">Vous devez veiller à ne pas effectuer d’actions dans les gestionnaires d’événements de contrôle de lecteur qui entraînent la destruction du contrôle.</span><span class="sxs-lookup"><span data-stu-id="b53a3-145">You must be careful not to take actions in Player control event handlers that will result in the control being destroyed.</span></span> <span data-ttu-id="b53a3-146">Par exemple, si vous incorporez le contrôle du lecteur Windows Media sur une diapositive d’une présentation PowerPoint, n’appelez pas la méthode PowerPoint **Next** à partir de l’événement **openStateChange** Player ou d’un autre événement.</span><span class="sxs-lookup"><span data-stu-id="b53a3-146">For example, if you embed the Windows Media Player control on a slide in a PowerPoint presentation, do not call the PowerPoint **Next** method from the Player **openStateChange** event or any other event.</span></span>

 

> [!Note]  
> <span data-ttu-id="b53a3-147">En outre, vous ne devez pas définir la propriété **Player. URL** à partir d’un gestionnaire d’événements de contrôle de joueur.</span><span class="sxs-lookup"><span data-stu-id="b53a3-147">In addition, you should not set the **Player.URL** property from a Player control event handler.</span></span>

 

<span data-ttu-id="b53a3-148">Dans FrontPage, ajoutez le contrôle du lecteur Windows Media à une page Web en sélectionnant **composant Web** dans le menu **insertion** .</span><span class="sxs-lookup"><span data-stu-id="b53a3-148">In FrontPage, add the Windows Media Player control to a webpage by selecting **Web Component** from the **Insert** menu.</span></span> <span data-ttu-id="b53a3-149">Dans la boîte de dialogue **Insérer un composant Web** , sélectionnez **contrôles avancés** dans la liste **type de composant** , puis sélectionnez **contrôle ActiveX** dans la liste des options de contrôle.</span><span class="sxs-lookup"><span data-stu-id="b53a3-149">In the **Insert Web Component** dialog box, select **Advanced Controls** from the **Component type** list, then select **ActiveX Control** from the list of control choices.</span></span> <span data-ttu-id="b53a3-150">Dans la fenêtre suivante de la boîte de dialogue, sélectionnez **lecteur Windows Media**.</span><span class="sxs-lookup"><span data-stu-id="b53a3-150">In the next window of the dialog box, select **Windows Media Player**.</span></span> <span data-ttu-id="b53a3-151">Si elle ne figure pas dans la liste, cliquez sur **personnaliser** , puis activez la case à cocher **lecteur Windows Media** dans la liste de **contrôles** .</span><span class="sxs-lookup"><span data-stu-id="b53a3-151">If it is not listed, click **Customize** and select the **Windows Media Player** check box in the **Control** list.</span></span>

<span data-ttu-id="b53a3-152">Une fois le contrôle du lecteur Windows Media incorporé, vous pouvez le positionner et le redimensionner, puis modifier ses propriétés en sélectionnant **Propriétés du contrôle ActiveX** dans le menu contextuel du contrôle.</span><span class="sxs-lookup"><span data-stu-id="b53a3-152">After the Windows Media Player control is embedded, you can position and resize it, and modify its properties by selecting **ActiveX Control Properties** from the shortcut menu for the control.</span></span> <span data-ttu-id="b53a3-153">Dans l’affichage HTML, les valeurs de propriété que vous spécifiez s’affichent dans l’élément objet représentant le contrôle du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="b53a3-153">In the HTML view, the property values that you specify appear in the OBJECT element representing the Windows Media Player control.</span></span> <span data-ttu-id="b53a3-154">Le nom de l’objet apparaît en tant qu’attribut d’ID, et les propriétés du contrôle apparaissent en tant que balises PARAM.</span><span class="sxs-lookup"><span data-stu-id="b53a3-154">The object name appears as the ID attribute, and the control properties appear as PARAM tags.</span></span> <span data-ttu-id="b53a3-155">Le nom de l’objet vous permet d’accéder au modèle objet de contrôle du lecteur Windows Media, que vous pouvez programmer à l’aide de Microsoft JScript.</span><span class="sxs-lookup"><span data-stu-id="b53a3-155">The object name gives you access to the Windows Media Player control object model, which you can program using Microsoft JScript.</span></span> <span data-ttu-id="b53a3-156">Pour plus d’informations, consultez [utilisation du contrôle du lecteur Windows Media dans une page Web](using-the-windows-media-player-control-in-a-web-page.md).</span><span class="sxs-lookup"><span data-stu-id="b53a3-156">For more information, see [Using the Windows Media Player Control in a Web Page](using-the-windows-media-player-control-in-a-web-page.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b53a3-157">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b53a3-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b53a3-158">**Guide de contrôle du lecteur**</span><span class="sxs-lookup"><span data-stu-id="b53a3-158">**Player Control Guide**</span></span>](player-control-guide.md)
</dt> </dl>

 

 




