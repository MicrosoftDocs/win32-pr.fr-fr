---
title: Message MIM_DATA (mmsystem. h)
description: Le \_ message de données MIM est envoyé à une fonction de rappel d’entrée MIDI lorsqu’un message MIDI est reçu par un périphérique d’entrée MIDI.
ms.assetid: 966aab84-420a-42ce-9989-da5910ced9c0
keywords:
- Message MIM_DATA Windows Multimedia
topic_type:
- apiref
api_name:
- MIM_DATA
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a11d2701d488fe29ae6d0bc0742c32c803b28076
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118404"
---
# <a name="mim_data-message"></a><span data-ttu-id="da8b5-104">\_Message de données MIM</span><span class="sxs-lookup"><span data-stu-id="da8b5-104">MIM\_DATA message</span></span>

<span data-ttu-id="da8b5-105">Le message de **\_ données MIM** est envoyé à une fonction de rappel d’entrée MIDI lorsqu’un message MIDI est reçu par un périphérique d’entrée MIDI.</span><span class="sxs-lookup"><span data-stu-id="da8b5-105">The **MIM\_DATA** message is sent to a MIDI input callback function when a MIDI message is received by a MIDI input device.</span></span>


```C++
MIM_DATA 
dwParam1 = dwMidiMessage 
dwParam2 = dwTimestamp 
```



## <a name="parameters"></a><span data-ttu-id="da8b5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="da8b5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da8b5-107"><span id="dwMidiMessage"></span><span id="dwmidimessage"></span><span id="DWMIDIMESSAGE"></span>*dwMidiMessage*</span><span class="sxs-lookup"><span data-stu-id="da8b5-107"><span id="dwMidiMessage"></span><span id="dwmidimessage"></span><span id="DWMIDIMESSAGE"></span>*dwMidiMessage*</span></span>
</dt> <dd>

<span data-ttu-id="da8b5-108">Message MIDI qui a été reçu.</span><span class="sxs-lookup"><span data-stu-id="da8b5-108">MIDI message that was received.</span></span> <span data-ttu-id="da8b5-109">Le message est empaqueté dans une valeur de mot double comme suit :</span><span class="sxs-lookup"><span data-stu-id="da8b5-109">The message is packed into a doubleword value as follows:</span></span>



| <span data-ttu-id="da8b5-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="da8b5-110">Requirement</span></span> | <span data-ttu-id="da8b5-111">Value</span><span class="sxs-lookup"><span data-stu-id="da8b5-111">Value</span></span> | <span data-ttu-id="da8b5-112">Description</span><span class="sxs-lookup"><span data-stu-id="da8b5-112">Description</span></span> |
|-----------|-----------------|-----------------------------------------------------|
| <span data-ttu-id="da8b5-113">Mot haut</span><span class="sxs-lookup"><span data-stu-id="da8b5-113">High word</span></span> | <span data-ttu-id="da8b5-114">Octet de poids fort</span><span class="sxs-lookup"><span data-stu-id="da8b5-114">High-order byte</span></span> | <span data-ttu-id="da8b5-115">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="da8b5-115">Not used.</span></span>                                           |
|           | <span data-ttu-id="da8b5-116">Octet de poids faible</span><span class="sxs-lookup"><span data-stu-id="da8b5-116">Low-order byte</span></span>  | <span data-ttu-id="da8b5-117">Contient un deuxième octet de données MIDI (si nécessaire).</span><span class="sxs-lookup"><span data-stu-id="da8b5-117">Contains a second byte of MIDI data (when needed).</span></span>  |
| <span data-ttu-id="da8b5-118">Mot bas</span><span class="sxs-lookup"><span data-stu-id="da8b5-118">Low word</span></span>  | <span data-ttu-id="da8b5-119">Octet de poids fort</span><span class="sxs-lookup"><span data-stu-id="da8b5-119">High-order byte</span></span> | <span data-ttu-id="da8b5-120">Contient le premier octet des données MIDI (si nécessaire).</span><span class="sxs-lookup"><span data-stu-id="da8b5-120">Contains the first byte of MIDI data (when needed).</span></span> |
|           | <span data-ttu-id="da8b5-121">Octet de poids faible</span><span class="sxs-lookup"><span data-stu-id="da8b5-121">Low-order byte</span></span>  | <span data-ttu-id="da8b5-122">Contient l’État MIDI.</span><span class="sxs-lookup"><span data-stu-id="da8b5-122">Contains the MIDI status.</span></span>                           |



 

<span data-ttu-id="da8b5-123">Les deux octets de données MIDI sont facultatifs, en fonction de l’octet d’État MIDI.</span><span class="sxs-lookup"><span data-stu-id="da8b5-123">The two MIDI data bytes are optional, depending on the MIDI status byte.</span></span>

</dd> <dt>

<span data-ttu-id="da8b5-124"><span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwTimestamp*</span><span class="sxs-lookup"><span data-stu-id="da8b5-124"><span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwTimestamp*</span></span>
</dt> <dd>

<span data-ttu-id="da8b5-125">Heure à laquelle le message a été reçu par le pilote de périphérique d’entrée.</span><span class="sxs-lookup"><span data-stu-id="da8b5-125">Time that the message was received by the input device driver.</span></span> <span data-ttu-id="da8b5-126">L’horodatage est spécifié en millisecondes, en commençant à zéro lorsque la fonction [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) a été appelée.</span><span class="sxs-lookup"><span data-stu-id="da8b5-126">The time stamp is specified in milliseconds, beginning at zero when the [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) function was called.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da8b5-127">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="da8b5-127">Return Value</span></span>

<span data-ttu-id="da8b5-128">Ce message ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="da8b5-128">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="da8b5-129">Remarques</span><span class="sxs-lookup"><span data-stu-id="da8b5-129">Remarks</span></span>

<span data-ttu-id="da8b5-130">L’état d’exécution des messages MIDI reçus d’un port d’entrée MIDI est désactivé ; chaque message est développé pour inclure l’octet d’État MIDI.</span><span class="sxs-lookup"><span data-stu-id="da8b5-130">MIDI messages received from a MIDI input port have running status disabled; each message is expanded to include the MIDI status byte.</span></span>

<span data-ttu-id="da8b5-131">Ce message n’est pas envoyé lorsqu’un message MIDI système exclusif est reçu.</span><span class="sxs-lookup"><span data-stu-id="da8b5-131">This message is not sent when a MIDI system-exclusive message is received.</span></span>

## <a name="requirements"></a><span data-ttu-id="da8b5-132">Spécifications</span><span class="sxs-lookup"><span data-stu-id="da8b5-132">Requirements</span></span>



| <span data-ttu-id="da8b5-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="da8b5-133">Requirement</span></span> | <span data-ttu-id="da8b5-134">Value</span><span class="sxs-lookup"><span data-stu-id="da8b5-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da8b5-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="da8b5-135">Minimum supported client</span></span><br/> | <span data-ttu-id="da8b5-136">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="da8b5-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="da8b5-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="da8b5-137">Minimum supported server</span></span><br/> | <span data-ttu-id="da8b5-138">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="da8b5-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="da8b5-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="da8b5-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="da8b5-140"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="da8b5-140"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da8b5-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="da8b5-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da8b5-142">Interface MIDI (Musical Instrument Digital Interface)</span><span class="sxs-lookup"><span data-stu-id="da8b5-142">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="da8b5-143">Messages MIDI</span><span class="sxs-lookup"><span data-stu-id="da8b5-143">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

