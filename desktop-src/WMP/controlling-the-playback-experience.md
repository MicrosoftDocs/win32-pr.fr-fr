---
title: Contrôle de l’expérience de lecture
description: Contrôle de l’expérience de lecture
ms.assetid: f130eee1-10ef-4cbe-b6ac-8ad24e1f0f34
keywords:
- Sélections de métafichiers Windows Media, contrôle de la lecture
- sélections, contrôle de la lecture
- sélections de métafichiers, contrôle de la lecture
- Sélections de métafichiers Windows Media, problèmes de lecture
- sélections, problèmes de lecture
- sélections de métafichiers, problèmes de lecture
- contrôle de la lecture
- Lecteur Windows Media, contrôle de la lecture
- Lecteur Windows Media, problèmes de lecture
- HTMLView, problèmes de lecture
- HTMLView, contrôle de la lecture
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6877b869be8ca38ef9266aedf9318103d0e547ca
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106517963"
---
# <a name="controlling-the-playback-experience"></a><span data-ttu-id="73f54-114">Contrôle de l’expérience de lecture</span><span class="sxs-lookup"><span data-stu-id="73f54-114">Controlling the Playback Experience</span></span>

<span data-ttu-id="73f54-115">Cette section décrit certains des problèmes de lecture que vous pouvez rencontrer lors de l’utilisation de la fonctionnalité HTMLView.</span><span class="sxs-lookup"><span data-stu-id="73f54-115">This section discusses some of the playback issues you may encounter when using the HTMLView feature.</span></span>

## <a name="requiring-the-user-to-view-web-based-content"></a><span data-ttu-id="73f54-116">Demander à l’utilisateur d’afficher le contenu Web</span><span class="sxs-lookup"><span data-stu-id="73f54-116">Requiring the user to view Web-based content</span></span>

<span data-ttu-id="73f54-117">Vous pouvez décider que vous souhaitez que les utilisateurs puissent bénéficier de votre contenu multimédia numérique lorsque le contenu Web HTMLView est également affiché.</span><span class="sxs-lookup"><span data-stu-id="73f54-117">You may decide that you only want users to be able to enjoy your digital media content when the HTMLView Web-based content is also displayed.</span></span> <span data-ttu-id="73f54-118">Vous pouvez inclure le code de script dans votre page Web HTMLView qui arrête la lecture du contenu multimédia numérique si l’utilisateur quitte la fonctionnalité de **lecture** en cours.</span><span class="sxs-lookup"><span data-stu-id="73f54-118">You can include script code in your HTMLView webpage that stops playback of the digital media content if the user switches away from the **Now Playing** feature.</span></span> <span data-ttu-id="73f54-119">Pour ce faire, vous pouvez spécifier un gestionnaire d’événements pour l’événement **Unload** dans le cadre de l’élément **Body** , comme le montre le code HTML suivant :</span><span class="sxs-lookup"><span data-stu-id="73f54-119">To do this, you can specify an event handler for the **unload** event as part of the **BODY** element, as the following HTML code demonstrates:</span></span>


```XML
<BODY onunload = "UnloadMe();">

```



<span data-ttu-id="73f54-120">Vous pouvez ensuite inclure le code de script dans votre fonction de gestionnaire d’événements pour fermer le fichier dans le lecteur.</span><span class="sxs-lookup"><span data-stu-id="73f54-120">Then you can include script code in your event handler function to close the file in the Player.</span></span> <span data-ttu-id="73f54-121">L’exemple de code suivant effectue cette opérations :</span><span class="sxs-lookup"><span data-stu-id="73f54-121">The following example code does this:</span></span>


```XML
function UnloadMe()
{
   Player.close();
}

```



<span data-ttu-id="73f54-122">Quand l’utilisateur quitte la **lecture** en cliquant sur un bouton pour ouvrir une autre fonctionnalité du lecteur Windows Media, telle que la bibliothèque, le lecteur ferme le navigateur incorporé.</span><span class="sxs-lookup"><span data-stu-id="73f54-122">When the user switches away from **Now Playing** by clicking a button to open another Windows Media Player feature, such as the library, the Player closes the embedded browser.</span></span> <span data-ttu-id="73f54-123">L’événement **onunload** se produit alors, en exécutant le script dans la fonction nommée **UnloadMe**.</span><span class="sxs-lookup"><span data-stu-id="73f54-123">This causes the **onunload** event to occur, running the script in the function named **UnloadMe**.</span></span> <span data-ttu-id="73f54-124">La méthode [Player. Close](player-close.md) arrête la lecture et décharge le fichier multimédia numérique en cours.</span><span class="sxs-lookup"><span data-stu-id="73f54-124">The [Player.close](player-close.md) method stops playback and unloads the current digital media file.</span></span> <span data-ttu-id="73f54-125">Pour réafficher le contenu, l’utilisateur doit rouvrir le fichier. asx d’origine.</span><span class="sxs-lookup"><span data-stu-id="73f54-125">To view the content again, the user must reopen the original .asx file.</span></span> <span data-ttu-id="73f54-126">Cette technique arrête également la lecture lorsque l’utilisateur quitte la page Web HTMLView.</span><span class="sxs-lookup"><span data-stu-id="73f54-126">This technique also stops playback when the user navigates away from the HTMLView webpage.</span></span> <span data-ttu-id="73f54-127">Notez que cette technique ne peut pas empêcher l’utilisateur d’afficher le contenu multimédia numérique lorsqu’il bascule en mode apparence.</span><span class="sxs-lookup"><span data-stu-id="73f54-127">Note that this technique cannot prevent the user from viewing the digital media content when he or she switches to skin mode.</span></span>

<span data-ttu-id="73f54-128">Vous vous souvenez que le paramètre HTMLView peut être appliqué à chaque élément **entry** dans un fichier. asx.</span><span class="sxs-lookup"><span data-stu-id="73f54-128">You will recall that the HTMLView parameter can be applied to each **ENTRY** element in an .asx file.</span></span> <span data-ttu-id="73f54-129">Vous pouvez tirer parti de cette fonctionnalité pour vous assurer que votre contenu HTMLView s’affiche chaque fois qu’un nouveau fichier multimédia numérique démarre.</span><span class="sxs-lookup"><span data-stu-id="73f54-129">You can take advantage of this feature to ensure that your HTMLView content is displayed each time a new digital media file starts.</span></span> <span data-ttu-id="73f54-130">Pour ce faire, associez un élément **param** pour HTMLView à chaque entrée de votre sélection. asx.</span><span class="sxs-lookup"><span data-stu-id="73f54-130">To do this, associate a **PARAM** element for HTMLView with each entry in your .asx playlist.</span></span> <span data-ttu-id="73f54-131">Quand chaque entrée est lue, le lecteur revient en mode complet et affiche le contenu HTMLView que vous avez spécifié dans la sélection.</span><span class="sxs-lookup"><span data-stu-id="73f54-131">When each entry plays, the Player returns to full mode and displays the HTMLView content you specified in the playlist.</span></span>

## <a name="url-and-file-script-command-types-are-disabled-by-default"></a><span data-ttu-id="73f54-132">Les types de commandes de script d’URL et de fichier sont désactivés par défaut</span><span class="sxs-lookup"><span data-stu-id="73f54-132">URL and FILE script command types are disabled by default</span></span>

<span data-ttu-id="73f54-133">Le lecteur Windows Media série 9 ou version ultérieure fournit des paramètres qui permettent à l’utilisateur de spécifier si les commandes de script de type URL et fichier peuvent s’exécuter.</span><span class="sxs-lookup"><span data-stu-id="73f54-133">Windows Media Player 9 Series or later provides settings that enable the user to specify whether URL and FILE type script commands are able to run.</span></span> <span data-ttu-id="73f54-134">Par défaut, ces deux types de commandes de script ne s’exécutent pas.</span><span class="sxs-lookup"><span data-stu-id="73f54-134">By default, both of these script command types do not run.</span></span> <span data-ttu-id="73f54-135">Si vous utilisez des types de commande de script personnalisés, ils continuent à s’exécuter, quel que soit le paramètre de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="73f54-135">If you use custom script command types, they will continue to run, regardless of the user setting.</span></span> <span data-ttu-id="73f54-136">Si vous devez utiliser des commandes de script de type URL et fichier, vous devez inviter l’utilisateur à modifier les paramètres.</span><span class="sxs-lookup"><span data-stu-id="73f54-136">If you must use URL and FILE type script commands, you must prompt the user to change the settings.</span></span> <span data-ttu-id="73f54-137">Pour modifier les paramètres, cliquez sur **Outils**, puis sur **options** et sur **sécurité**.</span><span class="sxs-lookup"><span data-stu-id="73f54-137">To change the settings, click **Tools**, then **Options**, and then **Security**.</span></span>

## <a name="reopening-an-htmlview-does-not-reload-the-webpage"></a><span data-ttu-id="73f54-138">La réouverture d’un HTMLView ne recharge pas la page Web</span><span class="sxs-lookup"><span data-stu-id="73f54-138">Reopening an HTMLView does not reload the webpage</span></span>

<span data-ttu-id="73f54-139">Lorsque l’utilisateur ouvre un fichier. asx qui comprend un paramètre HTMLView et réouvre ensuite le même fichier, le lecteur Windows Media n’actualise pas la page Web HTMLView.</span><span class="sxs-lookup"><span data-stu-id="73f54-139">When the user opens an .asx file that includes an HTMLView parameter and subsequently reopens the same file, Windows Media Player does not refresh the HTMLView webpage.</span></span> <span data-ttu-id="73f54-140">Cela signifie également que si vous avez autorisé les utilisateurs à quitter votre page Web HTMLView, le lecteur ne retourne pas le navigateur incorporé à la page Web initiale HTMLView.</span><span class="sxs-lookup"><span data-stu-id="73f54-140">This also means that if you have allowed users to navigate away from your HTMLView webpage, the Player does not return the embedded browser to the initial HTMLView webpage.</span></span>

## <a name="hiding-the-content-location"></a><span data-ttu-id="73f54-141">Masquage de l’emplacement du contenu</span><span class="sxs-lookup"><span data-stu-id="73f54-141">Hiding the content location</span></span>

<span data-ttu-id="73f54-142">Vous pouvez décider de ne pas que le lecteur Windows Media affiche l’emplacement de votre contenu multimédia numérique lors de la lecture d’un fichier. asx.</span><span class="sxs-lookup"><span data-stu-id="73f54-142">You might decide that you don't want Windows Media Player to display the location of your digital media content while it is playing an .asx file.</span></span> <span data-ttu-id="73f54-143">En règle générale, le lecteur Windows Media affiche uniquement des informations sur la liste de lecture elle-même lors de la diffusion en continu du contenu à partir d’Internet.</span><span class="sxs-lookup"><span data-stu-id="73f54-143">Usually, Windows Media Player only shows information about the playlist itself when streaming content from the Internet.</span></span> <span data-ttu-id="73f54-144">Toutefois, il existe des étapes supplémentaires que vous pouvez prendre pour empêcher les utilisateurs de déterminer l’emplacement de votre contenu.</span><span class="sxs-lookup"><span data-stu-id="73f54-144">However, there are further steps you can take to prevent users from determining the location of your content.</span></span> <span data-ttu-id="73f54-145">Par exemple, l’une des méthodes permettant de s’assurer que le lecteur n’affiche pas le chemin d’accès à votre contenu consiste à diffuser votre contenu à l’aide des sélections côté serveur de Windows Media Services.</span><span class="sxs-lookup"><span data-stu-id="73f54-145">For example, one way to ensure that the Player does not display the path to your content is to stream your content using Windows Media Services server-side playlists.</span></span> <span data-ttu-id="73f54-146">Ainsi, lorsque l’utilisateur consulte les propriétés du contenu, il voit l’URL du serveur et non l’URL de votre contenu.</span><span class="sxs-lookup"><span data-stu-id="73f54-146">That way, when the user views the properties for the content, he or she sees the URL of the server and not the URL of your content.</span></span>

## <a name="related-topics"></a><span data-ttu-id="73f54-147">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="73f54-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="73f54-148">**Affichage des pages Web dans le lecteur Windows Media**</span><span class="sxs-lookup"><span data-stu-id="73f54-148">**Displaying Web Pages in Windows Media Player**</span></span>](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[<span data-ttu-id="73f54-149">**Élément PARAM**</span><span class="sxs-lookup"><span data-stu-id="73f54-149">**PARAM Element**</span></span>](param-element.md)
</dt> </dl>

 

 




