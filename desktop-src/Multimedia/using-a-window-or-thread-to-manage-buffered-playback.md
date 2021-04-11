---
title: Utilisation d’une fenêtre ou d’un thread pour gérer la lecture mise en mémoire tampon
description: Utilisation d’une fenêtre ou d’un thread pour gérer la lecture mise en mémoire tampon
ms.assetid: 3c8145a8-e56a-449d-ad45-2ae016f79697
keywords:
- Interface MIDI (Musical Instrument Digital Interface), lecture mise en mémoire tampon
- MIDI (Musical Instrument Digital Interface), lecture mise en mémoire tampon
- lecture de fichiers MIDI, lecture en mémoire tampon
- lecture mise en mémoire tampon
- Message MM_MOM_CLOSE
- Message MM_MOM_DONE
- Message MM_MOM_OPEN
- MIDI (Musical Instrument Digital Interface), envoi de messages
- MIDI (Musical Instrument Digital Interface), envoi de messages
- Jeux de fichiers MIDI, envoi de messages
- envoi de messages MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c8c120504a4a25ddcf01474db341a367a2e9854
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104315012"
---
# <a name="using-a-window-or-thread-to-manage-buffered-playback"></a>Utilisation d’une fenêtre ou d’un thread pour gérer la lecture mise en mémoire tampon

Les messages suivants peuvent être envoyés à une fenêtre ou un thread pour la gestion de la lecture de messages ou de mémoires tampons de flux exclusifs système MIDI.



| Valeur                                  | Signification                                                                                                                                                                  |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_fermeture MOM de mm \_**](mm-mom-close.md) | Envoyé lorsque l’appareil est fermé à l’aide de la fonction [**midiOutClose**](/windows/win32/api/mmeapi/nf-mmeapi-midioutclose) .                                                                               |
| [**MM \_ MOM \_ terminé**](mm-mom-done.md)   | Envoyé lorsque le pilote de périphérique est terminé avec un bloc de données envoyé à l’aide de la fonction [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg) ou [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) . |
| [**\_ouverture de MOM mm \_**](mm-mom-open.md)   | Envoyé lorsque l’appareil est ouvert à l’aide de la fonction [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) .                                                                                 |



 

Un paramètre *wParam* et un paramètre *lParam* sont associés à chacun de ces messages. Le paramètre *wParam* spécifie toujours le descripteur d’un appareil MIDI ouvert. Pour [**la \_ \_ fin de mm MOM**](mm-mom-done.md), *lParam* spécifie une adresse d’une structure [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) identifiant le bloc de données terminé. Le paramètre *lParam* n’est pas utilisé pour la [**\_ \_ fermeture de MOM mm**](mm-mom-close.md) et l' [**\_ \_ ouverture de MOM**](mm-mom-open.md).

Le message le plus utile est probablement un \_ MOM \_ terminé. À moins que vous n’ayez besoin d’allouer de la mémoire ou d’initialiser des variables, il est probable que vous n’avez pas besoin de traiter l' \_ ouverture de MOM \_ et la fermeture de \_ Microsoft mm \_ . Lorsque la lecture d’un bloc de données est terminée, vous pouvez nettoyer et libérer le bloc de données.

 

 