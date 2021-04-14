---
title: Navigation entre les volets des tâches de service
description: Navigation entre les volets des tâches de service
ms.assetid: cb26a26d-a80d-4af5-9c5f-fab01129d83c
keywords:
- Windows Media Player Online stores, navigation
- magasins en ligne, navigation
- tapez 2 magasins en ligne, navigation
- Magasins en ligne du lecteur Windows Media, volets des tâches du service
- magasins en ligne, volets des tâches de service
- types 2 magasins en ligne, volets de tâches de service
- Windows Media Player Online stores, volets des tâches
- magasins en ligne, volets des tâches
- tapez 2 magasins en ligne, volets des tâches
- navigation dans les magasins de type 2 en ligne
- Windows Media Player, service, volets Office
- Windows Media Player, volets des tâches
- volets de tâches du service
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86035215f822c67bb40c528f141422977efc8653
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310030"
---
# <a name="navigating-between-service-task-panes"></a><span data-ttu-id="6bc27-116">Navigation entre les volets des tâches de service</span><span class="sxs-lookup"><span data-stu-id="6bc27-116">Navigating between Service Task Panes</span></span>

<span data-ttu-id="6bc27-117">Pour naviguer entre les volets des tâches de service dans le lecteur Windows Media, utilisez la méthode **NavigateTaskPaneURL** , qui est disponible à l’aide de l’objet **Window. external** .</span><span class="sxs-lookup"><span data-stu-id="6bc27-117">To navigate between service task panes in Windows Media Player, you use the **NavigateTaskPaneURL** method, which is available by using the **window.external** object.</span></span> <span data-ttu-id="6bc27-118">Lorsque vous utilisez cette méthode, vous spécifiez des valeurs pour trois paramètres :</span><span class="sxs-lookup"><span data-stu-id="6bc27-118">When you use this method, you specify values for three parameters:</span></span>

-   <span data-ttu-id="6bc27-119">*bstrKeyName*.</span><span class="sxs-lookup"><span data-stu-id="6bc27-119">*bstrKeyName*.</span></span> <span data-ttu-id="6bc27-120">Il s’agit du nom de clé du magasin en ligne.</span><span class="sxs-lookup"><span data-stu-id="6bc27-120">This is the key name of the online store.</span></span> <span data-ttu-id="6bc27-121">Lorsque vous naviguez dans un magasin en ligne, utilisez le nom de clé du magasin actuel.</span><span class="sxs-lookup"><span data-stu-id="6bc27-121">When navigating within an online store, use the key name of the current store.</span></span>
-   <span data-ttu-id="6bc27-122">*bstrTaskPane*.</span><span class="sxs-lookup"><span data-stu-id="6bc27-122">*bstrTaskPane*.</span></span> <span data-ttu-id="6bc27-123">Cette chaîne contient le nom du volet de tâches du service auquel vous souhaitez accéder.</span><span class="sxs-lookup"><span data-stu-id="6bc27-123">This string contains the name of the service task pane to which you want to navigate.</span></span>
-   <span data-ttu-id="6bc27-124">*bstrParams*.</span><span class="sxs-lookup"><span data-stu-id="6bc27-124">*bstrParams*.</span></span> <span data-ttu-id="6bc27-125">Cette chaîne contient les paramètres de chaîne de requête que vous souhaitez ajouter à l’URL de la page Web hébergée par le volet de tâches du service auquel vous souhaitez accéder.</span><span class="sxs-lookup"><span data-stu-id="6bc27-125">This string contains the query string parameters you want to append to the URL for the webpage hosted by the service task pane to which you want to navigate.</span></span>

<span data-ttu-id="6bc27-126">La navigation est gérée par une page Web que vous créez, appelée page naviguer.</span><span class="sxs-lookup"><span data-stu-id="6bc27-126">Navigation is managed by a webpage you create, called the navigate page.</span></span> <span data-ttu-id="6bc27-127">L’URL de la page Navigate est spécifiée par l’élément **Navigate** dans le document serviceInfo.</span><span class="sxs-lookup"><span data-stu-id="6bc27-127">The URL for the navigate page is specified by the **Navigate** element in the ServiceInfo document.</span></span> <span data-ttu-id="6bc27-128">Quand vous appelez **NavigateTaskPaneURL**, le lecteur Windows Media ouvre la page naviguer, pas la page Web spécifiée par les éléments **ServiceTask1**, **ServiceTask2** ou **ServiceTask3** .</span><span class="sxs-lookup"><span data-stu-id="6bc27-128">When you call **NavigateTaskPaneURL**, Windows Media Player opens the navigate page, not the webpage specified by the **ServiceTask1**, **ServiceTask2**, or **ServiceTask3** elements.</span></span> <span data-ttu-id="6bc27-129">Il s’agit de la page de navigation qui reçoit la chaîne de requête spécifiée par *bstrParams*.</span><span class="sxs-lookup"><span data-stu-id="6bc27-129">It is the navigate page that receives the query string specified by *bstrParams*.</span></span> <span data-ttu-id="6bc27-130">La page naviguer doit contenir les règles qui déterminent le contenu qui s’affiche dans un volet de tâches de service après la navigation.</span><span class="sxs-lookup"><span data-stu-id="6bc27-130">The navigate page should contain the rules that determine which content displays in a service task pane after navigation.</span></span>

<span data-ttu-id="6bc27-131">Par exemple, supposons que vous souhaitez que les utilisateurs cliquent sur un lien pour naviguer de **ServiceTask1** à **ServiceTask2**.</span><span class="sxs-lookup"><span data-stu-id="6bc27-131">For example, suppose you want users to click a link to navigate from **ServiceTask1** to **ServiceTask2**.</span></span> <span data-ttu-id="6bc27-132">Vous pouvez utiliser le code HTML suivant pour créer le lien :</span><span class="sxs-lookup"><span data-stu-id="6bc27-132">You could use the following HTML to create the link:</span></span>


```C++
<A HREF = "javascript:window.external.NavigateTaskPaneURL('MSSampleMusic', 'ServiceTask2', 'From=Music&To=2')">Video</A>

```



<span data-ttu-id="6bc27-133">Quand l’utilisateur clique sur le lien vidéo, le lecteur Windows Media bascule vers **ServiceTask2** et ouvre la page naviguer, en ajoutant la chaîne de requête suivante à son URL.</span><span class="sxs-lookup"><span data-stu-id="6bc27-133">When the user clicks the Video link, Windows Media Player switches to **ServiceTask2** and opens the navigate page, appending the following query string to its URL.</span></span>


```C++
?From=Music&To=2

```



<span data-ttu-id="6bc27-134">Le paramètre from identifie la page à partir de laquelle l’utilisateur a cliqué sur le lien et le paramètre to identifie le numéro du volet de tâches du service auquel il souhaite naviguer.</span><span class="sxs-lookup"><span data-stu-id="6bc27-134">The From parameter identifies the page from which the user clicked the link and the To parameter identifies the number of the service task pane to which he or she wants to navigate.</span></span> <span data-ttu-id="6bc27-135">(Notez qu’il n’y a rien de spécial concernant ces paramètres.</span><span class="sxs-lookup"><span data-stu-id="6bc27-135">(Note that there is nothing special about these parameters.</span></span> <span data-ttu-id="6bc27-136">Vous pouvez utiliser tous les paramètres que vous souhaitez pour les besoins de votre choix.)</span><span class="sxs-lookup"><span data-stu-id="6bc27-136">You can use any parameters you like for any purpose you choose.)</span></span>

<span data-ttu-id="6bc27-137">Par exemple, l’exemple de code suivant montre l’élément **Navigate** dans un document serviceInfo :</span><span class="sxs-lookup"><span data-stu-id="6bc27-137">For instance, the following example code shows the **Navigate** element in a ServiceInfo document:</span></span>


```C++
<Navigate
        BaseURL = "https://www.proseware.com/service/html/navigate.asp">
```



<span data-ttu-id="6bc27-138">L’URL qui en résulte, avec la chaîne de requête, est présentée dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="6bc27-138">The resulting URL, complete with query string, is shown in the following example:</span></span>


```C++
https://www.proseware.com/service/html/navigate.asp?From=Music&To=2

```



<span data-ttu-id="6bc27-139">L’exemple de code suivant affiche la page naviguer :</span><span class="sxs-lookup"><span data-stu-id="6bc27-139">The following example code shows the navigate page:</span></span>


```C++
<%
    Dim sURL
    Dim sQS
    Dim sTo

    sURL = ""
    sQS = Request.ServerVariables("QUERY_STRING")
    sTo = "" & Request.QueryString("To")
 
    Select Case sTo
       Case "1" sURL = sURL & "Music_Music.asp"
       Case "2" sURL = sURL & "Music_Video.asp"
       Case "3" sURL = sURL & "Music_Radio.asp"
       Case Else sURL = sURL & "Music_Music.asp"
    End Select
     
    sURL = sURL & "?" & sQS

    Response.Redirect(sURL)    
%>

```



<span data-ttu-id="6bc27-140">Le code précédent crée simplement une URL et y redirige le navigateur.</span><span class="sxs-lookup"><span data-stu-id="6bc27-140">The preceding code simply creates a URL and redirects the browser to it.</span></span> <span data-ttu-id="6bc27-141">Tout d’abord, le code récupère les valeurs à partir de la chaîne de requête d’URL et de la chaîne de requête elle-même.</span><span class="sxs-lookup"><span data-stu-id="6bc27-141">First, the code retrieves To values from the URL query string and the query string itself.</span></span> <span data-ttu-id="6bc27-142">Elle utilise la valeur du paramètre to pour déterminer la page à afficher.</span><span class="sxs-lookup"><span data-stu-id="6bc27-142">It uses the value of the To parameter to determine which page to display.</span></span> <span data-ttu-id="6bc27-143">Il ajoute ensuite la chaîne de requête d’origine à l’URL.</span><span class="sxs-lookup"><span data-stu-id="6bc27-143">It then appends the original query string to the URL.</span></span> <span data-ttu-id="6bc27-144">Enfin, il parcourt le navigateur à l’aide d’une URL semblable à la suivante :</span><span class="sxs-lookup"><span data-stu-id="6bc27-144">Finally, it navigates the browser using a URL similar to the following:</span></span>


```C++
https://www.proseware.com/service/html/Video.asp?locale=409&geoid=f4&version=10.0.0.3600&userlocale=409&From=Music&To=2

```



<span data-ttu-id="6bc27-145">Chaque fois que vous effectuez la navigation de cette manière, veillez à spécifier [External. SelectedTaskPane](external-selectedtaskpane.md) pour vous assurer que le bouton de tâche correct est mis en surbrillance.</span><span class="sxs-lookup"><span data-stu-id="6bc27-145">Whenever you perform navigation in this manner, be sure to specify [External.SelectedTaskPane](external-selectedtaskpane.md) to ensure that the correct task button is highlighted.</span></span>

-   <span data-ttu-id="6bc27-146">**Avertissement** Veillez à utiliser les paramètres de chaîne de requête pour la navigation.</span><span class="sxs-lookup"><span data-stu-id="6bc27-146">**Warning** Be careful how you use query string parameters for navigation.</span></span>

<span data-ttu-id="6bc27-147">Les pages Web HTMLView peuvent être fournies par toute personne qui crée une sélection ASX.</span><span class="sxs-lookup"><span data-stu-id="6bc27-147">HTMLView webpages can be provided by anyone who creates an ASX playlist.</span></span> <span data-ttu-id="6bc27-148">Cela signifie que les sites Web malveillants peuvent transmettre des valeurs de chaîne de requête à votre magasin en ligne à l’aide de **NavigateTaskPaneURL**.</span><span class="sxs-lookup"><span data-stu-id="6bc27-148">This means that malicious websites can pass query string values to your online store using **NavigateTaskPaneURL**.</span></span> <span data-ttu-id="6bc27-149">Vous devez prévoir cette possibilité pour garantir la sécurité de votre magasin en ligne.</span><span class="sxs-lookup"><span data-stu-id="6bc27-149">You must plan for this possibility to keep your online store secure.</span></span> <span data-ttu-id="6bc27-150">Par exemple, si votre magasin en ligne affiche simplement une valeur de chaîne de requête à l’utilisateur, un site Web malveillant peut afficher du texte inattendu.</span><span class="sxs-lookup"><span data-stu-id="6bc27-150">For example, if your online store simply displays a query string value to the user, a malicious website could display unexpected text.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6bc27-151">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6bc27-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6bc27-152">**Affichage des pages Web dans le lecteur Windows Media**</span><span class="sxs-lookup"><span data-stu-id="6bc27-152">**Displaying Web Pages in Windows Media Player**</span></span>](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[<span data-ttu-id="6bc27-153">**Élément Navigate**</span><span class="sxs-lookup"><span data-stu-id="6bc27-153">**Navigate Element**</span></span>](navigate-element.md)
</dt> <dt>

[<span data-ttu-id="6bc27-154">**Navigation pour les magasins de type 2 en ligne**</span><span class="sxs-lookup"><span data-stu-id="6bc27-154">**Navigation for Type 2 Online Stores**</span></span>](navigation-for-type-2-online-stores.md)
</dt> </dl>

 

 




