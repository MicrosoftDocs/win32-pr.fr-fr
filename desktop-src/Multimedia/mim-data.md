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
ms.openlocfilehash: 48f96d2c23e64700a7a923cdd7633dabfcba9d1d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844402"
---
# <a name="mim_data-message"></a><span data-ttu-id="23c86-104">\_Message de données MIM</span><span class="sxs-lookup"><span data-stu-id="23c86-104">MIM\_DATA message</span></span>

<span data-ttu-id="23c86-105">Le message de **\_ données MIM** est envoyé à une fonction de rappel d’entrée MIDI lorsqu’un message MIDI est reçu par un périphérique d’entrée MIDI.</span><span class="sxs-lookup"><span data-stu-id="23c86-105">The **MIM\_DATA** message is sent to a MIDI input callback function when a MIDI message is received by a MIDI input device.</span></span>


```C++
MIM_DATA 
dwParam1 = dwMidiMessage 
dwParam2 = dwTimestamp 
```



## <a name="parameters"></a><span data-ttu-id="23c86-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="23c86-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23c86-107"><span id="dwMidiMessage"></span><span id="dwmidimessage"></span><span id="DWMIDIMESSAGE"></span>*dwMidiMessage*</span><span class="sxs-lookup"><span data-stu-id="23c86-107"><span id="dwMidiMessage"></span><span id="dwmidimessage"></span><span id="DWMIDIMESSAGE"></span>*dwMidiMessage*</span></span>
</dt> <dd>

<span data-ttu-id="23c86-108">Message MIDI qui a été reçu.</span><span class="sxs-lookup"><span data-stu-id="23c86-108">MIDI message that was received.</span></span> <span data-ttu-id="23c86-109">Le message est empaqueté dans une valeur de mot double comme suit :</span><span class="sxs-lookup"><span data-stu-id="23c86-109">The message is packed into a doubleword value as follows:</span></span>



| <span data-ttu-id="23c86-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="23c86-110">Requirement</span></span> | <span data-ttu-id="23c86-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="23c86-111">Value</span></span> |
|-----------|-----------------|-----------------------------------------------------|
| <span data-ttu-id="23c86-112">Mot haut</span><span class="sxs-lookup"><span data-stu-id="23c86-112">High word</span></span> | <span data-ttu-id="23c86-113">Octet de poids fort</span><span class="sxs-lookup"><span data-stu-id="23c86-113">High-order byte</span></span> | <span data-ttu-id="23c86-114">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="23c86-114">Not used.</span></span>                                           |
|           | <span data-ttu-id="23c86-115">Octet de poids faible</span><span class="sxs-lookup"><span data-stu-id="23c86-115">Low-order byte</span></span>  | <span data-ttu-id="23c86-116">Contient un deuxième octet de données MIDI (si nécessaire).</span><span class="sxs-lookup"><span data-stu-id="23c86-116">Contains a second byte of MIDI data (when needed).</span></span>  |
| <span data-ttu-id="23c86-117">Mot bas</span><span class="sxs-lookup"><span data-stu-id="23c86-117">Low word</span></span>  | <span data-ttu-id="23c86-118">Octet de poids fort</span><span class="sxs-lookup"><span data-stu-id="23c86-118">High-order byte</span></span> | <span data-ttu-id="23c86-119">Contient le premier octet des données MIDI (si nécessaire).</span><span class="sxs-lookup"><span data-stu-id="23c86-119">Contains the first byte of MIDI data (when needed).</span></span> |
|           | <span data-ttu-id="23c86-120">Octet de poids faible</span><span class="sxs-lookup"><span data-stu-id="23c86-120">Low-order byte</span></span>  | <span data-ttu-id="23c86-121">Contient l’État MIDI.</span><span class="sxs-lookup"><span data-stu-id="23c86-121">Contains the MIDI status.</span></span>                           |



 

<span data-ttu-id="23c86-122">Les deux octets de données MIDI sont facultatifs, en fonction de l’octet d’État MIDI.</span><span class="sxs-lookup"><span data-stu-id="23c86-122">The two MIDI data bytes are optional, depending on the MIDI status byte.</span></span>

</dd> <dt>

<span data-ttu-id="23c86-123"><span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwTimestamp*</span><span class="sxs-lookup"><span data-stu-id="23c86-123"><span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwTimestamp*</span></span>
</dt> <dd>

<span data-ttu-id="23c86-124">Heure à laquelle le message a été reçu par le pilote de périphérique d’entrée.</span><span class="sxs-lookup"><span data-stu-id="23c86-124">Time that the message was received by the input device driver.</span></span> <span data-ttu-id="23c86-125">L’horodatage est spécifié en millisecondes, en commençant à zéro lorsque la fonction [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) a été appelée.</span><span class="sxs-lookup"><span data-stu-id="23c86-125">The time stamp is specified in milliseconds, beginning at zero when the [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) function was called.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23c86-126">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="23c86-126">Return Value</span></span>

<span data-ttu-id="23c86-127">Ce message ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="23c86-127">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="23c86-128">Notes</span><span class="sxs-lookup"><span data-stu-id="23c86-128">Remarks</span></span>

<span data-ttu-id="23c86-129">L’état d’exécution des messages MIDI reçus d’un port d’entrée MIDI est désactivé ; chaque message est développé pour inclure l’octet d’État MIDI.</span><span class="sxs-lookup"><span data-stu-id="23c86-129">MIDI messages received from a MIDI input port have running status disabled; each message is expanded to include the MIDI status byte.</span></span>

<span data-ttu-id="23c86-130">Ce message n’est pas envoyé lorsqu’un message MIDI système exclusif est reçu.</span><span class="sxs-lookup"><span data-stu-id="23c86-130">This message is not sent when a MIDI system-exclusive message is received.</span></span>

## <a name="requirements"></a><span data-ttu-id="23c86-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="23c86-131">Requirements</span></span>



| <span data-ttu-id="23c86-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="23c86-132">Requirement</span></span> | <span data-ttu-id="23c86-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="23c86-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23c86-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="23c86-134">Minimum supported client</span></span><br/> | <span data-ttu-id="23c86-135">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="23c86-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="23c86-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="23c86-136">Minimum supported server</span></span><br/> | <span data-ttu-id="23c86-137">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="23c86-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="23c86-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="23c86-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="23c86-139"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="23c86-139"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23c86-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="23c86-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23c86-141">Interface MIDI (Musical Instrument Digital Interface)</span><span class="sxs-lookup"><span data-stu-id="23c86-141">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="23c86-142">Messages MIDI</span><span class="sxs-lookup"><span data-stu-id="23c86-142">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

