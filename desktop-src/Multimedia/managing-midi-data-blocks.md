---
title: Gestion des blocs de données MIDI
description: Gestion des blocs de données MIDI
ms.assetid: f29fbc08-ef67-489c-aedf-5a2bc65233f7
keywords:
- Interface MIDI (Musical Instrument Digital Interface), gestion des blocs de données
- MIDI (Musical Instrument Digital Interface), gestion des blocs de données
- Services MIDI, gestion des blocs de données
- gestion des blocs de données MIDI
- MIDI (Musical Instrument Digital Interface), traitement des messages de pilote
- MIDI (Musical Instrument Digital Interface), traitement des messages de pilote
- Services MIDI, traitement des messages de pilote
- traitement des messages du pilote
- MIDI (Musical Instrument Digital Interface), blocs de données
- MIDI (Musical Instrument Digital Interface), blocs de données
- Services MIDI, blocs de données
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af348d6c53d2944bf22c026674704baa1fe74e07
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124364399"
---
# <a name="managing-midi-data-blocks"></a>Gestion des blocs de données MIDI

Les applications qui utilisent des blocs de données pour transmettre des messages système exclusifs (à l’aide des fonctions [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg) et [**midiInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-midiinaddbuffer) ) et des mémoires tampons de flux (à l’aide de la fonction [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) ) doivent continuellement fournir au pilote de périphérique des blocs de données jusqu’à la fin de la lecture ou de l’enregistrement.

Même si un bloc de données unique est utilisé, une application doit être en mesure de déterminer à quel moment un pilote de périphérique est terminé avec le bloc de données afin de libérer la mémoire associée au bloc de données et à la structure d’en-tête. Trois méthodes peuvent être utilisées pour déterminer quand un pilote de périphérique est terminé avec un bloc de données :

-   Spécifiez une fonction de rappel pour recevoir un message envoyé par le pilote lorsqu’il a terminé avec un bloc de données. Pour obtenir des données d’entrée MIDI horodatées, vous devez utiliser une fonction de rappel.
-   Utilisez un rappel d’événement (pour la sortie uniquement).
-   Utilisez un rappel de fenêtre ou de thread pour recevoir un message envoyé par le pilote lorsqu’il a terminé avec un bloc de données.

Si une application n’obtient pas de bloc de données au pilote de périphérique quand cela est nécessaire, un décalage audible de lecture ou une perte d’informations d’enregistrement entrantes peut se produire. Au minimum, une application doit utiliser un schéma de double mise en mémoire tampon pour conserver au moins un bloc de données avant le pilote de périphérique.

## <a name="using-a-callback-function-to-process-driver-messages"></a>Utilisation d’une fonction de rappel pour traiter des messages de pilote

Vous pouvez écrire votre propre fonction de rappel pour traiter les messages envoyés par le pilote de périphérique. Pour utiliser une fonction de rappel, spécifiez l’indicateur de fonction de rappel \_ dans le paramètre *dwFlags* et l’adresse de la fonction de rappel dans le paramètre *DwCallback* de la fonction [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) ou [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) .

Les messages envoyés à une fonction de rappel sont similaires aux messages envoyés à une fenêtre, sauf qu’ils ont deux paramètres de mot double au lieu d’un paramètre entier non signé et d’un paramètre de type double. Pour plus d’informations sur ces messages, consultez [envoi de messages System-Exclusive](sending-system-exclusive-messages.md) et [gestion de l’enregistrement midi](managing-midi-recording.md).

Utilisez l’une des techniques suivantes pour passer des données d’instance d’une application à une fonction de rappel :

-   Utilisez le paramètre *dwCallbackInstance* de la fonction qui ouvre le pilote de périphérique.
-   Utilisez le membre **dwUser** de la structure [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) qui identifie un bloc de données envoyé à un pilote de périphérique MIDI.

Si vous avez besoin de plus de 32 bits de données d’instance, transmettez l’adresse d’une structure contenant les informations supplémentaires.

## <a name="using-an-event-callback-to-process-driver-messages"></a>Utilisation d’un rappel d’événement pour traiter des messages de pilote

Pour utiliser un rappel d’événement, utilisez la fonction [CreateEvent](/windows/win32/api/synchapi/nf-synchapi-createeventa) pour récupérer le handle d’un événement et spécifiez l’événement de rappel \_ dans l’appel à la fonction [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) .

Un rappel d’événement est défini par tout ce qui peut provoquer un rappel de fonction. Contrairement aux fonctions de rappel et aux rappels de fenêtre ou de thread, les rappels d’événements ne reçoivent pas de notifications de fermeture, de fin ou d’ouverture spécifiques. Par conséquent, une application peut être amenée à vérifier l’état du processus en attente lorsque l’événement se produit.

Pour plus d’informations sur les rappels d’événements, consultez [utilisation d’un rappel d’événement pour gérer la lecture mise en mémoire tampon](using-an-callback-to-manage-buffered-playback.md).

## <a name="using-a-window-or-thread-callback-to-process-driver-messages"></a>Utilisation d’une fenêtre ou d’un rappel de thread pour traiter des messages de pilote

Pour utiliser un rappel de fenêtre, spécifiez l' \_ indicateur de fenêtre de rappel dans le paramètre *dwFlags* et un handle de fenêtre dans le mot de poids faible du paramètre *DwCallback* de la fonction [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) ou [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) . Les messages de pilote seront envoyés à la fonction de procédure de fenêtre pour la fenêtre identifiée par le handle dans *dwCallback*.

De même, pour utiliser un rappel de thread, spécifiez l’indicateur de thread de rappel \_ et un identificateur de thread dans l’appel à **MidiInOpen** ou **midiOutOpen**. Dans ce cas, les messages sont publiés dans le thread spécifié et non dans une fenêtre.

Les messages envoyés à une fenêtre ou un rappel de thread sont spécifiques au périphérique MIDI utilisé. Pour plus d’informations sur ces messages, consultez [envoi de messages System-Exclusive](sending-system-exclusive-messages.md) et [gestion de l’enregistrement midi](managing-midi-recording.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Services MIDI](midi-services.md)
</dt> </dl>

 

 