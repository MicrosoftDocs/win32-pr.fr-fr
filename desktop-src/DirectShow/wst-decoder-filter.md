---
description: Filtre de décodage WST
ms.assetid: 2d33ae3f-565d-4e69-8fb0-117ff582a4d0
title: Filtre de décodage WST
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eb6804f82e5d15aa324feb163261544969e3c45
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908477"
---
# <a name="wst-decoder-filter"></a>Filtre de décodage WST

Ce composant a été supprimé de Windows Vista et des systèmes d’exploitation ultérieurs. Il peut être utilisé dans les systèmes d’exploitation Windows XP et Windows Server 2003.

> [!Note]  
> À compter de Windows Vista, DirectShow ne fournit pas de filtre pour décoder le télécode WST (World standard Teletext).

 

Le décodeur WST est un filtre en mode noyau qui accepte les données de télétexte non standard décodées du [codec WST](wst-codec-filter.md) et remet les bitmaps à la broche 2 sur le [mélangeur de superposition](overlay-mixer-filter.md) à l’aide des polices fournies par Microsoft. Seules les langues d’Europe occidentale sont prises en charge pour l’instant ; aucune police Unicode n’est actuellement fournie.

Ce filtre peut être ajouté automatiquement au graphique en appelant [**ICaptureGraphBuilder2 :: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream), à l’aide de la broche de sortie du codec WST.



| Étiquette | Valeur |
|------------------------------------------|---------------------------------------------------------------|
| Interfaces de filtre                        | ISpecifyPropertyPages, [ **IAMWstDecoder**](/previous-versions/windows/desktop/api/Iwstdec/nn-iwstdec-iamwstdecoder) |
| Types de média de broche d’entrée                    | MEDIATYPE \_ VBI, \_ TÉLÉtexte MEDIASUBTYPE                        |
| Interfaces pin d’entrée                     | [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)                                          |
| Types de média de broche de sortie                   | Vidéo de MEDIATYPE \_                                              |
| Interfaces de broche de sortie                    | [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)                                          |
| CLSID du filtre                             | CLSID \_ WSTDecoder                                             |
| CLSID de page de propriétés                      | CLSID \_ WstDecoderPropertyPage                                 |
| Exécutable                               | Wstdecod.DLL                                                  |
| [Mérite](merit.md)                       | MÉRITE \_ normal                                                 |
| [Catégorie de filtre](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                 |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Filtres DirectShow](directshow-filters.md)
</dt> <dt>

[Affichage du télétexte standard du monde](viewing-world-standard-teletext.md)
</dt> </dl>

 

 



