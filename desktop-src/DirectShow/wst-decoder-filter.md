---
description: Filtre de décodage WST
ms.assetid: 2d33ae3f-565d-4e69-8fb0-117ff582a4d0
title: Filtre de décodage WST
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d61da0540c683e8c4646074715b0518717b4e1958beea5b8ca2ae41fb4629790
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119290769"
---
# <a name="wst-decoder-filter"></a>Filtre de décodage WST

ce composant a été supprimé de Windows Vista et des systèmes d’exploitation ultérieurs. il peut être utilisé dans les systèmes d’exploitation Windows XP et Windows Server 2003.

> [!Note]  
> à partir de Windows Vista, DirectShow ne fournit pas de filtre pour décoder WST (World Standard teletext).

 

le décodeur WST est un filtre en mode noyau qui accepte les données de télétexte non Standard décodées du [Codec WST](wst-codec-filter.md) et remet les bitmaps à la broche 2 sur la [superposition Mixer](overlay-mixer-filter.md) à l’aide des polices fournies par Microsoft. Seules les langues d’Europe occidentale sont prises en charge pour l’instant ; aucune police Unicode n’est actuellement fournie.

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

[DirectShow Filtres](directshow-filters.md)
</dt> <dt>

[Affichage du télétexte standard du monde](viewing-world-standard-teletext.md)
</dt> </dl>

 

 



