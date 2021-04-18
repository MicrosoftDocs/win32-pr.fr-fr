---
description: Cette rubrique explique comment utiliser DirectShow pour lire des fichiers multimédias protégés par Windows Media Digital Rights Management (DRM).
ms.assetid: a014942a-01e5-49d4-8a25-4604cd40f374
title: Lecture de fichiers DRM-Protected ASF dans DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff3a90b61982d6c7c444ddcf53948c225b6fc685
ms.sourcegitcommit: b7a1da2711221fa99072079bf52399cbdfc6bd9d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "106520242"
---
# <a name="reading-drm-protected-asf-files-in-directshow"></a><span data-ttu-id="7658a-103">Lecture de fichiers DRM-Protected ASF dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="7658a-103">Reading DRM-Protected ASF Files in DirectShow</span></span>

<span data-ttu-id="7658a-104">Cette rubrique explique comment utiliser DirectShow pour lire des fichiers multimédias protégés par Windows Media Digital Rights Management (DRM).</span><span class="sxs-lookup"><span data-stu-id="7658a-104">This topic describes how to use DirectShow to play media files that are protected with Windows Media Digital Rights Management (DRM).</span></span>

## <a name="drm-concepts"></a><span data-ttu-id="7658a-105">Concepts DRM</span><span class="sxs-lookup"><span data-stu-id="7658a-105">DRM Concepts</span></span>

<span data-ttu-id="7658a-106">La protection d’un fichier multimédia avec Windows Media DRM implique deux étapes distinctes :</span><span class="sxs-lookup"><span data-stu-id="7658a-106">Protecting a media file with Windows Media DRM involves two distinct steps:</span></span>

-   <span data-ttu-id="7658a-107">Le fournisseur de contenu empaquette le fichier, c’est-à-dire chiffre le fichier et joint les informations de licence à l’en-tête de fichier ASF.</span><span class="sxs-lookup"><span data-stu-id="7658a-107">The content provider packages the file—that is, encrypts the file and attaches licensing information to the ASF file header.</span></span> <span data-ttu-id="7658a-108">Les informations de licence incluent une URL où le client peut obtenir la licence.</span><span class="sxs-lookup"><span data-stu-id="7658a-108">The licensing information includes a URL where the client can obtain the license.</span></span>
-   <span data-ttu-id="7658a-109">L’application cliente acquiert une licence pour le contenu.</span><span class="sxs-lookup"><span data-stu-id="7658a-109">The client application acquires a license for the content.</span></span>

<span data-ttu-id="7658a-110">L’empaquetage se produit avant la distribution du fichier.</span><span class="sxs-lookup"><span data-stu-id="7658a-110">Packaging happens before the file is distributed.</span></span> <span data-ttu-id="7658a-111">L’acquisition de licence se produit lorsque l’utilisateur tente de lire ou de copier le fichier.</span><span class="sxs-lookup"><span data-stu-id="7658a-111">License acquisition occurs when the user tries to play or copy the file.</span></span> <span data-ttu-id="7658a-112">L’acquisition de licence peut être *silencieuse* ou *non silencieuse*.</span><span class="sxs-lookup"><span data-stu-id="7658a-112">License acquisition may be either *silent* or *non-silent*.</span></span> <span data-ttu-id="7658a-113">L’acquisition en mode silencieux ne requiert aucune interaction avec l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7658a-113">Silent acquisition does not require any interaction with the user.</span></span> <span data-ttu-id="7658a-114">L’acquisition non silencieuse nécessite que l’application ouvre une fenêtre de navigateur et affiche une page Web pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7658a-114">Non-silent acquisition requires the application to open a browser window and display a web page to the user.</span></span> <span data-ttu-id="7658a-115">À ce stade, l’utilisateur peut avoir besoin de fournir des informations au fournisseur de contenu.</span><span class="sxs-lookup"><span data-stu-id="7658a-115">At that point, the user might need to provide some kind of information to the content provider.</span></span> <span data-ttu-id="7658a-116">Toutefois, les deux types d’acquisition de licence requièrent que le client envoie une requête HTTP à un serveur de licences.</span><span class="sxs-lookup"><span data-stu-id="7658a-116">However, both types of license acquisition require the client to submit an HTTP request to a license server.</span></span>

### <a name="drm-versions"></a><span data-ttu-id="7658a-117">Versions DRM</span><span class="sxs-lookup"><span data-stu-id="7658a-117">DRM Versions</span></span>

<span data-ttu-id="7658a-118">Plusieurs versions de Windows Media DRM existent.</span><span class="sxs-lookup"><span data-stu-id="7658a-118">Several versions of Windows Media DRM exist.</span></span> <span data-ttu-id="7658a-119">Du point de vue d’une application cliente, elles peuvent être regroupées en deux catégories : DRM version 1 et DRM version 7 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="7658a-119">From the perspective of a client application, they can be grouped into two categories: DRM version 1, and DRM version 7 or later.</span></span> <span data-ttu-id="7658a-120">(La deuxième catégorie comprend les versions 9 et 10 de DRM, ainsi que la version 7.) La catégorisation des versions DRM de cette façon est que les licences de la version 1 sont gérées différemment des licences de version 7 ou ultérieures.</span><span class="sxs-lookup"><span data-stu-id="7658a-120">(The second category includes DRM versions 9 and 10, as well as version 7.) The reason for categorizing DRM versions this way is that version 1 licenses are handled somewhat differently than version 7 or later licenses.</span></span> <span data-ttu-id="7658a-121">Dans cette documentation, le terme *licence version 7* correspond à la version 7 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="7658a-121">In this documentation, the term *version 7 license* means version 7 or later.</span></span>

<span data-ttu-id="7658a-122">Il est également important de distinguer l’empaquetage DRM de la licence DRM.</span><span class="sxs-lookup"><span data-stu-id="7658a-122">It is also important to distinguish the DRM packaging from the DRM license.</span></span> <span data-ttu-id="7658a-123">Si le fichier est empaqueté à l’aide de Windows Media Rights Manager version 7 ou ultérieure, l’en-tête DRM peut contenir une URL de licence de version 1 en plus de l’URL de licence de la version 7.</span><span class="sxs-lookup"><span data-stu-id="7658a-123">If the file is packaged using Windows Media Rights Manager version 7 or later, the DRM header can contain a version 1 license URL in addition to the version 7 license URL.</span></span> <span data-ttu-id="7658a-124">L’URL de licence de la version 1 permet aux anciens lecteurs qui ne prennent pas en charge la version 7 d’obtenir une licence pour le contenu.</span><span class="sxs-lookup"><span data-stu-id="7658a-124">The version 1 license URL enables older players that do not support version 7 to obtain a license for the content.</span></span> <span data-ttu-id="7658a-125">Toutefois, l’inverse n’est pas vrai, donc un fichier avec l’empaquetage version 1 ne peut pas avoir une URL de licence de version 7.</span><span class="sxs-lookup"><span data-stu-id="7658a-125">However, the converse is not true, so a file with version 1 packaging cannot have a version 7 license URL.</span></span>

### <a name="application-security-level"></a><span data-ttu-id="7658a-126">Niveau de sécurité de l’application</span><span class="sxs-lookup"><span data-stu-id="7658a-126">Application Security Level</span></span>

<span data-ttu-id="7658a-127">Pour lire des fichiers protégés par DRM, l’application cliente doit être liée à une bibliothèque statique qui est fournie sous forme binaire par Microsoft.</span><span class="sxs-lookup"><span data-stu-id="7658a-127">To play DRM-protected files, the client application must be linked to a static library that is provided in binary form by Microsoft.</span></span> <span data-ttu-id="7658a-128">Cette bibliothèque, qui identifie de façon unique l’application, est parfois appelée bibliothèque stub.</span><span class="sxs-lookup"><span data-stu-id="7658a-128">This library, which uniquely identifies the application, is sometimes called the stub library.</span></span> <span data-ttu-id="7658a-129">La bibliothèque stub a un niveau de sécurité attribué, dont la valeur est déterminée par le contrat de licence que vous avez signé quand vous avez obtenu la bibliothèque stub.</span><span class="sxs-lookup"><span data-stu-id="7658a-129">The stub library has an assigned security level, the value of which is determined by the license agreement that you signed when you obtained the stub library.</span></span>

<span data-ttu-id="7658a-130">Le fournisseur de contenu définit un niveau de sécurité minimal nécessaire pour acquérir la licence.</span><span class="sxs-lookup"><span data-stu-id="7658a-130">The content provider sets a minimum security level needed to acquire the license.</span></span> <span data-ttu-id="7658a-131">Si le niveau de sécurité de votre bibliothèque stub est inférieur au niveau de sécurité minimal requis par le serveur de licences, l’application ne peut pas obtenir la licence.</span><span class="sxs-lookup"><span data-stu-id="7658a-131">If the security level of your stub library is less than the minimum security level required by the license server, the application cannot obtain the license.</span></span>

### <a name="individualization"></a><span data-ttu-id="7658a-132">Individualisation</span><span class="sxs-lookup"><span data-stu-id="7658a-132">Individualization</span></span>

<span data-ttu-id="7658a-133">Pour renforcer la sécurité, une application peut mettre à jour les composants DRM sur l’ordinateur du client.</span><span class="sxs-lookup"><span data-stu-id="7658a-133">To increase security, an application may update the DRM components on the client's computer.</span></span> <span data-ttu-id="7658a-134">Cette mise à jour, appelée individualisation, différencie la copie de l’application de l’utilisateur de toutes les autres copies de la même application.</span><span class="sxs-lookup"><span data-stu-id="7658a-134">This update, called individualization, differentiates the user's copy of the application from all other copies of the same application.</span></span> <span data-ttu-id="7658a-135">L’en-tête DRM d’un fichier protégé peut spécifier un niveau d’individualisation minimal.</span><span class="sxs-lookup"><span data-stu-id="7658a-135">The DRM header of a protected file may specify may specify a minimum individualization level.</span></span> <span data-ttu-id="7658a-136">(Pour plus d’informations, consultez la documentation de WMRMHeader. IndividualizedVersion dans le kit de développement logiciel (SDK) Windows Media Rights Manager.)</span><span class="sxs-lookup"><span data-stu-id="7658a-136">(For more information, see the documentation for WMRMHeader.IndividualizedVersion in the Windows Media Rights Manager SDK.)</span></span>

<span data-ttu-id="7658a-137">Étant donné que le service d’individualisation de Microsoft gère les informations de l’utilisateur, vous devez afficher la politique de confidentialité de Microsoft ou fournir un lien vers cette page sur le site Web de Microsoft avant de procéder à l’individualisation de votre application : <https://go.microsoft.com/fwlink/p/?linkid=10240> .</span><span class="sxs-lookup"><span data-stu-id="7658a-137">Because the Microsoft Individualization Service handles information from the user, you must display the Microsoft privacy policy or provide a link to that page at the Microsoft website before your application individualizes: <https://go.microsoft.com/fwlink/p/?linkid=10240>.</span></span>

## <a name="provide-the-software-certificate"></a><span data-ttu-id="7658a-138">Fournir le certificat logiciel</span><span class="sxs-lookup"><span data-stu-id="7658a-138">Provide the Software Certificate</span></span>

<span data-ttu-id="7658a-139">Pour permettre à l’application d’utiliser la licence DRM, l’application doit fournir un certificat ou une *clé* de logiciel au gestionnaire de graphes de filtre.</span><span class="sxs-lookup"><span data-stu-id="7658a-139">To enable the application to use the DRM license, the application must provide a software certificate or *key* to the Filter Graph Manager.</span></span> <span data-ttu-id="7658a-140">Cette clé est contenue dans une bibliothèque statique qui est individualisée pour l’application.</span><span class="sxs-lookup"><span data-stu-id="7658a-140">This key is contained in a static library that is individualized for the application.</span></span> <span data-ttu-id="7658a-141">Pour plus d’informations sur l’obtention de la bibliothèque individualisée, consultez [obtention de la bibliothèque DRM requise](../wmformat/obtaining-the-required-drm-library.md) dans la documentation du kit de développement logiciel (SDK) Windows Media format.</span><span class="sxs-lookup"><span data-stu-id="7658a-141">For information about obtaining the individualized library, see [Obtaining the Required DRM Library](../wmformat/obtaining-the-required-drm-library.md) in the Windows Media Format SDK documentation.</span></span>

<span data-ttu-id="7658a-142">Pour fournir la clé logicielle, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="7658a-142">To provide the software key, perform the following steps:</span></span>

1.  <span data-ttu-id="7658a-143">Lien vers la bibliothèque statique.</span><span class="sxs-lookup"><span data-stu-id="7658a-143">Link to the static library.</span></span>
2.  <span data-ttu-id="7658a-144">Implémentez l’interface **IServiceProvider** .</span><span class="sxs-lookup"><span data-stu-id="7658a-144">Implement the **IServiceProvider** interface.</span></span>
3.  <span data-ttu-id="7658a-145">Interrogez le gestionnaire du graphique de filtre pour l’interface [**IObjectWithSite**](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite) .</span><span class="sxs-lookup"><span data-stu-id="7658a-145">Query the Filter Graph Manager for the [**IObjectWithSite**](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite) interface.</span></span>
4.  <span data-ttu-id="7658a-146">Appelez [**IObjectWithSite :: SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) avec un pointeur vers votre implémentation de **IServiceProvider**.</span><span class="sxs-lookup"><span data-stu-id="7658a-146">Call [**IObjectWithSite::SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) with a pointer to your implementation of **IServiceProvider**.</span></span>
5.  <span data-ttu-id="7658a-147">Le gestionnaire de graphique de filtre appellera **IServiceProvider :: QueryService**, en spécifiant **IID \_ IWMReader** pour l’identificateur de service.</span><span class="sxs-lookup"><span data-stu-id="7658a-147">The Filter Graph Manager will call **IServiceProvider::QueryService**, specifying **IID\_IWMReader** for the service identifier.</span></span>
6.  <span data-ttu-id="7658a-148">Dans votre implémentation de **QueryService**, appelez [**WMCreateCertificate**](/previous-versions/windows/desktop/legacy/dd757745(v=vs.85)) pour créer la clé logicielle.</span><span class="sxs-lookup"><span data-stu-id="7658a-148">In your implementation of **QueryService**, call [**WMCreateCertificate**](/previous-versions/windows/desktop/legacy/dd757745(v=vs.85)) to create the software key.</span></span>

<span data-ttu-id="7658a-149">Le code suivant montre comment implémenter la méthode **QueryService** :</span><span class="sxs-lookup"><span data-stu-id="7658a-149">The following code shows how to implement the **QueryService** method:</span></span>


```C++
STDMETHODIMP Player::QueryService(REFIID siid, REFIID riid, void **ppv)
{
    if (ppv == NULL ) 
    { 
        return E_POINTER; 
    }

    if (siid == __uuidof(IWMReader) && riid == __uuidof(IUnknown))
    {
        IUnknown *punkCert;

        HRESULT hr = WMCreateCertificate(&punkCert);

        if (SUCCEEDED(hr))
        {
            *ppv = (void *) punkCert;
        }

        return hr;
    }
    return E_NOINTERFACE;
}
```



<span data-ttu-id="7658a-150">Le code suivant montre comment appeler [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) sur le gestionnaire de graphique de filtre :</span><span class="sxs-lookup"><span data-stu-id="7658a-150">The following code shows how to call [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) on the Filter Graph Manager:</span></span>


```C++
HRESULT Player::CreateFilterGraph()
{
    CComPtr<IObjectWithSite> pSite;

    HRESULT hr = pGraph.CoCreateInstance(CLSID_FilterGraph);

    if (FAILED(hr))
    {
        goto done;
    }

    // Register the application as a site (service).
    hr = pGraph->QueryInterface(&pSite);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSite->SetSite(this);


done:
    return hr;
}
```





## <a name="building-the-playback-graph"></a><span data-ttu-id="7658a-151">Génération du graphique de lecture</span><span class="sxs-lookup"><span data-stu-id="7658a-151">Building the Playback Graph</span></span>

<span data-ttu-id="7658a-152">Pour lire un fichier ASF protégé par DRM, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="7658a-152">To play a DRM-protected ASF file, perform the following steps:</span></span>

1.  <span data-ttu-id="7658a-153">Créez le [Gestionnaire de graphe de filtre](filter-graph-manager.md) et utilisez l’interface [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) pour vous inscrire aux événements de graphique.</span><span class="sxs-lookup"><span data-stu-id="7658a-153">Create the [Filter Graph Manager](filter-graph-manager.md) and use the [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) interface to register for graph events.</span></span>
2.  <span data-ttu-id="7658a-154">Appelez [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) pour créer une nouvelle instance du filtre de [lecteur ASF WM](wm-asf-reader-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="7658a-154">Call [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to create a new instance of the [WM ASF Reader](wm-asf-reader-filter.md) filter.</span></span>
3.  <span data-ttu-id="7658a-155">Appelez [**IFilterGraph :: AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) pour ajouter le filtre au graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="7658a-155">Call [**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) to add the filter to the filter graph.</span></span>
4.  <span data-ttu-id="7658a-156">Interrogez le filtre de l’interface [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter) .</span><span class="sxs-lookup"><span data-stu-id="7658a-156">Query the filter for the [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter) interface.</span></span>
5.  <span data-ttu-id="7658a-157">Appelez [**IFileSourceFilter :: Load**](/windows/desktop/api/Strmif/nf-strmif-ifilesourcefilter-load) avec l’URL du fichier.</span><span class="sxs-lookup"><span data-stu-id="7658a-157">Call [**IFileSourceFilter::Load**](/windows/desktop/api/Strmif/nf-strmif-ifilesourcefilter-load) with the URL of the file.</span></span>
6.  <span data-ttu-id="7658a-158">Gérez les événements d’événement d’un [**\_ \_ événement WMT**](ec-wmt-event.md) .</span><span class="sxs-lookup"><span data-stu-id="7658a-158">Handle [**EC\_WMT\_EVENT**](ec-wmt-event.md) events.</span></span>
7.  <span data-ttu-id="7658a-159">Sur le premier événement d’événement de l' [**\_ \_ événement WMT**](ec-wmt-event.md) de l’EC, interrogez le filtre de [lecteur ASF WM](wm-asf-reader-filter.md) pour l’interface **IServiceProvider** .</span><span class="sxs-lookup"><span data-stu-id="7658a-159">On the first [**EC\_WMT\_EVENT**](ec-wmt-event.md) event, query the [WM ASF Reader](wm-asf-reader-filter.md) filter for the **IServiceProvider** interface.</span></span>
8.  <span data-ttu-id="7658a-160">Appelez **IServiceProvider :: QueryService** pour obtenir un pointeur vers l’interface [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) .</span><span class="sxs-lookup"><span data-stu-id="7658a-160">Call **IServiceProvider::QueryService** to get a pointer to the [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) interface.</span></span>
9.  <span data-ttu-id="7658a-161">Appelez [**IGraphBuilder :: Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) pour restituer les broches de sortie du filtre de [lecteur ASF WM](wm-asf-reader-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="7658a-161">Call [**IGraphBuilder::Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) to render the output pins of the [WM ASF Reader](wm-asf-reader-filter.md) filter.</span></span>

> [!Note]  
> <span data-ttu-id="7658a-162">Lors de l’ouverture d’un fichier protégé par DRM, n’appelez pas [**IGraphBuilder :: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) pour créer le graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="7658a-162">When opening a DRM-protected file, do not call [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) to create the filter graph.</span></span> <span data-ttu-id="7658a-163">Le filtre de lecteur ASF WM ne peut pas se connecter à d’autres filtres tant que la licence DRM n’a pas été acquise.</span><span class="sxs-lookup"><span data-stu-id="7658a-163">The WM ASF Reader filter cannot connect to any other filters until the DRM license is acquired.</span></span> <span data-ttu-id="7658a-164">Cette étape nécessite que l’application utilise l’interface [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) , qui doit être obtenue à partir du filtre, comme décrit dans les étapes 7 à 8.</span><span class="sxs-lookup"><span data-stu-id="7658a-164">This step requires the application to use the [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) interface, which must be obtained from the filter, as described in steps 7–8.</span></span> <span data-ttu-id="7658a-165">Par conséquent, vous devez créer le filtre et l’ajouter au graphique</span><span class="sxs-lookup"><span data-stu-id="7658a-165">Therefore, you must create the filter and add it to the graph</span></span>

 

> [!Note]  
> <span data-ttu-id="7658a-166">Il est important de s’inscrire pour les événements de graphique (étape 1) avant d’ajouter le filtre de [lecteur ASF WM](wm-asf-reader-filter.md) au graphique (étape 3), car l’application doit gérer les événements d’événements de l' [**\_ \_ événement**](ec-wmt-event.md) de la transaction de transaction.</span><span class="sxs-lookup"><span data-stu-id="7658a-166">It is important to register for graph events (step 1) before adding the [WM ASF Reader](wm-asf-reader-filter.md) filter to the graph (step 3), because the application must handle the [**EC\_WMT\_EVENT**](ec-wmt-event.md) events.</span></span> <span data-ttu-id="7658a-167">Les événements sont envoyés lorsque le [**chargement**](/windows/desktop/api/Strmif/nf-strmif-ifilesourcefilter-load) est appelé (étape 5).</span><span class="sxs-lookup"><span data-stu-id="7658a-167">The events are sent when [**Load**](/windows/desktop/api/Strmif/nf-strmif-ifilesourcefilter-load) is called (step 5).</span></span>

 

<span data-ttu-id="7658a-168">Le code suivant montre comment générer le graphique :</span><span class="sxs-lookup"><span data-stu-id="7658a-168">The following code shows how to build the graph:</span></span>


```C++
HRESULT Player::LoadMediaFile(PCWSTR pwszFile)
{


    BOOL bIsWindowsMediaFile = IsWindowsMediaFile(pwszFile);

    HRESULT hr = S_OK;

    // If this is the first time opening the file, create the
    // filter graph and add the WM ASF Reader filter.

    if (m_DRM.State() == DRM_INITIAL)
    {
        hr = CreateFilterGraph();
        if (FAILED(hr))
        {
            goto done;
        }

        // Use special handling for Windows Media files.
        if (bIsWindowsMediaFile)
        {
            // Add the ASF Reader filter to the graph.
            hr = m_pReader.CoCreateInstance(CLSID_WMAsfReader);
            if (FAILED(hr))
            {
                goto done;
            }

            hr = pGraph->AddFilter(m_pReader, NULL);
            if (FAILED(hr))
            {
                goto done;
            }

            hr = m_pReader->QueryInterface(&m_pFileSource);
            if (FAILED(hr))
            {
                goto done;
            }
        }
    }

    if (bIsWindowsMediaFile)
    {
            hr = m_pFileSource->Load(pwszFile, NULL);
```

<span codelanguage="ManagedCPlusPlus"></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7658a-169">C++</span><span class="sxs-lookup"><span data-stu-id="7658a-169">C++</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>            if (FAILED(hr))
            {
                goto done;
            }
            hr = RenderOutputPins(pGraph, m_pReader);
    }
    else
    {
        // Not a Windows Media file, so just render the standard way.
        hr = pGraph->RenderFile(pwszFile, NULL);
    }

done:
    return hr;
}</code></pre></td>
</tr>
</tbody>
</table>



<span data-ttu-id="7658a-170">Dans le code précédent, la `RenderOutputPins` fonction énumère les broches de sortie sur le filtre de [lecteur ASF WM](wm-asf-reader-filter.md) et appelle [**IGraphBuilder :: Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) pour chaque pin.</span><span class="sxs-lookup"><span data-stu-id="7658a-170">In the previous code, the `RenderOutputPins` function enumerates the output pins on the [WM ASF Reader](wm-asf-reader-filter.md) filter and calls [**IGraphBuilder::Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) for each pin.</span></span>


```C++
HRESULT RenderOutputPins(IGraphBuilder *pGraph, IBaseFilter *pFilter)
{
    CComPtr<IEnumPins>  pEnumPin = NULL;
    CComPtr<IPin>       pConnectedPin;
    CComPtr<IPin>       pPin;

    // Enumerate all pins on the filter
    HRESULT hr = pFilter->EnumPins(&pEnumPin);
    if (FAILED(hr))
    {
        goto done;
    }

    // Step through every pin, looking for the output pins.
    while (S_OK == (hr = pEnumPin->Next(1, &pPin, NULL)))
    {
        // Skip connected pins.
        hr = pPin->ConnectedTo(&pConnectedPin);
        if (hr == VFW_E_NOT_CONNECTED)
        {
            PIN_DIRECTION PinDirection;
            hr = pPin->QueryDirection(&PinDirection);

            if ((S_OK == hr) && (PinDirection == PINDIR_OUTPUT))
            {
                hr = pGraph->Render(pPin);
            }
        }

        pConnectedPin.Release();
        pPin.Release();

        // If there was an error, stop enumerating.
        if (FAILED(hr))
        {
            break;
        }
    }

done:
    return hr;
}
```



<span data-ttu-id="7658a-171">Le code suivant montre comment obtenir un pointeur vers l’interface [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) à partir du [lecteur ASF WM](wm-asf-reader-filter.md):</span><span class="sxs-lookup"><span data-stu-id="7658a-171">The following code shows how to get a pointer to the [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) interface from the [WM ASF Reader](wm-asf-reader-filter.md):</span></span>


```C++
HRESULT DrmManager::Initialize(IBaseFilter *pFilter)
{


    CComPtr<IServiceProvider> pService;
    CComPtr<IWMDRMReader> pDrmReader;

    HRESULT hr = pFilter->QueryInterface(&pService);
    if (SUCCEEDED(hr))
    {
        hr = pService->QueryService(
            __uuidof(IWMDRMReader), IID_PPV_ARGS(&m_pDrmReader));
    }
    return hr;
}
```





## <a name="related-topics"></a><span data-ttu-id="7658a-172">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7658a-172">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7658a-173">Lecture de fichiers ASF dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="7658a-173">Reading ASF Files in DirectShow</span></span>](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 
