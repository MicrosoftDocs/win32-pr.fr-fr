---
title: Utilisation d’un script dans une page Web affichée par Firefox
description: Utilisation d’un script dans une page Web affichée par Firefox
ms.assetid: 0f1d21b1-1824-4ba9-9c0e-bd23ba847d9d
keywords:
- Lecteur Windows Media, incorporer un contrôle ActiveX
- Modèle objet du lecteur Windows Media, incorporer un contrôle ActiveX
- modèle objet, incorporer un contrôle ActiveX
- Windows Media Player Mobile, incorporer un contrôle ActiveX
- Contrôle ActiveX du lecteur Windows Media, incorporation
- Windows Media Player Mobile, contrôle ActiveX, incorporation
- Contrôle ActiveX, incorporation
- Contrôle ActiveX du lecteur Windows Media, pages Web
- Windows Media Player Mobile contrôle ActiveX, pages Web
- Contrôle ActiveX, pages Web
- Contrôle ActiveX du lecteur Windows Media, exemple de script
- Contrôle ActiveX mobile pour Windows Media Player, exemple de script
- Contrôle ActiveX, exemple de script
- incorporation, pages Web
- Incorporation de page Web, exemple de script
- Lecteur Windows Media, Firefox
- Windows Media Player Object Model, Firefox
- modèle objet, Firefox
- Windows Media Player Mobile, Firefox
- Contrôle ActiveX du lecteur Windows Media, Firefox
- Windows Media Player Mobile contrôle ActiveX, Firefox
- Contrôle ActiveX, Firefox
- Firefox, exemple de script
- Incorporation de pages Web, Firefox
- exemple de script pour l’incorporation de pages Web
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8629f87f954d12602999f76483fdd36ab279290
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/21/2019
ms.locfileid: "106510849"
---
# <a name="using-script-in-a-web-page-displayed-by-firefox"></a><span data-ttu-id="653cc-128">Utilisation d’un script dans une page Web affichée par Firefox</span><span class="sxs-lookup"><span data-stu-id="653cc-128">Using Script in a Web Page Displayed by Firefox</span></span>

<span data-ttu-id="653cc-129">Un script sur une page Web peut utiliser le modèle objet de lecteur pour contrôler le lecteur lorsque l’utilisateur interagit avec la page.</span><span class="sxs-lookup"><span data-stu-id="653cc-129">Script on a webpage can use the Player object model to control the Player as the user interacts with the page.</span></span> <span data-ttu-id="653cc-130">Par exemple, l’élément d’entrée suivant contient un script qui définit le volume du lecteur.</span><span class="sxs-lookup"><span data-stu-id="653cc-130">For example, the following INPUT element has script that sets the Player volume.</span></span>


```HTML
<INPUT type="button" value="Vol" OnClick="ChangeVolume()"/>
 
<SCRIPT>
  function ChangeVolume()
  {
    Player.settings.volume = 90;
  }
</SCRIPT>

```



<span data-ttu-id="653cc-131">La plupart des objets du modèle objet du lecteur Windows Media sont pris en charge par Internet Explorer et par le plug-in Firefox.</span><span class="sxs-lookup"><span data-stu-id="653cc-131">Many of the objects in the Windows Media Player object model are supported by Internet Explorer and by the Firefox plug-in.</span></span> <span data-ttu-id="653cc-132">Toutefois, certains objets ne sont pas pris en charge par le plug-in Firefox.</span><span class="sxs-lookup"><span data-stu-id="653cc-132">However, there are some objects that are not supported by the Firefox plug-in.</span></span> <span data-ttu-id="653cc-133">Le tableau suivant répertorie tous les objets du modèle objet de lecteur et indique les objets pris en charge par le plug-in Firefox.</span><span class="sxs-lookup"><span data-stu-id="653cc-133">The following table lists all of the objects in the Player object model and shows which objects are supported by the Firefox plug-in.</span></span>



| <span data-ttu-id="653cc-134">Object</span><span class="sxs-lookup"><span data-stu-id="653cc-134">Object</span></span>                                              | <span data-ttu-id="653cc-135">Prise en charge de Firefox</span><span class="sxs-lookup"><span data-stu-id="653cc-135">Firefox support</span></span> |
|-----------------------------------------------------|-----------------|
| [<span data-ttu-id="653cc-136">-</span><span class="sxs-lookup"><span data-stu-id="653cc-136">Cdrom</span></span>](cdrom-object.md)                           | <span data-ttu-id="653cc-137">non</span><span class="sxs-lookup"><span data-stu-id="653cc-137">no</span></span>              |
| [<span data-ttu-id="653cc-138">CdromCollection</span><span class="sxs-lookup"><span data-stu-id="653cc-138">CdromCollection</span></span>](cdromcollection-object.md)       | <span data-ttu-id="653cc-139">non</span><span class="sxs-lookup"><span data-stu-id="653cc-139">no</span></span>              |
| [<span data-ttu-id="653cc-140">ClosedCaption</span><span class="sxs-lookup"><span data-stu-id="653cc-140">ClosedCaption</span></span>](closedcaption-object.md)           | <span data-ttu-id="653cc-141">Oui</span><span class="sxs-lookup"><span data-stu-id="653cc-141">yes</span></span>             |
| [<span data-ttu-id="653cc-142">Contrôles</span><span class="sxs-lookup"><span data-stu-id="653cc-142">Controls</span></span>](controls-object.md)                     | <span data-ttu-id="653cc-143">non</span><span class="sxs-lookup"><span data-stu-id="653cc-143">no</span></span>              |
| [<span data-ttu-id="653cc-144">DVD</span><span class="sxs-lookup"><span data-stu-id="653cc-144">DVD</span></span>](dvd-object.md)                               | <span data-ttu-id="653cc-145">non</span><span class="sxs-lookup"><span data-stu-id="653cc-145">no</span></span>              |
| [<span data-ttu-id="653cc-146">Error</span><span class="sxs-lookup"><span data-stu-id="653cc-146">Error</span></span>](error-object.md)                           | <span data-ttu-id="653cc-147">Oui</span><span class="sxs-lookup"><span data-stu-id="653cc-147">yes</span></span>             |
| [<span data-ttu-id="653cc-148">ErrorItem</span><span class="sxs-lookup"><span data-stu-id="653cc-148">ErrorItem</span></span>](erroritem-object.md)                   | <span data-ttu-id="653cc-149">Oui</span><span class="sxs-lookup"><span data-stu-id="653cc-149">yes</span></span>             |
| [<span data-ttu-id="653cc-150">Média</span><span class="sxs-lookup"><span data-stu-id="653cc-150">Media</span></span>](media-object.md)                           | <span data-ttu-id="653cc-151">Oui</span><span class="sxs-lookup"><span data-stu-id="653cc-151">yes</span></span>             |
| [<span data-ttu-id="653cc-152">MediaCollection</span><span class="sxs-lookup"><span data-stu-id="653cc-152">MediaCollection</span></span>](mediacollection-object.md)       | <span data-ttu-id="653cc-153">non</span><span class="sxs-lookup"><span data-stu-id="653cc-153">no</span></span>              |
| [<span data-ttu-id="653cc-154">MetadataPicture</span><span class="sxs-lookup"><span data-stu-id="653cc-154">MetadataPicture</span></span>](metadatapicture-object.md)       | <span data-ttu-id="653cc-155">non</span><span class="sxs-lookup"><span data-stu-id="653cc-155">no</span></span>              |
| [<span data-ttu-id="653cc-156">MetadataText</span><span class="sxs-lookup"><span data-stu-id="653cc-156">MetadataText</span></span>](metadatatext-object.md)             | <span data-ttu-id="653cc-157">non</span><span class="sxs-lookup"><span data-stu-id="653cc-157">no</span></span>              |
| [<span data-ttu-id="653cc-158">Réseau</span><span class="sxs-lookup"><span data-stu-id="653cc-158">Network</span></span>](network-object.md)                       | <span data-ttu-id="653cc-159">Oui</span><span class="sxs-lookup"><span data-stu-id="653cc-159">yes</span></span>             |
| [<span data-ttu-id="653cc-160">Lecteur</span><span class="sxs-lookup"><span data-stu-id="653cc-160">Player</span></span>](player-object.md)                         | <span data-ttu-id="653cc-161">Oui</span><span class="sxs-lookup"><span data-stu-id="653cc-161">yes</span></span>             |
| [<span data-ttu-id="653cc-162">PlayerApplication</span><span class="sxs-lookup"><span data-stu-id="653cc-162">PlayerApplication</span></span>](playerapplication-object.md)   | <span data-ttu-id="653cc-163">non</span><span class="sxs-lookup"><span data-stu-id="653cc-163">no</span></span>              |
| [<span data-ttu-id="653cc-164">Playlist</span><span class="sxs-lookup"><span data-stu-id="653cc-164">Playlist</span></span>](playlist-object.md)                     | <span data-ttu-id="653cc-165">Oui</span><span class="sxs-lookup"><span data-stu-id="653cc-165">yes</span></span>             |
| [<span data-ttu-id="653cc-166">PlaylistArray</span><span class="sxs-lookup"><span data-stu-id="653cc-166">PlaylistArray</span></span>](playlistarray-object.md)           | <span data-ttu-id="653cc-167">non</span><span class="sxs-lookup"><span data-stu-id="653cc-167">no</span></span>              |
| [<span data-ttu-id="653cc-168">PlaylistCollection</span><span class="sxs-lookup"><span data-stu-id="653cc-168">PlaylistCollection</span></span>](playlistcollection-object.md) | <span data-ttu-id="653cc-169">non</span><span class="sxs-lookup"><span data-stu-id="653cc-169">no</span></span>              |
| [<span data-ttu-id="653cc-170">Requête</span><span class="sxs-lookup"><span data-stu-id="653cc-170">Query</span></span>](query-object.md)                           | <span data-ttu-id="653cc-171">non</span><span class="sxs-lookup"><span data-stu-id="653cc-171">no</span></span>              |
| [<span data-ttu-id="653cc-172">Paramètres</span><span class="sxs-lookup"><span data-stu-id="653cc-172">Settings</span></span>](settings-object.md)                     | <span data-ttu-id="653cc-173">Oui</span><span class="sxs-lookup"><span data-stu-id="653cc-173">yes</span></span>             |
| [<span data-ttu-id="653cc-174">StringCollection</span><span class="sxs-lookup"><span data-stu-id="653cc-174">StringCollection</span></span>](stringcollection-object.md)     | <span data-ttu-id="653cc-175">non</span><span class="sxs-lookup"><span data-stu-id="653cc-175">no</span></span>              |



 

<span data-ttu-id="653cc-176">Le plug-in Firefox prend en charge l’objet **Player** , mais certaines propriétés de l’objet **Player** renvoient la **valeur null** dans un navigateur Firefox.</span><span class="sxs-lookup"><span data-stu-id="653cc-176">The Firefox plug-in supports the **Player** object, but certain properties of the **Player** object return **NULL** in a Firefox browser.</span></span> <span data-ttu-id="653cc-177">Par exemple, la propriété [cdromCollection](player-cdromcollection.md) de l’objet **Player** retourne la **valeur null** , car le plug-in Firefox ne prend pas en charge l’objet **cdrom** .</span><span class="sxs-lookup"><span data-stu-id="653cc-177">For example, the [cdromCollection](player-cdromcollection.md) property of the **Player** object returns **NULL** because the Firefox plug-in does not support the **Cdrom** object.</span></span> <span data-ttu-id="653cc-178">De même, les propriétés [DVD](player-dvd.md), [mediaCollection](player-mediacollection.md), [playerApplication](player-playerapplication.md)et [playlistCollection](player-playlistcollection.md) de l’objet **Player** renvoient la **valeur null** dans un navigateur Firefox.</span><span class="sxs-lookup"><span data-stu-id="653cc-178">Similarly, the [dvd](player-dvd.md), [mediaCollection](player-mediacollection.md), [playerApplication](player-playerapplication.md), and [playlistCollection](player-playlistcollection.md) properties of the **Player** object return **NULL** in a Firefox browser.</span></span>

<span data-ttu-id="653cc-179">La propriété **Player. pluginVersionInfo** est prise en charge par le plug-in Firefox, mais pas par Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="653cc-179">The **Player.pluginVersionInfo** property is supported by the Firefox plug-in but not by Internet Explorer.</span></span> <span data-ttu-id="653cc-180">Cette propriété retourne la version du plug-in Firefox.</span><span class="sxs-lookup"><span data-stu-id="653cc-180">This property returns the version of the Firefox plug-in.</span></span>

<span data-ttu-id="653cc-181">Le plug-in Firefox prend en charge l’objet **Media** , y compris la propriété [getItemInfoByType](media-getiteminfobytype.md) .</span><span class="sxs-lookup"><span data-stu-id="653cc-181">The Firefox plug-in supports the **Media** object, including the [getItemInfoByType](media-getiteminfobytype.md) property.</span></span> <span data-ttu-id="653cc-182">Toutefois, dans un navigateur Firefox, la propriété **getItemInfoByType** ne prend pas en charge les types de retour **MetadataText** et **MetadataPicture** .</span><span class="sxs-lookup"><span data-stu-id="653cc-182">However, in a Firefox browser, the **getItemInfoByType** property does not support the **MetadataText** and **MetadataPicture** return types.</span></span>

<span data-ttu-id="653cc-183">Le plug-in Firefox prend en charge l’objet [Settings](settings-object.md) , à l’exception de la méthode [setMode](settings-setmode.md) et de la propriété [requestMediaAccessRights](settings-requestmediaaccessrights.md) .</span><span class="sxs-lookup"><span data-stu-id="653cc-183">The Firefox plug-in supports the [Settings](settings-object.md) object except for the [setMode](settings-setmode.md) method and the [requestMediaAccessRights](settings-requestmediaaccessrights.md) property.</span></span> <span data-ttu-id="653cc-184">Dans un navigateur Firefox, la propriété **requestMediaAccessRight** retourne toujours false.</span><span class="sxs-lookup"><span data-stu-id="653cc-184">In a Firefox browser, the **requestMediaAccessRight** property always returns false.</span></span>

## <a name="related-topics"></a><span data-ttu-id="653cc-185">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="653cc-185">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="653cc-186">**Utilisation du contrôle du lecteur Windows Media avec Firefox**</span><span class="sxs-lookup"><span data-stu-id="653cc-186">**Using the Windows Media Player Control with Firefox**</span></span>](using-the-windows-media-player-control-with-firefox.md)
</dt> </dl>

 

 




