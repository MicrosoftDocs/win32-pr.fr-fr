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
ms.openlocfilehash: ececb41bc0f9dc0cef187c083afc72ba5fc899a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743932"
---
# <a name="mim_moredata-message"></a><span data-ttu-id="8ade3-104">\_Message MIM MOREDATA</span><span class="sxs-lookup"><span data-stu-id="8ade3-104">MIM\_MOREDATA message</span></span>

<span data-ttu-id="8ade3-105">Le message **MIM \_ MOREDATA** est envoyé à une fonction de rappel d’entrée MIDI lorsqu’un message MIDI est reçu par un périphérique d’entrée MIDI, mais que l’application ne traite pas les messages de [**\_ données MIM**](mim-data.md) suffisamment rapidement pour suivre le pilote de périphérique d’entrée.</span><span class="sxs-lookup"><span data-stu-id="8ade3-105">The **MIM\_MOREDATA** message is sent to a MIDI input callback function when a MIDI message is received by a MIDI input device but the application is not processing [**MIM\_DATA**](mim-data.md) messages fast enough to keep up with the input device driver.</span></span> <span data-ttu-id="8ade3-106">La fonction de rappel reçoit ce message uniquement lorsque l’application spécifie l' \_ État des e/s midi \_ dans l’appel à la fonction [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) .</span><span class="sxs-lookup"><span data-stu-id="8ade3-106">The callback function receives this message only when the application specifies MIDI\_IO\_STATUS in the call to the [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) function.</span></span>


```C++
MIM_MOREDATA 
dwParam1 = dwMidiMessage 
dwParam2 = dwTimestamp 
```



## <a name="parameters"></a><span data-ttu-id="8ade3-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8ade3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ade3-108"><span id="dwMidiMessage"></span><span id="dwmidimessage"></span><span id="DWMIDIMESSAGE"></span>*dwMidiMessage*</span><span class="sxs-lookup"><span data-stu-id="8ade3-108"><span id="dwMidiMessage"></span><span id="dwmidimessage"></span><span id="DWMIDIMESSAGE"></span>*dwMidiMessage*</span></span>
</dt> <dd>

<span data-ttu-id="8ade3-109">Spécifie le message MIDI qui a été reçu.</span><span class="sxs-lookup"><span data-stu-id="8ade3-109">Specifies the MIDI message that was received.</span></span> <span data-ttu-id="8ade3-110">Le message est compressé dans une valeur **DWORD** comme suit :</span><span class="sxs-lookup"><span data-stu-id="8ade3-110">The message is packed into a **DWORD** value as follows:</span></span>



| <span data-ttu-id="8ade3-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8ade3-111">Requirement</span></span> | <span data-ttu-id="8ade3-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="8ade3-112">Value</span></span> |
|-----------|-----------------|-----------------------------------------------------|
| <span data-ttu-id="8ade3-113">Mot haut</span><span class="sxs-lookup"><span data-stu-id="8ade3-113">High word</span></span> | <span data-ttu-id="8ade3-114">Octet de poids fort</span><span class="sxs-lookup"><span data-stu-id="8ade3-114">High-order byte</span></span> | <span data-ttu-id="8ade3-115">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="8ade3-115">Not used.</span></span>                                           |
|           | <span data-ttu-id="8ade3-116">Octet de poids faible</span><span class="sxs-lookup"><span data-stu-id="8ade3-116">Low-order byte</span></span>  | <span data-ttu-id="8ade3-117">Contient un deuxième octet de données MIDI (si nécessaire).</span><span class="sxs-lookup"><span data-stu-id="8ade3-117">Contains a second byte of MIDI data (when needed).</span></span>  |
| <span data-ttu-id="8ade3-118">Mot bas</span><span class="sxs-lookup"><span data-stu-id="8ade3-118">Low word</span></span>  | <span data-ttu-id="8ade3-119">Octet de poids fort</span><span class="sxs-lookup"><span data-stu-id="8ade3-119">High-order byte</span></span> | <span data-ttu-id="8ade3-120">Contient le premier octet des données MIDI (si nécessaire).</span><span class="sxs-lookup"><span data-stu-id="8ade3-120">Contains the first byte of MIDI data (when needed).</span></span> |
|           | <span data-ttu-id="8ade3-121">Octet de poids faible</span><span class="sxs-lookup"><span data-stu-id="8ade3-121">Low-order byte</span></span>  | <span data-ttu-id="8ade3-122">Contient l’État MIDI.</span><span class="sxs-lookup"><span data-stu-id="8ade3-122">Contains the MIDI status.</span></span>                           |



 

<span data-ttu-id="8ade3-123">Les deux octets de données MIDI sont facultatifs, en fonction de l’octet d’État MIDI.</span><span class="sxs-lookup"><span data-stu-id="8ade3-123">The two MIDI data bytes are optional, depending on the MIDI status byte.</span></span>

</dd> <dt>

<span data-ttu-id="8ade3-124"><span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwTimestamp*</span><span class="sxs-lookup"><span data-stu-id="8ade3-124"><span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwTimestamp*</span></span>
</dt> <dd>

<span data-ttu-id="8ade3-125">Spécifie l’heure à laquelle le message a été reçu par le pilote de périphérique d’entrée.</span><span class="sxs-lookup"><span data-stu-id="8ade3-125">Specifies the time that the message was received by the input device driver.</span></span> <span data-ttu-id="8ade3-126">L’horodatage est spécifié en millisecondes, en commençant à 0 lorsque la fonction [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) a été appelée.</span><span class="sxs-lookup"><span data-stu-id="8ade3-126">The time stamp is specified in milliseconds, beginning at 0 when the [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) function was called.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ade3-127">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="8ade3-127">Return Value</span></span>

<span data-ttu-id="8ade3-128">Ce message ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="8ade3-128">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ade3-129">Notes</span><span class="sxs-lookup"><span data-stu-id="8ade3-129">Remarks</span></span>

<span data-ttu-id="8ade3-130">Une application ne doit effectuer qu’une quantité minime de traitement des \_ messages MIM MOREDATA.</span><span class="sxs-lookup"><span data-stu-id="8ade3-130">An application should do only a minimal amount of processing of MIM\_MOREDATA messages.</span></span> <span data-ttu-id="8ade3-131">(En particulier, les applications ne doivent pas appeler la fonction [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea) lors du traitement de MIM \_ MOREDATA.) Au lieu de cela, l’application doit placer les données d’événement dans une mémoire tampon, puis retourner.</span><span class="sxs-lookup"><span data-stu-id="8ade3-131">(In particular, applications should not call the [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea) function while processing MIM\_MOREDATA.) Instead, the application should place the event data into a buffer and then return.</span></span>

<span data-ttu-id="8ade3-132">Lorsqu’une application reçoit un message de [**\_ données MIM**](mim-data.md) après une série de \_ messages MIM MOREDATA, elle a détecté des événements MIDI entrants et peut appeler en toute sécurité des fonctions nécessitant beaucoup de temps.</span><span class="sxs-lookup"><span data-stu-id="8ade3-132">When an application receives an [**MIM\_DATA**](mim-data.md) message after a series of MIM\_MOREDATA messages, it has caught up with incoming MIDI events and can safely call time-intensive functions.</span></span>

<span data-ttu-id="8ade3-133">L’état d’exécution des messages MIDI reçus d’un port d’entrée MIDI est désactivé ; chaque message est développé pour inclure l’octet d’État MIDI.</span><span class="sxs-lookup"><span data-stu-id="8ade3-133">MIDI messages received from a MIDI input port have running status disabled; each message is expanded to include the MIDI status byte.</span></span>

<span data-ttu-id="8ade3-134">Ce message n’est pas envoyé lorsqu’un message MIDI système exclusif est reçu.</span><span class="sxs-lookup"><span data-stu-id="8ade3-134">This message is not sent when a MIDI system-exclusive message is received.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ade3-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8ade3-135">Requirements</span></span>



| <span data-ttu-id="8ade3-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8ade3-136">Requirement</span></span> | <span data-ttu-id="8ade3-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="8ade3-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ade3-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8ade3-138">Minimum supported client</span></span><br/> | <span data-ttu-id="8ade3-139">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8ade3-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="8ade3-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8ade3-140">Minimum supported server</span></span><br/> | <span data-ttu-id="8ade3-141">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8ade3-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="8ade3-142">En-tête</span><span class="sxs-lookup"><span data-stu-id="8ade3-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="8ade3-143"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8ade3-143"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ade3-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8ade3-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ade3-145">Interface MIDI (Musical Instrument Digital Interface)</span><span class="sxs-lookup"><span data-stu-id="8ade3-145">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="8ade3-146">Messages MIDI</span><span class="sxs-lookup"><span data-stu-id="8ade3-146">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

