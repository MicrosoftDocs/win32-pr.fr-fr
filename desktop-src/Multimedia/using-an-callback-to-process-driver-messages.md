---
title: Utilisation d’un rappel d’événement pour traiter des messages de pilote
description: Utilisation d’un rappel d’événement pour traiter des messages de pilote
ms.assetid: 5b17ff93-ed00-46ee-828c-baf716c9257c
keywords:
- audio Wave, rappel d’événement
- blocs de données audio, rappel d’événement
- audio Wave, traitement des messages de pilote
- blocs de données audio, traitement des messages de pilote
- traitement des messages du pilote
- CreateEvent (fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cbfeb95fcf0e5d83f9a54fc0cf3cd223ac6ce19
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725413"
---
# <a name="using-an-event-callback-to-process-driver-messages"></a>Utilisation d’un rappel d’événement pour traiter des messages de pilote

Pour utiliser un rappel d’événement, utilisez la fonction [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa) pour créer un événement de réinitialisation manuelle. Dans l’appel à la fonction [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) , spécifiez l' **\_ événement de rappel** pour le paramètre *fdwOpen* . Après avoir appelé la fonction [**waveOutPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutprepareheader) , mais avant d’envoyer des données Waveform-Audio à l’appareil, placez l’événement dans un État non signalé en appelant la fonction [**ResetEvent**](/windows/desktop/api/synchapi/nf-synchapi-resetevent) . Ensuite, à l’intérieur d’une boucle qui vérifie si l’indicateur **\_ done WHDR** est défini dans le membre **DwFlags** de la structure [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) , appelez la fonction [WaitForSingleObject](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) , en spécifiant comme paramètres le handle d’événement et une valeur de délai d’attente.

Étant donné que les rappels d’événements ne reçoivent pas de notifications de fermeture, de fin ou d’ouverture spécifiques, une application peut être obligée de vérifier l’état du processus qu’il attend après l’événement. Il est possible qu’un certain nombre de tâches aient été effectuées par le temps que [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) retourne.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Blocs de données audio](audio-data-blocks.md)
</dt> </dl>

 

 