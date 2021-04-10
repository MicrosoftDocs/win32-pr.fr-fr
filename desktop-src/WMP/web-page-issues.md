---
title: Problèmes de page Web
description: Problèmes de page Web
ms.assetid: fd97540e-21e9-443e-99ec-ed29f4a2570a
keywords:
- Sélections de métafichiers Windows Media, pages Web
- sélections, pages Web
- sélections de métafichiers, pages Web
- Sélections de métafichiers Windows Media, personnalisation de HTMLView
- sélections, personnalisation de HTMLView
- sélections de métafichiers, personnalisation de HTMLView
- Sélections de métafichiers Windows Media, personnalisation de HTMLView
- sélections, HTMLView personnalisation
- sélections de métafichiers, personnalisation de HTMLView
- personnalisation de HTMLView
- Windows Media Player, pages Web
- Lecteur Windows Media, personnalisation de HTMLView
- Lecteur Windows Media, personnalisation de HTMLView
- HTMLView, personnalisation
- HTMLView, pages Web
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 882d8993ba3690cf8c4a068f9861ccf39cd1a95c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675134"
---
# <a name="web-page-issues"></a><span data-ttu-id="1dcf1-118">Problèmes de page Web</span><span class="sxs-lookup"><span data-stu-id="1dcf1-118">Web Page Issues</span></span>

<span data-ttu-id="1dcf1-119">Certains éléments sont à prendre en compte lorsque vous créez une page Web à afficher dans la fonctionnalité de **lecture à présent** du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="1dcf1-119">There are some things to consider when you create a webpage to be displayed in the Windows Media Player **Now Playing** feature.</span></span> <span data-ttu-id="1dcf1-120">Cette section présente certains des problèmes que vous pouvez rencontrer lors de la création de votre contenu Web.</span><span class="sxs-lookup"><span data-stu-id="1dcf1-120">This section discusses some of the issues you might encounter when creating your Web-based content.</span></span>

## <a name="customizing-htmlview"></a><span data-ttu-id="1dcf1-121">Personnalisation de HTMLView</span><span class="sxs-lookup"><span data-stu-id="1dcf1-121">Customizing HTMLView</span></span>

<span data-ttu-id="1dcf1-122">Votre page Web HTMLView peut être aussi simple ou complexe que vous le souhaitez.</span><span class="sxs-lookup"><span data-stu-id="1dcf1-122">Your HTMLView webpage can be as simple or complex as you want.</span></span> <span data-ttu-id="1dcf1-123">Vous pouvez inclure l’un des éléments que vous utilisez généralement dans votre contenu Web.</span><span class="sxs-lookup"><span data-stu-id="1dcf1-123">You can include any of the elements you usually use in your Web-based content.</span></span> <span data-ttu-id="1dcf1-124">Si vous incorporez le contrôle du lecteur Windows Media, vous pouvez afficher l’une des interfaces utilisateur fournies par le contrôle, créer votre propre interface utilisateur à l’aide de code HTML et de script ou ne fournir aucune interface utilisateur (ce qui signifie que l’utilisateur peut utiliser les contrôles de transport du lecteur en mode complet).</span><span class="sxs-lookup"><span data-stu-id="1dcf1-124">If you embed the Windows Media Player control, you can display one of the user interfaces supplied by the control, create your own user interface using HTML and script code, or provide no UI at all (which means that the user can use the transport controls of the full-mode Player).</span></span>

<span data-ttu-id="1dcf1-125">La taille recommandée pour les pages Web affichées à l’aide de la fonctionnalité HTMLView est de 575 x 345 pixels.</span><span class="sxs-lookup"><span data-stu-id="1dcf1-125">The recommended size for webpages displayed by using the HTMLView feature is 575 x 345 pixels.</span></span> <span data-ttu-id="1dcf1-126">Toutefois, l’utilisateur a la possibilité de redimensionner le lecteur Windows Media et de choisir la résolution d’écran.</span><span class="sxs-lookup"><span data-stu-id="1dcf1-126">The user, however, has the ability to resize Windows Media Player and choose the screen resolution.</span></span> <span data-ttu-id="1dcf1-127">Si la page Web HTMLView est supérieure à la taille prise en charge par la fonctionnalité de **lecture** en cours, le lecteur affiche des barres de défilement horizontales et verticales qui permettent à l’utilisateur de voir la page entière.</span><span class="sxs-lookup"><span data-stu-id="1dcf1-127">If the HTMLView webpage is larger than the size accommodated by the **Now Playing** feature, the Player displays horizontal and vertical scroll bars that enable the user to see the entire page.</span></span> <span data-ttu-id="1dcf1-128">Vous devez tester votre contenu HTMLView à l’aide d’une variété de résolutions d’écran et de tailles de lecteur pour déterminer la taille optimale de votre page Web.</span><span class="sxs-lookup"><span data-stu-id="1dcf1-128">You should test your HTMLView content using a variety of screen resolutions and Player sizes to determine the best size for your webpage.</span></span>

<span data-ttu-id="1dcf1-129">Le lecteur Windows Media ne fournit pas de méthode qui vous permet de spécifier une taille pour le lecteur en mode plein.</span><span class="sxs-lookup"><span data-stu-id="1dcf1-129">Windows Media Player does not provide a method that enables you to specify a size for the full-mode Player.</span></span>

## <a name="web-page-navigation"></a><span data-ttu-id="1dcf1-130">Navigation entre les pages Web</span><span class="sxs-lookup"><span data-stu-id="1dcf1-130">Web page navigation</span></span>

<span data-ttu-id="1dcf1-131">Le lecteur Windows Media ne fournit pas de barre d’outils de navigation pour les pages Web affichées dans la fonctionnalité de **lecture** en cours.</span><span class="sxs-lookup"><span data-stu-id="1dcf1-131">Windows Media Player does not provide a navigation toolbar for webpages displayed in the **Now Playing** feature.</span></span> <span data-ttu-id="1dcf1-132">Cela signifie que vous avez un contrôle total sur le fait que les utilisateurs puissent quitter votre page Web HTMLView.</span><span class="sxs-lookup"><span data-stu-id="1dcf1-132">This means that you have complete control over whether users can navigate away from your HTMLView webpage.</span></span> <span data-ttu-id="1dcf1-133">Si vous souhaitez permettre aux utilisateurs d’accéder à d’autres pages Web, vous devez inclure des éléments dans votre code HTML pour fournir cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="1dcf1-133">If you want to enable users to navigate to other webpages, you must include elements in your HTML code to provide that functionality.</span></span>

## <a name="retrieving-the-parent-window"></a><span data-ttu-id="1dcf1-134">Récupération de la fenêtre parente</span><span class="sxs-lookup"><span data-stu-id="1dcf1-134">Retrieving the parent window</span></span>

<span data-ttu-id="1dcf1-135">Si votre code de script existant utilise **Window. parent** pour récupérer l’objet de fenêtre parente, ce code ne fonctionnera pas dans votre page Web HTMLView.</span><span class="sxs-lookup"><span data-stu-id="1dcf1-135">If your existing script code uses **window.parent** to retrieve the parent window object, this code will not work in your HTMLView webpage.</span></span> <span data-ttu-id="1dcf1-136">Quand vous utilisez HTMLView, il n’y a pas d’objet de fenêtre parente. par conséquent, cette fonctionnalité de script n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="1dcf1-136">When you use HTMLView, there is no parent window object; therefore, this scripting feature is unavailable.</span></span>

## <a name="about-the-embedded-browser"></a><span data-ttu-id="1dcf1-137">À propos du navigateur incorporé</span><span class="sxs-lookup"><span data-stu-id="1dcf1-137">About the embedded browser</span></span>

<span data-ttu-id="1dcf1-138">Étant donné que le lecteur Windows Media utilise une instance incorporée d’Internet Explorer pour afficher le contenu de HTMLView, les paramètres et stratégies utilisateur pour Internet Explorer s’appliquent à toutes les pages Web affichées dans le lecteur.</span><span class="sxs-lookup"><span data-stu-id="1dcf1-138">Because Windows Media Player uses an embedded instance of Internet Explorer to display HTMLView content, the user settings and policies for Internet Explorer apply to any webpages displayed in the Player.</span></span> <span data-ttu-id="1dcf1-139">Par exemple, si l’utilisateur a configuré Internet Explorer pour empêcher les pages Web de télécharger des cookies sur l’ordinateur, il est également interdit à votre page Web HTMLView de le faire.</span><span class="sxs-lookup"><span data-stu-id="1dcf1-139">For example, if the user has configured Internet Explorer to prevent webpages from downloading cookies to the computer, your HTMLView webpage is also prevented from doing this.</span></span>

<span data-ttu-id="1dcf1-140">Les pages Web ouvertes à l’aide de la fonctionnalité HTMLView s’exécutent toujours dans la zone de sécurité **Internet** d’Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="1dcf1-140">Web pages opened by using the HTMLView feature always run in the Internet Explorer **Internet** security zone.</span></span>

<span data-ttu-id="1dcf1-141">Le contrôle de navigateur Web incorporé utilise les mêmes règles pour mettre en cache les pages Web que la version autonome d’Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="1dcf1-141">The embedded Web browser control uses the same rules to cache webpages as the stand-alone version of Internet Explorer.</span></span> <span data-ttu-id="1dcf1-142">Il est judicieux d’utiliser des pages de Active Server (ASP) lors de la création de votre contenu pour vous assurer que le contenu est remis à partir de votre serveur Web chaque fois que le lecteur Windows Media accède à la page Web HTMLView.</span><span class="sxs-lookup"><span data-stu-id="1dcf1-142">It's a good idea to use Active Server Pages (ASP) when creating your content to ensure that the content is delivered from your web server each time Windows Media Player accesses the HTMLView webpage.</span></span> <span data-ttu-id="1dcf1-143">L’utilisation de pages ASP peut être aussi simple que l’attribution d’un nouveau nom à votre page Web pour utiliser une extension de nom de fichier. asp.</span><span class="sxs-lookup"><span data-stu-id="1dcf1-143">Using ASP pages can be as simple as renaming your webpage to use an .asp file name extension.</span></span>

## <a name="about-local-web-content"></a><span data-ttu-id="1dcf1-144">À propos du contenu Web local</span><span class="sxs-lookup"><span data-stu-id="1dcf1-144">About local Web content</span></span>

<span data-ttu-id="1dcf1-145">La fonctionnalité HTMLView ne vous permet pas d’ouvrir des pages Web qui sont stockées sur l’ordinateur de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1dcf1-145">The HTMLView feature does not allow you to open webpages that are stored on the user's computer.</span></span>

## <a name="prompting-the-user"></a><span data-ttu-id="1dcf1-146">Invitation de l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="1dcf1-146">Prompting the user</span></span>

<span data-ttu-id="1dcf1-147">Vous pouvez utiliser **Window. prompt** pour inviter l’utilisateur à fournir des informations.</span><span class="sxs-lookup"><span data-stu-id="1dcf1-147">You can use **window.prompt** to prompt the user for information.</span></span> <span data-ttu-id="1dcf1-148">Toutefois, **Window. Alert** et **Window. Confirm** ne sont pas disponibles lors de l’utilisation de HTMLView.</span><span class="sxs-lookup"><span data-stu-id="1dcf1-148">However, **window.alert** and **window.confirm** are not available when using HTMLView.</span></span>

## <a name="timing-issues"></a><span data-ttu-id="1dcf1-149">Problèmes de synchronisation</span><span class="sxs-lookup"><span data-stu-id="1dcf1-149">Timing issues</span></span>

<span data-ttu-id="1dcf1-150">Vous pouvez rencontrer des problèmes de synchronisation lors de l’utilisation d’un contrôle de lecteur Windows Media incorporé dans votre page Web HTMLView.</span><span class="sxs-lookup"><span data-stu-id="1dcf1-150">You may encounter timing issues when using an embedded Windows Media Player control in your HTMLView webpage.</span></span> <span data-ttu-id="1dcf1-151">Dans HTMLView, un contrôle de lecteur incorporé partage son moteur de lecture avec le lecteur Windows Media autonome.</span><span class="sxs-lookup"><span data-stu-id="1dcf1-151">In HTMLView, an embedded Player control shares its playback engine with the stand-alone Windows Media Player.</span></span> <span data-ttu-id="1dcf1-152">Il est possible que le joueur autonome puisse ouvrir et commencer la lecture de la première entrée de la sélection avant que la page Web (et, par conséquent, le contrôle du lecteur) termine le chargement.</span><span class="sxs-lookup"><span data-stu-id="1dcf1-152">It is possible that the stand-alone Player may open and begin playing the first playlist entry before the webpage (and, therefore, the Player control) finishes loading.</span></span> <span data-ttu-id="1dcf1-153">Cela signifie que si vous gérez les événements **OpenStateChange** ou **PlayStateChange** , le code de script ne recevra pas de notifications d’événements pour ces événements tant que le contrôle du lecteur et ses objets associés ne seront pas chargés.</span><span class="sxs-lookup"><span data-stu-id="1dcf1-153">This means that if you handle the **OpenStateChange** or **PlayStateChange** events, the script code will not receive event notifications for these events until the Player control and its associated objects are loaded.</span></span>

<span data-ttu-id="1dcf1-154">Vous pouvez prendre des mesures dans votre code pour retarder la lecture jusqu’à ce que le contrôle du lecteur Windows Media soit instancié.</span><span class="sxs-lookup"><span data-stu-id="1dcf1-154">You can take steps in your code to delay playback until the Windows Media Player control is instantiated.</span></span> <span data-ttu-id="1dcf1-155">Pour ce faire, vous pouvez faire en sorte que la première entrée de votre sélection de métafichier pointe vers un fichier image et définir la durée du fichier sur une durée qui autorise le chargement du contrôle du lecteur.</span><span class="sxs-lookup"><span data-stu-id="1dcf1-155">One way to do this is to make the first entry in your metafile playlist point to an image file and set the duration of the file to a length of time that allows the Player control to load.</span></span> <span data-ttu-id="1dcf1-156">L’exemple de code suivant illustre cette option :</span><span class="sxs-lookup"><span data-stu-id="1dcf1-156">The following example code demonstrates this option:</span></span>


```XML
<ASX version="3.0">
   <PARAM name="HTMLView" value="https://www.proseware.com/htmlview1.htm"/>

<ENTRY>
   <REF href="https://www.proseware.com/blank.jpg"/>
   <DURATION  VALUE = "1:00"/>
</ENTRY>

<ENTRY>
   <REF href="rtsp://www.proseware.com/content1.wma"/>
</ENTRY>

</ASX>

```



<span data-ttu-id="1dcf1-157">Lorsque la sélection précédente s’ouvre, le lecteur Windows Media attend la première entrée de la sélection pendant une minute maximum pendant que le lecteur charge la page Web HTMLView.</span><span class="sxs-lookup"><span data-stu-id="1dcf1-157">When the preceding playlist opens, Windows Media Player waits at the first entry in the playlist for up to one minute while the Player loads the HTMLView webpage.</span></span>

<span data-ttu-id="1dcf1-158">Ensuite, dans votre page Web HTMLView, écrivez le code de script pour gérer l’événement **OnLoad** de l’élément **Body** .</span><span class="sxs-lookup"><span data-stu-id="1dcf1-158">Next, in your HTMLView webpage, write script code to handle the **onload** event for the **BODY** element.</span></span> <span data-ttu-id="1dcf1-159">Dans la fonction de gestionnaire d’événements, appelez la méthode Player **Controls. Next** pour commencer la lecture de la deuxième entrée de la playlist.</span><span class="sxs-lookup"><span data-stu-id="1dcf1-159">In the event handler function, call the Player **Controls.Next** method to begin playback of the second entry in the playlist.</span></span>


```XML
<HTML>
<!-- Define the event handler function. -->
<BODY  onload = "OnLoad();">

<OBJECT id = "Player" 
    CLASSID = "CLSID:6BF52A52-394A-11d3-B153-00C04F79FAA6"> 
        <PARAM Name = "autoStart"  Value = "true">
        <PARAM Name = "uiMode" Value = "none">

</OBJECT>

<!-- Handle the BODY onload event. -->
<SCRIPT>
function OnLoad()
{
   // Advance to the second entry in the playlist.
   Player.controls.next();
}
</SCRIPT>

</BODY>
</HTML>

```



<span data-ttu-id="1dcf1-160">À la fin du chargement de la page Web de l’exemple précédent, le lecteur Windows Media passe immédiatement à la deuxième entrée de la sélection.</span><span class="sxs-lookup"><span data-stu-id="1dcf1-160">When the webpage in the preceding example finishes loading, Windows Media Player immediately advances to the second entry in the playlist.</span></span> <span data-ttu-id="1dcf1-161">Cette valeur remplace la durée spécifiée pour le premier élément de la sélection, ce qui signifie que l’utilisateur n’a pas besoin d’attendre la totalité d’une minute avant de voir le contenu souhaité. il doit attendre la fin du chargement de la page Web.</span><span class="sxs-lookup"><span data-stu-id="1dcf1-161">This overrides the duration specified for the first element in the playlist, meaning that the user doesn't have to wait the full one minute before seeing the desired content; he or she only has to wait for the webpage to finish loading.</span></span> <span data-ttu-id="1dcf1-162">Étant donné que le contrôle Player est entièrement instancié à ce stade, les événements **OpenStateChange** et **PlayStateChange** peuvent être gérés de la manière habituelle.</span><span class="sxs-lookup"><span data-stu-id="1dcf1-162">Because the Player control is completely instantiated at this point, the **OpenStateChange** and **PlayStateChange** events can be handled in the usual manner.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1dcf1-163">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1dcf1-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1dcf1-164">**Affichage des pages Web dans le lecteur Windows Media**</span><span class="sxs-lookup"><span data-stu-id="1dcf1-164">**Displaying Web Pages in Windows Media Player**</span></span>](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[<span data-ttu-id="1dcf1-165">**Événement Player. PlayStateChange**</span><span class="sxs-lookup"><span data-stu-id="1dcf1-165">**Player.PlayStateChange Event**</span></span>](player-player-playstatechange.md)
</dt> <dt>

[<span data-ttu-id="1dcf1-166">**Événement Player. OpenStateChange**</span><span class="sxs-lookup"><span data-stu-id="1dcf1-166">**Player.OpenStateChange Event**</span></span>](player-player-openstatechange.md)
</dt> </dl>

 

 




