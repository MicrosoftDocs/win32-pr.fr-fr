---
description: Filtre de l’analyseur MIDI
ms.assetid: a56576ad-f949-48fa-85e0-3e9898d2970d
title: Filtre de l’analyseur MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c5907c36e668a39494b46ec6bbc67e4d8cb4870357df9c1f0303c882bc86f0d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119256509"
---
# <a name="midi-parser-filter"></a>Filtre de l’analyseur MIDI

Le filtre de l’analyseur MIDI lit les données MIDI qui se trouvent dans. MID et. Fichiers RMI. Le filtre accepte un flux à partir de la source du [fichier Async](file-source--async--filter.md) ou des filtres de la [source du fichier URL](file-source--url--filter.md) et génère des échantillons midi dans le [**Convertisseur midi**](midi-renderer-filter.md) pour la lecture.



| Étiquette | Valeur |
|------------------------------------------|----------------------------------------------------------------------------------------------------------|
| Interfaces de filtre                        | [**IAMMediaContent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent), [ **IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                           |
| Types de média de broche d’entrée                    | \_Flux de MediaType, MEDIASUBTYPE \_ midi                                                                    |
| Interfaces pin d’entrée                     | [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin), [ **IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                         |
| Types de média de broche de sortie                   | \_Midi MediaType, MEDIASUBTYPE \_ null                                                                      |
| Interfaces de broche de sortie                    | [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol), [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin) |
| CLSID du filtre                             | CLSID \_ MIDIParser                                                                                        |
| CLSID de page de propriétés                      | Aucune page de propriétés                                                                                         |
| Exécutable                               | quartz.dll                                                                                               |
| [Mérite](merit.md)                       | MÉRITE \_ improbable                                                                                          |
| [Catégorie de filtre](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                            |



 

## <a name="remarks"></a>Remarques

Pour plus d’informations, consultez la page relative au [**Convertisseur midi**](midi-renderer-filter.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[DirectShow Filtres](directshow-filters.md)
</dt> </dl>

 

 



