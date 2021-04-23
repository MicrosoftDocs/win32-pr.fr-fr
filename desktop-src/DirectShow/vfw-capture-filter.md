---
description: Filtre de capture VFW
ms.assetid: 663b6b3b-2a50-4586-9506-600a59869abe
title: Filtre de capture VFW
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1eadc2c8a22ed6e00ff76d79a0b7ce2db012abb4
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908397"
---
# <a name="vfw-capture-filter"></a>Filtre de capture VFW

Ce filtre fonctionne avec l’ancien matériel de capture vidéo qui utilise la vidéo pour Windows.

Ce filtre a deux broches de sortie. L’une est appelée capture et l’autre est appelée aperçu ou superposition.



| Étiquette | Valeur |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces de filtre                        | **IPersistPropertyBag**, [**IAMVfwCaptureDialogs**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcapturedialogs), [**IAMFilterMiscFlags**](/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), **ISpecifyPropertyPages**, [**IOverlayNotify**](/windows/desktop/api/Strmif/nn-strmif-ioverlaynotify)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Types de média de broche d’entrée                    | Non applicable.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Interfaces pin d’entrée                     | Non applicable.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Types de média de broche de sortie                   | Capture : \_ vidéo MediaType, MEDIASUBTYPE \_ null, format \_ VideoInfoOverlay : MediaType \_ Video, MEDIASUBTYPE \_ Overlay, format \_ videoinfo<br/> Aperçu : \_ vidéo MediaType, MEDIASUBTYPE \_ null, format \_ videoinfo<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Interfaces de broche de sortie                    | Code PIN de capture : [**IAMBufferNegotiation**](/windows/desktop/api/Strmif/nn-strmif-iambuffernegotiation), [**IAMDroppedFrames**](/windows/desktop/api/Strmif/nn-strmif-iamdroppedframes), [**IAMPushSource**](/windows/desktop/api/Strmif/nn-strmif-iampushsource), [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol), [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression), [**IKsPropertySet**](ikspropertyset.md), [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)Overlay pin : [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol), [**IKsPropertySet**](ikspropertyset.md), [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/> Pin de l’aperçu : [**IAMPushSource**](/windows/desktop/api/Strmif/nn-strmif-iampushsource), [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol), [**IKsPropertySet**](ikspropertyset.md), [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/> |
| CLSID du filtre                             | CLSID \_ VfwCapture                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| CLSID de page de propriétés                      | CLSID \_ CaptureProperties                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Exécutable                               | qcap.dll                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [Mérite](merit.md)                       | MÉRITE \_ n' \_ \_ utilise pas                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [Catégorie de filtre](filter-categories.md) | CLSID \_ VideoInputDeviceCategory                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |



 

## <a name="remarks"></a>Remarques

Bien que le code confidentiel de capture expose l’interface [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) , seules les méthodes **SetFormat** et **GetFormat** sont implémentées pour cette interface.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Filtres DirectShow](directshow-filters.md)
</dt> <dt>

[Capture vidéo](video-capture.md)
</dt> </dl>

 

 




