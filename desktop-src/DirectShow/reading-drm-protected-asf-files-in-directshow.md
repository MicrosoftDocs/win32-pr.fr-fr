---
description: cette rubrique explique comment utiliser DirectShow pour lire des fichiers multimédias protégés par Windows media Digital Rights Management (DRM).
ms.assetid: a014942a-01e5-49d4-8a25-4604cd40f374
title: Lecture DRM-Protected fichiers ASF dans DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 178dc0dbaa9a8b8e2e849164106816afc6990c89
ms.sourcegitcommit: 4e94fc75fad7b2a0f3c92a26f97e89924e59b7a9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/24/2021
ms.locfileid: "122786965"
---
# <a name="reading-drm-protected-asf-files-in-directshow"></a>Lecture DRM-Protected fichiers ASF dans DirectShow

cette rubrique explique comment utiliser DirectShow pour lire des fichiers multimédias protégés par Windows media Digital Rights Management (DRM).

## <a name="drm-concepts"></a>Concepts DRM

la protection d’un fichier multimédia avec Windows media DRM implique deux étapes distinctes :

-   Le fournisseur de contenu empaquette le fichier, c’est-à-dire chiffre le fichier et joint les informations de licence à l’en-tête de fichier ASF. Les informations de licence incluent une URL où le client peut obtenir la licence.
-   L’application cliente acquiert une licence pour le contenu.

L’empaquetage se produit avant la distribution du fichier. L’acquisition de licence se produit lorsque l’utilisateur tente de lire ou de copier le fichier. L’acquisition de licence peut être *silencieuse* ou *non silencieuse*. L’acquisition en mode silencieux ne requiert aucune interaction avec l’utilisateur. L’acquisition non silencieuse nécessite que l’application ouvre une fenêtre de navigateur et affiche une page Web pour l’utilisateur. À ce stade, l’utilisateur peut avoir besoin de fournir des informations au fournisseur de contenu. Toutefois, les deux types d’acquisition de licence requièrent que le client envoie une requête HTTP à un serveur de licences.

### <a name="drm-versions"></a>Versions DRM

plusieurs versions de Windows Media DRM existent. Du point de vue d’une application cliente, elles peuvent être regroupées en deux catégories : DRM version 1 et DRM version 7 ou ultérieure. (La deuxième catégorie comprend les versions 9 et 10 de DRM, ainsi que la version 7.) La catégorisation des versions DRM de cette façon est que les licences de la version 1 sont gérées différemment des licences de version 7 ou ultérieures. Dans cette documentation, le terme *licence version 7* correspond à la version 7 ou ultérieure.

Il est également important de distinguer l’empaquetage DRM de la licence DRM. si le fichier est empaqueté à l’aide d’Windows Media Rights Manager version 7 ou ultérieure, l’en-tête DRM peut contenir une url de licence de version 1 en plus de l’url de licence de la version 7. L’URL de licence de la version 1 permet aux anciens lecteurs qui ne prennent pas en charge la version 7 d’obtenir une licence pour le contenu. Toutefois, l’inverse n’est pas vrai, donc un fichier avec l’empaquetage version 1 ne peut pas avoir une URL de licence de version 7.

### <a name="application-security-level"></a>Niveau de sécurité de l’application

Pour lire des fichiers protégés par DRM, l’application cliente doit être liée à une bibliothèque statique qui est fournie sous forme binaire par Microsoft. Cette bibliothèque, qui identifie de façon unique l’application, est parfois appelée bibliothèque stub. La bibliothèque stub a un niveau de sécurité attribué, dont la valeur est déterminée par le contrat de licence que vous avez signé quand vous avez obtenu la bibliothèque stub.

Le fournisseur de contenu définit un niveau de sécurité minimal nécessaire pour acquérir la licence. Si le niveau de sécurité de votre bibliothèque stub est inférieur au niveau de sécurité minimal requis par le serveur de licences, l’application ne peut pas obtenir la licence.

### <a name="individualization"></a>Individualisation

Pour renforcer la sécurité, une application peut mettre à jour les composants DRM sur l’ordinateur du client. Cette mise à jour, appelée individualisation, différencie la copie de l’application de l’utilisateur de toutes les autres copies de la même application. L’en-tête DRM d’un fichier protégé peut spécifier un niveau d’individualisation minimal. (pour plus d’informations, consultez la documentation de WMRMHeader. IndividualizedVersion dans Windows le kit de développement logiciel (SDK) Media Rights Manager.)

Étant donné que le service d’individualisation de Microsoft gère les informations de l’utilisateur, vous devez afficher la politique de confidentialité de Microsoft ou fournir un lien vers cette page sur le site Web de Microsoft avant de procéder à l’individualisation de votre application : <https://go.microsoft.com/fwlink/p/?linkid=10240> .

## <a name="provide-the-software-certificate"></a>Fournir le certificat logiciel

pour permettre à l’application d’utiliser la licence DRM, l’application doit fournir un certificat ou une *clé* de logiciel au gestionnaire de Graph de filtre. Cette clé est contenue dans une bibliothèque statique qui est individualisée pour l’application. pour plus d’informations sur l’obtention de la bibliothèque individualisée, consultez [obtention de la bibliothèque DRM requise](../wmformat/obtaining-the-required-drm-library.md) dans la documentation du kit de développement logiciel (SDK) Windows Media Format.

Pour fournir la clé logicielle, procédez comme suit :

1.  Lien vers la bibliothèque statique.
2.  Implémentez l’interface **IServiceProvider** .
3.  interrogez le gestionnaire de Graph de filtre pour l’interface [**IObjectWithSite**](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite) .
4.  Appelez [**IObjectWithSite :: SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) avec un pointeur vers votre implémentation de **IServiceProvider**.
5.  le gestionnaire de Graph de filtre appellera **IServiceProvider :: QueryService**, en spécifiant **IID \_ IWMReader** pour l’identificateur de service.
6.  Dans votre implémentation de **QueryService**, appelez [**WMCreateCertificate**](/previous-versions/windows/desktop/legacy/dd757745(v=vs.85)) pour créer la clé logicielle.

Le code suivant montre comment implémenter la méthode **QueryService** :


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



le code suivant montre comment appeler [**setsite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) sur le filtre Graph Manager :


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





## <a name="building-the-playback-graph"></a>Génération de la Graph de lecture

Pour lire un fichier ASF protégé par DRM, procédez comme suit :

1.  créez le [gestionnaire de Graph de filtre](filter-graph-manager.md) et utilisez l’interface [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) pour vous inscrire aux événements de graphique.
2.  Appelez [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) pour créer une nouvelle instance du filtre de [lecteur ASF WM](wm-asf-reader-filter.md) .
3.  Appelez [**IFilterGraph :: AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) pour ajouter le filtre au graphique de filtre.
4.  Interrogez le filtre de l’interface [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter) .
5.  Appelez [**IFileSourceFilter :: Load**](/windows/desktop/api/Strmif/nf-strmif-ifilesourcefilter-load) avec l’URL du fichier.
6.  Gérez les événements d’événement d’un [**\_ \_ événement WMT**](ec-wmt-event.md) .
7.  Sur le premier événement d’événement de l' [**\_ \_ événement WMT**](ec-wmt-event.md) de l’EC, interrogez le filtre de [lecteur ASF WM](wm-asf-reader-filter.md) pour l’interface **IServiceProvider** .
8.  Appelez **IServiceProvider :: QueryService** pour obtenir un pointeur vers l’interface [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) .
9.  Appelez [**IGraphBuilder :: Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) pour restituer les broches de sortie du filtre de [lecteur ASF WM](wm-asf-reader-filter.md) .

> [!Note]  
> Lors de l’ouverture d’un fichier protégé par DRM, n’appelez pas [**IGraphBuilder :: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) pour créer le graphique de filtre. Le filtre de lecteur ASF WM ne peut pas se connecter à d’autres filtres tant que la licence DRM n’a pas été acquise. Cette étape nécessite que l’application utilise l’interface [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) , qui doit être obtenue à partir du filtre, comme décrit dans les étapes 7 à 8. Par conséquent, vous devez créer le filtre et l’ajouter au graphique

 

> [!Note]  
> Il est important de s’inscrire pour les événements de graphique (étape 1) avant d’ajouter le filtre de [lecteur ASF WM](wm-asf-reader-filter.md) au graphique (étape 3), car l’application doit gérer les événements d’événements de l' [**\_ \_ événement**](ec-wmt-event.md) de la transaction de transaction. Les événements sont envoyés lorsque le [**chargement**](/windows/desktop/api/Strmif/nf-strmif-ifilesourcefilter-load) est appelé (étape 5).

 

Le code suivant montre comment générer le graphique :


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




| C++ | 
|-----|
| <pre><code>            if (FAILED(hr))            {                goto done;            }            hr = RenderOutputPins(pGraph, m_pReader);    }    else    {        // Not a Windows Media file, so just render the standard way.        hr = pGraph-&gt;RenderFile(pwszFile, NULL);    }done:    return hr;}</code></pre> | 




Dans le code précédent, la `RenderOutputPins` fonction énumère les broches de sortie sur le filtre de [lecteur ASF WM](wm-asf-reader-filter.md) et appelle [**IGraphBuilder :: Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) pour chaque pin.


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



Le code suivant montre comment obtenir un pointeur vers l’interface [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) à partir du [lecteur ASF WM](wm-asf-reader-filter.md):


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





## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Lecture des fichiers ASF dans DirectShow](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 
