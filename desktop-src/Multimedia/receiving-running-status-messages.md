---
title: Réception des messages de Running-Status
description: Réception des messages de Running-Status
ms.assetid: 4f2e8e41-89f6-45e3-ae16-47b856f0e63e
keywords:
- MIDI (Musical Instrument Digital Interface), état d’exécution
- MIDI (Musical Instrument Digital Interface), état d’exécution
- enregistrement de l’audio MIDI, état d’exécution
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f4d782e1e25c718ddd177d1d9baf471d0715d70680b65920052e85d6fffc551
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118371344"
---
# <a name="receiving-running-status-messages"></a>Réception des messages de Running-Status

La spécification *fichiers midi Standard 1,0* permet l’utilisation de l' *État d’exécution* lorsqu’un message a le même octet d’État que le message précédent. Lorsque l’état d’exécution est utilisé, l’octet d’état des messages suivants peut être omis. Tous les pilotes de périphérique d’entrée MIDI sont requis pour étendre les messages à l’aide de l’état d’exécution dans des messages complets, afin que vous receviez toujours des messages MIDI complets à partir d’un pilote de périphérique d’entrée MIDI.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Enregistrement d’un fichier audio MIDI](recording-midi-audio.md)
</dt> </dl>

 

 




