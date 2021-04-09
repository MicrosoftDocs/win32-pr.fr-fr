---
title: Modification du volume du synthétiseur MIDI interne
description: Modification du volume du synthétiseur MIDI interne
ms.assetid: 75ab7ff5-f394-4a79-8dcc-f4eef434a36e
keywords:
- L’interface MIDI (Musical Instrument Digital Interface), synthétiseurs internes
- MIDI (Musical Instrument Digital Interface), synthétiseurs internes
- lire des fichiers MIDI, des synthétiseurs internes
- synthétiseurs MIDI internes
- MIDI (Musical Instrument Digital Interface), modification du volume
- MIDI (Musical Instrument Digital Interface), modification du volume
- Jeux de fichiers MIDI, modification du volume
- modification du volume MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2369b13483ce6fa45d82ee177282a0de5e86538e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103940961"
---
# <a name="changing-internal-midi-synthesizer-volume"></a>Modification du volume du synthétiseur MIDI interne

Windows fournit les fonctions suivantes pour récupérer et définir le niveau de volume des appareils de synthétiseur MIDI internes :



| Valeur                                        | Signification                                                                       |
|----------------------------------------------|-------------------------------------------------------------------------------|
| [**midiOutGetVolume**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetvolume) | Récupère le niveau de volume du périphérique de synthétiseur MIDI interne spécifié. |
| [**midiOutSetVolume**](/windows/win32/api/mmeapi/nf-mmeapi-midioutsetvolume) | Définit le niveau de volume du périphérique de synthétiseur MIDI interne spécifié.      |



 

Tous les périphériques de sortie MIDI ne prennent pas en charge les modifications de volume. Certains appareils peuvent prendre en charge des modifications de volume individuelles sur les canaux gauche et droit. Pour plus d’informations sur la façon de déterminer si un appareil particulier prend en charge les modifications de volume, consultez [interrogation des périphériques de sortie MIDI](querying-midi-output-devices.md).

À moins que votre application ne soit conçue pour être une application de contrôle de volume maître (fournit à l’utilisateur un contrôle du volume pour tous les périphériques audio d’un système), vous devez ouvrir un périphérique audio avant de modifier son volume. Vous devez également vérifier le niveau de volume avant de le modifier et restaurer le niveau de volume précédent le plus rapidement possible.

Le volume est spécifié sous la forme d’une valeur de mot double. Les 16 bits supérieurs spécifient le volume relatif du canal droit, tandis que les 16 bits inférieurs spécifient le volume relatif du canal de gauche.

Pour les appareils qui ne prennent pas en charge les modifications de volume individuelles sur les canaux gauche et droit, les 16 bits de poids faible spécifient le niveau de volume et les 16 bits supérieurs sont ignorés. Les valeurs de la plage de niveau de volume 0x0 (silence) à 0xFFFF (volume maximal) et sont interprétées de façon logarithmique. L’augmentation du volume perçu est la même lors de l’augmentation du niveau de volume de 0x5000 à 0x6000, comme c’est le cas de 0x4000 à 0x5000.

 

 