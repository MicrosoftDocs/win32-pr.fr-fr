---
title: Message MIM_MOREDATA (mmsystem. h)
description: Le \_ message MIM MOREDATA est envoyé à une fonction de rappel d’entrée MIDI lorsqu’un message MIDI est reçu par un périphérique d’entrée MIDI, mais que l’application ne traite pas les \_ messages de données MIM suffisamment rapidement pour suivre le pilote de périphérique d’entrée.
ms.assetid: 74ed46ab-a18e-4df5-bf36-ab3dec7fafa5
keywords:
- Message MIM_MOREDATA Windows Multimedia
topic_type:
- apiref
api_name:
- MIM_MOREDATA
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6342823e13a085b377a3e71f28a0f9ff016681c
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119404"
---
# <a name="mim_moredata-message"></a><span data-ttu-id="7ae02-104">\_Message MIM MOREDATA</span><span class="sxs-lookup"><span data-stu-id="7ae02-104">MIM\_MOREDATA message</span></span>

<span data-ttu-id="7ae02-105">Le message **MIM \_ MOREDATA** est envoyé à une fonction de rappel d’entrée MIDI lorsqu’un message MIDI est reçu par un périphérique d’entrée MIDI, mais que l’application ne traite pas les messages de [**\_ données MIM**](mim-data.md) suffisamment rapidement pour suivre le pilote de périphérique d’entrée.</span><span class="sxs-lookup"><span data-stu-id="7ae02-105">The **MIM\_MOREDATA** message is sent to a MIDI input callback function when a MIDI message is received by a MIDI input device but the application is not processing [**MIM\_DATA**](mim-data.md) messages fast enough to keep up with the input device driver.</span></span> <span data-ttu-id="7ae02-106">La fonction de rappel reçoit ce message uniquement lorsque l’application spécifie l' \_ État des e/s midi \_ dans l’appel à la fonction [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) .</span><span class="sxs-lookup"><span data-stu-id="7ae02-106">The callback function receives this message only when the application specifies MIDI\_IO\_STATUS in the call to the [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) function.</span></span>


```C++
MIM_MOREDATA 
dwParam1 = dwMidiMessage 
dwParam2 = dwTimestamp 
```



## <a name="parameters"></a><span data-ttu-id="7ae02-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7ae02-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ae02-108"><span id="dwMidiMessage"></span><span id="dwmidimessage"></span><span id="DWMIDIMESSAGE"></span>*dwMidiMessage*</span><span class="sxs-lookup"><span data-stu-id="7ae02-108"><span id="dwMidiMessage"></span><span id="dwmidimessage"></span><span id="DWMIDIMESSAGE"></span>*dwMidiMessage*</span></span>
</dt> <dd>

<span data-ttu-id="7ae02-109">Spécifie le message MIDI qui a été reçu.</span><span class="sxs-lookup"><span data-stu-id="7ae02-109">Specifies the MIDI message that was received.</span></span> <span data-ttu-id="7ae02-110">Le message est compressé dans une valeur **DWORD** comme suit :</span><span class="sxs-lookup"><span data-stu-id="7ae02-110">The message is packed into a **DWORD** value as follows:</span></span>



| <span data-ttu-id="7ae02-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7ae02-111">Requirement</span></span> | <span data-ttu-id="7ae02-112">Value</span><span class="sxs-lookup"><span data-stu-id="7ae02-112">Value</span></span> | <span data-ttu-id="7ae02-113">Description</span><span class="sxs-lookup"><span data-stu-id="7ae02-113">Description</span></span> |
|-----------|-----------------|-----------------------------------------------------|
| <span data-ttu-id="7ae02-114">Mot haut</span><span class="sxs-lookup"><span data-stu-id="7ae02-114">High word</span></span> | <span data-ttu-id="7ae02-115">Octet de poids fort</span><span class="sxs-lookup"><span data-stu-id="7ae02-115">High-order byte</span></span> | <span data-ttu-id="7ae02-116">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="7ae02-116">Not used.</span></span>                                           |
|           | <span data-ttu-id="7ae02-117">Octet de poids faible</span><span class="sxs-lookup"><span data-stu-id="7ae02-117">Low-order byte</span></span>  | <span data-ttu-id="7ae02-118">Contient un deuxième octet de données MIDI (si nécessaire).</span><span class="sxs-lookup"><span data-stu-id="7ae02-118">Contains a second byte of MIDI data (when needed).</span></span>  |
| <span data-ttu-id="7ae02-119">Mot bas</span><span class="sxs-lookup"><span data-stu-id="7ae02-119">Low word</span></span>  | <span data-ttu-id="7ae02-120">Octet de poids fort</span><span class="sxs-lookup"><span data-stu-id="7ae02-120">High-order byte</span></span> | <span data-ttu-id="7ae02-121">Contient le premier octet des données MIDI (si nécessaire).</span><span class="sxs-lookup"><span data-stu-id="7ae02-121">Contains the first byte of MIDI data (when needed).</span></span> |
|           | <span data-ttu-id="7ae02-122">Octet de poids faible</span><span class="sxs-lookup"><span data-stu-id="7ae02-122">Low-order byte</span></span>  | <span data-ttu-id="7ae02-123">Contient l’État MIDI.</span><span class="sxs-lookup"><span data-stu-id="7ae02-123">Contains the MIDI status.</span></span>                           |



 

<span data-ttu-id="7ae02-124">Les deux octets de données MIDI sont facultatifs, en fonction de l’octet d’État MIDI.</span><span class="sxs-lookup"><span data-stu-id="7ae02-124">The two MIDI data bytes are optional, depending on the MIDI status byte.</span></span>

</dd> <dt>

<span data-ttu-id="7ae02-125"><span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwTimestamp*</span><span class="sxs-lookup"><span data-stu-id="7ae02-125"><span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwTimestamp*</span></span>
</dt> <dd>

<span data-ttu-id="7ae02-126">Spécifie l’heure à laquelle le message a été reçu par le pilote de périphérique d’entrée.</span><span class="sxs-lookup"><span data-stu-id="7ae02-126">Specifies the time that the message was received by the input device driver.</span></span> <span data-ttu-id="7ae02-127">L’horodatage est spécifié en millisecondes, en commençant à 0 lorsque la fonction [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) a été appelée.</span><span class="sxs-lookup"><span data-stu-id="7ae02-127">The time stamp is specified in milliseconds, beginning at 0 when the [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) function was called.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ae02-128">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="7ae02-128">Return Value</span></span>

<span data-ttu-id="7ae02-129">Ce message ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="7ae02-129">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7ae02-130">Remarques</span><span class="sxs-lookup"><span data-stu-id="7ae02-130">Remarks</span></span>

<span data-ttu-id="7ae02-131">Une application ne doit effectuer qu’une quantité minime de traitement des \_ messages MIM MOREDATA.</span><span class="sxs-lookup"><span data-stu-id="7ae02-131">An application should do only a minimal amount of processing of MIM\_MOREDATA messages.</span></span> <span data-ttu-id="7ae02-132">(En particulier, les applications ne doivent pas appeler la fonction [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea) lors du traitement de MIM \_ MOREDATA.) Au lieu de cela, l’application doit placer les données d’événement dans une mémoire tampon, puis retourner.</span><span class="sxs-lookup"><span data-stu-id="7ae02-132">(In particular, applications should not call the [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea) function while processing MIM\_MOREDATA.) Instead, the application should place the event data into a buffer and then return.</span></span>

<span data-ttu-id="7ae02-133">Lorsqu’une application reçoit un message de [**\_ données MIM**](mim-data.md) après une série de \_ messages MIM MOREDATA, elle a détecté des événements MIDI entrants et peut appeler en toute sécurité des fonctions nécessitant beaucoup de temps.</span><span class="sxs-lookup"><span data-stu-id="7ae02-133">When an application receives an [**MIM\_DATA**](mim-data.md) message after a series of MIM\_MOREDATA messages, it has caught up with incoming MIDI events and can safely call time-intensive functions.</span></span>

<span data-ttu-id="7ae02-134">L’état d’exécution des messages MIDI reçus d’un port d’entrée MIDI est désactivé ; chaque message est développé pour inclure l’octet d’État MIDI.</span><span class="sxs-lookup"><span data-stu-id="7ae02-134">MIDI messages received from a MIDI input port have running status disabled; each message is expanded to include the MIDI status byte.</span></span>

<span data-ttu-id="7ae02-135">Ce message n’est pas envoyé lorsqu’un message MIDI système exclusif est reçu.</span><span class="sxs-lookup"><span data-stu-id="7ae02-135">This message is not sent when a MIDI system-exclusive message is received.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ae02-136">Spécifications</span><span class="sxs-lookup"><span data-stu-id="7ae02-136">Requirements</span></span>



| <span data-ttu-id="7ae02-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7ae02-137">Requirement</span></span> | <span data-ttu-id="7ae02-138">Value</span><span class="sxs-lookup"><span data-stu-id="7ae02-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ae02-139">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7ae02-139">Minimum supported client</span></span><br/> | <span data-ttu-id="7ae02-140">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7ae02-140">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="7ae02-141">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7ae02-141">Minimum supported server</span></span><br/> | <span data-ttu-id="7ae02-142">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7ae02-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="7ae02-143">En-tête</span><span class="sxs-lookup"><span data-stu-id="7ae02-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ae02-144"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7ae02-144"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ae02-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7ae02-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ae02-146">Interface MIDI (Musical Instrument Digital Interface)</span><span class="sxs-lookup"><span data-stu-id="7ae02-146">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="7ae02-147">Messages MIDI</span><span class="sxs-lookup"><span data-stu-id="7ae02-147">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

