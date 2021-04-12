---
title: Format de mémoire tampon de flux
description: Format de mémoire tampon de flux
ms.assetid: 4b24c12e-b43f-492e-a000-af4f59d5e16f
keywords:
- MIDI (Musical Instrument Digital Interface), mémoires tampons de flux
- MIDI (Musical Instrument Digital Interface), mémoires tampons de flux
- mémoires tampons de flux, format
- MIDIHDR, structure
- MIDIEVENT, structure
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 801a7f0dbeabd0d7aebeae0387af415a831e4658
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104381785"
---
# <a name="stream-buffer-format"></a><span data-ttu-id="e6c43-108">Format de mémoire tampon de flux</span><span class="sxs-lookup"><span data-stu-id="e6c43-108">Stream Buffer Format</span></span>

<span data-ttu-id="e6c43-109">Le membre **lpData** de la structure [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) pointe vers une mémoire tampon de flux, et le membre **dwBufferLength** spécifie la taille réelle de cette mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="e6c43-109">The **lpData** member of the [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure points to a stream buffer, and the **dwBufferLength** member specifies the actual size of this buffer.</span></span> <span data-ttu-id="e6c43-110">Le membre **dwBytesRecorded** de **MIDIHDR** spécifie le nombre d’octets dans la mémoire tampon qui sont réellement utilisés par les événements MIDI ; Cette valeur doit être inférieure ou égale à la valeur spécifiée par **dwBufferLength**.</span><span class="sxs-lookup"><span data-stu-id="e6c43-110">The **dwBytesRecorded** member of **MIDIHDR** specifies the number of bytes in the buffer that are actually used by the MIDI events; this value must be less than or equal to the value specified by **dwBufferLength**.</span></span>

<span data-ttu-id="e6c43-111">Chacun des événements MIDI dans la mémoire tampon de flux est spécifié par une structure [**MIDIEVENT**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) , qui contient l’heure de l’événement, un identificateur de flux, un code d’événement et, le cas échéant, les paramètres de l’événement.</span><span class="sxs-lookup"><span data-stu-id="e6c43-111">Each of the MIDI events in the stream buffer is specified by a [**MIDIEVENT**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) structure, which contains the time for the event, a stream identifier, an event code, and, when appropriate, parameters for the event.</span></span> <span data-ttu-id="e6c43-112">Chacune de ces structures **MIDIEVENT** doit commencer sur une limite de mot double.</span><span class="sxs-lookup"><span data-stu-id="e6c43-112">Each of these **MIDIEVENT** structures must begin on a doubleword boundary.</span></span> <span data-ttu-id="e6c43-113">Si nécessaire, les octets de remplissage doivent être ajoutés à la fin de la structure pour s’assurer que le suivant démarre sur une limite de mot double.</span><span class="sxs-lookup"><span data-stu-id="e6c43-113">If necessary, pad bytes must be added to the end of the structure to ensure that the next one starts on a doubleword boundary.</span></span>

 

 