---
title: Gestion de la connexion
description: Gestion de la connexion
ms.assetid: 5cafcd3a-e819-4524-b7a9-580ff36fc4f8
keywords:
- Windows Media Player Online stores, gestion des connexions
- magasins en ligne, gestion des connexions
- tapez 1 magasins en ligne, gestion des connexions
- Windows Media Player Online stores, connexions
- magasins en ligne, connexions
- tapez 1 magasins en ligne, connexions
- Windows Media Player Online stores, processus de connexion standard
- magasins en ligne, processus de connexion standard
- types 1 magasins en ligne, processus de connexion standard
- Magasins en ligne du lecteur Windows Media, processus de déconnexion
- magasins en ligne, processus de déconnexion
- type 1 magasins en ligne, processus de déconnexion
- processus de connexion standard
- processus de déconnexion
- connexions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 633042692ab9193f46ab83415df13237d3a279e8
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104381521"
---
# <a name="managing-login"></a><span data-ttu-id="1c123-118">Gestion de la connexion</span><span class="sxs-lookup"><span data-stu-id="1c123-118">Managing Login</span></span>

<span data-ttu-id="1c123-119">Le lecteur Windows Media prend en charge différentes méthodes permettant à l’utilisateur de se connecter à un magasin de type 1 en ligne.</span><span class="sxs-lookup"><span data-stu-id="1c123-119">Windows Media Player supports a variety of methods for the user to log in to a type 1 online store.</span></span> <span data-ttu-id="1c123-120">Le lecteur fournit une boîte de dialogue de connexion standard, mais le magasin en ligne peut fournir une page Web qui constitue une alternative à la boîte de dialogue standard.</span><span class="sxs-lookup"><span data-stu-id="1c123-120">The Player provides a standard log-in dialog box, but the online store can provide a webpage that serves as an alternative to the standard dialog box.</span></span>

<span data-ttu-id="1c123-121">L’utilisateur peut lancer une tentative de connexion en interagissant avec l’interface utilisateur du lecteur Windows Media ou en interagissant avec une page de découverte fournie par le magasin en ligne.</span><span class="sxs-lookup"><span data-stu-id="1c123-121">The user can initiate a log-in attempt by interacting with the Windows Media Player user interface or by interacting with a discovery page provided by the online store.</span></span> <span data-ttu-id="1c123-122">Si l’utilisateur initie une tentative de connexion en interagissant avec une page de découverte, le script sur la page de découverte appelle la méthode [External. attemptLogin](external-attemptlogin.md) .</span><span class="sxs-lookup"><span data-stu-id="1c123-122">If the user initiates a log-in attempt by interacting with a discovery page, script on the discovery page calls the [External.attemptLogin](external-attemptlogin.md) method.</span></span>

<span data-ttu-id="1c123-123">L’état de connexion de l’utilisateur est géré par le magasin en ligne.</span><span class="sxs-lookup"><span data-stu-id="1c123-123">The user's log-in state is maintained by the online store.</span></span> <span data-ttu-id="1c123-124">Lorsque l’état de connexion de l’utilisateur change, ou si une tentative de connexion échoue, le plug-in du magasin en ligne avertit le lecteur Windows Media en appelant [IWMPContentPartnerCallback :: Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-notify), en passant wmpcnLoginStateChange dans le paramètre de *type* .</span><span class="sxs-lookup"><span data-stu-id="1c123-124">When the user's log-in state changes, or if a log-in attempt fails, the online store's plug-in notifies Windows Media Player by calling [IWMPContentPartnerCallback::Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-notify), passing wmpcnLoginStateChange in the *type* parameter.</span></span> <span data-ttu-id="1c123-125">Le joueur transmet la notification en même temps que la page de découverte en déclenchant l’événement [External. OnLoginChange](external-onloginchange-event.md) .</span><span class="sxs-lookup"><span data-stu-id="1c123-125">The Player passes the notification along to the discovery page by raising the [External.OnLoginChange](external-onloginchange-event.md) event.</span></span>

<span data-ttu-id="1c123-126">Un appel à **OnLoginChange** ne signifie pas nécessairement que l’état de connexion de l’utilisateur a changé ; Cela peut signifier qu’une tentative de connexion a échoué.</span><span class="sxs-lookup"><span data-stu-id="1c123-126">A call to **OnLoginChange** does not necessarily mean that the user's log-in state changed; it could mean that an attempt to log in failed.</span></span> <span data-ttu-id="1c123-127">Pour déterminer l’état de connexion de l’utilisateur, le gestionnaire d’événements **OnLoginChange** peut inspecter la propriété [External. userLoggedIn](external-userloggedin.md) .</span><span class="sxs-lookup"><span data-stu-id="1c123-127">To determine the user's log-in state, the **OnLoginChange** event handler can inspect the [External.userLoggedIn](external-userloggedin.md) property.</span></span>

<span data-ttu-id="1c123-128">Les sections suivantes décrivent le processus de connexion standard, le processus de connexion alternatif et le processus de déconnexion.</span><span class="sxs-lookup"><span data-stu-id="1c123-128">The following sections describe the standard log-in process, the alternative log-in process, and the log-out process.</span></span>

## <a name="standard-log-in"></a><span data-ttu-id="1c123-129">Connexion standard</span><span class="sxs-lookup"><span data-stu-id="1c123-129">Standard Log-in</span></span>

<span data-ttu-id="1c123-130">Le processus de connexion standard implique les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="1c123-130">The standard log-in process involves the following steps:</span></span>

1.  <span data-ttu-id="1c123-131">L’utilisateur initie une tentative de connexion en interagissant avec l’interface utilisateur du lecteur Windows Media ou en interagissant avec une page de découverte.</span><span class="sxs-lookup"><span data-stu-id="1c123-131">The user initiates a log-in attempt by interacting with the Windows Media Player user interface or by interacting with a discovery page.</span></span>
2.  <span data-ttu-id="1c123-132">Le lecteur Windows Media affiche une boîte de dialogue qui invite l’utilisateur à entrer un nom d’utilisateur et un mot de passe.</span><span class="sxs-lookup"><span data-stu-id="1c123-132">Windows Media Player displays a dialog box that prompts the user for a user-name and password.</span></span>
3.  <span data-ttu-id="1c123-133">Quand l’utilisateur clique sur le bouton **se connecter** dans la boîte de dialogue, le lecteur Windows Media appelle [IWMPContentPartner :: login](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-login), qui est implémenté par le plug-in du magasin en ligne.</span><span class="sxs-lookup"><span data-stu-id="1c123-133">When the user clicks the **Sign In** button in the dialog box, Windows Media Player calls [IWMPContentPartner::Login](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-login), which is implemented by the online store's plug-in.</span></span>
4.  <span data-ttu-id="1c123-134">Le plug-in communique avec le magasin en ligne et réussit ou ne parvient pas à se connecter à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1c123-134">The plug-in communicates with the online store and either succeeds or fails to log in the user.</span></span>
5.  <span data-ttu-id="1c123-135">Si la tentative de connexion réussit, le plug-in avertit le lecteur Windows Media en appelant **IWMPContentPartnerCallback :: Notify**, en passant \_ la valeur variant true dans le membre **boolVal** du paramètre *pContext* .</span><span class="sxs-lookup"><span data-stu-id="1c123-135">If the log-in attempt succeeds, the plug-in notifies Windows Media Player by calling **IWMPContentPartnerCallback::Notify**, passing VARIANT\_TRUE in the **boolVal** member of the *pContext* parameter.</span></span> <span data-ttu-id="1c123-136">Si la tentative de connexion échoue, le plug-in avertit le lecteur Windows Media en appelant **IWMPContentPartnerCallback :: Notify**, en passant une valeur 32 bits dans le membre **UlVal** du paramètre *pContext* .</span><span class="sxs-lookup"><span data-stu-id="1c123-136">If the log-in attempt fails, the plug-in notifies Windows Media Player by calling **IWMPContentPartnerCallback::Notify**, passing a 32-bit value in the **ulVal** member of the *pContext* parameter.</span></span> <span data-ttu-id="1c123-137">Le lecteur transmet ensuite cette valeur 32 bits à [IWMPContentPartner :: GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo) pour obtenir l’URL d’une page Web qui peut gérer l’échec.</span><span class="sxs-lookup"><span data-stu-id="1c123-137">The Player then passes that 32-bit value to [IWMPContentPartner::GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo) to get the URL of a webpage that can handle the failure.</span></span>

## <a name="alternative-login"></a><span data-ttu-id="1c123-138">Autre connexion</span><span class="sxs-lookup"><span data-stu-id="1c123-138">Alternative Login</span></span>

<span data-ttu-id="1c123-139">Si l’indicateur ALTLOGIN de l’abonnement \_ \_ est défini dans l’entrée de Registre **Capabilities** pour le plug-in du magasin en ligne, le lecteur Windows Media n’utilise pas la boîte de dialogue de connexion standard.</span><span class="sxs-lookup"><span data-stu-id="1c123-139">If the SUBSCRIPTION\_CAP\_ALTLOGIN flag is set in the **Capabilities** registry entry for the online store's plug-in, Windows Media Player does not use the standard log-in dialog box.</span></span> <span data-ttu-id="1c123-140">Au lieu de cela, le lecteur Windows Media appelle **IWMPContentPartner :: GetItemInfo** pour récupérer l’URL d’une page Web qui exécute le processus de connexion.</span><span class="sxs-lookup"><span data-stu-id="1c123-140">Instead, Windows Media Player calls **IWMPContentPartner::GetItemInfo** to retrieve the URL of a webpage that performs the log-in process.</span></span> <span data-ttu-id="1c123-141">Pour plus d’informations sur l’entrée de Registre **Capabilities** , consultez [clés et entrées de Registre pour un magasin de type 1 en ligne](registry-keys-and-entries-for-a-type-1-online-store.md).</span><span class="sxs-lookup"><span data-stu-id="1c123-141">For more information about the **Capabilities** registry entry, see [Registry Keys and Entries for a Type 1 Online Store](registry-keys-and-entries-for-a-type-1-online-store.md).</span></span>

<span data-ttu-id="1c123-142">Le lecteur appelle **GetItemInfo** deux fois : après avoir passé g \_ szItemInfo \_ ALTLOGINURL pour récupérer l’URL de la page Web de connexion et après avoir passé g \_ szItemInfo \_ ALTLoginCaption pour récupérer la légende de la fenêtre qui héberge la page Web.</span><span class="sxs-lookup"><span data-stu-id="1c123-142">The Player calls **GetItemInfo** twice: once passing g\_szItemInfo\_ALTLoginURL to retrieve the URL of the log-in webpage and once passing g\_szItemInfo\_ALTLoginCaption to retrieve the caption for the window that hosts the webpage.</span></span> <span data-ttu-id="1c123-143">Quand **GetItemInfo** retourne l’URL de la page Web de connexion, il peut spécifier la taille de la fenêtre de connexion en ajoutant la chaîne de paramètre suivante à l’URL :</span><span class="sxs-lookup"><span data-stu-id="1c123-143">When **GetItemInfo** returns the URL of the log-in webpage, it can specify the size of the log-in window by appending the following parameter string to the URL:</span></span>

<span data-ttu-id="1c123-144">? DlgX =*width*&DlgY =*hauteur*</span><span class="sxs-lookup"><span data-stu-id="1c123-144">?DlgX=*width*&DlgY=*height*</span></span>

<span data-ttu-id="1c123-145">Dans la chaîne de paramètre, la *largeur* et la *hauteur* sont la largeur et la hauteur de la fenêtre en pixels.</span><span class="sxs-lookup"><span data-stu-id="1c123-145">In the parameter string, *width* and *height* are the width and height of the window in pixels.</span></span> <span data-ttu-id="1c123-146">Par exemple, **GetItemInfo** peut retourner la chaîne suivante pour spécifier que AltLogin.htm doit être affiché dans une fenêtre qui a une largeur de 800 pixels et une hauteur de 400 pixels</span><span class="sxs-lookup"><span data-stu-id="1c123-146">For example **GetItemInfo** could return the following string to specify that AltLogin.htm should be displayed in a window that has a width of 800 pixels and a height of 400 pixels</span></span>


```C++
https://proseware.com/AltLogin.htm?DlgX=800&DlgY=400
```



<span data-ttu-id="1c123-147">Le processus de connexion alternatif implique les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="1c123-147">The alternative log-in process involves the following steps:</span></span>

1.  <span data-ttu-id="1c123-148">L’utilisateur initie une tentative de connexion en interagissant avec l’interface utilisateur du lecteur Windows Media ou en interagissant avec une page de découverte.</span><span class="sxs-lookup"><span data-stu-id="1c123-148">The user initiates a log-in attempt by interacting with the Windows Media Player user interface or by interacting with a discovery page.</span></span>
2.  <span data-ttu-id="1c123-149">Le lecteur Windows Media ouvre une fenêtre modale qui affiche la page Web de connexion fournie par le magasin en ligne.</span><span class="sxs-lookup"><span data-stu-id="1c123-149">Windows Media Player opens a modal window that displays the log-in webpage provided by the online store.</span></span>
3.  <span data-ttu-id="1c123-150">La page Web communique avec le magasin en ligne et réussit ou ne parvient pas à se connecter à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1c123-150">The webpage communicates with the online store and either succeeds or fails to log in the user.</span></span>
4.  <span data-ttu-id="1c123-151">Si la tentative de connexion aboutit, la page Web avertit le plug-in du magasin en ligne en appelant [External. SendMessage](external-sendmessage.md), ce qui entraîne un appel à [IWMPContentPartner :: SendMessage](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-sendmessage).</span><span class="sxs-lookup"><span data-stu-id="1c123-151">If the log-in attempt succeeds, the webpage notifies the online store's plug-in by calling [External.sendMessage](external-sendmessage.md), which results in a call to [IWMPContentPartner::SendMessage](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-sendmessage).</span></span> <span data-ttu-id="1c123-152">Le plug-in du magasin en ligne détermine que la tentative de connexion a réussi en examinant les paramètres passés à **IWMPContentPartner :: SendMessage**.</span><span class="sxs-lookup"><span data-stu-id="1c123-152">The online store's plug-in determines that the log-in attempt succeeded by inspecting the parameters passed to **IWMPContentPartner::SendMessage**.</span></span> <span data-ttu-id="1c123-153">Ces paramètres ne sont pas interprétés par le lecteur Windows Media ; ils n’ont de sens que dans le magasin en ligne.</span><span class="sxs-lookup"><span data-stu-id="1c123-153">Those parameters are not interpreted by Windows Media Player; they have meaning only to the online store.</span></span> <span data-ttu-id="1c123-154">Le plug-in appelle **IWMPContentPartnerCallback :: Notify**, en passant \_ la valeur variant true dans le membre **boolVal** du paramètre *pContext* .</span><span class="sxs-lookup"><span data-stu-id="1c123-154">The plug-in calls **IWMPContentPartnerCallback::Notify**, passing VARIANT\_TRUE in the **boolVal** member of the *pContext* parameter.</span></span> <span data-ttu-id="1c123-155">Si la connexion échoue, le magasin en ligne doit déterminer comment aider l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1c123-155">If the log-in fails, the online store must determine how to assist the user.</span></span> <span data-ttu-id="1c123-156">L’une des possibilités consiste à afficher une nouvelle page Web dans la fenêtre modale qui héberge l’autre page de connexion.</span><span class="sxs-lookup"><span data-stu-id="1c123-156">One possibility is to display a new webpage in the modal window that hosts the alternative log-in webpage.</span></span>

## <a name="log-out"></a><span data-ttu-id="1c123-157">Déconnectez-vous.</span><span class="sxs-lookup"><span data-stu-id="1c123-157">Log-out</span></span>

<span data-ttu-id="1c123-158">Le processus de déconnexion implique les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="1c123-158">The log-out process involves the following steps.</span></span>

1.  <span data-ttu-id="1c123-159">L’utilisateur lance une tentative de déconnexion en interagissant avec l’interface utilisateur du lecteur Windows Media ou en interagissant avec une page de découverte.</span><span class="sxs-lookup"><span data-stu-id="1c123-159">The user initiates a log-out attempt by interacting with the Windows Media Player user interface or by interacting with a discovery page.</span></span>
2.  <span data-ttu-id="1c123-160">Le lecteur Windows Media appelle [IWMPContentPartner :: Logout](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-logout), qui est implémenté par le plug-in du magasin en ligne.</span><span class="sxs-lookup"><span data-stu-id="1c123-160">Windows Media Player calls [IWMPContentPartner::Logout](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-logout), which is implemented by the online store's plug-in.</span></span>
3.  <span data-ttu-id="1c123-161">Le plug-in communique avec le magasin en ligne et réussit ou ne parvient pas à déconnecter l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1c123-161">The plug-in communicates with the online store and either succeeds or fails to log out the user.</span></span>
4.  <span data-ttu-id="1c123-162">Si la tentative de déconnexion réussit, le plug-in avertit le lecteur Windows Media en appelant **IWMPContentPartnerCallback :: Notify**, en passant \_ la valeur variant false dans le membre **boolVal** du paramètre *pContext* .</span><span class="sxs-lookup"><span data-stu-id="1c123-162">If the log-out attempt succeeds, the plug-in notifies Windows Media Player by calling **IWMPContentPartnerCallback::Notify**, passing VARIANT\_FALSE in the **boolVal** member of the *pContext* parameter.</span></span>

<span data-ttu-id="1c123-163">En cas de réussite d’une tentative de connexion ou d’extraction, le plug-in du magasin en ligne appelle **IWMPContentPartnerCallback :: Notify**, en passant wmpcnLoginStateChange dans le paramètre de *type* .</span><span class="sxs-lookup"><span data-stu-id="1c123-163">When an attempt to log in or out is successful, the online store's plug-in calls **IWMPContentPartnerCallback::Notify**, passing wmpcnLoginStateChange in the *type* parameter.</span></span> <span data-ttu-id="1c123-164">Le plug-in utilise le paramètre *pContext* pour spécifier l’état actuel de la connexion de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1c123-164">The plug-in uses the *pContext* parameter to specify the user's current log-in state.</span></span> <span data-ttu-id="1c123-165">Si le plug-in affecte à *pContext* -> **boolVal** la \_ valeur true, l’utilisateur est connecté.</span><span class="sxs-lookup"><span data-stu-id="1c123-165">If the plug-in sets *pContext*->**boolVal** to VARIANT\_TRUE, the user is logged in.</span></span> <span data-ttu-id="1c123-166">Si le plug-in affecte à *pContext* -> **boolVal** la \_ valeur false, l’utilisateur se déconnecte. Notez que *pContext* n’indique pas la réussite ou l’échec de la tentative ; au lieu de cela, il indique l’état de connexion actuel de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1c123-166">If the plug-in sets *pContext*->**boolVal** to VARIANT\_FALSE, the user is logged out. Note that *pContext* does not indicate the success or failure of the attempt; rather, it indicates user's current log-in state.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1c123-167">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1c123-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1c123-168">**External. attemptLogin**</span><span class="sxs-lookup"><span data-stu-id="1c123-168">**External.attemptLogin**</span></span>](external-attemptlogin.md)
</dt> <dt>

[<span data-ttu-id="1c123-169">**External. OnLoginChange, événement**</span><span class="sxs-lookup"><span data-stu-id="1c123-169">**External.OnLoginChange Event**</span></span>](external-onloginchange-event.md)
</dt> <dt>

[<span data-ttu-id="1c123-170">**External. userLoggedIn**</span><span class="sxs-lookup"><span data-stu-id="1c123-170">**External.userLoggedIn**</span></span>](external-userloggedin.md)
</dt> <dt>

[<span data-ttu-id="1c123-171">**IWMPContentPartner :: login**</span><span class="sxs-lookup"><span data-stu-id="1c123-171">**IWMPContentPartner::Login**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-login)
</dt> <dt>

[<span data-ttu-id="1c123-172">**IWMPContentPartner :: Logout**</span><span class="sxs-lookup"><span data-stu-id="1c123-172">**IWMPContentPartner::Logout**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-logout)
</dt> <dt>

[<span data-ttu-id="1c123-173">**Guide de programmation pour les magasins de type 1 en ligne**</span><span class="sxs-lookup"><span data-stu-id="1c123-173">**Programming Guide for Type 1 Online Stores**</span></span>](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




