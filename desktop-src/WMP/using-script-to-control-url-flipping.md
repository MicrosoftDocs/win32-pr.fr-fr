---
title: Utilisation d’un script pour contrôler le basculement d’URL
description: Utilisation d’un script pour contrôler le basculement d’URL
ms.assetid: ec504ecf-10ef-4b90-bee6-8d149c251ee5
keywords:
- Windows Media Player, présentations basées sur le Web
- Modèle objet du lecteur Windows Media, présentations basées sur le Web
- modèle objet, présentations basées sur le Web
- Windows Media Player Mobile, présentations basées sur le Web
- Contrôle ActiveX du lecteur Windows Media, présentations basées sur le Web
- Windows Media Player Mobile contrôle ActiveX, présentations basées sur le Web
- Contrôle ActiveX, présentations basées sur le Web
- Lecteur Windows Media, basculement d’URL
- Windows Media Player Object Model, retournement d’URL
- modèle objet, basculement d’URL
- Windows Media Player Mobile, basculement d’URL
- Contrôle ActiveX du lecteur Windows Media, retournement d’URL
- Windows Media Player Mobile Control, basculement d’URL
- Contrôle ActiveX, basculement d’URL
- Présentations basées sur le Web, retournement d’URL
- création de présentations basées sur le Web, retournement d’URL
- Retournement d’URL
- Lecteur Windows Media, diffusion multimédia riche
- Modèle objet du lecteur Windows Media, diffusion multimédia riche
- modèle objet, diffusion multimédia riche
- Windows Media Player Mobile, diffusion multimédia riche
- Contrôle ActiveX du lecteur Windows Media, diffusion multimédia riche
- Windows Media Player Mobile contrôle ActiveX, diffusion multimédia riche
- Contrôle ActiveX, diffusion multimédia riche
- Présentations basées sur le Web, diffusion multimédia riche
- création de présentations basées sur le Web, diffusion multimédia riche
- diffusion multimédia enrichie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4815562bba92d67bb4b02ea0317d6c29accd9262
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/21/2019
ms.locfileid: "104380473"
---
# <a name="using-script-to-control-url-flipping"></a><span data-ttu-id="e4fc6-130">Utilisation d’un script pour contrôler le basculement d’URL</span><span class="sxs-lookup"><span data-stu-id="e4fc6-130">Using Script to Control URL Flipping</span></span>

<span data-ttu-id="e4fc6-131">Lorsqu’un utilisateur se connecte à un flux multimédia riche alors que le flux est déjà en cours, il est possible que la page Web en continu s’affiche avant que tous les éléments soient arrivés et mis en cache si le lecteur Windows Media appelle automatiquement l’URL.</span><span class="sxs-lookup"><span data-stu-id="e4fc6-131">When a user connects to a rich media stream while the stream is already in progress, it is possible for the streamed webpage to display before all the elements have arrived and been cached if Windows Media Player automatically invokes the URL.</span></span> <span data-ttu-id="e4fc6-132">Dans ce cas, l’utilisateur voit une page Web vide ou incomplète jusqu’à ce que le jeu de données suivant arrive dans le cache.</span><span class="sxs-lookup"><span data-stu-id="e4fc6-132">When this happens, the user sees a blank or incomplete webpage until the next set of data arrives in the cache.</span></span>

<span data-ttu-id="e4fc6-133">Vous pouvez éviter d’afficher une page Web vide ou incomplète en appelant l’URL à l’aide d’un script au lieu de laisser le lecteur Windows Media le faire automatiquement.</span><span class="sxs-lookup"><span data-stu-id="e4fc6-133">You can avoid displaying a blank or incomplete webpage by invoking the URL using script instead of letting Windows Media Player do it automatically.</span></span> <span data-ttu-id="e4fc6-134">De cette façon, vous pouvez ignorer la première inversion de l’URL, puis appeler les URL suivantes à l’aide du code de script.</span><span class="sxs-lookup"><span data-stu-id="e4fc6-134">That way, you can ignore the first URL flip and then invoke subsequent URLs by using script code.</span></span>

> [!Note]  
> <span data-ttu-id="e4fc6-135">Cette section part du principe que vous diffusez en continu du code HTML à l’aide du kit de développement logiciel (SDK) Windows Media Encoder 9 et que vous avez défini le flux HTML sur REPEAT.</span><span class="sxs-lookup"><span data-stu-id="e4fc6-135">This section assumes that you are streaming HTML using the Windows Media Encoder 9 Series SDK and that you have set the HTML stream to repeat.</span></span>

 

<span data-ttu-id="e4fc6-136">Tout d’abord, vous devez créer une page Web de jeu de frames pour contenir le frame avec le lecteur incorporé et le frame qui affiche le HTML de diffusion en continu.</span><span class="sxs-lookup"><span data-stu-id="e4fc6-136">First, you must create a frameset webpage to contain the frame with the embedded Player and the frame that displays the streaming HTML.</span></span> <span data-ttu-id="e4fc6-137">Chacun de ces deux frames affiche une page Web distincte. vous allez donc créer un total de trois pages Web.</span><span class="sxs-lookup"><span data-stu-id="e4fc6-137">Each of these two frames will display a separate webpage initially, so you will create a total of three webpages.</span></span> <span data-ttu-id="e4fc6-138">L’exemple de code suivant illustre la page Web du jeu de cadres :</span><span class="sxs-lookup"><span data-stu-id="e4fc6-138">The following example code demonstrates the frameset webpage:</span></span>


```HTML
<HTML>
<HEAD>
</HEAD>

<FRAMESET cols = "350, *">
  <FRAME  name = "player" src = "embed_player.htm">
  <FRAME  name = "content" src = "blank.htm">

  <NOFRAMES>
  <BODY>

  <P>This page uses frames, but your browser doesn't support them.</P>

  </BODY>
  </NOFRAMES>

</FRAMESET>
</HTML>

```



<span data-ttu-id="e4fc6-139">L’exemple de page Web précédent incorpore deux frames.</span><span class="sxs-lookup"><span data-stu-id="e4fc6-139">The preceding webpage example incorporates two frames.</span></span> <span data-ttu-id="e4fc6-140">La première image s’affiche dans la moitié gauche de la fenêtre du navigateur et affiche la page Web nommée incorporer \_player.htm.</span><span class="sxs-lookup"><span data-stu-id="e4fc6-140">The first frame displays in the left half of the browser window and displays the webpage named embed\_player.htm.</span></span> <span data-ttu-id="e4fc6-141">L’exemple de code suivant crée cette page Web :</span><span class="sxs-lookup"><span data-stu-id="e4fc6-141">The following example code creates this webpage:</span></span>


```HTML
<HTML>
<HEAD>
</HEAD>
<BODY>

<!-- Embed Windows Media Player and disable the invokeURLs parameter -->
<OBJECT CLASSID = "CLSID:6BF52A52-394A-11D3-B153-00C04F79FAA6" ID = "Player">
  <PARAM name = "URL"  value = "https://www.proseware.com/Media/video.wmv">
  <PARAM name = "invokeURLs"  value = "false">
</OBJECT>

<SCRIPT LANGUAGE = "JScript">
  var bFirstURL = true; // Global flag for first URL flip.
</SCRIPT>

<!-- Create an event handler for script commands. -->
<SCRIPT LANGUAGE = "JScript"  FOR = "Player" EVENT = "ScriptCommand(scType, scParam)">

  if("URL" == scType)
  {
    if ( bFirstURL == false )
    {
      // Show the next URL flip.
      parent.content.location = scParam;
    }
    else
    {
      bFirstURL = false; // Set the flag.
    }
  }

</SCRIPT>

</BODY>
</HTML>

```



<span data-ttu-id="e4fc6-142">Le deuxième Frame dans le jeu de frames s’affiche dans la moitié droite de la fenêtre du navigateur et affiche une page Web nommée « blank.htm ».</span><span class="sxs-lookup"><span data-stu-id="e4fc6-142">The second frame in the frameset displays in the right half of the browser window and displays a webpage named "blank.htm".</span></span> <span data-ttu-id="e4fc6-143">L’exemple de code suivant crée cette page Web :</span><span class="sxs-lookup"><span data-stu-id="e4fc6-143">The following example code creates this webpage:</span></span>


```HTML
<HTML>
<HEAD>
</HEAD>
<BODY>

Loading...
</BODY>
</HTML>

```



<span data-ttu-id="e4fc6-144">Lorsque la page du jeu de cadres est chargée dans le navigateur, le frame de gauche montre le lecteur incorporé et le cadre de droite affiche le texte « chargement en cours... ». pour informer l’utilisateur que des données supplémentaires sont à venir.</span><span class="sxs-lookup"><span data-stu-id="e4fc6-144">When the frameset page loads in the browser, the left frame shows the embedded Player and the right frame shows the text "Loading..." to inform the user that more data is forthcoming.</span></span> <span data-ttu-id="e4fc6-145">Lorsque la première commande de script d’URL arrive à partir du flux HTML, le gestionnaire d’événements modifie simplement la valeur de l’indicateur **booléen** .</span><span class="sxs-lookup"><span data-stu-id="e4fc6-145">When the first URL script command arrives from the HTML stream, the event handler simply changes the value of the **Boolean** flag.</span></span> <span data-ttu-id="e4fc6-146">Lorsque chaque commande de script d’URL suivante arrive à partir du flux HTML, le script du gestionnaire d’événements charge la nouvelle URL dans le frame nommé « content » et la page Web complète s’affiche dans le frame situé dans la moitié droite de la fenêtre du navigateur.</span><span class="sxs-lookup"><span data-stu-id="e4fc6-146">When each subsequent URL script command arrives from the HTML stream, the script in the event handler loads the new URL into the frame named "content", and the complete webpage displays in the frame located in the right half of the browser window.</span></span>

<span data-ttu-id="e4fc6-147">Pour plus d’informations sur la diffusion en continu HTML à l’aide de Windows Media, consultez le kit de développement logiciel Windows Media Encoder.</span><span class="sxs-lookup"><span data-stu-id="e4fc6-147">For more information about streaming HTML using Windows Media, see the Windows Media Encoder SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e4fc6-148">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e4fc6-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e4fc6-149">**Diffusion multimédia enrichie**</span><span class="sxs-lookup"><span data-stu-id="e4fc6-149">**Rich Media Streaming**</span></span>](rich-media-streaming.md)
</dt> <dt>

[<span data-ttu-id="e4fc6-150">**Retournement d’URL**</span><span class="sxs-lookup"><span data-stu-id="e4fc6-150">**URL Flipping**</span></span>](url-flipping.md)
</dt> </dl>

 

 




