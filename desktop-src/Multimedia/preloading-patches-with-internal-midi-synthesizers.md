---
title: Préchargement des correctifs avec des synthétiseurs MIDI internes
description: Préchargement des correctifs avec des synthétiseurs MIDI internes
ms.assetid: c200aa91-ab91-48e8-b3b5-8e7f36e511be
keywords:
- L’interface MIDI (Musical Instrument Digital Interface), synthétiseurs internes
- MIDI (Musical Instrument Digital Interface), synthétiseurs internes
- lire des fichiers MIDI, des synthétiseurs internes
- synthétiseurs MIDI internes
- Interface MIDI (Musical Instrument Digital Interface), préchargement des correctifs
- MIDI (Musical Instrument Digital Interface), préchargement des correctifs
- Jeux de fichiers MIDI, préchargement des correctifs
- préchargement des correctifs MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc54eccdaa0a0c9aa16f206e7e036f322b615d96
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127119521"
---
# <a name="preloading-patches-with-internal-midi-synthesizers"></a>Préchargement des correctifs avec des synthétiseurs MIDI internes

Certains appareils de synthétiseur MIDI internes ne peuvent pas conserver tous les correctifs chargés simultanément. Ces appareils doivent précharger leurs données de correctifs.

Windows fournit les fonctions suivantes pour demander à un synthétiseur de précharger et de mettre en cache les correctifs spécifiés.



| Valeur                                                      | Signification                                                                                                     |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**midiOutCachePatches**](/windows/win32/api/mmeapi/nf-mmeapi-midioutcachepatches)         | Demande qu’un appareil de synthétiseur MIDI interne précharge et met en cache les correctifs Melodic spécifiés.              |
| [**midiOutCacheDrumPatches**](/windows/win32/api/mmeapi/nf-mmeapi-midioutcachedrumpatches) | Demande qu’un appareil de synthétiseur MIDI interne précharge et met en cache les correctifs à percussion clé spécifiés. |



 

Pour plus d’informations sur la façon de déterminer si un appareil particulier prend en charge le préchargement des correctifs, consultez [interrogation des périphériques de sortie MIDI](querying-midi-output-devices.md).

 

 