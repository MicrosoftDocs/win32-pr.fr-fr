---
description: Événements de source de Sequencer
ms.assetid: 28654bae-9ce2-467b-b769-63279d69b173
title: Événements de source de Sequencer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f6237d5b79be9555f6d3f00da870ac461b86395e84d837bd0cc5818040e20cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118058116"
---
# <a name="sequencer-source-events"></a>Événements de source de Sequencer

Lorsque la [source de Sequencer](sequencer-source.md) joue une séquence de fichiers, la session multimédia envoie généralement tous les événements qui sont envoyés pendant la lecture normale et qui sont répertoriés dans [événements de session multimédia](media-session-events.md). L’application obtient ces événements à l’aide de l’interface [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) de la session de média.

En outre, certains événements sont spécifiques aux segments de sélection.



| Événement                                                                                                   | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MENewPresentation](menewpresentation.md)                                                              | Signale à l’application qu’elle doit Prérouler la topologie suivante.<br/> Pour fournir une transition transparente entre deux présentations consécutives, la source Sequencer charge la topologie suivante à l’avance. Alors que la topologie Active est toujours en cours d’exécution, la source Sequencer envoie cet événement pour la topologie suivante, à condition qu’une topologie suivante soit disponible dans la source.<br/> Ces données d’événement pour cet événement sont le descripteur de présentation de la topologie suivante. L’application est chargée de définir la topologie correspondante sur la session multimédia, comme décrit dans [utilisation de la source de Sequencer](using-the-sequencer-source.md).<br/> |
| [MEEndOfPresentationSegment](meendofpresentationsegment.md)                                            | La source de Sequencer déclenche cet événement lorsque la session multimédia est terminée en lisant le segment actuel, si ce segment est suivi d’un autre segment. (Si le segment actuel est le dernier, la source Sequencer déclenche l’événement [MEEndOfPresentation](meendofpresentation.md) à la place.)<br/> La session multimédia transmet cet événement à l’application. En règle générale, l’application reçoit [MEEndOfPresentationSegment](meendofpresentationsegment.md) une fois que la session multimédia a démarré le traitement du segment suivant, mais alors que les récepteurs multimédia fournissent toujours les exemples pour le segment précédent.<br/>                            |
| [MESessionTopologyStatus](mesessiontopologystatus.md), avec état **MF \_ TOPOSTATUS \_ récepteur \_ commuté**. | La session multimédia déclenche cet événement lorsqu’elle effectue une transition vers la topologie suivante dans la source de Sequencer et que les récepteurs de média ont terminé la création de la topologie précédente. Cet événement contient un pointeur vers la topologie suivante.                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

## <a name="example-1-playback-without-skipping"></a>Exemple 1 : lecture sans saut

Lorsque la source de Sequencer est impliquée, le nombre d’événements que vous recevez de la session de média peut prêter à confusion, en particulier parce que les événements associés à un segment sont souvent entrelacés avec les événements du segment suivant.

Dans le premier exemple, l’application met en file d’attente trois segments, S1, S2 et S3. Le troisième segment a le **\_ dernier indicateur SequencerTopologyFlags** , pour signaler qu’il s’agit du dernier segment de la séquence. Le segment auquel chaque événement correspond est indiqué entre parenthèses. Les appels [**SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) de l’application sont également répertoriés, afin de rendre l’ordre des opérations plus clair.

-   L’application appelle [**IMFMediaSession :: SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) (S1)
-   [MESessionTopologySet](mesessiontopologyset.md) (S1)
-   [MESessionTopologyStatus](mesessiontopologystatus.md): **MF \_ TOPOSTATUS \_ Ready** (S1)
-   [MENewPresentation](menewpresentation.md) (préroll S2)
-   L’application appelle [**IMFMediaSession :: SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) (S2)
-   [MESessionTopologyStatus](mesessiontopologystatus.md): **MF \_ TOPOSTATUS \_ Started \_ source** (Start of S1)
-   [MESessionTopologySet](mesessiontopologyset.md) (S2)
-   [MEEndOfPresentationSegment](meendofpresentationsegment.md) (fin de S1)
-   [MESessionTopologyStatus](mesessiontopologystatus.md): **MF \_ TOPOSTATUS \_ terminé** (S1)
-   [MESessionTopologyStatus](mesessiontopologystatus.md): **\_ récepteur TOPOSTATUS \_ MF \_ commuté** (transition vers S2)
-   [MESessionTopologyStatus](mesessiontopologystatus.md): **MF \_ TOPOSTATUS \_ Ready** (S2)
-   [MESessionTopologyStatus](mesessiontopologystatus.md): **MF \_ TOPOSTATUS \_ Started \_ source** (début de S2)
-   [MENewPresentation](menewpresentation.md) (préroll S3)
-   L’application appelle [**IMFMediaSession :: SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) (S2)
-   [MESessionTopologySet](mesessiontopologyset.md) (S3)
-   [MEEndOfPresentationSegment](meendofpresentationsegment.md) (fin de S2)
-   [MESessionTopologyStatus](mesessiontopologystatus.md): **MF \_ TOPOSTATUS \_ terminé** (S2)
-   [MESessionTopologyStatus](mesessiontopologystatus.md): **\_ récepteur TOPOSTATUS \_ MF \_ commuté** (transition vers S3)
-   [MESessionTopologyStatus](mesessiontopologystatus.md): **MF \_ TOPOSTATUS \_ Ready** (S3)
-   [MESessionTopologyStatus](mesessiontopologystatus.md): **MF \_ TOPOSTATUS \_ Started \_ source** (début de S3)
-   [MEEndOfPresentation](meendofpresentation.md) (fin de S3 ; dernier segment)
-   [MESessionTopologyStatus](mesessiontopologystatus.md): **MF \_ TOPOSTATUS \_ terminé**
-   [MESessionEnded](mesessionended.md)

Cette liste n’inclut pas tous les événements que vous pouvez recevoir. (Par exemple, il omet l’événement [MESessionCapabilitiesChanged](mesessioncapabilitieschanged.md) , qui est envoyé chaque fois que les fonctionnalités de session changent. Une application reçoit généralement plusieurs événements MESessionCapabilitiesChanged dans une présentation.) Les événements répertoriés ici sont ceux qui indiquent la transition d’un segment à l’autre. Les événements les plus importants sont [MENewPresentation](menewpresentation.md), qui indique à l’application de Prérouler la topologie suivante, et [MEEndOfPresentationSegment](meendofpresentationsegment.md), qui signale la fin d’un segment (à l’exception du dernier segment).

Étant donné que les événements dans Media Foundation sont asynchrones et ne sont pas sérialisés avec les appels de méthode, l’ordre exact peut varier. Par exemple, vous pouvez recevoir **la \_ \_ \_ source lancée MF TOPOSTATUS** pour S1 avant que l’application n’appelle [**SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) pour S2.

En outre, vous risquez de ne pas recevoir tous les événements répertoriés ici. Les événements [MEEndOfPresentation](meendofpresentation.md) et [MESessionEnded](mesessionended.md) , par exemple, ne sont pas envoyés, sauf si le dernier segment a le **\_ dernier indicateur SequencerTopologyFlags** .

Enfin, cette liste n’indique pas le passage de l’heure. L’heure du « début de S1 » à « fin de S1 » correspond à la durée totale de S1, qui peut être de quelques secondes ou plusieurs heures, en fonction de la source.

## <a name="example-2-playback-with-segment-skipping"></a>Exemple 2 : lecture avec saut de segment ignoré

Dans cet exemple, l’application met en file d’attente les mêmes segments, mais ignore le segment 3 pendant la diffusion du segment 1. Dans ce cas, les événements suivants sont envoyés :

-   L’application appelle [**IMFMediaSession :: SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) (S1)
-   [MESessionTopologySet](mesessiontopologyset.md) (S1)
-   [MESessionTopologyStatus](mesessiontopologystatus.md): **MF \_ TOPOSTATUS \_ Ready** (S1)
-   [MENewPresentation](menewpresentation.md) (préroll S2)
-   L’application appelle [**IMFMediaSession :: SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) (S2)
-   [MESessionTopologyStatus](mesessiontopologystatus.md): **MF \_ TOPOSTATUS \_ Started \_ source** (Start of S1)
-   [MESessionTopologySet](mesessiontopologyset.md) (S2)
-   L’application appelle [**IMFMediaSession :: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) (passez à S3)
-   [MENewPresentation](menewpresentation.md) (préroll S3)
-   L’application appelle [**IMFMediaSession :: SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) (S3)
-   [MESessionStarted](mesessionstarted.md)
-   [MEEndOfPresentationSegment](meendofpresentationsegment.md) (S1 annulé)
-   [MESessionTopologyStatus](mesessiontopologystatus.md): **MF \_ TOPOSTATUS \_ terminé** (S1)
-   [MESessionTopologySet](mesessiontopologyset.md) (S3)
-   [MESessionTopologyStatus](mesessiontopologystatus.md): **\_ récepteur TOPOSTATUS \_ MF \_ commuté** (transition vers S2)
-   [MESessionTopologyStatus](mesessiontopologystatus.md): **MF \_ TOPOSTATUS \_ Ready** (S2)
-   [MESessionTopologyStatus](mesessiontopologystatus.md): **MF \_ TOPOSTATUS \_ Started \_ source** (S2)
-   [MEEndOfPresentationSegment](meendofpresentationsegment.md) (S2 annulé)
-   [MESessionTopologyStatus](mesessiontopologystatus.md): **MF \_ TOPOSTATUS \_ terminé** (S2)
-   [MESessionTopologyStatus](mesessiontopologystatus.md): **\_ récepteur TOPOSTATUS \_ MF \_ commuté** (transition vers S3)
-   [MESessionTopologyStatus](mesessiontopologystatus.md): **TOPOSTATUS \_ Ready** (S3)
-   [MESessionTopologyStatus](mesessiontopologystatus.md): **MF \_ TOPOSTATUS \_ Started \_ source** (S3)

Lorsque l’application appelle [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) pour passer au segment 3, la source Sequencer annule le segment 1, qui est toujours en cours d’exécution. L’événement [MEEndOfPresentationSegment](meendofpresentationsegment.md) pour ce segment contient l’attribut d’annulation de la topologie de la [**\_ \_ source d' \_ \_ événements MF**](mf-event-source-topology-canceled-attribute.md) , indiquant que le segment s’est terminé car il a été annulé. Ensuite, étant donné que segment 2 est déjà préinstallé, ce segment est démarré, puis immédiatement annulé. L’événement MEEndOfPresentationSegment pour le segment 2 contient également l’attribut de topologie de la **\_ source d’événements MF \_ \_ \_ annulé** . La session peut ensuite basculer vers segment 3 et la lire normalement.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos de la source de Sequencer](about-the-sequencer-source.md)
</dt> <dt>

[Source de Sequencer](sequencer-source.md)
</dt> </dl>

 

 




