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
ms.openlocfilehash: 24214dd3f6cd13ca034b2555398f6055e4ce2da1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103940883"
---
# <a name="managing-midi-thru"></a>Gestion de MIDI via

Vous pouvez connecter un périphérique d’entrée MIDI directement à un périphérique de sortie MIDI afin que, lorsque l’appareil d’entrée reçoit un message MIM, le système envoie un message avec les mêmes données d’événement MIDI au pilote de périphérique de sortie. [**\_**](mim-data.md) Pour connecter un périphérique de sortie MIDI à un périphérique d’entrée MIDI, utilisez la fonction [**midiConnect**](/windows/win32/api/mmeapi/nf-mmeapi-midiconnect) .

Pour obtenir les meilleures performances possibles avec plusieurs sorties, une application peut choisir de fournir une forme spéciale de pilote de sortie MIDI, appelée *pilote via*. Bien que le système autorise un seul périphérique de sortie MIDI à être connecté à un périphérique d’entrée MIDI, plusieurs périphériques de sortie MIDI peuvent être connectés à un pilote via. Une application sur un système de ce type peut connecter l’appareil d’entrée MIDI à ce périphérique et connecter l’appareil MIDI à autant d’appareils de sortie MIDI que nécessaire. Pour plus d’informations sur les pilotes, consultez la documentation relative au pilote de périphérique Windows.

## <a name="using-messages-to-manage-midi-recording"></a>Utilisation de messages pour gérer l’enregistrement MIDI

Les messages suivants peuvent être envoyés à une procédure de rappel de fenêtre ou de thread pour la gestion de l’enregistrement MIDI.



| Valeur                                          | Signification                                                                                                                                |
|------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**MM \_ MIM \_ proche**](mm-mim-close.md)         | Envoyé lorsqu’un périphérique d’entrée MIDI est fermé à l’aide de la fonction [**midiInClose**](/windows/win32/api/mmeapi/nf-mmeapi-midiinclose) .                                      |
| [**MM \_ \_ données MIM**](mm-mim-data.md)           | Envoyé lors de la réception d’un message MIDI complet. (Ce message est utilisé pour tous les messages MIDI, à l’exception des messages System-exclusive).          |
| [**MM \_ \_ erreur MIM**](mm-mim-error.md)         | Envoyé lors de la réception d’un message MIDI non valide. (Ce message est utilisé pour tous les messages MIDI, à l’exception des messages System-exclusive).          |
| [**MM \_ \_ LONGDATA MIM**](mm-mim-longdata.md)   | Envoyé lorsqu’un message MIDI système exclusif complet est reçu ou lorsqu’une mémoire tampon a été remplie avec des données système exclusives.     |
| [**MM \_ \_ LONGERROR MIM**](mm-mim-longerror.md) | Envoyé lors de la réception d’un message de système d’exclusivité MIDI non valide.                                                                        |
| [**MM \_ \_ MOREDATA MIM**](mm-mim-moredata.md)   | Envoyé lorsqu’une application ne traite pas les messages de [**\_ données MIM**](mim-data.md) suffisamment rapidement pour suivre le pilote de périphérique d’entrée. |
| [**MM \_ MIM \_ ouvert**](mm-mim-open.md)           | Envoyé lorsqu’un périphérique d’entrée MIDI est ouvert à l’aide de la fonction [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) .                                        |



 

Un paramètre *wParam* et un paramètre *lParam* sont associés à chacun de ces messages. Le paramètre *wParam* spécifie toujours le descripteur d’un appareil MIDI ouvert. Le paramètre *lParam* n’est pas utilisé pour les messages d’ouverture MIM de [**\_ \_ fermeture**](mm-mim-close.md) et [**mm \_ MIM \_**](mm-mim-open.md) .

Pour le message [**mm \_ MIM \_ LONGDATA**](mm-mim-longdata.md) , *lpMidiHdr* spécifie l’adresse d’une structure [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) qui identifie la mémoire tampon pour les messages système-exclusifs. La mémoire tampon ne peut pas être complètement remplie, car la taille des messages système exclusifs n’est généralement pas connue avant d’être enregistrée et parce que les tampons dont la taille totale peut contenir le plus grand message attendu doivent être alloués. Pour déterminer la quantité de données valides présentes dans la mémoire tampon, utilisez le membre **dwBytesRecorded** de la structure **MIDIHDR** .

## <a name="using-a-callback-function-to-manage-midi-recording"></a>Utilisation d’une fonction de rappel pour gérer l’enregistrement MIDI

Vous pouvez définir votre propre fonction de rappel pour gérer l’enregistrement des périphériques d’entrée MIDI. La fonction de rappel est documentée en tant que [**MidiInProc**](/previous-versions//dd798460(v=vs.85)).

Les messages suivants peuvent être envoyés au paramètre *wMsg* de la fonction de rappel **MidiInProc** .



| Valeur                                   | Signification                                                                                                                                |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**\_fermeture MIM**](mim-close.md)         | Envoyé lorsque l’appareil est fermé à l’aide de la fonction [**midiInClose**](/windows/win32/api/mmeapi/nf-mmeapi-midiinclose) .                                               |
| [**\_données MIM**](mim-data.md)           | Envoyé lors de la réception d’un message MIDI complet (ce message est utilisé pour tous les messages MIDI, à l’exception des messages System-exclusive).           |
| [**\_erreur MIM**](mim-error.md)         | Envoyé lors de la réception d’un message MIDI non valide (ce message est utilisé pour tous les messages MIDI, à l’exception des messages System-exclusive).           |
| [**\_LONGDATA MIM**](mim-longdata.md)   | Envoyé lorsqu’un message MIDI système exclusif complet est reçu ou lorsqu’une mémoire tampon a été remplie avec des données système exclusives.     |
| [**\_LONGERROR MIM**](mim-longerror.md) | Envoyé lors de la réception d’un message de système d’exclusivité MIDI non valide.                                                                        |
| [**\_MOREDATA MIM**](mim-moredata.md)   | Envoyé lorsqu’une application ne traite pas les messages de [**\_ données MIM**](mim-data.md) suffisamment rapidement pour suivre le pilote de périphérique d’entrée. |
| [**MIM \_ ouvert**](mim-open.md)           | Envoyé lorsque l’appareil d’entrée MIDI est ouvert à l’aide de la fonction [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) .                                      |



 

Ces messages sont similaires à ceux envoyés aux fonctions de procédure de fenêtre, mais les paramètres sont différents. Un handle de l’appareil MIDI ouvert est passé en tant que paramètre à la fonction de rappel, avec le mot double des données d’instance qui a été passé à l’aide de **midiInOpen**.

Pour le message [**MIM \_ LONGDATA**](mim-longdata.md) , *lpMidiHdr* spécifie l’adresse d’une structure [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) qui identifie la mémoire tampon pour les messages System-exclusives. La mémoire tampon n’est peut-être pas complètement remplie. Pour déterminer la quantité de données valides présentes dans la mémoire tampon, utilisez le membre **dwBytesRecorded** de la structure **MIDIHDR** .

Une fois que le pilote de périphérique est terminé par un bloc de données, vous pouvez nettoyer et libérer le bloc de données.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Enregistrement d’un fichier audio MIDI](recording-midi-audio.md)
</dt> </dl>

 

 