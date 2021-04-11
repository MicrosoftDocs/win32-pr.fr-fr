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
# <a name="using-a-window-or-thread-to-manage-buffered-playback"></a><span data-ttu-id="3a40c-114">Utilisation d’une fenêtre ou d’un thread pour gérer la lecture mise en mémoire tampon</span><span class="sxs-lookup"><span data-stu-id="3a40c-114">Using a Window or Thread to Manage Buffered Playback</span></span>

<span data-ttu-id="3a40c-115">Les messages suivants peuvent être envoyés à une fenêtre ou un thread pour la gestion de la lecture de messages ou de mémoires tampons de flux exclusifs système MIDI.</span><span class="sxs-lookup"><span data-stu-id="3a40c-115">The following messages can be sent to a window or thread for managing playback of MIDI system-exclusive messages or stream buffers.</span></span>



| <span data-ttu-id="3a40c-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="3a40c-116">Value</span></span>                                  | <span data-ttu-id="3a40c-117">Signification</span><span class="sxs-lookup"><span data-stu-id="3a40c-117">Meaning</span></span>                                                                                                                                                                  |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3a40c-118">**\_fermeture MOM de mm \_**</span><span class="sxs-lookup"><span data-stu-id="3a40c-118">**MM\_MOM\_CLOSE**</span></span>](mm-mom-close.md) | <span data-ttu-id="3a40c-119">Envoyé lorsque l’appareil est fermé à l’aide de la fonction [**midiOutClose**](/windows/win32/api/mmeapi/nf-mmeapi-midioutclose) .</span><span class="sxs-lookup"><span data-stu-id="3a40c-119">Sent when the device is closed by using the [**midiOutClose**](/windows/win32/api/mmeapi/nf-mmeapi-midioutclose) function.</span></span>                                                                               |
| [<span data-ttu-id="3a40c-120">**MM \_ MOM \_ terminé**</span><span class="sxs-lookup"><span data-stu-id="3a40c-120">**MM\_MOM\_DONE**</span></span>](mm-mom-done.md)   | <span data-ttu-id="3a40c-121">Envoyé lorsque le pilote de périphérique est terminé avec un bloc de données envoyé à l’aide de la fonction [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg) ou [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) .</span><span class="sxs-lookup"><span data-stu-id="3a40c-121">Sent when the device driver is finished with a data block sent by using the [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg) or [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) function.</span></span> |
| [<span data-ttu-id="3a40c-122">**\_ouverture de MOM mm \_**</span><span class="sxs-lookup"><span data-stu-id="3a40c-122">**MM\_MOM\_OPEN**</span></span>](mm-mom-open.md)   | <span data-ttu-id="3a40c-123">Envoyé lorsque l’appareil est ouvert à l’aide de la fonction [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) .</span><span class="sxs-lookup"><span data-stu-id="3a40c-123">Sent when the device is opened by using the [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) function.</span></span>                                                                                 |



 

<span data-ttu-id="3a40c-124">Un paramètre *wParam* et un paramètre *lParam* sont associés à chacun de ces messages.</span><span class="sxs-lookup"><span data-stu-id="3a40c-124">A *wParam* parameter and an *lParam* parameter are associated with each of these messages.</span></span> <span data-ttu-id="3a40c-125">Le paramètre *wParam* spécifie toujours le descripteur d’un appareil MIDI ouvert.</span><span class="sxs-lookup"><span data-stu-id="3a40c-125">The *wParam* parameter always specifies the handle of an open MIDI device.</span></span> <span data-ttu-id="3a40c-126">Pour [**la \_ \_ fin de mm MOM**](mm-mom-done.md), *lParam* spécifie une adresse d’une structure [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) identifiant le bloc de données terminé.</span><span class="sxs-lookup"><span data-stu-id="3a40c-126">For [**MM\_MOM\_DONE**](mm-mom-done.md), *lParam* specifies an address of a [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure identifying the completed data block.</span></span> <span data-ttu-id="3a40c-127">Le paramètre *lParam* n’est pas utilisé pour la [**\_ \_ fermeture de MOM mm**](mm-mom-close.md) et l' [**\_ \_ ouverture de MOM**](mm-mom-open.md).</span><span class="sxs-lookup"><span data-stu-id="3a40c-127">The *lParam* parameter is unused for [**MM\_MOM\_CLOSE**](mm-mom-close.md) and [**MM\_MOM\_OPEN**](mm-mom-open.md).</span></span>

<span data-ttu-id="3a40c-128">Le message le plus utile est probablement un \_ MOM \_ terminé.</span><span class="sxs-lookup"><span data-stu-id="3a40c-128">The most useful message is probably MM\_MOM\_DONE.</span></span> <span data-ttu-id="3a40c-129">À moins que vous n’ayez besoin d’allouer de la mémoire ou d’initialiser des variables, il est probable que vous n’avez pas besoin de traiter l' \_ ouverture de MOM \_ et la fermeture de \_ Microsoft mm \_ .</span><span class="sxs-lookup"><span data-stu-id="3a40c-129">Unless you need to allocate memory or initialize variables, you probably do not need to process MM\_MOM\_OPEN and MM\_MOM\_CLOSE.</span></span> <span data-ttu-id="3a40c-130">Lorsque la lecture d’un bloc de données est terminée, vous pouvez nettoyer et libérer le bloc de données.</span><span class="sxs-lookup"><span data-stu-id="3a40c-130">When playback of a data block is complete, you can clean up and free the data block.</span></span>

 

 