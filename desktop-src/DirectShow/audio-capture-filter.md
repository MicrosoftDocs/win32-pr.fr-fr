---
description: Filtre de capture audio
ms.assetid: f76d5c82-33b2-4579-9420-8f97eca53ede
title: Filtre de capture audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73da50653a4a159d30a6ca1b83ebc1f37a6de42c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747260"
---
# <a name="audio-capture-filter"></a>Filtre de capture audio

Le filtre de capture audio représente un périphérique de capture audio. Il possède une broche de sortie de capture et plusieurs broches d’entrée (une pour chaque type d’entrée sur la carte, par exemple ligne in, MIC, CD et MIDI).

Ce filtre peut fonctionner avec plusieurs périphériques matériels. par conséquent, l’appel de CoCreateInstance pour créer le filtre ne fonctionne pas. Utilisez plutôt l' [énumérateur du périphérique système](system-device-enumerator.md). L’énumérateur de périphérique système retourne un moniker unique pour chaque appareil. Le nom convivial du moniker correspond au nom de l’appareil. (Il s’agit du nom qui s’affiche dans GraphEdit.) Pour plus d’informations, consultez [énumération des appareils et des filtres](enumerating-devices-and-filters.md).



|                                          |                                                                                                                                                                                                                                                                                                    |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces de filtre                        | [**IAMAudioInputMixer**](/windows/desktop/api/Strmif/nn-strmif-iamaudioinputmixer), [**IAMFilterMiscFlags**](/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags), [**IAMResourceControl**](/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), IPersistPropertyBag, ISpecifyPropertyPages                                                               |
| Types de média de broche d’entrée                    | MEDIATYPE \_ AnalogAudio, MEDIASUBTYPE \_ null                                                                                                                                                                                                                                                         |
| Interfaces pin d’entrée                     | [**IAMAudioInputMixer**](/windows/desktop/api/Strmif/nn-strmif-iamaudioinputmixer), [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                                                           |
| Types de média de broche de sortie                   | MEDIATYPE \_ audio, MEDIASUBTYPE \_ null                                                                                                                                                                                                                                                               |
| Interfaces de broche de sortie                    | [**IAMBufferNegotiation**](/windows/desktop/api/Strmif/nn-strmif-iambuffernegotiation), [**IAMPushSource**](/windows/desktop/api/Strmif/nn-strmif-iampushsource), [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol), [**IKsPropertySet**](ikspropertyset.md), [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| CLSID du filtre                             | Non applicable                                                                                                                                                                                                                                                                                     |
| CLSID de page de propriétés                      | CLSID \_ AudioInputMixerProperties                                                                                                                                                                                                                                                                   |
| Exécutable                               | qcap.dll                                                                                                                                                                                                                                                                                           |
| [Mérite](merit.md)                       | MÉRITE \_ n' \_ \_ utilise pas                                                                                                                                                                                                                                                                                |
| [Catégorie de filtre](filter-categories.md) | CLSID \_ AudioInputDeviceCategory                                                                                                                                                                                                                                                                    |



 

## <a name="remarks"></a>Notes

Les broches d’entrée représentent des connexions matérielles physiques et ne sont jamais connectées à d’autres filtres dans DirectShow.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Filtres DirectShow](directshow-filters.md)
</dt> <dt>

[Capture audio](audio-capture.md)
</dt> </dl>

 

 



