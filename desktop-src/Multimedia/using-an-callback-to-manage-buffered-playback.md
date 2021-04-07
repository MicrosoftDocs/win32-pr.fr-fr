---
title: Utilisation d’un rappel d’événement pour gérer la lecture mise en mémoire tampon
description: Utilisation d’un rappel d’événement pour gérer la lecture mise en mémoire tampon
ms.assetid: 3b60daea-574d-430b-b14e-1fefceb69dfb
keywords:
- Interface MIDI (Musical Instrument Digital Interface), lecture mise en mémoire tampon
- MIDI (Musical Instrument Digital Interface), lecture mise en mémoire tampon
- lecture de fichiers MIDI, lecture en mémoire tampon
- lecture mise en mémoire tampon
- CreateEvent (fonction)
- MIDI (Musical Instrument Digital Interface), rappel d’événement
- MIDI (Musical Instrument Digital Interface), rappel d’événement
- Jeux de fichiers MIDI, rappel d’événements
- rappel d’événement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fc6f6cc7bec7971c117cb81b2f823d7184bc2fd
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725420"
---
# <a name="using-an-event-callback-to-manage-buffered-playback"></a>Utilisation d’un rappel d’événement pour gérer la lecture mise en mémoire tampon

Pour utiliser un rappel d’événement, utilisez la fonction [CreateEvent](/windows/win32/api/synchapi/nf-synchapi-createeventa) pour récupérer le handle d’un événement. Dans un appel à la fonction [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) , spécifiez \_ l’événement de rappel pour le paramètre *dwFlags* . Après avoir utilisé la fonction [**midiOutPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midioutprepareheader) mais avant d’envoyer des événements midi à l’appareil, créez un événement non signalé en appelant la fonction [ResetEvent](/windows/win32/api/synchapi/nf-synchapi-resetevent) , en spécifiant le descripteur d’événement récupéré par **CreateEvent**. Ensuite, à l’intérieur d’une boucle qui vérifie si le \_ bit MHDR Done est défini dans le membre **dwFlags** de la structure [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) , utilisez la fonction [WaitForSingleObject](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) , en spécifiant le handle d’événement et une valeur de délai d’attente infinie comme paramètres.

Un rappel d’événement est défini par tout ce qui peut provoquer un rappel de fonction.

Étant donné que les rappels d’événements ne reçoivent pas de notifications de fermeture, de fin ou d’ouverture spécifiques, une application peut avoir besoin de vérifier l’état du processus qu’il attend après l’événement. Il est possible qu’un certain nombre de tâches soient terminées par le temps que **WaitForSingleObject** retourne.

 

 