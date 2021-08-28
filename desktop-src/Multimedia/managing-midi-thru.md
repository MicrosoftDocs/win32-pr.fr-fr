---
title: Gestion de MIDI via
description: Gestion de MIDI via
ms.assetid: ba03a2a1-d998-498d-ad53-027ba2b6e276
keywords:
- Interface MIDI (Musical Instrument Digital Interface), via le pilote
- MIDI (Musical Instrument Digital Interface), via le pilote
- enregistrement de l’audio MIDI, via le pilote
- Pilote MIDI via
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c108ac13fbbfb80d1f7c41960984c904374db31e3a790f14c326cf9e7946dac9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118138942"
---
# <a name="managing-midi-thru"></a>Gestion de MIDI via

vous pouvez connecter un périphérique d’entrée midi directement à un périphérique de sortie midi afin que, lorsque l’appareil d’entrée reçoit un message de [**\_ données MIM**](mim-data.md) , le système envoie un message avec les mêmes données d’événement MIDI au pilote de périphérique de sortie. Pour connecter un périphérique de sortie MIDI à un périphérique d’entrée MIDI, utilisez la fonction [**midiConnect**](/windows/win32/api/mmeapi/nf-mmeapi-midiconnect) .

Pour obtenir les meilleures performances possibles avec plusieurs sorties, une application peut choisir de fournir une forme spéciale de pilote de sortie MIDI, appelée *pilote via*. Bien que le système autorise un seul périphérique de sortie MIDI à être connecté à un périphérique d’entrée MIDI, plusieurs périphériques de sortie MIDI peuvent être connectés à un pilote via. Une application sur un système de ce type peut connecter l’appareil d’entrée MIDI à ce périphérique et connecter l’appareil MIDI à autant d’appareils de sortie MIDI que nécessaire. pour plus d’informations sur les pilotes, consultez la documentation Windows device-driver.

## <a name="using-messages-to-manage-midi-recording"></a>Utilisation de messages pour gérer l’enregistrement MIDI

Les messages suivants peuvent être envoyés à une procédure de rappel de fenêtre ou de thread pour la gestion de l’enregistrement MIDI.



| Valeur                                          | Signification                                                                                                                                |
|------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**MM \_ MIM \_ fermer**](mm-mim-close.md)         | Envoyé lorsqu’un périphérique d’entrée MIDI est fermé à l’aide de la fonction [**midiInClose**](/windows/win32/api/mmeapi/nf-mmeapi-midiinclose) .                                      |
| [**MM \_ MIM \_ données**](mm-mim-data.md)           | Envoyé lors de la réception d’un message MIDI complet. (Ce message est utilisé pour tous les messages MIDI, à l’exception des messages System-exclusive).          |
| [**MM \_ MIM \_ erreur**](mm-mim-error.md)         | Envoyé lors de la réception d’un message MIDI non valide. (Ce message est utilisé pour tous les messages MIDI, à l’exception des messages System-exclusive).          |
| [**MM \_ MIM \_ LONGDATA**](mm-mim-longdata.md)   | Envoyé lorsqu’un message MIDI système exclusif complet est reçu ou lorsqu’une mémoire tampon a été remplie avec des données système exclusives.     |
| [**MM \_ MIM \_ LONGERROR**](mm-mim-longerror.md) | Envoyé lors de la réception d’un message de système d’exclusivité MIDI non valide.                                                                        |
| [**MM \_ MIM \_ MOREDATA**](mm-mim-moredata.md)   | envoyé lorsqu’une application ne traite pas [**MIM \_**](mim-data.md) messages de données suffisamment rapidement pour suivre le pilote de périphérique d’entrée. |
| [**MM \_ MIM \_ ouverts**](mm-mim-open.md)           | Envoyé lorsqu’un périphérique d’entrée MIDI est ouvert à l’aide de la fonction [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) .                                        |



 

Un paramètre *wParam* et un paramètre *lParam* sont associés à chacun de ces messages. Le paramètre *wParam* spécifie toujours le descripteur d’un appareil MIDI ouvert. le paramètre *lParam* est inutilisé pour les [**\_ MIM mm \_**](mm-mim-close.md) et [**mm MIM des messages \_ \_ ouverts**](mm-mim-open.md) .

pour le message [**MM \_ MIM \_ LONGDATA**](mm-mim-longdata.md) , *lpMidiHdr* spécifie l’adresse d’une structure [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) qui identifie la mémoire tampon pour les messages système-exclusifs. La mémoire tampon ne peut pas être complètement remplie, car la taille des messages système exclusifs n’est généralement pas connue avant d’être enregistrée et parce que les tampons dont la taille totale peut contenir le plus grand message attendu doivent être alloués. Pour déterminer la quantité de données valides présentes dans la mémoire tampon, utilisez le membre **dwBytesRecorded** de la structure **MIDIHDR** .

## <a name="using-a-callback-function-to-manage-midi-recording"></a>Utilisation d’une fonction de rappel pour gérer l’enregistrement MIDI

Vous pouvez définir votre propre fonction de rappel pour gérer l’enregistrement des périphériques d’entrée MIDI. La fonction de rappel est documentée en tant que [**MidiInProc**](/previous-versions//dd798460(v=vs.85)).

Les messages suivants peuvent être envoyés au paramètre *wMsg* de la fonction de rappel **MidiInProc** .



| Valeur                                   | Signification                                                                                                                                |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**MIM \_ PLUS**](mim-close.md)         | Envoyé lorsque l’appareil est fermé à l’aide de la fonction [**midiInClose**](/windows/win32/api/mmeapi/nf-mmeapi-midiinclose) .                                               |
| [**MIM \_ MÉTADONNÉE**](mim-data.md)           | Envoyé lors de la réception d’un message MIDI complet (ce message est utilisé pour tous les messages MIDI, à l’exception des messages System-exclusive).           |
| [**MIM \_ Erreurs**](mim-error.md)         | Envoyé lors de la réception d’un message MIDI non valide (ce message est utilisé pour tous les messages MIDI, à l’exception des messages System-exclusive).           |
| [**MIM \_ LONGDATA**](mim-longdata.md)   | Envoyé lorsqu’un message MIDI système exclusif complet est reçu ou lorsqu’une mémoire tampon a été remplie avec des données système exclusives.     |
| [**MIM \_ LONGERROR**](mim-longerror.md) | Envoyé lors de la réception d’un message de système d’exclusivité MIDI non valide.                                                                        |
| [**MIM \_ MOREDATA**](mim-moredata.md)   | envoyé lorsqu’une application ne traite pas [**MIM \_**](mim-data.md) messages de données suffisamment rapidement pour suivre le pilote de périphérique d’entrée. |
| [**MIM \_ AFFICHER**](mim-open.md)           | Envoyé lorsque l’appareil d’entrée MIDI est ouvert à l’aide de la fonction [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) .                                      |



 

Ces messages sont similaires à ceux envoyés aux fonctions de procédure de fenêtre, mais les paramètres sont différents. Un handle de l’appareil MIDI ouvert est passé en tant que paramètre à la fonction de rappel, avec le mot double des données d’instance qui a été passé à l’aide de **midiInOpen**.

pour le message [**MIM \_ LONGDATA**](mim-longdata.md) , *lpMidiHdr* spécifie l’adresse d’une structure [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) qui identifie la mémoire tampon pour les messages system-exclusives. La mémoire tampon n’est peut-être pas complètement remplie. Pour déterminer la quantité de données valides présentes dans la mémoire tampon, utilisez le membre **dwBytesRecorded** de la structure **MIDIHDR** .

Une fois que le pilote de périphérique est terminé par un bloc de données, vous pouvez nettoyer et libérer le bloc de données.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Enregistrement d’un fichier audio MIDI](recording-midi-audio.md)
</dt> </dl>

 

 