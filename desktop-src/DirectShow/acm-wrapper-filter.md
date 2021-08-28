---
description: Filtre de wrappers ACM
ms.assetid: f3cd8e90-8949-482a-8ada-47711f6c935f
title: Filtre de wrappers ACM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f0688150ab417c6ebb71313a438f72ef7839042
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122985352"
---
# <a name="acm-wrapper-filter"></a>Filtre de wrappers ACM

Le filtre de wrapper ACM permet aux codecs du gestionnaire de compression audio (ACM) de joindre un graphique de filtre. Il peut agir soit comme filtre de décompression, soit comme filtre de compression.

en tant que filtre de décompression, le Wrapper ACM apparaît dans la catégorie « filtres de DirectShow » (CLSID \_ LegacyAmFilterCategory) et a un mérite de mérite \_ NORMAL. Le type de support de connexion sur la broche d’entrée détermine le codec utilisé par le filtre. En règle générale, l’application n’a pas besoin d’ajouter le filtre au graphique de filtre ; elle est automatiquement extraite par le gestionnaire de Graph de filtre quand cela est nécessaire. La décompression concerne uniquement les signaux audio PCM.

En tant que filtre de compression, le wrapper ACM apparaît dans la catégorie « compresseurs audio » (CLSID \_ AudioCompressorCategory) et a un mérite de mérite \_ n' \_ \_ utilise pas. Chaque codec s’affiche sous la forme d’une instance distincte. Pour la compression, vous ne pouvez pas créer directement le filtre avec CoCreateInstance. Au lieu de cela, vous devez utiliser l’énumérateur du périphérique système. Pour plus d’informations, consultez [utilisation de l’énumérateur de périphérique système](using-the-system-device-enumerator.md).




| Étiquette | Valeur |
|--------|-------|
| Interfaces de filtre | <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, IPersist, IPersistPropertyBag | 
| Types de média de broche d’entrée | MEDIATYPE_Audio, MEDIASUBTYPE_NULL FORMAT_WaveFormatEx | 
| Interfaces pin d’entrée | <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPIN</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | 
| Types de média de broche de sortie | MEDIATYPE_Audio, MEDIASUBTYPE_PCM FORMAT_WaveFormatEx. les combinaisons suivantes sont possibles :<br /><ul><li>Échantillons par seconde (kHz) : 44,1, 22,05, 11,025 ou 8,0.</li><li>Canaux : stéréo ou mono.</li><li>Bits par échantillon : 8 ou 16.</li></ul> | 
| Interfaces de broche de sortie | <a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig"><strong>IAMStreamConfig</strong></a>, <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPIN</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | 
| CLSID du filtre | CLSID_ACMWrapper | 
| CLSID de page de propriétés | Aucune page de propriétés. | 
| Exécutable | Quartz.dll | 
| <a href="merit.md">Mérite</a> | MERIT_NORMAL ou MERIT_DO_NOT_USE | 
| <a href="filter-categories.md">Catégorie de filtre</a> | CLSID_LegacyAmFilterCategory ou CLSID_AudioCompressorCategory | 




 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[DirectShow Filtres](directshow-filters.md)
</dt> </dl>

 

 




