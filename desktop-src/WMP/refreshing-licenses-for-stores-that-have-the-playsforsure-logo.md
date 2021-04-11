---
title: Actualisation des licences des magasins qui ont le logo PlaysForSure
description: Actualisation des licences des magasins qui ont le logo PlaysForSure
ms.assetid: d08d6b6e-937e-4dec-b7ca-376cdad069f9
keywords:
- Windows Media Player Online stores, actualisation des licences
- magasins en ligne, actualisation des licences
- Windows Media Player Online stores, actualisation des licences
- magasins en ligne, actualisation des licences
- Windows Media Player Online stores, logo PlaysForSure
- magasins en ligne, logo PlaysForSure
- actualisation des licences
- licences, actualisation
- PlaysForSure
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42e48a3ddfd2b0670e3720f7c71587d0330a69a7
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104101289"
---
# <a name="refreshing-licenses-for-stores-that-have-the-playsforsure-logo"></a><span data-ttu-id="b991a-112">Actualisation des licences des magasins qui ont le logo PlaysForSure</span><span class="sxs-lookup"><span data-stu-id="b991a-112">Refreshing Licenses for Stores That Have the PlaysForSure Logo</span></span>

<span data-ttu-id="b991a-113">Certains magasins de musique en ligne ont le logo PlaysForSure mais ne sont pas intégrés au lecteur Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="b991a-113">Certain online music stores have the PlaysForSure logo but are not integrated with Windows Media Player 11.</span></span> <span data-ttu-id="b991a-114">Ces magasins doivent fournir un document ServiceInfo et un composant léger afin que le lecteur Windows Media 11 puisse obtenir et mettre à jour des licences pour son contenu.</span><span class="sxs-lookup"><span data-stu-id="b991a-114">Those stores must provide a ServiceInfo document and a lightweight component so that Windows Media Player 11 can obtain and update licenses for their content.</span></span>

<span data-ttu-id="b991a-115">L’exemple suivant illustre le fonctionnement du processus de mise à jour de la licence.</span><span class="sxs-lookup"><span data-stu-id="b991a-115">The following example illustrates how the license updating process works.</span></span>

1.  <span data-ttu-id="b991a-116">L’utilisateur obtient des pistes de musique 50 à partir du magasin en ligne proseware.</span><span class="sxs-lookup"><span data-stu-id="b991a-116">The user obtains 50 music tracks from the Proseware online store.</span></span> <span data-ttu-id="b991a-117">Chaque piste est un fichier avec l’extension de nom de fichier. WMA.</span><span class="sxs-lookup"><span data-stu-id="b991a-117">Each track is a file with the .wma file name extension.</span></span> <span data-ttu-id="b991a-118">Avec les pistes, l’utilisateur obtient des licences pour lire les pistes.</span><span class="sxs-lookup"><span data-stu-id="b991a-118">Along with the tracks, the user obtains licenses to play the tracks.</span></span>
2.  <span data-ttu-id="b991a-119">L’utilisateur copie les pistes 50 sur un nouvel ordinateur sur lequel est installé le lecteur Windows Media 11 et ajoute les pistes à la bibliothèque du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="b991a-119">The user copies the 50 tracks to a new computer that has Windows Media Player 11 installed and adds the tracks to the Windows Media Player library.</span></span>
3.  <span data-ttu-id="b991a-120">Plus tard, le module d’actualisation des licences (LRM), qui fait partie du lecteur Windows Media 11, inspecte les métadonnées dans les pistes 50 et détermine que Proseware est le fournisseur de contenu.</span><span class="sxs-lookup"><span data-stu-id="b991a-120">At some later time, the License Refresh Module (LRM), which is part of Windows Media Player 11, inspects the metadata in the fifty tracks and determines that Proseware is the content provider.</span></span>
    > [!Note]  
    > <span data-ttu-id="b991a-121">Le lecteur Windows Media est en mesure d’identifier le fournisseur de contenu en inspectant l’attribut **ContentDistributor** dans un fichier multimédia.</span><span class="sxs-lookup"><span data-stu-id="b991a-121">Windows Media Player is able to identify the content provider by inspecting the **ContentDistributor** attribute in a media file.</span></span> <span data-ttu-id="b991a-122">Si un magasin en ligne contenant le logo PlaysForSure fournit un fichier multimédia qui utilise Windows Media Digital Rights Management (WMDRM), le magasin en ligne doit placer l’attribut **ContentDistributor** dans le fichier multimédia.</span><span class="sxs-lookup"><span data-stu-id="b991a-122">If an online store that has the PlaysForSure logo provides a media file that uses Windows Media Digital Rights Management (WMDRM), the online store must place the **ContentDistributor** attribute in the media file.</span></span> <span data-ttu-id="b991a-123">Pour plus d’informations, consultez Ajout de l’attribut content Distributor dans le kit de développement logiciel (SDK) du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="b991a-123">For more information, see Adding the Content Distributor Attribute in the Windows Media Player SDK.</span></span>

     

4.  <span data-ttu-id="b991a-124">LRM recherche l’URL du document ServiceInfo de Proseware, télécharge le document et inspecte l’élément d' **installation** du document afin d’obtenir l’URL d’un package que le LRM peut utiliser pour installer le composant de proseware.</span><span class="sxs-lookup"><span data-stu-id="b991a-124">The LRM looks up the URL of Proseware's ServiceInfo document, downloads the document, and inspects the document's **Install** element to obtain the URL of a package that the LRM can use to install Proseware's component.</span></span> <span data-ttu-id="b991a-125">Le LRM installe et charge le composant.</span><span class="sxs-lookup"><span data-stu-id="b991a-125">The LRM installs and loads the component.</span></span>
5.  <span data-ttu-id="b991a-126">Pour chacune des pistes 50, LRM appelle la méthode [IWMPSubscriptionService :: allowPlay](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowplay) du composant proseware.</span><span class="sxs-lookup"><span data-stu-id="b991a-126">For each of the 50 tracks, the LRM calls the Proseware component's [IWMPSubscriptionService::allowPlay](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowplay) method.</span></span> <span data-ttu-id="b991a-127">La méthode **allowPlay** place une licence pour la piste individuelle sur le nouvel ordinateur et retourne la **valeur true** dans le paramètre *pfAllowPlay* .</span><span class="sxs-lookup"><span data-stu-id="b991a-127">The **allowPlay** method places a license for the individual track on the new computer and returns **TRUE** in the *pfAllowPlay* parameter.</span></span>
    > [!Note]  
    > <span data-ttu-id="b991a-128">Le composant Proseware doit fournir toutes les licences requises pour lire la piste individuelle. Autrement dit, le composant doit fournir une licence racine et une licence feuille si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="b991a-128">The Proseware component must provide all licenses required to play the individual track. That is, the component must provide both a root license and a leaf license if needed.</span></span>

     

    <span data-ttu-id="b991a-129">Lors du premier appel à la méthode **allowPlay** , le composant Proseware doit afficher une boîte de dialogue pour vérifier que l’utilisateur actuel possède un compte Proseware et a le droit de lire la piste. Lors des appels suivants à **allowPlay**, le composant peut utiliser les informations d’identification qu’il a obtenues dans le premier appel pour vérifier que l’utilisateur a le droit de lire les pistes restantes.</span><span class="sxs-lookup"><span data-stu-id="b991a-129">During the first call to the **allowPlay** method, the Proseware component must display a dialog box to verify that the current user has a Proseware account and has the right to play the track. During subsequent calls to **allowPlay**, the component can use the credentials that it obtained in the first call to verify that the user has the right to play the remaining tracks.</span></span>

<span data-ttu-id="b991a-130">Le composant, qui est écrit par le magasin en ligne, doit implémenter la méthode **allowPlay** de l’interface **IWMPSubscriptionService** .</span><span class="sxs-lookup"><span data-stu-id="b991a-130">The component, which is written by the online store, must implement the **allowPlay** method of the **IWMPSubscriptionService** interface.</span></span> <span data-ttu-id="b991a-131">Le composant doit retourner E \_ NOTIMPL à partir de chacune des trois autres méthodes : **allowCDBurn**, **allowPDATransfer** et **startBackgroundProcessing**.</span><span class="sxs-lookup"><span data-stu-id="b991a-131">The component must return E\_NOTIMPL from each of the other three methods: **allowCDBurn**, **allowPDATransfer**, and **startBackgroundProcessing**.</span></span> <span data-ttu-id="b991a-132">En outre, le composant doit définir la valeur de l’entrée de Registre **Capabilities** sur 1 ; autrement dit, l’indicateur de capacité ALLOWPLAY de l’abonnement \_ Cap \_ doit être défini, et tous les autres indicateurs de capacité doivent être effacés.</span><span class="sxs-lookup"><span data-stu-id="b991a-132">Also, the component must set the value of the **Capabilities** registry entry to 1; that is, the SUBSCRIPTION\_CAP\_ALLOWPLAY capability flag must be set, and all other capability flags must be cleared.</span></span> <span data-ttu-id="b991a-133">Pour plus d’informations sur l’inscription du composant, consultez [clés et entrées de Registre pour un magasin de type 2 en ligne](registry-keys-and-entries-for-a-type-2-online-store.md).</span><span class="sxs-lookup"><span data-stu-id="b991a-133">For more information about registering the component, see [Registry Keys and Entries for a Type 2 Online Store](registry-keys-and-entries-for-a-type-2-online-store.md).</span></span>

<span data-ttu-id="b991a-134">Pour plus d’informations sur la création d’un composant qui implémente l’interface **IWMPSubscriptionService** , consultez [génération du plug-in pour un magasin de type 2 en ligne](building-the-plug-in-for-a-type-2-online-store.md).</span><span class="sxs-lookup"><span data-stu-id="b991a-134">For information about creating a component that implements the **IWMPSubscriptionService** interface, see [Building the Plug-in for a Type 2 Online Store](building-the-plug-in-for-a-type-2-online-store.md).</span></span>

<span data-ttu-id="b991a-135">Pour plus d’informations sur la façon de fournir un document ServiceInfo à Microsoft, envoyez un e-mail à l’équipe des services virtuels du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="b991a-135">For information about providing Microsoft with a ServiceInfo document, send email to the Windows Media Player Virtual Services team.</span></span> <span data-ttu-id="b991a-136">L’adresse de messagerie de l’équipe est mpsvctm@microsoft.com .</span><span class="sxs-lookup"><span data-stu-id="b991a-136">The team's email address is mpsvctm@microsoft.com.</span></span>

<span data-ttu-id="b991a-137">Pour obtenir des conseils techniques sur l’utilisation de divers kits de développement logiciel (SDK) Windows Media pour créer un service proposant du contenu multimédia numérique sous licence, accédez au [Centre de développement Microsoft Windows Media](https://msdn.microsoft.com/windowsmedia/default.aspx) et recherchez « création d’un magasin en ligne d’abonnement Windows Media Player 10 ».</span><span class="sxs-lookup"><span data-stu-id="b991a-137">For technical guidance on using a variety of Windows Media SDKs to create a service that offers licensed digital media content, go to the [Microsoft Windows Media Developer Center](https://msdn.microsoft.com/windowsmedia/default.aspx) and search for "Creating a Windows Media Player 10 Subscription Online Store".</span></span>

## <a name="related-topics"></a><span data-ttu-id="b991a-138">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b991a-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b991a-139">**Document ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="b991a-139">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> <dt>

[<span data-ttu-id="b991a-140">**Windows Media Player Online stores**</span><span class="sxs-lookup"><span data-stu-id="b991a-140">**Windows Media Player Online Stores**</span></span>](windows-media-player-online-stores.md)
</dt> </dl>

 

 




