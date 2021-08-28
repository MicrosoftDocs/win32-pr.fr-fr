---
description: Filtre de convertisseur audio (WaveOut)
ms.assetid: a3f2776b-974b-4886-82a3-38e00b607a07
title: Filtre de convertisseur audio (WaveOut)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d66d92357b41b6fa23018acf6d44b966eb77fab
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987652"
---
# <a name="audio-renderer-waveout-filter"></a>Filtre de convertisseur audio (WaveOut)

Ce filtre utilise l' \* API WaveOut pour restituer l’audio de forme d’onde. Toutefois, le [filtre de convertisseur DirectSound](directsound-renderer-filter.md) fournit les mêmes fonctionnalités à l’aide de DirectSound. par défaut, le gestionnaire de Graph de filtre utilise le convertisseur DirectSound à la place de ce filtre. Le mixage audio est désactivé dans le convertisseur audio waveOut. par conséquent, si vous devez mélanger plusieurs flux audio pendant la lecture, utilisez le convertisseur DirectSound.

Ce filtre ne vérifie pas le sous-type du flux audio. La structure [**WaveFormat**](/windows/win32/api/mmreg/ns-mmreg-waveformat) ou [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) passée dans le format contient les informations nécessaires à la connexion.

Ce filtre prend en charge une plage de taux d’échantillonnage qui dépend du pilote audio.




| Étiquette | Valeur |
|--------|-------|
| Interfaces de filtre | <ul><li><a href="/windows/desktop/api/Strmif/nn-strmif-iamaudiorendererstats"><strong>IAMAudioRendererStats</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-iamclockslave"><strong>IAMClockSlave</strong></a></li><li><a href="/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound"><strong>IAMDirectSound</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol"><strong>IAMResourceControl</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></li><li><a href="/windows/desktop/api/Control/nn-control-ibasicaudio"><strong>IBasicAudio</strong></a></li><li><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></li><li>IPersistPropertyBag</li><li>IPersistStream</li><li><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ireferenceclock"><strong>IReferenceClock</strong></a></li></ul> | 
| Types de média de broche d’entrée | <strong>MEDIATYPE_Audio</strong> | 
| Interfaces pin d’entrée | <ul><li><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></li></ul> | 
| Types de média de broche de sortie | Non applicable. | 
| Interfaces de broche de sortie | Non applicable. | 
| CLSID du filtre | <strong>CLSID_AudioRender</strong> | 
| CLSID de page de propriétés | <strong>CLSID_AudioProperties</strong>, <strong>CLSID_AudioRendererAdvancedProperties</strong> | 
| Exécutable | quartz.dll | 
| <a href="merit.md">Mérite</a> | <strong>MERIT_DO_NOT_USE</strong> | 
| <a href="filter-categories.md">Catégorie de filtre</a> | <strong>CLSID_AudioRendererCategory</strong> | 




 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[DirectShow Filtres](directshow-filters.md)
</dt> </dl>

 

 
