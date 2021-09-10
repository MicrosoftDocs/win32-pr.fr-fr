---
title: Mappage des appareils Waveform-Audio
description: Mappage des appareils Waveform-Audio
ms.assetid: e23919c9-c5fa-4406-920c-1fdbeea4821d
keywords:
- audio multimédia, mappage d’appareils Wave Audio
- audio, mappage d’une forme d’onde-périphériques audio
- Audio Compression Manager (ACM), mappage d’appareils Wave Audio
- ACM (gestionnaire de compression audio), mappage d’appareils Wave-Audio
- mappage d’appareils Wave-Audio
- audio multimédia, Mappeur
- audio, Mappeur
- Audio Compression Manager (ACM), Mappeur
- ACM (gestionnaire de compression audio), Mappeur
- mappeur
- sons Waveform, périphériques de mappage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9cdd269e21eb992244dd0e5979c7e0d193ba92b
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369119"
---
# <a name="mapping-waveform-audio-devices"></a>Mappage des appareils Waveform-Audio

Windows fournit un ensemble de fonctions standard pour les périphériques audio. Ces fonctions émettent des appels aux pilotes de périphériques qui gèrent les périphériques matériels. Le système utilise un module appelé « mappeur » pour gérer les appareils installés. Le Mappeur utilise des raccordements spéciaux dans l’interface de pilote pour intercepter les appels et agir comme intermédiaire entre le système et les pilotes installés dans le système. Le Mappeur est responsable de la correspondance des demandes d’une application pour l’accès à un appareil avec les appareils disponibles et pour la recherche d’un appareil qui répond aux exigences audio de l’application actuelle. Le système fournit des mappeurs pour les types de pilotes standard : Waveform-Audio, MIDI (Musical Instrument Digital Interface) et appareils auxiliaires.

L’ACM est une extension du système multimédia de base et est installé en tant que Mappeur. Cela signifie que l’ACM utilise les crochets du mappeur de l’interface du pilote pour les périphériques audio Waveform. L’utilisation de ces hooks permet à l’ACM de décoder ou de coder des données Waveform Audio avant de les transmettre vers ou à partir d’un pilote de périphérique Wave-audio. La différence entre l’ACM et le mappeur de système standard est que l’ACM peut rechercher un périphérique Wave-audio qui prend en charge un format spécifié ou une combinaison d’un périphérique audio Waveform et d’un compresseur ou décompresseur ACM qui prend en charge un format spécifié.

Quand une application demande que le système ouvre un appareil Waveform Audio pour l’entrée ou la sortie, la demande spécifie le format et l’appareil. Lorsque l’appareil spécifié est le Mappeur, le Mappeur doit trouver un appareil qui prend en charge le format spécifié. Le Mappeur implémenté dans l’ACM recherche un périphérique Wave-Audio installé qui prend en charge le format spécifié. Si l’ACM ne trouve pas ce type d’appareil, il recherche un périphérique Wave-audio et un compresseur ou un décompresseur qui, ensemble, prennent en charge le format. Plus précisément, l’ACM recherche un compresseur ou un décompresseur qui convertit le format spécifié dans un format pris en charge par un périphérique audio Wave installé. Une fois que l’ACM a trouvé un appareil qui prend en charge le format converti, il peut honorer les demandes de lecture ou d’enregistrement du format demandé à l’origine, même si aucun périphérique Wave-Audio installé ne prend directement en charge ce format.

Outre la conversion de format, l’ACM offre également des services pour prendre en charge la compression, la décompression, le filtrage, la sélection de format et la sélection de filtres. Il fournit une API standard qu’il prend en charge en appelant ses propres pilotes.

 

 




