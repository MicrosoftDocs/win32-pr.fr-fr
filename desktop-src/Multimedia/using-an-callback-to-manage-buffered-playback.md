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
# <a name="using-an-event-callback-to-manage-buffered-playback"></a><span data-ttu-id="46ad0-112">Utilisation d’un rappel d’événement pour gérer la lecture mise en mémoire tampon</span><span class="sxs-lookup"><span data-stu-id="46ad0-112">Using an Event Callback to Manage Buffered Playback</span></span>

<span data-ttu-id="46ad0-113">Pour utiliser un rappel d’événement, utilisez la fonction [CreateEvent](/windows/win32/api/synchapi/nf-synchapi-createeventa) pour récupérer le handle d’un événement.</span><span class="sxs-lookup"><span data-stu-id="46ad0-113">To use an event callback, use the [CreateEvent](/windows/win32/api/synchapi/nf-synchapi-createeventa) function to retrieve the handle of an event.</span></span> <span data-ttu-id="46ad0-114">Dans un appel à la fonction [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) , spécifiez \_ l’événement de rappel pour le paramètre *dwFlags* .</span><span class="sxs-lookup"><span data-stu-id="46ad0-114">In a call to the [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) function, specify CALLBACK\_EVENT for the *dwFlags* parameter.</span></span> <span data-ttu-id="46ad0-115">Après avoir utilisé la fonction [**midiOutPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midioutprepareheader) mais avant d’envoyer des événements midi à l’appareil, créez un événement non signalé en appelant la fonction [ResetEvent](/windows/win32/api/synchapi/nf-synchapi-resetevent) , en spécifiant le descripteur d’événement récupéré par **CreateEvent**.</span><span class="sxs-lookup"><span data-stu-id="46ad0-115">After using the [**midiOutPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midioutprepareheader) function but before sending MIDI events to the device, create a nonsignaled event by calling the [ResetEvent](/windows/win32/api/synchapi/nf-synchapi-resetevent) function, specifying the event handle retrieved by **CreateEvent**.</span></span> <span data-ttu-id="46ad0-116">Ensuite, à l’intérieur d’une boucle qui vérifie si le \_ bit MHDR Done est défini dans le membre **dwFlags** de la structure [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) , utilisez la fonction [WaitForSingleObject](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) , en spécifiant le handle d’événement et une valeur de délai d’attente infinie comme paramètres.</span><span class="sxs-lookup"><span data-stu-id="46ad0-116">Then, inside a loop that checks whether the MHDR\_DONE bit is set in the **dwFlags** member of the [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure, use the [WaitForSingleObject](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) function, specifying the event handle and a time-out value of INFINITE as parameters.</span></span>

<span data-ttu-id="46ad0-117">Un rappel d’événement est défini par tout ce qui peut provoquer un rappel de fonction.</span><span class="sxs-lookup"><span data-stu-id="46ad0-117">An event callback is set by anything that might cause a function callback.</span></span>

<span data-ttu-id="46ad0-118">Étant donné que les rappels d’événements ne reçoivent pas de notifications de fermeture, de fin ou d’ouverture spécifiques, une application peut avoir besoin de vérifier l’état du processus qu’il attend après l’événement.</span><span class="sxs-lookup"><span data-stu-id="46ad0-118">Because event callbacks do not receive specific close, done, or open notifications, an application may need to check the status of the process it is waiting for after the event occurs.</span></span> <span data-ttu-id="46ad0-119">Il est possible qu’un certain nombre de tâches soient terminées par le temps que **WaitForSingleObject** retourne.</span><span class="sxs-lookup"><span data-stu-id="46ad0-119">It is possible that a number of tasks could be completed by the time **WaitForSingleObject** returns.</span></span>

 

 