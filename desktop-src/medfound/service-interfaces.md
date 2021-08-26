---
description: Interfaces de service
ms.assetid: 264a0e86-49e9-4777-956b-a83e9db52a25
title: Interfaces de service
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d99155eb5cfb8c435281a5f23567759931cc53fae3743d9c76ce7be75f68c380
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060410"
---
# <a name="service-interfaces"></a>Interfaces de service

Certaines interfaces dans Media Foundation doivent être obtenues en appelant [**IMFGetService :: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) au lieu de en appelant **QueryInterface**. La méthode [**GetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) fonctionne comme QueryInterface, mais avec les différences suivantes :

-   Il prend un GUID d’identificateur de service en plus de l’identificateur d’interface.
-   Elle peut retourner un pointeur vers un autre objet qui implémente l’interface, au lieu de retourner un pointeur vers l’objet d’origine interrogé.

> [!Note]  
> L’interface [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) est très similaire à l’interface **IServiceProvider** utilisée dans d’autres API.

 

Un *service* est une interface particulière obtenue à partir d’une classe particulière d’objets par le biais de l’interface [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) . Les services suivants sont définis.



| Identificateur de service                          | Interface                                                                                                                                | Objets susceptibles d’exposer ce service                                                                                                            |
|---------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| \_service de fournisseur de métadonnées MF \_ \_             | [**IMFMetadataProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider)                                                                                       | Sources multimédias                                                                                                                                     |
| \_service MF MEDIASOURCE \_                    | [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)                                                                                                 | pris en charge dans Windows 8.1 et versions ultérieures.<br/>                                                                                                    |
| \_contexte du \_ serveur \_ PMP MF                    | [**IMFPMPServer**](/windows/desktop/api/mfidl/nn-mfidl-imfpmpserver)                                                                                                     | Session de média du chemin d’accès au média (PMP) protégé.                                                                                                         |
| \_services de qualité MF \_                       | [**IMFQualityAdvise**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)                                                                                             | Sources multimédias.                                                                                                                                    |
| SERVICE de contrôle de la \_ fréquence MF \_ \_                  | [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)                                                                                                 | Sources multimédias, session multimédia                                                                                                                      |
| SERVICE de contrôle de la \_ fréquence MF \_ \_                  | [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)                                                                                                 | Sources multimédias, récepteurs multimédia, session multimédia                                                                                                         |
| \_proxy distant \_ MF                           | [**IMFRemoteProxy**](/windows/desktop/api/mfidl/nn-mfidl-imfremoteproxy)                                                                                                 | Proxies pour les objets distants.                                                                                                                       |
| \_service sami \_ MF                           | [**IMFSAMIStyle**](/windows/desktop/api/mfidl/nn-mfidl-imfsamistyle)                                                                                                     | Source de média SAMI (Synchronized Accessible Media Interchange).                                                                                    |
| \_service de \_ fournisseur de présentation source \_ MF \_ | [**IMFMediaSourcePresentationProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcepresentationprovider)                                                         | Source de Sequencer                                                                                                                                  |
| \_service de code temporel MF \_                       | [**IMFTimecodeTranslate**](/windows/desktop/api/mfidl/nn-mfidl-imftimecodetranslate)                                                                                     | Source du média ASF.                                                                                                                                 |
| SERVICE de l’éditeur d’attributs MF \_ TOPONODE \_ \_ \_    | [**IMFTopologyNodeAttributeEditor**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynodeattributeeditor)                                                                 | Session multimédia                                                                                                                                     |
| \_objet encapsulé \_ MF                         | [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)                                                                                                   | Objets encapsulés                                                                                                                                   |
| \_service de \_ mémoire tampon encapsulé MF \_                |                                                                                                                                          | pris en charge dans Windows 8.1 et versions ultérieures.<br/>                                                                                                    |
| \_exemple de \_ \_ service MF encapsulé                 |                                                                                                                                          | pris en charge dans Windows 8.1 et versions ultérieures.<br/>                                                                                                    |
| \_services WORKQUEUE \_ MF                     | [**IMFWorkQueueServices**](/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices)                                                                                     | Session multimédia                                                                                                                                     |
| \_service MFNET SAVEJOB \_                     | [**IMFSaveJob**](/windows/desktop/api/mfidl/nn-mfidl-imfsavejob)                                                                                                         | Flux d’octets                                                                                                                                      |
| \_service de statistiques MFNETSOURCE \_            | **IPropertyStore**                                                                                                                       | Source réseau. Utilisez ce service pour récupérer des statistiques réseau. Consultez [**la \_ propriété MFNETSOURCE Statistics**](mfnetsource-statistics-property.md). |
| \_service de \_ stratégie \_ audio Mr                  | [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy)                                                                                                 | Convertisseur audio                                                                                                                                    |
| \_service de mémoire tampon Mr \_                         | **IDirect3DSurface9**                                                                                                                    | Mémoires tampons de surface DirectX                                                                                                                           |
| SERVICE de volume de la \_ stratégie de capture RM \_ \_ \_        | [**IMFSimpleAudioVolume**](/windows/desktop/api/mfidl/nn-mfidl-imfsimpleaudiovolume)                                                                                     | Source de capture audio                                                                                                                              |
| \_service de \_ volume de stratégie Mr \_                 | [**IMFSimpleAudioVolume**](/windows/desktop/api/mfidl/nn-mfidl-imfsimpleaudiovolume)                                                                                     | Convertisseur audio                                                                                                                                    |
| \_service de \_ volume de flux Mr \_                 | [**IMFAudioStreamVolume**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiostreamvolume)                                                                                     | Convertisseur audio                                                                                                                                    |
| \_ \_ service accélérateur vidéo \_ Mr            | [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9), [ **IDirectXVideoAccelerationService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoaccelerationservice) | Rendu vidéo amélioré (EVR)                                                                                                                     |
| \_ \_ service accélérateur vidéo \_ Mr            | [**IDirectXVideoMemoryConfiguration**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration)                                                             | épingles d’entrée sur le filtre EVR DirectShow                                                                                                           |
| \_ \_ service accélérateur vidéo \_ Mr            | [**Interface IMFVideoSampleAllocator**](/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocator)                                                                     | Récepteurs de flux EVR.                                                                                                                                 |
| \_service de \_ mixage \_ vidéo Mr                   | Différentes interfaces exposées par le mélangeur EVR. consultez [utilisation des contrôles Video Mixer](using-the-video-mixer-controls.md).                   | EVR                                                                                                                                               |
| \_service de \_ rendu \_ vidéo Mr                  | Différentes interfaces exposées par le présentateur EVR. Consultez [utilisation des contrôles d’affichage vidéo](using-the-video-display-controls.md).           | EVR                                                                                                                                               |



 

Vous devez utiliser [**GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) pour récupérer les interfaces listées dans ce tableau à partir des objets listés dans ce tableau.

Dans certains cas, une interface est retournée en tant que service par une classe d’objets et retournée via **QueryInterface** par une autre classe d’objets. Les pages de référence pour chaque interface indiquent quand utiliser [**GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) et quand utiliser **QueryInterface**.

> [!Caution]  
> Un objet peut être implémenté de manière à retourner une interface de service via **QueryInterface** et [**GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice). Toutefois, l’utilisation de **QueryInterface** quand **GetService** est requis peut entraîner des problèmes de compatibilité plus tard.

 

La fonction [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) est une fonction d’assistance qui interroge un objet pour [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) , puis appelle la méthode [**GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) de l’objet.

## <a name="examples"></a>Exemples

L’exemple suivant interroge la session multimédia pour [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) et obtient l’interface [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) .


```C++
IMFGetService *pGetService = NULL;
IMFRateControl *pRateControl = NULL;
HRESULT hr = S_OK;

hr = pMediaSession->QueryInterface(
    IID_IMFGetService, 
    (void**)&pGetService);

if (SUCCEEDED(hr))
{
    hr = pGetService->GetService(
        MF_RATE_CONTROL_SERVICE, 
        IID_IMFRateControl,
        (void**)&pRateControl);
}
if (SUCCEEDED(hr))
{
    // Use IMFRateControl. (Not shown.)
}

// Clean up.
SAFE_REELEASE(pGetService);
SAFE_RELEASE(pRateControl);
```



L’exemple suivant est équivalent à l’exemple précédent, mais utilise la fonction [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) .


```C++
IMFRateControl *pRateControl = NULL;
HRESULT hr = S_OK;

hr = MFGetService(
    pMediaSession, 
    MF_RATE_CONTROL_SERVICE, 
    IID_IMFRateControl, 
    (void**) &pRateCtl 
); 
if (SUCCEEDED(hr))
{
    // Use IMFRateControl. (Not shown.)
}

// Clean up.
SAFE_RELEASE(pRateControl);
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Interface IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
</dt> <dt>

[API de plateforme Media Foundation](media-foundation-platform-apis.md)
</dt> </dl>

 

 




