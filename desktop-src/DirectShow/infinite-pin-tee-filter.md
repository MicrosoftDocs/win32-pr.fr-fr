---
description: Filtre tee de code confidentiel infini
ms.assetid: 5f3e06ec-adee-4bc7-8ea8-cce3030d3baa
title: Filtre tee de code confidentiel infini
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3433a0c2f5fe55fa59c42ed6e02d34f6e2cf0e6d
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909227"
---
# <a name="infinite-pin-tee-filter"></a>Filtre tee de code confidentiel infini

Ce filtre remet les exemples livrés à sa broche d’entrée à un nombre variable de broches de sortie. Lorsqu’une instance du filtre est créée, elle possède une broche de sortie. Chaque fois qu’une broche de sortie est connectée, le filtre crée une autre broche de sortie. Toutes les broches de sortie partagent le même type de support que la broche d’entrée.

Une version de ce filtre est également fournie en tant qu’exemple de kit de développement logiciel (SDK). Consultez [exemple de filtre InfTee](inftee-filter-sample.md).



| Étiquette | Valeur |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces de filtre                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                                                                 |
| Types de média de broche d’entrée                    | Tout type de média                                                                                                                                     |
| Interfaces pin d’entrée                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                             |
| Types de média de broche de sortie                   | Tout type de média. Le type de sortie correspond toujours au type d’entrée, pour toutes les broches de sortie                                                                 |
| Interfaces de broche de sortie                    | [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| CLSID du filtre                             | CLSID \_ InfTee                                                                                                                                      |
| CLSID de page de propriétés                      | Aucune page de propriétés                                                                                                                                   |
| Exécutable                               | qcap.dll                                                                                                                                           |
| [Mérite](merit.md)                       | MÉRITE \_ n' \_ \_ utilise pas                                                                                                                                |
| [Catégorie de filtre](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                                                      |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Filtres DirectShow](directshow-filters.md)
</dt> </dl>

 

 



