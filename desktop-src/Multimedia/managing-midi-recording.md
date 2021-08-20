---
title: Gestion de l’enregistrement MIDI
description: Gestion de l’enregistrement MIDI
ms.assetid: 48b2d815-72cf-4c96-8d93-247d2426b8f2
keywords:
- MIDI (Musical Instrument Digital Interface), enregistrement
- MIDI (Musical Instrument Digital Interface), enregistrement
- enregistrement d’un fichier audio MIDI, gestion
- Enregistrement MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29bf4ac85ad0cc9735a08bab3ee07d744eecb0d75308ee323ec93c1c69b1a9e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118139060"
---
# <a name="managing-midi-recording"></a>Gestion de l’enregistrement MIDI

Après avoir ouvert un appareil MIDI, vous pouvez commencer à enregistrer des données MIDI. Windows fournit les fonctions suivantes pour la gestion de l’enregistrement MIDI.



| Valeur                                      | Signification                                                                                           |
|--------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**midiInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-midiinaddbuffer) | Envoie une mémoire tampon au pilote de périphérique afin qu’il puisse être rempli avec les données MIDI exclusives système enregistrées. |
| [**midiInReset**](/windows/win32/api/mmeapi/nf-mmeapi-midiinreset)         | Arrête l’enregistrement MIDI et marque toutes les mémoires tampons en attente comme terminées.                                       |
| [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart)         | Démarre l’enregistrement MIDI et réinitialise l’horodatage à zéro.                                          |
| [**midiInStop**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstop)           | Arrête l’enregistrement MIDI.                                                                             |



 

Pour envoyer des tampons au pilote de périphérique afin d’enregistrer des messages système exclusifs, utilisez [**midiInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-midiinaddbuffer). L’application est avertie lorsque les mémoires tampons sont remplies avec des données enregistrées exclusives du système. Pour plus d’informations sur les techniques de notification, consultez [gestion des blocs de données MIDI](managing-midi-data-blocks.md).

La fonction [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) commence le processus d’enregistrement. Lors de l’enregistrement de messages système exclusifs, envoyez au moins une mémoire tampon au pilote avant de commencer l’enregistrement. Pour arrêter l’enregistrement, utilisez [**midiInStop**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstop). Avant de fermer l’appareil à l’aide de la fonction [**midiInClose**](/windows/win32/api/mmeapi/nf-mmeapi-midiinclose) , marquez les blocs de données en attente comme étant effectués en appelant [**midiInReset**](/windows/win32/api/mmeapi/nf-mmeapi-midiinreset).

Les applications qui requièrent des données horodatées utilisent une fonction de rappel pour recevoir les données MIDI. Si vos exigences de synchronisation ne sont pas strictes, vous pouvez utiliser une fenêtre ou un rappel de thread. Toutefois, vous ne pouvez pas utiliser un rappel d’événement pour recevoir des données MIDI.

Pour enregistrer des messages système exclusifs avec des applications qui n’utilisent pas de mémoires tampons de flux, vous devez fournir le pilote de périphérique avec des tampons. Ces mémoires tampons sont spécifiées à l’aide d’une structure [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Enregistrement d’un fichier audio MIDI](recording-midi-audio.md)
</dt> </dl>

 

 