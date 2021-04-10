---
title: Mappages de correctifs
description: Mappages de correctifs
ms.assetid: d0c91001-d19d-439c-9773-78d6228a6642
keywords:
- L’interface MIDI (Musical Instrument Digital Interface), le Mappeur MIDI
- MIDI (Musical Instrument Digital Interface), Mappeur MIDI
- Mappeur MIDI, mappages de correctifs
- mappages de correctifs
- Programme MIDI-modification des messages
- Messages du contrôleur de volume MIDI
- programme-modifier les messages
- messages du contrôleur de volume
- Mappeur MIDI, messages de modification de programme
- Mappeur MIDI, messages de contrôleur de volume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e418b0616d9ba9d2c2bcd05ebcb312ba0176ef5c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309850"
---
# <a name="patch-maps"></a><span data-ttu-id="cf375-113">Mappages de correctifs</span><span class="sxs-lookup"><span data-stu-id="cf375-113">Patch Maps</span></span>

<span data-ttu-id="cf375-114">Chaque entrée de mappage de canal peut être associée à une carte de correctif.</span><span class="sxs-lookup"><span data-stu-id="cf375-114">Each channel map entry can have an associated patch map.</span></span> <span data-ttu-id="cf375-115">Les mappages de correctifs affectent les messages de modification de programme MIDI et de contrôleur de volume.</span><span class="sxs-lookup"><span data-stu-id="cf375-115">Patch maps affect MIDI program-change and volume-controller messages.</span></span> <span data-ttu-id="cf375-116">Programme : les messages de modification indiquent à un synthétiseur de modifier le son de l’instrument (patch) pour un canal spécifié.</span><span class="sxs-lookup"><span data-stu-id="cf375-116">Program-change messages tell a synthesizer to change the instrument sound (patch) for a specified channel.</span></span> <span data-ttu-id="cf375-117">Les messages du contrôleur de volume définissent le volume d’un canal.</span><span class="sxs-lookup"><span data-stu-id="cf375-117">Volume-controller messages set the volume for a channel.</span></span>

<span data-ttu-id="cf375-118">Une carte de correctifs possède une table de traduction avec une entrée pour chacune des valeurs de modification de programme 128.</span><span class="sxs-lookup"><span data-stu-id="cf375-118">A patch map has a translation table with an entry for each of the 128 program-change values.</span></span> <span data-ttu-id="cf375-119">Chaque mappage de correctif spécifie les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="cf375-119">Each patch map specifies the following:</span></span>

-   <span data-ttu-id="cf375-120">Une valeur de changement de programme de destination.</span><span class="sxs-lookup"><span data-stu-id="cf375-120">A destination program-change value.</span></span>
-   <span data-ttu-id="cf375-121">Scalaire de volume.</span><span class="sxs-lookup"><span data-stu-id="cf375-121">A volume scalar.</span></span> <span data-ttu-id="cf375-122">(Pour plus d’informations, consultez [volume Scalar](the-volume-scalar.md).)</span><span class="sxs-lookup"><span data-stu-id="cf375-122">(For more information, see [The Volume Scalar](the-volume-scalar.md).)</span></span>
-   <span data-ttu-id="cf375-123">Mappage de clé facultatif.</span><span class="sxs-lookup"><span data-stu-id="cf375-123">An optional key map.</span></span> <span data-ttu-id="cf375-124">(Pour plus d’informations, consultez [mappages de clés](key-maps.md).)</span><span class="sxs-lookup"><span data-stu-id="cf375-124">(For more information, see [Key Maps](key-maps.md).)</span></span>

<span data-ttu-id="cf375-125">Lorsque le Mappeur MIDI reçoit des messages de modification de programme, la valeur de modification du programme de destination est remplacée par la valeur de modification du programme dans le message.</span><span class="sxs-lookup"><span data-stu-id="cf375-125">When program-change messages are received by the MIDI Mapper, the destination program-change value is substituted for the program-change value in the message.</span></span> <span data-ttu-id="cf375-126">Par exemple, si la valeur de modification du programme de destination pour le programme-modification 16 est 18, le Mappeur MIDI modifie le message MIDI de modification de programme comme indiqué dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="cf375-126">For example, if the destination program-change value for program-change 16 is 18, the MIDI Mapper modifies the MIDI program-change message as shown in the following illustration.</span></span>

![image du mappeur midi](images/mmap-a03.gif)

 

 




