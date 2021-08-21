---
description: utilisation du filtre EVR DirectShow
ms.assetid: 4d85aed0-4b11-4c5f-bfc0-cad0a7d2f490
title: utilisation du filtre EVR DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bc454b6d298546afdbb5a06b7081505d9ddd7c2ab87a816e79bdb13836e9a51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118737312"
---
# <a name="using-the-directshow-evr-filter"></a>utilisation du filtre EVR DirectShow

Pour créer le filtre EVR (Enhanced Video Renderer), appelez **CoCreateInstance**. Le CLSID est CLSID \_ EnhancedVideoRenderer, défini dans UUID. h. Vous n’avez pas besoin d’appeler [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) ou [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) pour utiliser le filtre EVR.

pour plus d’informations sur l’utilisation du filtre EVR dans une application DirectShow, consultez [lecture Audio/vidéo dans DirectShow](../directshow/audio-video-playback-in-directshow.md).

Le filtre EVR commence par une broche d’entrée, qui correspond au flux de référence. Pour ajouter des codes confidentiels pour les sous-flux, interrogez le filtre de l’interface [**IEVRFilterConfig**](/windows/desktop/api/evr/nn-evr-ievrfilterconfig) et appelez [**IEVRFilterConfig :: SetNumberOfStreams**](/windows/desktop/api/evr/nf-evr-ievrfilterconfig-setnumberofstreams). Appelez cette méthode avant de connecter des broches d’entrée. La broche 0 est toujours le flux de référence. Connecter ce code pin avant tout autre pin, car le format du flux de référence peut limiter les formats de sous-flux disponibles.

Avant de démarrer le graphique, définissez la fenêtre de découpage vidéo et le rectangle de destination. Pour plus d’informations, consultez [utilisation des contrôles d’affichage vidéo](using-the-video-display-controls.md).

Contrairement au convertisseur de mixage vidéo (VMR), le EVR n’a pas de modes opérationnels (fenêtre, sans fenêtre, etc.). En particulier :

-   EVR ne prend pas en charge le mode fenêtre. L’application doit fournir la fenêtre de découpage.
-   Le EVR n’a pas de mode sans rendu. Pour remplacer le présentateur par défaut, appelez [**IMFVideoRenderer :: InitializeRenderer**](/windows/desktop/api/evr/nf-evr-imfvideorenderer-initializerenderer).
-   Le EVR n’a pas de mode de mélange. Le EVR crée toujours le mélangeur. Si vous avez un flux d’entrée, il n’est pas nécessaire d’appeler [**SetNumberOfStreams**](/windows/desktop/api/evr/nf-evr-ievrfilterconfig-setnumberofstreams) pour forcer le EVR à utiliser le mélangeur.

## <a name="filter-interfaces"></a>Interfaces de filtre

Le filtre EVR expose les interfaces suivantes. certaines de ces interfaces sont documentées dans le kit de développement logiciel (SDK) DirectShow. Utilisez **QueryInterface** pour récupérer les pointeurs vers ces interfaces :

-   [**IAMCertifiedOutputProtection**](/windows/win32/api/strmif/nn-strmif-iamcertifiedoutputprotection) (DirectShow)
-   [**IAMFilterMiscFlags**](/windows/win32/api/strmif/nn-strmif-iamfiltermiscflags) (DirectShow)
-   [**IBaseFilter**](/windows/win32/api/strmif/nn-strmif-ibasefilter) (DirectShow)
-   [**IEVRFilterConfig**](/windows/desktop/api/evr/nn-evr-ievrfilterconfig)
-   [**IKsPropertySet**](../directshow/ikspropertyset.md) (DirectShow)
-   [**IMediaEventSink**](/windows/win32/api/strmif/nn-strmif-imediaeventsink) (DirectShow)
-   [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   [**IMFVideoPositionMapper**](/windows/desktop/api/evr/nn-evr-imfvideopositionmapper)
-   [**IMFVideoRenderer**](/windows/desktop/api/evr/nn-evr-imfvideorenderer)
-   **IPersistStream**
-   [**IQualityControl**](/windows/win32/api/strmif/nn-strmif-iqualitycontrol) (DirectShow)
-   [**IQualProp**](/previous-versions/windows/desktop/api/amvideo/nn-amvideo-iqualprop) (DirectShow)
-   **ISpecifyPropertyPages**

## <a name="input-pin-interfaces"></a>Interfaces pin d’entrée

Les broches d’entrée sur le filtre EVR exposent les interfaces suivantes. Utilisez **QueryInterface** pour récupérer les pointeurs vers ces interfaces :

-   [**IEVRVideoStreamControl**](/windows/desktop/api/evr9/nn-evr9-ievrvideostreamcontrol)
-   [**IMemInputPin**](/windows/win32/api/strmif/nn-strmif-imeminputpin) (DirectShow)
-   [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   [**IPIN**](/windows/win32/api/strmif/nn-strmif-ipin) (DirectShow)
-   [**IQualityControl**](/windows/win32/api/strmif/nn-strmif-iqualitycontrol) (DirectShow)

En outre, vous pouvez utiliser l’interface [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) pour récupérer l’interface suivante :

-   [**IDirectXVideoMemoryConfiguration**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Lecture audio/vidéo en DirectShow](../directshow/audio-video-playback-in-directshow.md)
</dt> <dt>

[Convertisseur vidéo amélioré](enhanced-video-renderer.md)
</dt> </dl>

 

 
