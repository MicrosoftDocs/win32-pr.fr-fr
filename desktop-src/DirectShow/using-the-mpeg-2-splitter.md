---
description: Utilisation du séparateur MPEG-2
ms.assetid: a08e079c-41be-475a-9e88-ee46d17fe938
title: Utilisation du séparateur MPEG-2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e43ba5a45d20de7af5e996b8e2837971de08c0f486a880e01f9f28a45f8ab385
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120049549"
---
# <a name="using-the-mpeg-2-splitter"></a>Utilisation du séparateur MPEG-2

> [!Note]  
> à partir de Microsoft® Windows® XP, le filtre de séparateur MPEG-2 est déconseillé. Utilisez plutôt le [démultiplexeur MPEG-2](mpeg-2-demultiplexer.md) .

 

Le filtre de séparateur MPEG-2 prend en charge la lecture en mode Pull des flux de programme MPEG-2 qui contiennent au moins l’un des types de flux suivants.

-   Vidéo MPEG-2
-   Audio MPEG-2
-   Audio Dolby AC-3 encodé comme défini pour DVD-Video
-   LPCM (linéaire Pulse Code modulé) encodé comme défini pour DVD-Video

Pour obtenir la liste des types de médias pris en charge par le séparateur MPEG-2, consultez [types de média MPEG-2 Splitter](mpeg-2-splitter-media-types.md).

Le séparateur MPEG-2 n’analyse pas les flux de transport. Utilisez le filtre de démultiplexage MPEG-2 pour les flux de transport (mode Push uniquement).

**Horodatages**

Lors de la diffusion de flux de programme MPEG-2, le filtre de séparateur MPEG-2 traite la première référence de l’horloge système qu’il rencontre comme origine de l’heure de n’importe quel flux. Cela diffère du [séparateur de flux MPEG-1](mpeg-1-stream-splitter-filter.md), qui utilise des horodatages de présentation. La méthode [**IAMParse :: GetParseTime**](/previous-versions/windows/desktop/api/Amparse/nf-amparse-iamparse-getparsetime) retourne l’heure de l’horloge du système de flux (éventuellement estimé) pour les données qu’elle a traitées.

Si le filtre de séparateur MPEG-2 rencontre un exemple d’entrée avec le jeu de propriétés de discontinu (la propriété discontinu peut être définie à l’aide de [**IMediaSample :: SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) ou [**IMediaSample2 :: SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-setproperties)), il ignore les données jusqu’à ce qu’il trouve le premier pack dans les données et ajuste ses horodatages afin que la référence de l’horloge système (SCR) de ce pack soit considérée comme identique à l’heure SCR avant la discontinuation. Si l’horloge SCR s’affiche pour aller vers le haut ou pour avancer d’une seconde, puis (en ligne avec la spécification du flux de programme MPEG-2), elle est également traitée comme une discontinuité d’horloge et l’écart d’horloge apparent est soustrait des horodatages passés aux filtres en aval.

**Sélection de flux**

Lors de la lecture du flux de programme MPEG-2, le premier flux vidéo et le premier flux audio trouvés parcourant le flux de programme sont choisis. Jusqu’à un audio et une broche de sortie vidéo sont pris en charge. Par le biais de l’interface [**IAMStreamSelect**](/windows/desktop/api/Strmif/nn-strmif-iamstreamselect) , différents flux du même type peuvent être sélectionnés jusqu’au nombre spécifié par la limite audio dans l’en-tête système. Pour le son MPEG-2, il est actuellement supposé que les flux forment une plage contiguë à partir du flux 0xC0.

**Interfaces prises en charge**

Le filtre de séparateur MPEG-2 prend en charge les interfaces suivantes.

-   [**IAMParse**](/previous-versions/windows/desktop/api/Amparse/nn-amparse-iamparse). Flux de programme MPEG-2 uniquement.
-   [**IAMStreamSelect**](/windows/desktop/api/Strmif/nn-strmif-iamstreamselect). Flux de programme MPEG-2 uniquement, flux audio uniquement.
-   [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking). Comprend la recherche en mode octet.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Prise en charge de MPEG-2 dans DirectShow](mpeg-2-support-in-directshow.md)
</dt> </dl>

 

 



