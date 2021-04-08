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
# <a name="using-an-event-callback-to-process-driver-messages"></a><span data-ttu-id="aca8f-109">Utilisation d’un rappel d’événement pour traiter des messages de pilote</span><span class="sxs-lookup"><span data-stu-id="aca8f-109">Using an Event Callback to Process Driver Messages</span></span>

<span data-ttu-id="aca8f-110">Pour utiliser un rappel d’événement, utilisez la fonction [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa) pour créer un événement de réinitialisation manuelle.</span><span class="sxs-lookup"><span data-stu-id="aca8f-110">To use an event callback, use the [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa) function to create a manual-reset event.</span></span> <span data-ttu-id="aca8f-111">Dans l’appel à la fonction [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) , spécifiez l' **\_ événement de rappel** pour le paramètre *fdwOpen* .</span><span class="sxs-lookup"><span data-stu-id="aca8f-111">In the call to the [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) function, specify **CALLBACK\_EVENT** for the *fdwOpen* parameter.</span></span> <span data-ttu-id="aca8f-112">Après avoir appelé la fonction [**waveOutPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutprepareheader) , mais avant d’envoyer des données Waveform-Audio à l’appareil, placez l’événement dans un État non signalé en appelant la fonction [**ResetEvent**](/windows/desktop/api/synchapi/nf-synchapi-resetevent) .</span><span class="sxs-lookup"><span data-stu-id="aca8f-112">After you call the [**waveOutPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutprepareheader) function, but before sending waveform-audio data to the device, put the event into a nonsignaled state by calling the [**ResetEvent**](/windows/desktop/api/synchapi/nf-synchapi-resetevent) function.</span></span> <span data-ttu-id="aca8f-113">Ensuite, à l’intérieur d’une boucle qui vérifie si l’indicateur **\_ done WHDR** est défini dans le membre **DwFlags** de la structure [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) , appelez la fonction [WaitForSingleObject](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) , en spécifiant comme paramètres le handle d’événement et une valeur de délai d’attente.</span><span class="sxs-lookup"><span data-stu-id="aca8f-113">Then, inside a loop that checks whether the **WHDR\_DONE** flag is set in the **dwFlags** member of the [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure, call the [WaitForSingleObject](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) function, specifying as parameters the event handle and a time-out value.</span></span>

<span data-ttu-id="aca8f-114">Étant donné que les rappels d’événements ne reçoivent pas de notifications de fermeture, de fin ou d’ouverture spécifiques, une application peut être obligée de vérifier l’état du processus qu’il attend après l’événement.</span><span class="sxs-lookup"><span data-stu-id="aca8f-114">Because event callbacks do not receive specific close, done, or open notifications, an application might have to check the status of the process it is waiting for after the event occurs.</span></span> <span data-ttu-id="aca8f-115">Il est possible qu’un certain nombre de tâches aient été effectuées par le temps que [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) retourne.</span><span class="sxs-lookup"><span data-stu-id="aca8f-115">It is possible that a number of tasks could have been completed by the time [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) returns.</span></span>

## <a name="related-topics"></a><span data-ttu-id="aca8f-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="aca8f-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aca8f-117">Blocs de données audio</span><span class="sxs-lookup"><span data-stu-id="aca8f-117">Audio Data Blocks</span></span>](audio-data-blocks.md)
</dt> </dl>

 

 