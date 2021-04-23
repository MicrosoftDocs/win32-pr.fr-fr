---
description: Filtre de distributeur vidéo analogique
ms.assetid: 668f6a8b-a4ed-4e4a-956c-a87f165225fa
title: Filtre de distributeur vidéo analogique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d17d8700131dbc658a5233d56f339c39eac7a3a0
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909597"
---
# <a name="analog-video-crossbar-filter"></a>Filtre de distributeur vidéo analogique

Le filtre de distributeur vidéo analogique représente un distributeur vidéo sur un appareil de capture vidéo qui prend en charge le Windows Driver Model (WDM).

Ce filtre est un filtre de wrapper pour les filtres sur les périphériques de streaming WDM. Le nom convivial du filtre provient de l’appareil. Chaque broche de sortie représente un chemin d’accès matériel pour une vidéo de bande de bande analogique. L’une des broches d’entrée provient d’un tuner TV (le [filtre Tuner TV](tv-tuner-filter.md)). D’autres broches d’entrée prennent en charge les flux vidéo ou audio. Le filtre prend en charge tous les formats et sous-types de médias pris en charge sur les connexions en aval.

Vous ne pouvez pas créer directement ce filtre avec CoCreateInstance. L’interface [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) ajoute automatiquement ce filtre au graphique en fonction des besoins.

Pour plus d’informations sur les filtres de wrapper et les périphériques de streaming WDM, voir [Comment les périphériques matériels participent au graphique de filtre](how-hardware-devices-participate-in-the-filter-graph.md).



| Étiquette | Valeur |
|------------------------------------------|------------------------------------------------------------------------------------------------|
| Interfaces de filtre                        | [**IAMCrossbar**](/windows/desktop/api/Strmif/nn-strmif-iamcrossbar), ISpecifyPropertyPages, IPersistPropertyBag, IPersistStream |
| Types de média de broche d’entrée                    | MEDIATYPE \_ AnalogAudio, MediaType \_ AnalogVideo                                                 |
| Interfaces pin d’entrée                     | [**IKsPropertySet**](ikspropertyset.md)                                                       |
| Types de média de broche de sortie                   | MEDIATYPE \_ AnalogAudio, MediaType \_ AnalogVideo                                                 |
| Interfaces de broche de sortie                    | [**IKsPropertySet**](ikspropertyset.md)                                                       |
| CLSID du filtre                             | Non applicable                                                                                 |
| CLSID de page de propriétés                      | CLSID \_ CrossbarFilterPropertyPage                                                              |
| Exécutable                               | ksxbar.ax                                                                                      |
| [Mérite](merit.md)                       | Dépendant du pilote.                                                                              |
| [Catégorie de filtre](filter-categories.md) | \_KSCATEGORY \_                                                                       |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Filtres DirectShow](directshow-filters.md)
</dt> <dt>

[Utilisation des conversions](working-with-crossbars.md)
</dt> </dl>

 

 



