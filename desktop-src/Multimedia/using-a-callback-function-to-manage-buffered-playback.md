---
title: Utilisation d’une fonction de rappel pour gérer la lecture mise en mémoire tampon
description: Utilisation d’une fonction de rappel pour gérer la lecture mise en mémoire tampon
ms.assetid: aaaf9c5f-c9b2-4e55-a4c1-28c99cc03945
keywords:
- Interface MIDI (Musical Instrument Digital Interface), lecture mise en mémoire tampon
- MIDI (Musical Instrument Digital Interface), lecture mise en mémoire tampon
- lecture de fichiers MIDI, lecture en mémoire tampon
- lecture mise en mémoire tampon
- Message MOM_CLOSE
- Message MOM_DONE
- Message MOM_OPEN
- MIDI (Musical Instrument Digital Interface), envoi de messages
- MIDI (Musical Instrument Digital Interface), envoi de messages
- Jeux de fichiers MIDI, envoi de messages
- envoi de messages MIDI
- MIDI (Musical Instrument Digital Interface), fonctions de rappel
- MIDI (Musical Instrument Digital Interface), fonctions de rappel
- Jeux de fichiers MIDI, fonctions de rappel
- MidiOutProc fonction de rappel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bccccd8e5fb052b89e8ca1804b89de6da26cd5b7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127238541"
---
# <a name="using-a-callback-function-to-manage-buffered-playback"></a>Utilisation d’une fonction de rappel pour gérer la lecture mise en mémoire tampon

Vous pouvez définir votre propre fonction de rappel pour gérer la lecture en mémoire tampon des appareils de sortie MIDI. La fonction de rappel est documentée en tant que [**MidiOutProc**](/previous-versions//dd798478(v=vs.85)).

Les messages suivants peuvent être envoyés au paramètre *wMsg* de la fonction de rappel **MidiOutProc** .



| Valeur                           | Signification                                                                                                                                                                  |
|---------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_fermeture MOM**](mom-close.md) | Envoyé lorsque l’appareil est fermé à l’aide de la fonction [**midiOutClose**](/windows/win32/api/mmeapi/nf-mmeapi-midioutclose) .                                                                               |
| [**MOM \_ terminé**](mom-done.md)   | Envoyé lorsque le pilote de périphérique est terminé avec un bloc de données envoyé à l’aide de la fonction [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg) ou [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) . |
| [**MOM \_ ouvert**](mom-open.md)   | Envoyé lorsque l’appareil est ouvert à l’aide de la fonction [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) .                                                                                 |



 

Ces messages sont similaires à ceux envoyés aux fonctions de procédure de fenêtre, mais les paramètres sont différents. Un handle de l’appareil MIDI ouvert est passé en tant que paramètre à la fonction de rappel, avec le mot double des données d’instance passées à l’aide de **midiOutOpen**.

Une fois le pilote terminé avec un bloc de données, vous pouvez nettoyer et libérer le bloc de données. En raison des restrictions suggérées sur les fonctions de rappel, il est préférable de ne pas le faire à partir de la fonction de rappel.

 

 