---
description: Filtre Tuner TV
ms.assetid: a8e101dc-78ab-495f-9086-7b1d1e87c357
title: Filtre Tuner TV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b101dfcce4877570a2072d9e4c116466223e56889fb5e66de3e6ef0ec24afad6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015517"
---
# <a name="tv-tuner-filter"></a>Filtre Tuner TV

Le filtre Tuner TV sélectionne une diffusion analogique ou un canal câblé à afficher. Le flux de sortie unique est un chemin d’accès matériel pour la vidéo de bande de streaming analogique. Cette sortie doit se connecter au filtre de la vidéo analogique. Les broches d’entrée incluent une entrée pour Cable et une entrée d’antenne.



| Étiquette | Valeur |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces de filtre                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IAMTVTuner**](/windows/desktop/api/Strmif/nn-strmif-iamtvtuner), **ISpecifyPropertyPages**, **IPersistPropertyBag**, **IKsObject**, [**IKsPropertySet**](ikspropertyset.md) |
| Types de média de broche d’entrée                    | Non applicable.                                                                                                                                                                   |
| Interfaces pin d’entrée                     | Non applicable.                                                                                                                                                                   |
| Types de média de broche de sortie                   | Vidéo : MEDIATYPE \_ AnalogVideo, \_ sous-type KSDATAFORMAT \_ Aucun audio : MediaType \_ AnalogAudio, MEDIASUBTYPE \_ null                                                                      |
| Interfaces de broche de sortie                    | [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)                                                                                                                                                              |
| CLSID du filtre                             | CLSID \_ TVTunerFilter                                                                                                                                                              |
| CLSID de page de propriétés                      | CLSID \_ TVTunerFilterPropertyPage                                                                                                                                                  |
| Exécutable                               | KSTVTune.ax                                                                                                                                                                       |
| [Mérite](merit.md)                       | MÉRITE \_ n' \_ \_ utilise pas                                                                                                                                                               |
| [Catégorie de filtre](filter-categories.md) | AM \_ KSCATEGORY \_ TVTUNER                                                                                                                                                           |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[DirectShow Filtres](directshow-filters.md)
</dt> </dl>

 

 



