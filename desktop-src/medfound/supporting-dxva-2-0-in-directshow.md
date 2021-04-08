---
description: Cette rubrique décrit comment prendre en charge DirectX Video Acceleration (DXVA) 2,0 dans un filtre de décodeur DirectShow.
ms.assetid: 40deaddb-bb17-4a34-8294-5c7dc8a8a457
title: Prise en charge de DXVA 2,0 dans DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dda956b60d4905c2392e1a50bd62ee8421b944b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863406"
---
# <a name="supporting-dxva-20-in-directshow"></a>Prise en charge de DXVA 2,0 dans DirectShow

Cette rubrique décrit comment prendre en charge DirectX Video Acceleration (DXVA) 2,0 dans un filtre de décodeur DirectShow. Plus précisément, il décrit la communication entre le décodeur et le convertisseur vidéo. Cette rubrique ne décrit pas comment implémenter le décodage DXVA.

-   [Conditions préalables](#prerequisites)
-   [Remarques sur la migration](#migration-notes)
-   [Recherche d’une configuration de décodeur](#finding-a-decoder-configuration)
-   [Notification du convertisseur vidéo](#notifying-the-video-renderer)
-   [Allocation de mémoires tampons non compressées](#allocating-uncompressed-buffers)
-   [Décodage](#decoding)
-   [Rubriques connexes](#related-topics)

## <a name="prerequisites"></a>Prérequis

Cette rubrique suppose que vous êtes familiarisé avec l’écriture de filtres DirectShow. Pour plus d’informations, consultez la rubrique [écriture de filtres DirectShow](../directshow/writing-directshow-filters.md) dans la documentation du kit de développement logiciel (SDK) DirectShow. Les exemples de code de cette rubrique supposent que le filtre de décodeur est dérivé de la classe [**CTransformFilter**](../directshow/ctransformfilter.md) , avec la définition de classe suivante :


```C++
class CDecoder : public CTransformFilter
{
public:
    static CUnknown* WINAPI CreateInstance(IUnknown *pUnk, HRESULT *pHr);

    HRESULT CompleteConnect(PIN_DIRECTION direction, IPin *pPin);

    HRESULT InitAllocator(IMemAllocator **ppAlloc);
    HRESULT DecideBufferSize(IMemAllocator *pAlloc, ALLOCATOR_PROPERTIES *pProp);

    // TODO: The implementations of these methods depend on the specific decoder.
    HRESULT CheckInputType(const CMediaType *mtIn);
    HRESULT CheckTransform(const CMediaType *mtIn, const CMediaType *mtOut);
    HRESULT CTransformFilter::GetMediaType(int,CMediaType *);

private:
    CDecoder(HRESULT *pHr);
    ~CDecoder();

    CBasePin * GetPin(int n);

    HRESULT ConfigureDXVA2(IPin *pPin);
    HRESULT SetEVRForDXVA2(IPin *pPin);

    HRESULT FindDecoderConfiguration(
        /* [in] */  IDirectXVideoDecoderService *pDecoderService,
        /* [in] */  const GUID& guidDecoder, 
        /* [out] */ DXVA2_ConfigPictureDecode *pSelectedConfig,
        /* [out] */ BOOL *pbFoundDXVA2Configuration
        );

private:
    IDirectXVideoDecoderService *m_pDecoderService;

    DXVA2_ConfigPictureDecode m_DecoderConfig;
    GUID                      m_DecoderGuid;
    HANDLE                    m_hDevice;

    FOURCC                    m_fccOutputFormat;
};
```



Dans le reste de cette rubrique, le *décodeur* de terme fait référence au filtre de décodeur, qui reçoit une vidéo compressée et génère des sorties vidéo non compressées. L' *appareil décodeur* terme fait référence à un accélérateur vidéo matériel implémenté par le pilote Graphics.

Voici les étapes de base qu’un filtre de décodeur doit effectuer pour prendre en charge DXVA 2,0 :

1.  Négocier un type de média.
2.  Recherchez une configuration de décodeur DXVA.
3.  Informez le convertisseur vidéo que le décodeur utilise le décodage DXVA.
4.  Fournissez un allocateur personnalisé qui alloue des surfaces Direct3D.

Ces étapes sont décrites plus en détail dans le reste de cette rubrique.

## <a name="migration-notes"></a>Remarques sur la migration

Si vous effectuez une migration à partir de DXVA 1,0, vous devez être conscient des différences significatives entre les deux versions :

-   DXVA 2,0 n’utilise pas les interfaces [**IAMVideoAccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) et [**IAMVideoAcceleratorNotify**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoacceleratornotify) , car le décodeur peut accéder aux API DXVA 2,0 directement par le biais de l’interface [**IDirectXVideoDecoder**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder) .
-   Pendant la négociation de type de média, le décodeur n’utilise pas de GUID d’accélération vidéo comme sous-type. Au lieu de cela, le sous-type est simplement le format vidéo non compressé (par exemple, NV12), comme avec le décodage logiciel.
-   La procédure de configuration de l’accélérateur a changé. Dans DXVA 1,0, les appels du décodeur **s’exécutent** avec une structure **DXVA \_ ConfigPictureDecode** pour configurer accerlator. Dans DXVA 2,0, le décodeur utilise l’interface [**IDirectXVideoDecoderService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) , comme décrit dans la section suivante.
-   Le décodeur alloue les mémoires tampons non compressées. Le convertisseur vidéo ne les alloue plus.
-   Au lieu d’appeler [**IAMVideoAccelerator ::D isplayframe**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-displayframe) pour afficher le frame décodé, le décodeur remet le frame au convertisseur en appelant [**IMemInputPin :: Receive**](/windows/win32/api/strmif/nf-strmif-imeminputpin-receive), comme avec le décodage logiciel.
-   Le décodeur n’est plus responsable de la vérification de la sécurité des tampons de données pour les mises à jour. Par conséquent, DXVA 2,0 n’a pas de méthode équivalente à [**IAMVideoAccelerator :: QueryRenderStatus**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-queryrenderstatus).
-   La fusion de sous-image est effectuée par le convertisseur vidéo, à l’aide des API de processeur vidéo DXVA 2.0. Les décodeurs qui fournissent des sous-images (par exemple, des décodeurs DVD) doivent envoyer des données de sous-image sur une broche de sortie distincte.

Pour les opérations de décodage, DXVA 2,0 utilise les mêmes structures de données que DXVA 1,0.

Le filtre EVR (Enhanced Video Renderer) prend en charge la 2,0 DXVA. Les filtres de convertisseur de mixage vidéo (VMR-7 et VMR-9) prennent uniquement en charge DXVA 1,0.

## <a name="finding-a-decoder-configuration"></a>Recherche d’une configuration de décodeur

Une fois que le décodeur a négocié le type de média de sortie, il doit trouver une configuration compatible pour le périphérique décodeur DXVA. Vous pouvez effectuer cette étape à l’intérieur de la méthode [**CBaseOutputPin :: CompleteConnect**](../directshow/cbaseoutputpin-completeconnect.md) de la broche de sortie. Cette étape garantit que le pilote Graphics prend en charge les fonctionnalités requises par le décodeur, avant que le décodeur ne s’engage à utiliser DXVA.

Pour rechercher une configuration pour l’appareil décodeur, procédez comme suit :

1.  Interrogez la broche d’entrée du convertisseur pour l’interface [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) .
2.  Appelez [**IMFGetService :: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) pour obtenir un pointeur vers l’interface [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) . Le GUID du service est \_ un \_ service d’accélération vidéo \_ .
3.  Appelez [**IDirect3DDeviceManager9 :: OpenDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle) pour obtenir un handle sur le périphérique Direct3D du convertisseur.
4.  Appelez [**IDirect3DDeviceManager9 :: GetVideoService**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-getvideoservice) et transmettez le descripteur de l’appareil. Cette méthode retourne un pointeur vers l’interface [**IDirectXVideoDecoderService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) .
5.  Appelez [**IDirectXVideoDecoderService :: GetDecoderDeviceGuids**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderdeviceguids). Cette méthode retourne un tableau de GUID d’appareil de décodage.
6.  Parcourez le tableau de GUID de décodeur pour rechercher ceux que le filtre de décodeur prend en charge. Par exemple, pour un décodeur MPEG-2, vous devez rechercher **DXVA2 \_ ModeMPEG2 \_ MOCOMP**, **DXVA2 \_ ModeMPEG2 \_ IDCT** ou DXVA2 ModeMPEG2 **\_ \_ VLD**.

7.  Lorsque vous trouvez un GUID d’appareil décodeur candidat, transmettez le GUID à la méthode [**IDirectXVideoDecoderService :: GetDecoderRenderTargets**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderrendertargets) . Cette méthode retourne un tableau de formats de cible de rendu, spécifiés en tant que valeurs **D3DFORMAT** .
8.  Parcourez les formats de cible de rendu et recherchez-en un qui correspond à votre format de sortie. En règle générale, un appareil de décodage prend en charge un format de cible de rendu unique. Le filtre de décodeur doit se connecter au convertisseur à l’aide de ce sous-type. Dans le premier appel à [**CompleteConnect**](../directshow/cbaseoutputpin-completeconnect.md), le décodeur peut déterminer le format de la cible de rendu, puis retourner ce format comme type de sortie préféré.

9.  Appelez [**IDirectXVideoDecoderService :: GetDecoderConfigurations**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderconfigurations). Transmettez le même GUID de périphérique décodeur, ainsi qu’une structure [**DXVA2 \_ VideoDesc**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc) qui décrit le format proposé. La méthode retourne un tableau de structures [**DXVA2 \_ ConfigPictureDecode**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_configpicturedecode) . Chaque structure décrit une configuration possible pour l’appareil décodeur.

10. En supposant que les étapes précédentes sont réussies, stockez le descripteur de périphérique Direct3D, le GUID du périphérique décodeur et la structure de configuration. Le filtre utilise ces informations pour créer l’appareil de décodage.

Le code suivant montre comment rechercher une configuration de décodeur.


```C++
HRESULT CDecoder::ConfigureDXVA2(IPin *pPin)
{
    UINT    cDecoderGuids = 0;
    BOOL    bFoundDXVA2Configuration = FALSE;
    GUID    guidDecoder = GUID_NULL;

    DXVA2_ConfigPictureDecode config;
    ZeroMemory(&config, sizeof(config));

    // Variables that follow must be cleaned up at the end.

    IMFGetService               *pGetService = NULL;
    IDirect3DDeviceManager9     *pDeviceManager = NULL;
    IDirectXVideoDecoderService *pDecoderService = NULL;

    GUID   *pDecoderGuids = NULL; // size = cDecoderGuids
    HANDLE hDevice = INVALID_HANDLE_VALUE;

    // Query the pin for IMFGetService.
    HRESULT hr = pPin->QueryInterface(IID_PPV_ARGS(&pGetService));

    // Get the Direct3D device manager.
    if (SUCCEEDED(hr))
    {
        hr = pGetService->GetService(

            MR_VIDEO_ACCELERATION_SERVICE,
            IID_PPV_ARGS(&pDeviceManager)
            );
    }

    // Open a new device handle.
    if (SUCCEEDED(hr))
    {
        hr = pDeviceManager->OpenDeviceHandle(&hDevice);
    } 

    // Get the video decoder service.
    if (SUCCEEDED(hr))
    {
        hr = pDeviceManager->GetVideoService(
            hDevice, IID_PPV_ARGS(&pDecoderService));
    }

    // Get the decoder GUIDs.
    if (SUCCEEDED(hr))
    {
        hr = pDecoderService->GetDecoderDeviceGuids(
            &cDecoderGuids, &pDecoderGuids);
    }

    if (SUCCEEDED(hr))
    {
        // Look for the decoder GUIDs we want.
        for (UINT iGuid = 0; iGuid < cDecoderGuids; iGuid++)
        {
            // Do we support this mode?
            if (!IsSupportedDecoderMode(pDecoderGuids[iGuid]))
            {
                continue;
            }

            // Find a configuration that we support. 
            hr = FindDecoderConfiguration(pDecoderService, pDecoderGuids[iGuid],
                &config, &bFoundDXVA2Configuration);
            if (FAILED(hr))
            {
                break;
            }

            if (bFoundDXVA2Configuration)
            {
                // Found a good configuration. Save the GUID and exit the loop.
                guidDecoder = pDecoderGuids[iGuid];
                break;
            }
        }
    }

    if (!bFoundDXVA2Configuration)
    {
        hr = E_FAIL; // Unable to find a configuration.
    }

    if (SUCCEEDED(hr))
    {
        // Store the things we will need later.

        SafeRelease(&m_pDecoderService);
        m_pDecoderService = pDecoderService;
        m_pDecoderService->AddRef();

        m_DecoderConfig = config;
        m_DecoderGuid = guidDecoder;
        m_hDevice = hDevice;
    }

    if (FAILED(hr))
    {
        if (hDevice != INVALID_HANDLE_VALUE)
        {
            pDeviceManager->CloseDeviceHandle(hDevice);
        }
    }

    SafeRelease(&pGetService);
    SafeRelease(&pDeviceManager);
    SafeRelease(&pDecoderService);
    return hr;
}
HRESULT CDecoder::FindDecoderConfiguration(
    /* [in] */  IDirectXVideoDecoderService *pDecoderService,
    /* [in] */  const GUID& guidDecoder, 
    /* [out] */ DXVA2_ConfigPictureDecode *pSelectedConfig,
    /* [out] */ BOOL *pbFoundDXVA2Configuration
    )
{
    HRESULT hr = S_OK;
    UINT cFormats = 0;
    UINT cConfigurations = 0;

    D3DFORMAT                   *pFormats = NULL;     // size = cFormats
    DXVA2_ConfigPictureDecode   *pConfig = NULL;      // size = cConfigurations

    // Find the valid render target formats for this decoder GUID.
    hr = pDecoderService->GetDecoderRenderTargets(
        guidDecoder,
        &cFormats,
        &pFormats
        );

    if (SUCCEEDED(hr))
    {
        // Look for a format that matches our output format.
        for (UINT iFormat = 0; iFormat < cFormats;  iFormat++)
        {
            if (pFormats[iFormat] != (D3DFORMAT)m_fccOutputFormat)
            {
                continue;
            }

            // Fill in the video description. Set the width, height, format, 
            // and frame rate.
            DXVA2_VideoDesc videoDesc = {0};

            FillInVideoDescription(&videoDesc); // Private helper function.
            videoDesc.Format = pFormats[iFormat];

            // Get the available configurations.
            hr = pDecoderService->GetDecoderConfigurations(
                guidDecoder,
                &videoDesc,
                NULL, // Reserved.
                &cConfigurations,
                &pConfig
                );

            if (FAILED(hr))
            {
                break;
            }

            // Find a supported configuration.
            for (UINT iConfig = 0; iConfig < cConfigurations; iConfig++)
            {
                if (IsSupportedDecoderConfig(pConfig[iConfig]))
                {
                    // This configuration is good.
                    *pbFoundDXVA2Configuration = TRUE;
                    *pSelectedConfig = pConfig[iConfig];
                    break;
                }
            }

            CoTaskMemFree(pConfig);
            break;

        } // End of formats loop.
    }

    CoTaskMemFree(pFormats);

    // Note: It is possible to return S_OK without finding a configuration.
    return hr;
}
```



Comme cet exemple est générique, une partie de la logique a été placée dans des fonctions d’assistance qui doivent être implémentées par le décodeur. Le code suivant illustre les déclarations de ces fonctions :


```C++
// Returns TRUE if the decoder supports a given decoding mode.
BOOL IsSupportedDecoderMode(const GUID& mode);

// Returns TRUE if the decoder supports a given decoding configuration.
BOOL IsSupportedDecoderConfig(const DXVA2_ConfigPictureDecode& config);

// Fills in a DXVA2_VideoDesc structure based on the input format.
void FillInVideoDescription(DXVA2_VideoDesc *pDesc);
```



## <a name="notifying-the-video-renderer"></a>Notification du convertisseur vidéo

Si le décodeur trouve une configuration de décodeur, l’étape suivante consiste à informer le convertisseur vidéo que le décodeur utilisera l’accélération matérielle. Vous pouvez effectuer cette étape à l’intérieur de la méthode [**CompleteConnect**](../directshow/cbaseoutputpin-completeconnect.md) . Cette étape doit se produire avant que l’allocateur soit sélectionné, car il affecte la manière dont l’allocateur est sélectionné.

1.  Interrogez la broche d’entrée du convertisseur pour l’interface [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) .
2.  Appelez [**IMFGetService :: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) pour obtenir un pointeur vers l’interface [**IDirectXVideoMemoryConfiguration**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration) . Le GUID du service est un **\_ \_ \_ service d’accélération vidéo**.
3.  Appelez [**IDirectXVideoMemoryConfiguration :: GetAvailableSurfaceTypeByIndex**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideomemoryconfiguration-getavailablesurfacetypebyindex) dans une boucle, en incrémentant la variable *dwTypeIndex* à partir de zéro. S’arrête lorsque la méthode retourne la valeur **DXVA2 \_ SurfaceType \_ DecoderRenderTarget** dans le paramètre *pdwType* . Cette étape permet de s’assurer que le convertisseur vidéo prend en charge le décodage accéléré par le matériel. Cette étape sera toujours effectuée pour le filtre EVR.
4.  Si l’étape précédente a réussi, appelez [**IDirectXVideoMemoryConfiguration :: SetSurfaceType**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideomemoryconfiguration-setsurfacetype) avec la valeur DXVA2 \_ SurfaceType \_ DecoderRenderTarget. L’appel de **SetSurfaceType** avec cette valeur met le convertisseur vidéo en mode DXVA. Quand le convertisseur vidéo est dans ce mode, le décodeur doit fournir son propre allocateur.

Le code suivant montre comment notifier le convertisseur vidéo.


```C++
HRESULT CDecoder::SetEVRForDXVA2(IPin *pPin)
{
    HRESULT hr = S_OK;

    IMFGetService                       *pGetService = NULL;
    IDirectXVideoMemoryConfiguration    *pVideoConfig = NULL;

    // Query the pin for IMFGetService.
    hr = pPin->QueryInterface(__uuidof(IMFGetService), (void**)&pGetService);

    // Get the IDirectXVideoMemoryConfiguration interface.
    if (SUCCEEDED(hr))
    {
        hr = pGetService->GetService(
            MR_VIDEO_ACCELERATION_SERVICE, IID_PPV_ARGS(&pVideoConfig));
    }

    // Notify the EVR. 
    if (SUCCEEDED(hr))
    {
        DXVA2_SurfaceType surfaceType;

        for (DWORD iTypeIndex = 0; ; iTypeIndex++)
        {
            hr = pVideoConfig->GetAvailableSurfaceTypeByIndex(iTypeIndex, &surfaceType);
            
            if (FAILED(hr))
            {
                break;
            }

            if (surfaceType == DXVA2_SurfaceType_DecoderRenderTarget)
            {
                hr = pVideoConfig->SetSurfaceType(DXVA2_SurfaceType_DecoderRenderTarget);
                break;
            }
        }
    }

    SafeRelease(&pGetService);
    SafeRelease(&pVideoConfig);

    return hr;
}
```



Si le décodeur trouve une configuration valide et notifie correctement le convertisseur vidéo, le décodeur peut utiliser DXVA pour le décodage. Le décodeur doit implémenter un allocateur personnalisé pour sa broche de sortie, comme décrit dans la section suivante.

## <a name="allocating-uncompressed-buffers"></a>Allocation de mémoires tampons non compressées

Dans DXVA 2,0, le décodeur est chargé d’allouer des surfaces Direct3D à utiliser comme mémoires tampons vidéo non compressées. Par conséquent, le décodeur doit implémenter un allocateur personnalisé qui créera les surfaces. Les exemples de média fournis par cet allocateur contiennent des pointeurs vers les surfaces Direct3D. Le EVR récupère un pointeur vers la surface en appelant [**IMFGetService :: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) sur l’exemple de média. L’identificateur de service est **un \_ \_ service de mémoire tampon Mr**.

Pour fournir l’allocateur personnalisé, procédez comme suit :

1.  Définissez une classe pour les exemples de supports. Cette classe peut dériver de la classe [**CMediaSample**](../directshow/cmediasample.md) . À l’intérieur de cette classe, procédez comme suit :
    -   Stocke un pointeur vers la surface Direct3D.
    -   Implémentez l’interface [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) . Dans la méthode [**GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) , si le GUID du service est un **\_ \_ service de mémoire tampon Mr**, interrogez la surface Direct3D pour l’interface demandée. Dans le cas contraire, **GetService** peut retourner le **\_ \_ \_ service non pris en charge MF E**.
    -   Substituez la méthode [**CMediaSample :: GetPointer**](../directshow/cmediasample-getpointer.md) pour retourner E \_ NOTIMPL.
2.  Définissez une classe pour l’allocateur. L’allocateur peut dériver de la classe [**CBaseAllocator**](../directshow/cbaseallocator.md) . Dans cette classe, procédez comme suit.
    -   Substituez la méthode [**CBaseAllocator :: Alloc**](../directshow/cbaseallocator-alloc.md) . À l’intérieur de cette méthode, appelez [**IDirectXVideoAccelerationService :: CreateSurface**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoaccelerationservice-createsurface) pour créer les surfaces. (L’interface [**IDirectXVideoDecoderService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) hérite de cette méthode de [**IDirectXVideoAccelerationService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoaccelerationservice).)
    -   Substituez la méthode [**CBaseAllocator :: Free**](../directshow/cbaseallocator-free.md) pour libérer les surfaces.
3.  Dans la broche de sortie de votre filtre, remplacez la méthode [**CBaseOutputPin :: InitAllocator**](../directshow/cbaseoutputpin-initallocator.md) . À l’intérieur de cette méthode, créez une instance de votre allocateur personnalisé.
4.  Dans votre filtre, implémentez la méthode [**CTransformFilter ::D ecidebuffersize**](../directshow/ctransformfilter-decidebuffersize.md) . Le paramètre *pProperties* indique le nombre de surfaces requises par le EVR. Ajoutez à cette valeur le nombre de surfaces nécessaires à votre décodeur et appelez [**IMemAllocator :: SetProperties**](/windows/win32/api/strmif/nf-strmif-imemallocator-setproperties) sur l’allocateur.

Le code suivant montre comment implémenter la classe d’exemple de média :


```C++
class CDecoderSample : public CMediaSample, public IMFGetService
{
    friend class CDecoderAllocator;

public:

    CDecoderSample(CDecoderAllocator *pAlloc, HRESULT *phr)
        : CMediaSample(NAME("DecoderSample"), (CBaseAllocator*)pAlloc, phr, NULL, 0),
          m_pSurface(NULL),
          m_dwSurfaceId(0)
    { 
    }

    // Note: CMediaSample does not derive from CUnknown, so we cannot use the
    //       DECLARE_IUNKNOWN macro that is used by most of the filter classes.

    STDMETHODIMP QueryInterface(REFIID riid, void **ppv)
    {
        CheckPointer(ppv, E_POINTER);

        if (riid == IID_IMFGetService)
        {
            *ppv = static_cast<IMFGetService*>(this);
            AddRef();
            return S_OK;
        }
        else
        {
            return CMediaSample::QueryInterface(riid, ppv);
        }
    }
    STDMETHODIMP_(ULONG) AddRef()
    {
        return CMediaSample::AddRef();
    }

    STDMETHODIMP_(ULONG) Release()
    {
        // Return a temporary variable for thread safety.
        ULONG cRef = CMediaSample::Release();
        return cRef;
    }

    // IMFGetService::GetService
    STDMETHODIMP GetService(REFGUID guidService, REFIID riid, LPVOID *ppv)
    {
        if (guidService != MR_BUFFER_SERVICE)
        {
            return MF_E_UNSUPPORTED_SERVICE;
        }
        else if (m_pSurface == NULL)
        {
            return E_NOINTERFACE;
        }
        else
        {
            return m_pSurface->QueryInterface(riid, ppv);
        }
    }

    // Override GetPointer because this class does not manage a system memory buffer.
    // The EVR uses the MR_BUFFER_SERVICE service to get the Direct3D surface.
    STDMETHODIMP GetPointer(BYTE ** ppBuffer)
    {
        return E_NOTIMPL;
    }

private:

    // Sets the pointer to the Direct3D surface. 
    void SetSurface(DWORD surfaceId, IDirect3DSurface9 *pSurf)
    {
        SafeRelease(&m_pSurface);

        m_pSurface = pSurf;
        if (m_pSurface)
        {
            m_pSurface->AddRef();
        }

        m_dwSurfaceId = surfaceId;
    }

    IDirect3DSurface9   *m_pSurface;
    DWORD               m_dwSurfaceId;
};
```



Le code suivant montre comment implémenter la méthode [**Alloc**](../directshow/cbaseallocator-alloc.md) sur l’allocateur.


```C++
HRESULT CDecoderAllocator::Alloc()
{
    CAutoLock lock(this);

    HRESULT hr = S_OK;

    if (m_pDXVA2Service == NULL)
    {
        return E_UNEXPECTED;
    }

    hr = CBaseAllocator::Alloc();

    // If the requirements have not changed, do not reallocate.
    if (hr == S_FALSE)
    {
        return S_OK;
    }

    if (SUCCEEDED(hr))
    {
        // Free the old resources.
        Free();

        // Allocate a new array of pointers.
        m_ppRTSurfaceArray = new (std::nothrow) IDirect3DSurface9*[m_lCount];
        if (m_ppRTSurfaceArray == NULL)
        {
            hr = E_OUTOFMEMORY;
        }
        else
        {
            ZeroMemory(m_ppRTSurfaceArray, sizeof(IDirect3DSurface9*) * m_lCount);
        }
    }

    // Allocate the surfaces.
    if (SUCCEEDED(hr))
    {
        hr = m_pDXVA2Service->CreateSurface(
            m_dwWidth,
            m_dwHeight,
            m_lCount - 1,
            (D3DFORMAT)m_dwFormat,
            D3DPOOL_DEFAULT,
            0,
            DXVA2_VideoDecoderRenderTarget,
            m_ppRTSurfaceArray,
            NULL
            );
    }

    if (SUCCEEDED(hr))
    {
        for (m_lAllocated = 0; m_lAllocated < m_lCount; m_lAllocated++)
        {
            CDecoderSample *pSample = new (std::nothrow) CDecoderSample(this, &hr);

            if (pSample == NULL)
            {
                hr = E_OUTOFMEMORY;
                break;
            }
            if (FAILED(hr))
            {
                break;
            }
            // Assign the Direct3D surface pointer and the index.
            pSample->SetSurface(m_lAllocated, m_ppRTSurfaceArray[m_lAllocated]);

            // Add to the sample list.
            m_lFree.Add(pSample);
        }
    }

    if (SUCCEEDED(hr))
    {
        m_bChanged = FALSE;
    }
    return hr;
}
```



Voici le code de la méthode [**Free**](../directshow/cbaseallocator-free.md) :


```C++
void CDecoderAllocator::Free()
{
    CMediaSample *pSample = NULL;

    do
    {
        pSample = m_lFree.RemoveHead();
        if (pSample)
        {
            delete pSample;
        }
    } while (pSample);

    if (m_ppRTSurfaceArray)
    {
        for (long i = 0; i < m_lAllocated; i++)
        {
            SafeRelease(&m_ppRTSurfaceArray[i]);
        }

        delete [] m_ppRTSurfaceArray;
    }
    m_lAllocated = 0;
}
```



Pour plus d’informations sur l’implémentation d’allocators personnalisés, consultez la rubrique [fournissant un allocateur personnalisé](../directshow/providing-a-custom-allocator.md) dans la documentation du kit de développement logiciel (SDK) DirectShow.

## <a name="decoding"></a>Décodage

Pour créer l’appareil de décodage, appelez [**IDirectXVideoDecoderService :: CreateVideoDecoder**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-createvideodecoder). La méthode retourne un pointeur vers l’interface [**IDirectXVideoDecoder**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder) de l’appareil décodeur.

Sur chaque frame, appelez [**IDirect3DDeviceManager9 :: TestDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-testdevice) pour tester le handle de l’appareil. Si l’appareil a changé, la méthode retourne DXVA2 \_ E \_ New \_ Video \_ Device. Si cela se produit, procédez comme suit :

1.  Fermez le handle d’appareil en appelant [**IDirect3DDeviceManager9 :: CloseDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-closedevicehandle).
2.  Libérez les pointeurs [**IDirectXVideoDecoderService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) et [**IDirectXVideoDecoder**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder) .
3.  Ouvrez un nouveau descripteur d’appareil.
4.  Négocier une nouvelle configuration de décodeur, comme décrit dans la section [recherche d’une configuration de décodeur](#finding-a-decoder-configuration).
5.  Créez un appareil de décodage.

En supposant que le descripteur de l’appareil est valide, le processus de décodage fonctionne comme suit :

1.  Appelez [**IDirectXVideoDecoder :: BeginFrame**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-beginframe).
2.  Effectuez les opérations suivantes une ou plusieurs fois :
    1.  Appelez [**IDirectXVideoDecoder :: GetBuffer**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-getbuffer) pour obtenir une mémoire tampon de décodeur DXVA.
    2.  Remplir la mémoire tampon.
    3.  Appelez [**IDirectXVideoDecoder :: ReleaseBuffer**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-releasebuffer).
3.  Appelez [**IDirectXVideoDecoder :: Execute**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute) pour effectuer les opérations de décodage sur le frame.

DXVA 2,0 utilise les mêmes structures de données que DXVA 1,0 pour les opérations de décodage. Pour l’ensemble initial de profils DXVA (pour H. 261, H. 263 et MPEG-2), ces structures de données sont décrites dans la [spécification DXVA 1,0](/windows-hardware/drivers/display/directx-video-acceleration).

Au sein de chaque paire d’appels [**BeginFrame**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-beginframe) / [**Execute**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute) , vous pouvez appeler [**GetBuffer**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-getbuffer) plusieurs fois, mais une seule fois pour chaque type de mémoire tampon DXVA. Si vous l’appelez deux fois avec le même type de mémoire tampon, vous allez remplacer les données.

Après l’appel de l' [**instruction EXECUTE**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute), appelez [**IMemInputPin :: Receive**](/windows/win32/api/strmif/nf-strmif-imeminputpin-receive) pour remettre le frame au convertisseur vidéo, comme avec le décodage logiciel. La méthode **Receive** est asynchrone ; une fois retourné, le décodeur peut continuer à décoder le frame suivant. Le pilote d’affichage empêche les commandes de décodage de remplacer la mémoire tampon pendant que la mémoire tampon est en cours d’utilisation. Le décodeur ne doit pas réutiliser une surface pour décoder une autre image tant que le convertisseur n’a pas libéré l’exemple. Quand le convertisseur libère l’exemple, l’allocateur remet l’échantillon dans son pool d’exemples disponibles. Pour accéder à l’exemple disponible suivant, appelez [**CBaseOutputPin :: GetDeliveryBuffer**](../directshow/cbaseoutputpin-getdeliverybuffer.md), qui à son tour appelle [**IMemAllocator :: GetBuffer**](/windows/win32/api/strmif/nf-strmif-imemallocator-getbuffer). Pour plus d’informations, consultez la rubrique [vue d’ensemble du Data Flow dans DirectShow](../directshow/overview-of-data-flow-in-directshow.md) dans la documentation DirectShow.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Accélération vidéo DirectX 2,0](directx-video-acceleration-2-0.md)
</dt> </dl>

 

 
