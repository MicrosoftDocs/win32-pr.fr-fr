---
title: Types d’événements MIDI
description: Types d’événements MIDI
ms.assetid: 0b0984b7-3087-461e-90f2-a899dc1a88c6
keywords:
- MIDI (Musical Instrument Digital Interface), types d’événements
- MIDI (Musical Instrument Digital Interface), types d’événements
- MIDIEVENT, structure
- mémoires tampons de flux, types d’événements MIDI
- Types d’événements MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 823ce5ce7af898ca3178e0379fb814c54fbf06b7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104031219"
---
# <a name="midi-event-types"></a><span data-ttu-id="f1a23-108">Types d’événements MIDI</span><span class="sxs-lookup"><span data-stu-id="f1a23-108">MIDI Event Types</span></span>

<span data-ttu-id="f1a23-109">Le membre **dwEvent** de la structure [**MIDIEVENT**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) décrit l’événement midi qui doit avoir lieu.</span><span class="sxs-lookup"><span data-stu-id="f1a23-109">The **dwEvent** member of the [**MIDIEVENT**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) structure describes the MIDI event that is to take place.</span></span> <span data-ttu-id="f1a23-110">Les événements courts s’inscrivent entièrement dans ce membre.</span><span class="sxs-lookup"><span data-stu-id="f1a23-110">Short events fit entirely into this member.</span></span> <span data-ttu-id="f1a23-111">Les événements longs requièrent une ou plusieurs valeurs de mot double en plus du membre **dwEvent** pour stocker les descriptions des événements.</span><span class="sxs-lookup"><span data-stu-id="f1a23-111">Long events require one or more doubleword values in addition to the **dwEvent** member to store the event descriptions.</span></span>

<span data-ttu-id="f1a23-112">L’octet de poids fort du membre **dwEvent** contient des informations indiquant si l’événement est long ou bref et si un rappel est généré avec l’événement.</span><span class="sxs-lookup"><span data-stu-id="f1a23-112">The high byte of the **dwEvent** member contains information about whether the event is long or short and about whether a callback is generated along with the event.</span></span> <span data-ttu-id="f1a23-113">En outre, cet octet est utilisé pour décrire le type d’événement.</span><span class="sxs-lookup"><span data-stu-id="f1a23-113">In addition, this byte is used to describe the event type.</span></span> <span data-ttu-id="f1a23-114">Les 24 bits restants du membre **dwEvent** sont utilisés pour contenir les paramètres d’événement (pour les messages courts) ou pour contenir la longueur des paramètres d’événement (pour les messages longs).</span><span class="sxs-lookup"><span data-stu-id="f1a23-114">The remaining 24 bits of the **dwEvent** member are used either to contain the event parameters (for short messages) or to contain the length of the event parameters (for long messages).</span></span> <span data-ttu-id="f1a23-115">Pour extraire des informations du membre **dwEvent** , utilisez les macros [**MEVT \_ eventType**](/windows/win32/api/mmeapi/nf-mmeapi-mevt_eventtype) et [**MEVT \_ EVENTPARM**](/windows/win32/api/mmeapi/nf-mmeapi-mevt_eventparm) .</span><span class="sxs-lookup"><span data-stu-id="f1a23-115">To extract information from the **dwEvent** member, use the [**MEVT\_EVENTTYPE**](/windows/win32/api/mmeapi/nf-mmeapi-mevt_eventtype) and [**MEVT\_EVENTPARM**](/windows/win32/api/mmeapi/nf-mmeapi-mevt_eventparm) macros.</span></span>

<span data-ttu-id="f1a23-116">Pour obtenir une description des types d’événements prédéfinis, consultez la documentation de référence de la structure **MIDIEVENT** .</span><span class="sxs-lookup"><span data-stu-id="f1a23-116">For a description of the predefined event types, see the reference material for the **MIDIEVENT** structure.</span></span>

 

 