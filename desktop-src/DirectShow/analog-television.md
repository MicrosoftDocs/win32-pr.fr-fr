---
description: Télévision analogique
ms.assetid: 9f2c18ec-3684-42a8-a3df-5f8827b27642
title: Télévision analogique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33af8ba94831afed59d783598dbf6bc0eaee0ec6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109002"
---
# <a name="analog-television"></a>Télévision analogique

La télévision analogique diffère des autres scénarios de capture vidéo de plusieurs façons :

-   La carte tuner est paramétrée sur un signal analogique, qui est ensuite numérisé.
-   L’audio est transporté dans le signal analogique. La façon dont le son atteint la carte audio varie en fonction du matériel.
-   Le signal peut contenir des données supplémentaires dans l’intervalle de parasite vertical (VBI), par exemple les sous-titres (CC), le télétexte universel standard (WST) et les services de données étendus (XDS).

Le diagramme suivant montre un graphique de filtre classique pour la préversion de la télévision.

![graphique de télévision analogique](images/vidcap06.png)

-   Le filtre [Tuner TV](tv-tuner-filter.md) contrôle le paramétrage.
-   Le filtre [audio TV](tv-audio-filter.md) contrôle le décodage audio.
-   Si la carte tuner a plusieurs entrées physiques, le filtre de la barre d' [affichage vidéo analogique](analog-video-crossbar-filter.md) permet à l’application de sélectionner l’entrée qui est décodée et rendue.
-   Le filtre de [capture vidéo WDM](wdm-video-capture-filter.md) remet le flux vidéo numérisé.

Le générateur de graphiques de capture insère automatiquement tous les filtres qui sont requis en amont du filtre de capture.

Cette section contient les rubriques suivantes :

-   [Réglage de la télévision analogique](analog-television-tuning.md)
-   [Télévision analogique audio](analog-television-audio.md)
-   [Sous-titres et télétexte](closed-captions-and-teletext.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Capture vidéo](video-capture.md)
</dt> </dl>

 

 



