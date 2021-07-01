---
title: Message MM_MIM_MOREDATA (mmsystem. h)
description: Le \_ message mm MIM \_ MOREDATA est envoyé à une fenêtre de rappel lorsqu’un message MIDI est reçu par un périphérique d’entrée MIDI, mais que l’application ne traite pas les \_ messages de données MIM suffisamment rapidement pour suivre le pilote de périphérique d’entrée.
ms.assetid: 25d507f9-01d4-4a9a-afdd-693d74e3bd22
keywords:
- Message MM_MIM_MOREDATA Windows Multimedia
topic_type:
- apiref
api_name:
- MM_MIM_MOREDATA
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3079c537ddca056ca690537c27edd95826de1189
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120024"
---
# <a name="mm_mim_moredata-message"></a><span data-ttu-id="4ea4f-104">MM \_ \_ message MOREDATA MIM</span><span class="sxs-lookup"><span data-stu-id="4ea4f-104">MM\_MIM\_MOREDATA message</span></span>

<span data-ttu-id="4ea4f-105">Le message **mm \_ MIM \_ MOREDATA** est envoyé à une fenêtre de rappel lorsqu’un message MIDI est reçu par un périphérique d’entrée MIDI, mais que l’application ne traite pas les messages de [**\_ données MIM**](mim-data.md) suffisamment rapidement pour suivre le pilote de périphérique d’entrée.</span><span class="sxs-lookup"><span data-stu-id="4ea4f-105">The **MM\_MIM\_MOREDATA** message is sent to a callback window when a MIDI message is received by a MIDI input device but the application is not processing [**MIM\_DATA**](mim-data.md) messages fast enough to keep up with the input device driver.</span></span> <span data-ttu-id="4ea4f-106">La fenêtre reçoit ce message uniquement lorsque l’application spécifie l' \_ État des e/s midi \_ dans l’appel à la fonction [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) .</span><span class="sxs-lookup"><span data-stu-id="4ea4f-106">The window receives this message only when the application specifies MIDI\_IO\_STATUS in the call to the [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) function.</span></span>


```C++
MM_MIM_MOREDATA 
wParam = (WPARAM) hInput 
lParam = (LPARAM) (DWORD) lMidiMessage 
```



## <a name="parameters"></a><span data-ttu-id="4ea4f-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4ea4f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ea4f-108"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*</span><span class="sxs-lookup"><span data-stu-id="4ea4f-108"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*</span></span>
</dt> <dd>

<span data-ttu-id="4ea4f-109">Handle vers l’appareil d’entrée MIDI qui a reçu le message MIDI.</span><span class="sxs-lookup"><span data-stu-id="4ea4f-109">Handle to the MIDI input device that received the MIDI message.</span></span>

</dd> <dt>

<span data-ttu-id="4ea4f-110"><span id="lMidiMessage"></span><span id="lmidimessage"></span><span id="LMIDIMESSAGE"></span>*lMidiMessage*</span><span class="sxs-lookup"><span data-stu-id="4ea4f-110"><span id="lMidiMessage"></span><span id="lmidimessage"></span><span id="LMIDIMESSAGE"></span>*lMidiMessage*</span></span>
</dt> <dd>

<span data-ttu-id="4ea4f-111">Spécifie le message MIDI qui a été reçu.</span><span class="sxs-lookup"><span data-stu-id="4ea4f-111">Specifies the MIDI message that was received.</span></span> <span data-ttu-id="4ea4f-112">Le message est empaqueté dans une valeur de mot double comme suit :</span><span class="sxs-lookup"><span data-stu-id="4ea4f-112">The message is packed into a doubleword value as follows:</span></span>



| <span data-ttu-id="4ea4f-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4ea4f-113">Requirement</span></span> | <span data-ttu-id="4ea4f-114">Value</span><span class="sxs-lookup"><span data-stu-id="4ea4f-114">Value</span></span> | <span data-ttu-id="4ea4f-115">Description</span><span class="sxs-lookup"><span data-stu-id="4ea4f-115">Description</span></span> |
|-----------|-----------------|-----------------------------------------------------|
| <span data-ttu-id="4ea4f-116">Mot haut</span><span class="sxs-lookup"><span data-stu-id="4ea4f-116">High word</span></span> | <span data-ttu-id="4ea4f-117">Octet de poids fort</span><span class="sxs-lookup"><span data-stu-id="4ea4f-117">High-order byte</span></span> | <span data-ttu-id="4ea4f-118">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="4ea4f-118">Not used.</span></span>                                           |
|           | <span data-ttu-id="4ea4f-119">Octet de poids faible</span><span class="sxs-lookup"><span data-stu-id="4ea4f-119">Low-order byte</span></span>  | <span data-ttu-id="4ea4f-120">Contient un deuxième octet de données MIDI (si nécessaire).</span><span class="sxs-lookup"><span data-stu-id="4ea4f-120">Contains a second byte of MIDI data (when needed).</span></span>  |
| <span data-ttu-id="4ea4f-121">Mot bas</span><span class="sxs-lookup"><span data-stu-id="4ea4f-121">Low word</span></span>  | <span data-ttu-id="4ea4f-122">Octet de poids fort</span><span class="sxs-lookup"><span data-stu-id="4ea4f-122">High-order byte</span></span> | <span data-ttu-id="4ea4f-123">Contient le premier octet des données MIDI (si nécessaire).</span><span class="sxs-lookup"><span data-stu-id="4ea4f-123">Contains the first byte of MIDI data (when needed).</span></span> |
|           | <span data-ttu-id="4ea4f-124">Octet de poids faible</span><span class="sxs-lookup"><span data-stu-id="4ea4f-124">Low-order byte</span></span>  | <span data-ttu-id="4ea4f-125">Contient l’État MIDI.</span><span class="sxs-lookup"><span data-stu-id="4ea4f-125">Contains the MIDI status.</span></span>                           |



 

<span data-ttu-id="4ea4f-126">Les deux octets de données MIDI sont facultatifs, en fonction de l’octet d’État MIDI.</span><span class="sxs-lookup"><span data-stu-id="4ea4f-126">The two MIDI data bytes are optional, depending on the MIDI status byte.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ea4f-127">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="4ea4f-127">Return Value</span></span>

<span data-ttu-id="4ea4f-128">Ce message ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="4ea4f-128">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ea4f-129">Remarques</span><span class="sxs-lookup"><span data-stu-id="4ea4f-129">Remarks</span></span>

<span data-ttu-id="4ea4f-130">Si votre application reçoit des données MIDI plus rapidement qu’elle ne peut les traiter, vous ne devez pas utiliser un mécanisme de rappel de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="4ea4f-130">If your application will receive MIDI data faster than it can process it, you should not use a window callback mechanism.</span></span> <span data-ttu-id="4ea4f-131">Pour optimiser la vitesse, utilisez une fonction de rappel et utilisez le message [**MIM \_ MOREDATA**](mim-moredata.md) au lieu de mm \_ MIM \_ MOREDATA.</span><span class="sxs-lookup"><span data-stu-id="4ea4f-131">To maximize speed, use a callback function, and use the [**MIM\_MOREDATA**](mim-moredata.md) message instead of MM\_MIM\_MOREDATA.</span></span>

<span data-ttu-id="4ea4f-132">Une application ne doit effectuer qu’une quantité minime de traitement des \_ \_ messages MOREDATA MIM.</span><span class="sxs-lookup"><span data-stu-id="4ea4f-132">An application should do only a minimal amount of processing of MM\_MIM\_MOREDATA messages.</span></span> <span data-ttu-id="4ea4f-133">(En particulier, les applications ne doivent pas appeler la fonction [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea) pendant le traitement de mm \_ \_MOREDATA MIM.) Au lieu de cela, l’application doit placer les données d’événement dans une mémoire tampon, puis retourner.</span><span class="sxs-lookup"><span data-stu-id="4ea4f-133">(In particular, applications should not call the [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea) function while processing MM\_MIM\_MOREDATA.) Instead, the application should place the event data into a buffer and then return.</span></span>

<span data-ttu-id="4ea4f-134">Lorsqu’une application reçoit un message de [**\_ \_ données MIM**](mm-mim-data.md) de mm après une série \_ de \_ messages MOREDATA MIM, elle a détecté des événements MIDI entrants et peut appeler en toute sécurité des fonctions nécessitant beaucoup de temps.</span><span class="sxs-lookup"><span data-stu-id="4ea4f-134">When an application receives an [**MM\_MIM\_DATA**](mm-mim-data.md) message after a series of MM\_MIM\_MOREDATA messages, it has caught up with incoming MIDI events and can safely call time-intensive functions.</span></span>

<span data-ttu-id="4ea4f-135">L’état d’exécution des messages MIDI reçus d’un port d’entrée MIDI est désactivé ; chaque message est développé pour inclure l’octet d’État MIDI.</span><span class="sxs-lookup"><span data-stu-id="4ea4f-135">MIDI messages received from a MIDI input port have running status disabled; each message is expanded to include the MIDI status byte.</span></span>

<span data-ttu-id="4ea4f-136">Ce message n’est pas envoyé lorsqu’un message MIDI système exclusif est reçu.</span><span class="sxs-lookup"><span data-stu-id="4ea4f-136">This message is not sent when a MIDI system-exclusive message is received.</span></span> <span data-ttu-id="4ea4f-137">Aucun horodatage n’est disponible avec ce message.</span><span class="sxs-lookup"><span data-stu-id="4ea4f-137">No time stamp is available with this message.</span></span> <span data-ttu-id="4ea4f-138">Pour les données d’entrée horodatées, vous devez utiliser les messages envoyés aux fonctions de rappel.</span><span class="sxs-lookup"><span data-stu-id="4ea4f-138">For time-stamped input data, you must use the messages that are sent to callback functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ea4f-139">Spécifications</span><span class="sxs-lookup"><span data-stu-id="4ea4f-139">Requirements</span></span>



| <span data-ttu-id="4ea4f-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4ea4f-140">Requirement</span></span> | <span data-ttu-id="4ea4f-141">Value</span><span class="sxs-lookup"><span data-stu-id="4ea4f-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ea4f-142">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4ea4f-142">Minimum supported client</span></span><br/> | <span data-ttu-id="4ea4f-143">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4ea4f-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="4ea4f-144">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4ea4f-144">Minimum supported server</span></span><br/> | <span data-ttu-id="4ea4f-145">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4ea4f-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="4ea4f-146">En-tête</span><span class="sxs-lookup"><span data-stu-id="4ea4f-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="4ea4f-147"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4ea4f-147"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ea4f-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4ea4f-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ea4f-149">Interface MIDI (Musical Instrument Digital Interface)</span><span class="sxs-lookup"><span data-stu-id="4ea4f-149">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="4ea4f-150">Messages MIDI</span><span class="sxs-lookup"><span data-stu-id="4ea4f-150">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

