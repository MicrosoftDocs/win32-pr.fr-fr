---
description: Filtre de séparateur DV
ms.assetid: 099d1cc7-f0c5-4c50-a1d5-f2defde7e104
title: Filtre de séparateur DV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74ca8e856f1a49ff22ee05f7dc0ae341fad6aa91
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908407"
---
# <a name="dv-splitter-filter"></a>Filtre de séparateur DV

Ce filtre fractionne un flux vidéo (DV) entrelacé en son composant flux vidéo et audio.



| Étiquette | Valeur |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces de filtre                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [ **IDVSplitter**](/windows/desktop/api/Strmif/nn-strmif-idvsplitter)                                                                             |
| Types de média de broche d’entrée                    | MEDIATYPE \_ entrelacé, MEDIASUBTYPE \_ DVSD, format \_ DvInfo                                                                                         |
| Interfaces pin d’entrée                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                             |
| Types de média de broche de sortie                   | **Vidéo**: \_ vidéo MediaType, format \_ DvInfo<br/> **Audio**: MediaType \_ audio, MEDIASUBTYPE \_ PCM, format \_ WaveFormatEx<br/>             |
| Interfaces de broche de sortie                    | [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| CLSID du filtre                             | CLSID \_ DVSplitter                                                                                                                                  |
| CLSID de page de propriétés                      | Aucune page de propriétés.                                                                                                                                  |
| Exécutable                               | qdv.dll                                                                                                                                            |
| [Mérite](merit.md)                       | MÉRITE \_ normal                                                                                                                                      |
| [Catégorie de filtre](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                                                      |



 

## <a name="remarks"></a>Remarques

Les images DV contiennent des données audio et vidéo dans le même cadre. Le filtre de séparateur DV extrait les données audio et les remet sous la forme d’un ou de deux flux audio, à partir des broches de sortie audio. La trame DV d’origine est fournie à partir de la broche de sortie vidéo, sous la forme d’une image vidéo. Le type de média sur l’image vidéo est modifié de MEDIATYPE \_ entrelacé à MediaType \_ Video, mais les données ne sont pas modifiées. Le type de média est modifié pour signaler que les données audio dans le frame doivent être ignorées. Le séparateur DV ne définit pas un temps de support sur les échantillons de sortie. Si vous écrivez un filtre en aval qui requiert les temps de support, vous pouvez dériver les heures du nombre de frames.

Une seule broche de sortie à la fois expose les interfaces [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) et [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) .

Le filtre de séparateur DV peut accepter des modifications de format dynamiques dans le flux audio. Toutefois, si le filtre [multiplexeur AVI](avi-mux-filter.md) est en aval, il rejette la modification de format. Dans ce cas, le séparateur DV arrête de produire un flux audio. Cette limitation affecte uniquement la capture de fichier de type 2. Pour les fichiers de type 1, le flux entrelacé n’est pas fractionné en premier lieu. Pour la version préliminaire, il n’y a aucun filtre MUX AVI en aval.

Si la source DV est une caméra dynamique, il n’y a généralement aucune raison pour que le format audio change. Toutefois, le format peut changer si vous transmettez à partir d’une bande VTR contenant plusieurs sources hétérogènes.

Chaque image DV contient des métadonnées, en plus des données audio et vidéo. Ces métadonnées peuvent changer de frame en Frame. Les applications peuvent analyser les métadonnées en examinant les exemples d’entrée ou les exemples de sortie vidéo. Toutefois, DirectShow ne fournit pas de prise en charge directe pour l’analyse des métadonnées DV. Pour plus d’informations, consultez IEC 61834-4.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Filtres DirectShow](directshow-filters.md)
</dt> <dt>

[Vidéo numérique dans DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 




