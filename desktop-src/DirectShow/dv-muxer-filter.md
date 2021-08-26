---
description: Filtre DV du multiplexeur
ms.assetid: 4dd57202-f4de-40d9-b720-efaba8a60a7c
title: Filtre DV du multiplexeur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6ad8189d7430a150c6860ef9e390a0e66aabd00971b56197ffe8651cde8967b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102969"
---
# <a name="dv-muxer-filter"></a>Filtre DV du multiplexeur

Ce filtre combine un flux vidéo encodé en vidéo numérique (DV) avec un ou deux flux audio pour produire un flux DV entrelacé. Pour écrire le flux dans un fichier AVI, connectez ce filtre au filtre [multiplex MUX](avi-mux-filter.md) et connectez le fichier *AVI MUX* au filtre du [writer de fichier](file-writer-filter.md) . Pour plus d’informations, consultez [vidéo numérique dans DirectShow](digital-video-in-directshow.md).



| Étiquette | Valeur |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces de filtre                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [ **IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)                                                             |
| Types de média de broche d’entrée                    | **Vidéo**: MediaType \_ Video, MEDIASUBTYPE \_ DVSD, format \_ videoinfo **audio**: MediaType \_ audio, MEDIASUBTYPE \_ PCM, format \_ WaveFormatEx |
| Interfaces pin d’entrée                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                 |
| Types de média de broche de sortie                   | MEDIATYPE \_ entrelacé, MEDIASUBTYPE \_ DVSD, format \_ DvInfo                                                                             |
| Interfaces de broche de sortie                    | [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin), [ **IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                       |
| CLSID du filtre                             | CLSID \_ DVMux                                                                                                                           |
| CLSID de page de propriétés                      | Aucune page de propriétés                                                                                                                       |
| Exécutable                               | qdv.dll                                                                                                                                |
| [Mérite](merit.md)                       | MÉRITE \_ improbable                                                                                                                        |
| [Catégorie de filtre](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                                          |



 

## <a name="remarks"></a>Remarques

Le du multiplexeur DV peut créer deux broches d’entrée audio. Il prend en charge les formats audio indiqués dans le tableau suivant.



Code confidentiel audio 1

Code confidentiel audio 2

Format de sortie

Taux d’échantillonnage (kHz)

Bits/échantillon

Canaux

Échantillonnage

Bits/échantillon

Canaux

32

16

Mono

Non connecté

Canal SD 2

32

16

Stéréo

Non connecté

Canal SD 4

44,1 ou 48

16

Stéréo ou mono

Non connecté

Canal SD 2

Non connecté

32

16

Stéréo ou mono

Interdit

Non connecté

44,1 ou 48

16

Mono

Interdit

Non connecté

44,1 ou 48

16

Stéréo

Canal SD 2

32

16

Mono

32

16

Mono

Canal SD 2

32

16

Stéréo ou mono\*

32

16

Stéréo ou mono\*

Canal SD 4

44,1

16

Mono

44,1

16

Mono

Canal SD 2

48

16

Mono

48

16

Mono

Canal SD 2

\* Si au moins une broche d’entrée est stéréo.



 

Dans le cadre de cette table, la broche audio 1 est définie comme la première broche d’entrée connectée à une source audio, et la broche audio 2 est définie comme deuxième broche d’entrée connectée à une source audio. Une fois qu’une broche audio est connectée, ce schéma de numérotation reste effectif, à moins que les deux broches audio soient déconnectées. Par exemple, si vous connectez les deux broches audio, puis déconnectez la broche audio 1, le code confidentiel restant est toujours considéré comme étant pin 2.

L’audio fourni à la broche 1 est enregistré dans le premier bloc audio des images DV (CH1), et l’audio fourni au code confidentiel 2 est enregistré dans le deuxième bloc audio (CH2). Exception : si le filtre a une seule entrée stéréo à 44,1 kHz ou 48 kHz, le canal audio de gauche est enregistré dans le premier bloc audio, et le canal audio de droite est enregistré dans le second bloc audio.

Pour la sortie SD à 4 canaux : si l’entrée est stéréo, la piste de gauche est enregistrée en CHa ou CHc, et la piste appropriée est enregistrée dans CHb ou CHd. Si l’entrée est mono, l’audio est enregistré dans CHa ou CHc, et CHb et CHd sont silencieux.

En connectant et déconnectant le code PIN audio 1, il est possible d’atteindre un format non autorisé. Dans ce cas, la méthode [**IMediaFilter ::P ause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause) du filtre retourne VFW \_ E \_ non \_ connecté. Cette limitation empêche une situation dans laquelle le premier bloc audio n’a pas de son, mais le second bloc audio est audio. Le deuxième bloc doit avoir un audio uniquement si le premier bloc a également du son.

Le du multiplexeur DV n’autorise pas les entrées audio avec différents taux d’échantillonnage. toutefois, les méthodes de création de graphiques, telles que [**IGraphBuilder :: Connecter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) , ajoutent généralement le filtre de [wrappers ACM](acm-wrapper-filter.md) , qui convertit le deuxième flux audio pour correspondre au taux d’échantillonnage du premier flux.

Si l’entrée audio est 48 kHz ou 32 kHz, la sortie audio est verrouillée. (Il n’est pas possible de verrouiller l’audio 44,1-kHz.)

Si aucune broche audio n’est connectée, la sortie contient les données audio des images DV entrantes. Il peut s’agir d’un silence ou de données audio valides.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[DirectShow Filtres](directshow-filters.md)
</dt> <dt>

[Vidéo numérique en DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 



