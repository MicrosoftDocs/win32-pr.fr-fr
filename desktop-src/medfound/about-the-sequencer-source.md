---
description: À propos de la source de Sequencer
ms.assetid: 0d7ce9ca-9f34-4842-bd49-9211ae4454de
title: À propos de la source de Sequencer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09d81799a8bc1e46ade10989bbe485c69e839832fce0ded14220c536809e23e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118065556"
---
# <a name="about-the-sequencer-source"></a>À propos de la source de Sequencer

La source de Sequencer permet à une application de lire une collection de [sources multimédias](media-sources.md) séquentiellement, avec des transitions transparents entre les sources. La source de Sequencer peut être utilisée pour les scénarios suivants :

-   Créer une sélection qui bascule en toute transparence d’une source de média à la suivante.
-   Lire des flux à partir de plusieurs sources simultanément ; par exemple, lire l’audio d’un fichier avec la vidéo d’un autre fichier.
-   Basculer entre les flux dans différentes sources de média dans des entrées de playlist consécutives ; par exemple, une sélection peut avoir des entrées qui partagent la même source vidéo, tandis que chaque entrée contient une source audio différente.

Pour chaque élément d’une sélection, l’application crée une topologie distincte. Les sources multimédias de ces topologies sont appelées *sources natives* pour les distinguer de la source de Sequencer. Pendant la lecture, l’ensemble de la séquence de topologies est appelé une *Présentation*, et chaque topologie de la séquence est appelée un *segment*.

La lecture est contrôlée par la [session multimédia](media-session.md), qui fournit des contrôles de transport, tels que lecture, pause et arrêt. La session multimédia gère également l’heure de présentation et envoie des événements à l’application. (Les événements de la source de Sequencer sont transférés à l’application via la session multimédia.)

Pour créer une sélection, l’application crée une ou plusieurs topologies de lecture et les met en file d’attente sur la source de Sequencer dans l’ordre de lecture souhaité. En interne, la source de Sequencer modifie les topologies afin que les nœuds sources pointent vers la source de Sequencer au lieu de la source native. L’application envoie ces topologies modifiées, plutôt que les topologies d’origine, à la session multimédia. Cela permet à la source de Sequencer d’agréger les sources natives et de communiquer avec la session multimédia.

Pour obtenir des transitions transparents entre les segments, la source de Sequencer préroll chaque segment. Pendant la lecture d’un segment, et avant qu’il soit temps de lire le segment suivant, la source de Sequencer déclenche un événement [MENewPresentation](menewpresentation.md) contenant un descripteur de présentation. L’application utilise ce descripteur de présentation pour obtenir la topologie du segment suivant dans la présentation et met en file d’attente la topologie sur la session multimédia.

L’illustration suivante montre le workflow pour les entrées de playlist à travers la source de Sequencer. L’application utilise le programme de résolution source pour créer les sources natives, génère des topologies pour chaque segment et met les topologies en file d’attente sur la source de Sequencer.

![Diagramme montrant le workflow des segments imfmediasession, imfsequencersource et playlist conduisant à imfmediasource](images/dbf41a05-d8cc-4502-9cd3-74e5d1ce04a0.gif)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Comment créer une sélection](how-to-create-a-playlist.md)
</dt> <dt>

[Topologies](topologies.md)
</dt> <dt>

[Utilisation de la source de Sequencer](using-the-sequencer-source.md)
</dt> <dt>

[Source de Sequencer](sequencer-source.md)
</dt> </dl>

 

 



