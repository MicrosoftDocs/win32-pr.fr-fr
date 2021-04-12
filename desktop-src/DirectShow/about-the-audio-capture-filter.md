---
description: À propos du filtre de capture audio
ms.assetid: ff345670-5a75-40d3-a228-8bc22aa76708
title: À propos du filtre de capture audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf5e28bef37ca52f0a33fc95b6d2a387cbbe2fb3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109687"
---
# <a name="about-the-audio-capture-filter"></a>À propos du filtre de capture audio

DirectShow permet la capture à partir des entrées analogiques sur une carte son par le biais du [filtre de capture audio](audio-capture-filter.md). Ce filtre utilise les API Wave *xxx* pour contrôler tout appareil dont le pilote prend en charge ces API. Chaque carte sur le système est représentée par une instance distincte du filtre.

Le filtre de capture audio expose chaque entrée sur la carte, telle que le microphone ou l’entrée MIDI, en tant que broche d’entrée. Les broches d’entrée représentent ce que le pilote expose en tant que lignes de la source audio. Aucune donnée ne transite par ces broches d’entrée, mais elles ne se connectent pas à d’autres filtres DirectShow. Elles fournissent simplement un moyen pour une application de contrôler les entrées. L’application peut utiliser une broche d’entrée pour activer ou désactiver l’entrée, ou pour définir des propriétés de combinaison telles que l’égalisation des basses, l’égalisation des aigus, le panoramique, etc. La quantité de contrôle disponible dépend du pilote. Pour bien comprendre et exploiter les fonctionnalités d’une carte audio particulière, vous aurez besoin de la documentation du fabricant de la carte.

> [!Note]  
> Vous pouvez capturer à partir de l’entrée de CD-Audio, mais ce flux audio est déjà passé par le convertisseur numérique-analogique, de sorte qu’il y aura une perte de qualité du son sur le CD d’origine.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Capture audio](audio-capture.md)
</dt> </dl>

 

 



