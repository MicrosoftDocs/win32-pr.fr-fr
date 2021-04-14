---
title: Gestion des informations de session
description: Gestion des informations de session
ms.assetid: 2ab862dc-62e1-44d6-ac81-7d3c574a779f
keywords:
- Windows Media Player Online stores, gestionnaire de téléchargement
- magasins en ligne, gestionnaire de téléchargement
- tapez 2 magasins en ligne, gestionnaire de téléchargement
- Magasins en ligne du lecteur Windows Media, gestion des informations de session
- magasins en ligne, gestion des informations de session
- type 2 magasins en ligne, gestion des informations de session
- Windows Media Player Online stores, informations de session
- magasins en ligne, informations de session
- type 2 magasins en ligne, informations de session
- Lecteur Windows Media, gestionnaire de téléchargement
- Gestionnaire de téléchargement du lecteur Windows Media
- Gestionnaire de téléchargement
- gestion des informations de session
- informations de session
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 786892afebb26f64a97b300bd1a4bd7c46d44883
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311539"
---
# <a name="maintaining-session-information"></a><span data-ttu-id="9cce7-117">Gestion des informations de session</span><span class="sxs-lookup"><span data-stu-id="9cce7-117">Maintaining Session Information</span></span>

## <a name="how-the-sample-stores-information"></a><span data-ttu-id="9cce7-118">Comment l’exemple stocke les informations</span><span class="sxs-lookup"><span data-stu-id="9cce7-118">How the Sample Stores Information</span></span>

<span data-ttu-id="9cce7-119">L’exemple de page Web gère les données à l’aide de cookies.</span><span class="sxs-lookup"><span data-stu-id="9cce7-119">The sample webpage maintains data by using cookies.</span></span> <span data-ttu-id="9cce7-120">Les cookies sont simplement des paires nom/valeur permanentes que le navigateur Web peut stocker pour vous.</span><span class="sxs-lookup"><span data-stu-id="9cce7-120">Cookies are simply persistent name/value pairs that the Web browser can store for you.</span></span>

<span data-ttu-id="9cce7-121">À la fermeture de la page Web, la fonction **Shutdown** s’exécute.</span><span class="sxs-lookup"><span data-stu-id="9cce7-121">When the webpage closes, the **Shutdown** function runs.</span></span> <span data-ttu-id="9cce7-122">**Shutdown** appelle la fonction **SetPendingCookies**.</span><span class="sxs-lookup"><span data-stu-id="9cce7-122">**Shutdown** calls the function **SetPendingCookies**.</span></span> <span data-ttu-id="9cce7-123">Cette fonction effectue une boucle dans la liste de collection de téléchargements, stockée dans la zone de liste déroulante nommée selDLC.</span><span class="sxs-lookup"><span data-stu-id="9cce7-123">This function loops through the download collection list, stored in the drop-down list box named selDLC.</span></span> <span data-ttu-id="9cce7-124">Si une collection de téléchargements contient des éléments incomplets, la fonction appelle la méthode **setcookie**, en passant un nom et une valeur.</span><span class="sxs-lookup"><span data-stu-id="9cce7-124">If a download collection contains incomplete items, the function calls the method **SetCookie**, passing a name and a value.</span></span> <span data-ttu-id="9cce7-125">Pour déterminer la chaîne de nom, vous pouvez ajouter une valeur entière à une valeur constante, **WMPDLC**, qui est stockée dans la variable nommée g \_ sPreCookie.</span><span class="sxs-lookup"><span data-stu-id="9cce7-125">The name string is determined by appending an integer value to a constant value, **WMPDLC**, which is stored in the variable named g\_sPreCookie.</span></span> <span data-ttu-id="9cce7-126">Par exemple, pour la troisième collection de téléchargements en attente, le nom du cookie est « WMPDLC2 », car le mécanisme de comptage est de base zéro.</span><span class="sxs-lookup"><span data-stu-id="9cce7-126">For instance, for the third pending download collection, the cookie name would be "WMPDLC2", because the counting mechanism is zero-based.</span></span> <span data-ttu-id="9cce7-127">À mesure que chaque cookie est créé, la fonction incrémente la variable globale g \_ en attente pour conserver un nombre de téléchargements en attente.</span><span class="sxs-lookup"><span data-stu-id="9cce7-127">As each cookie is created, the function increments the global variable g\_Pending to keep a count of pending downloads.</span></span> <span data-ttu-id="9cce7-128">Le code est reproduit ici à des fins pratiques :</span><span class="sxs-lookup"><span data-stu-id="9cce7-128">The code is reproduced here for your convenience:</span></span>


```C++
// Write cookies for pending downloads.
function SetPendingCookies()
{
    g_Pending = 0; // Init the pending count.
    
    for(var i = 0; i < selDLC.length; i++)
    {
        var sCookieName = g_sPreCookie + i.toString(10);
        var sCookieVal = selDLC.options[i].text;
    
        // Write a cookie for each pending download.    
        if(IsDLCComplete(sCookieVal.valueOf()) == false)
        {      
            SetCookie(sCookieName, sCookieVal);
            g_Pending++;
        }        
    }
}

```



<span data-ttu-id="9cce7-129">**IsDLCComplete** est une fonction d’assistance qui effectue simplement une boucle sur chaque élément de téléchargement de la collection de téléchargements pour déterminer si un élément est en attente.</span><span class="sxs-lookup"><span data-stu-id="9cce7-129">**IsDLCComplete** is a helper function that simply loops through each download item in the download collection to determine whether any item is pending.</span></span> <span data-ttu-id="9cce7-130">S’il existe un élément en attente, la fonction retourne false.</span><span class="sxs-lookup"><span data-stu-id="9cce7-130">If there is a pending item, the function returns false.</span></span>

<span data-ttu-id="9cce7-131">**Setcookie** est la fonction qui crée le cookie.</span><span class="sxs-lookup"><span data-stu-id="9cce7-131">**SetCookie** is the function that creates the cookie.</span></span>

<span data-ttu-id="9cce7-132">Quand **SetPendingCookies** retourne, **Shutdown** crée le cookie Count, qui stocke la valeur de la variable g \_ en attente.</span><span class="sxs-lookup"><span data-stu-id="9cce7-132">When **SetPendingCookies** returns, **Shutdown** creates the count cookie, which stores the value from the variable g\_Pending.</span></span> <span data-ttu-id="9cce7-133">Cette valeur est importante, car la page Web a besoin d’un moyen de déterminer le nombre de cookies à récupérer lors du rechargement.</span><span class="sxs-lookup"><span data-stu-id="9cce7-133">This value is important because the webpage needs a way to determine how many cookies to retrieve when it reloads.</span></span> <span data-ttu-id="9cce7-134">Le nom du cookie de nombre est stocké dans la variable nommée g \_ sCountCookie.</span><span class="sxs-lookup"><span data-stu-id="9cce7-134">The count cookie name is stored in the variable named g\_sCountCookie.</span></span>

## <a name="how-the-sample-retrieves-information"></a><span data-ttu-id="9cce7-135">Comment l’exemple récupère des informations</span><span class="sxs-lookup"><span data-stu-id="9cce7-135">How the Sample Retrieves Information</span></span>

<span data-ttu-id="9cce7-136">Lors du chargement de la page Web, la fonction **init** s’exécute.</span><span class="sxs-lookup"><span data-stu-id="9cce7-136">When the webpage loads, the **Init** function runs.</span></span> <span data-ttu-id="9cce7-137">Tout d’abord, la fonction appelle **GetPendingDlCount** pour récupérer le cookie de nombre.</span><span class="sxs-lookup"><span data-stu-id="9cce7-137">First, the function calls **GetPendingDlCount** to retrieve the count cookie.</span></span> <span data-ttu-id="9cce7-138">Ensuite, il stocke cette valeur dans la variable nommée g \_ en attente.</span><span class="sxs-lookup"><span data-stu-id="9cce7-138">Next, it stores this value in the variable named g\_Pending.</span></span> <span data-ttu-id="9cce7-139">Ensuite, il appelle la fonction **PopulateDLList** pour récupérer chaque cookie de session de téléchargement et ajouter son identificateur à la zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="9cce7-139">Then it calls the **PopulateDLList** function to retrieve each download session cookie and add its identifier to the drop-down list box.</span></span> <span data-ttu-id="9cce7-140">Voici le code de cette fonction :</span><span class="sxs-lookup"><span data-stu-id="9cce7-140">Here is the code for that function:</span></span>


```C++
// Fill the drop-down list with pending download collection IDs.
function PopulateDlList(iCount)
{
    ClearList(selDLC);
     
    // For each cookie, add the value to the SELECT element.
    // The value represents a download collection ID.  
    for (var j = 0; j < iCount; j++)
    {
        var sCookieName = g_sPreCookie + j.toString(10);        
        var sCookieVal = GetCookie(sCookieName);
        DelCookie(sCookieName); // Don't leave the cookies lying around. 
  
        if(sCookieVal != null)
        {      
            var oOption = document.createElement("OPTION");
            oOption.text = sCookieVal;
            oOption.value = j;
            selDLC.add(oOption); 
        }          
    }
}

```



<span data-ttu-id="9cce7-141">La fonction **ClearList** supprime tous les éléments de la zone de liste.</span><span class="sxs-lookup"><span data-stu-id="9cce7-141">The function **ClearList** removes all items from the list box.</span></span>

<span data-ttu-id="9cce7-142">La fonction entre ensuite dans une boucle.</span><span class="sxs-lookup"><span data-stu-id="9cce7-142">The function then enters a loop.</span></span> <span data-ttu-id="9cce7-143">Chaque nom de cookie est généré sous la forme d’une chaîne, puis le cookie est récupéré en appelant la fonction d’assistance **getCookie**.</span><span class="sxs-lookup"><span data-stu-id="9cce7-143">Each cookie name is built as a string, and then the cookie is retrieved by calling the helper function **GetCookie**.</span></span> <span data-ttu-id="9cce7-144">Une fois récupéré, le cookie est supprimé en appelant **DelCookie**.</span><span class="sxs-lookup"><span data-stu-id="9cce7-144">Once retrieved, the cookie is deleted by calling **DelCookie**.</span></span> <span data-ttu-id="9cce7-145">Si le cookie a une valeur, la valeur est ajoutée à la zone de liste.</span><span class="sxs-lookup"><span data-stu-id="9cce7-145">If the cookie has a value, the value is added to the list box.</span></span> <span data-ttu-id="9cce7-146">Cette action déclenche l’événement **OnChange** pour la liste selDLC, qui à son tour appelle la fonction de gestionnaire nommée **OnSelectDLC**.</span><span class="sxs-lookup"><span data-stu-id="9cce7-146">This action initiates the **onChange** event for the selDLC list, which in turn calls the handler function named **OnSelectDLC**.</span></span> <span data-ttu-id="9cce7-147">Il s’agit de la même fonction que celle qui s’exécute lorsque l’utilisateur sélectionne une collection de téléchargements ; Il s’agit du code qui remplit la zone de liste télécharger l’élément.</span><span class="sxs-lookup"><span data-stu-id="9cce7-147">This is the same function that executes when the user selects a download collection; it is the code that fills the download item list box.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9cce7-148">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9cce7-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9cce7-149">**Utilisation du gestionnaire de téléchargement**</span><span class="sxs-lookup"><span data-stu-id="9cce7-149">**Using the Download Manager**</span></span>](using-the-download-manager.md)
</dt> </dl>

 

 




