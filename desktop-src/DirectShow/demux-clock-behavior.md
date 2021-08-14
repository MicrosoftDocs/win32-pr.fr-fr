---
description: Demux le comportement de l’horloge
ms.assetid: c8a067f7-4e4c-4f25-b26c-f6bb048060b0
title: Demux le comportement de l’horloge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06ab1976bf123e971f6c3ec08e18c743352d37b73de95901a67abfee5d10a054
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117821184"
---
# <a name="demux-clock-behavior"></a>Demux le comportement de l’horloge

En mode push, le démultiplexeur MPEG-2 (demux) expose l’interface [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) . Il agit comme une source dynamique, donc il est choisi comme horloge de référence graphique par défaut ; Pour plus d’informations, consultez la page [sources dynamiques](live-sources.md) .

-   Pour les flux de transport, demux synchronise son horloge avec le flux de données PCR qui correspond au flux audio ou vidéo le plus récemment mappé par l’application. En interne, le demux suit les tables PAT et VPM. Lorsque l’application mappe un PID de flux élémentaire à une broche de sortie, demux recherche le flux de la PCR pour ce PID et utilise ce flux de PCR. (Actuellement, il n’existe aucun moyen pour l’application de spécifier directement le PID PCR.)
-   Pour les flux de programme, demux synchronise son horloge avec le flux de la SCR.

La synchronisation de l’horloge de filtre avec le flux PCR ou SCR empêche le dépassement de capacité négatif ou de dépassement de capacité des données, ce qui peut se produire si l’horloge du graphique varie de l’horloge du flux. le demux convertit également les valeurs de PTS PES en DirectShow temps de référence, et utilise ces valeurs pour horodater les exemples de supports. Les horodatages s’appliquent à la limite de cadre suivante ; Il n’y a aucune garantie que la limite de cadre s’aligne sur le début de l’exemple de support.

Le demux garantit que les horodatages augmentent de manière monotone. Cela signifie, par exemple, que si un flux de transport comprend un segment tel qu’un commercial qui a été créé avec une horloge différente de celle du programme principal, demux ajuste les horodatages de la présentation pour masquer la discontinuité des filtres en aval.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation du démultiplexeur MPEG-2](using-the-mpeg-2-demultiplexer.md)
</dt> </dl>

 

 



