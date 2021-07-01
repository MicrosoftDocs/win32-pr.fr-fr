---
title: Message MM_MIM_DATA (mmsystem. h)
description: Le \_ message de \_ données MIM mm est envoyé à une fenêtre lorsqu’un message MIDI complet est reçu par un périphérique d’entrée MIDI.
ms.assetid: 9c580e48-78f3-4914-bdea-393823fb8482
keywords:
- Message MM_MIM_DATA Windows Multimedia
topic_type:
- apiref
api_name:
- MM_MIM_DATA
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2a79a5a4ab6b0422705fe737ba3da4a6fd4f923
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119694"
---
# <a name="mm_mim_data-message"></a><span data-ttu-id="689c0-104">MM \_ \_ message de données MIM</span><span class="sxs-lookup"><span data-stu-id="689c0-104">MM\_MIM\_DATA message</span></span>

<span data-ttu-id="689c0-105">Le message de **\_ \_ données MIM mm** est envoyé à une fenêtre lorsqu’un message MIDI complet est reçu par un périphérique d’entrée MIDI.</span><span class="sxs-lookup"><span data-stu-id="689c0-105">The **MM\_MIM\_DATA** message is sent to a window when a complete MIDI message is received by a MIDI input device.</span></span>


```C++
MM_MIM_DATA 
wParam = (WPARAM) hInput 
lParam = (LPARAM) (DWORD) lMidiMessage 
```



## <a name="parameters"></a><span data-ttu-id="689c0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="689c0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="689c0-107"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*</span><span class="sxs-lookup"><span data-stu-id="689c0-107"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*</span></span>
</dt> <dd>

<span data-ttu-id="689c0-108">Handle vers l’appareil d’entrée MIDI qui a reçu le message MIDI.</span><span class="sxs-lookup"><span data-stu-id="689c0-108">Handle to the MIDI input device that received the MIDI message.</span></span>

</dd> <dt>

<span data-ttu-id="689c0-109"><span id="lMidiMessage"></span><span id="lmidimessage"></span><span id="LMIDIMESSAGE"></span>*lMidiMessage*</span><span class="sxs-lookup"><span data-stu-id="689c0-109"><span id="lMidiMessage"></span><span id="lmidimessage"></span><span id="LMIDIMESSAGE"></span>*lMidiMessage*</span></span>
</dt> <dd>

<span data-ttu-id="689c0-110">Message MIDI qui a été reçu.</span><span class="sxs-lookup"><span data-stu-id="689c0-110">MIDI message that was received.</span></span> <span data-ttu-id="689c0-111">Le message est empaqueté dans une valeur de mot double comme suit :</span><span class="sxs-lookup"><span data-stu-id="689c0-111">The message is packed into a doubleword value as follows:</span></span>



| <span data-ttu-id="689c0-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="689c0-112">Requirement</span></span> | <span data-ttu-id="689c0-113">Value</span><span class="sxs-lookup"><span data-stu-id="689c0-113">Value</span></span> | <span data-ttu-id="689c0-114">Description</span><span class="sxs-lookup"><span data-stu-id="689c0-114">Description</span></span> |
|-----------|-----------------|-----------------------------------------------------|
| <span data-ttu-id="689c0-115">Mot haut</span><span class="sxs-lookup"><span data-stu-id="689c0-115">High word</span></span> | <span data-ttu-id="689c0-116">Octet de poids fort</span><span class="sxs-lookup"><span data-stu-id="689c0-116">High-order byte</span></span> | <span data-ttu-id="689c0-117">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="689c0-117">Not used.</span></span>                                           |
|           | <span data-ttu-id="689c0-118">Octet de poids faible</span><span class="sxs-lookup"><span data-stu-id="689c0-118">Low-order byte</span></span>  | <span data-ttu-id="689c0-119">Contient un deuxième octet de données MIDI (si nécessaire).</span><span class="sxs-lookup"><span data-stu-id="689c0-119">Contains a second byte of MIDI data (when needed).</span></span>  |
| <span data-ttu-id="689c0-120">Mot bas</span><span class="sxs-lookup"><span data-stu-id="689c0-120">Low word</span></span>  | <span data-ttu-id="689c0-121">Octet de poids fort</span><span class="sxs-lookup"><span data-stu-id="689c0-121">High-order byte</span></span> | <span data-ttu-id="689c0-122">Contient le premier octet des données MIDI (si nécessaire).</span><span class="sxs-lookup"><span data-stu-id="689c0-122">Contains the first byte of MIDI data (when needed).</span></span> |
|           | <span data-ttu-id="689c0-123">Octet de poids faible</span><span class="sxs-lookup"><span data-stu-id="689c0-123">Low-order byte</span></span>  | <span data-ttu-id="689c0-124">Contient l’État MIDI.</span><span class="sxs-lookup"><span data-stu-id="689c0-124">Contains the MIDI status.</span></span>                           |



 

<span data-ttu-id="689c0-125">Les deux octets de données MIDI sont facultatifs, en fonction de l’octet d’État MIDI.</span><span class="sxs-lookup"><span data-stu-id="689c0-125">The two MIDI data bytes are optional, depending on the MIDI status byte.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="689c0-126">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="689c0-126">Return Value</span></span>

<span data-ttu-id="689c0-127">Ce message ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="689c0-127">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="689c0-128">Remarques</span><span class="sxs-lookup"><span data-stu-id="689c0-128">Remarks</span></span>

<span data-ttu-id="689c0-129">L’état d’exécution des messages MIDI reçus d’un port d’entrée MIDI est désactivé ; chaque message est développé pour inclure l’octet d’État MIDI.</span><span class="sxs-lookup"><span data-stu-id="689c0-129">MIDI messages received from a MIDI input port have running status disabled; each message is expanded to include the MIDI status byte.</span></span>

<span data-ttu-id="689c0-130">Ce message n’est pas envoyé lorsqu’un message MIDI système exclusif est reçu.</span><span class="sxs-lookup"><span data-stu-id="689c0-130">This message is not sent when a MIDI system-exclusive message is received.</span></span> <span data-ttu-id="689c0-131">Aucun horodatage n’est disponible avec ce message.</span><span class="sxs-lookup"><span data-stu-id="689c0-131">No time stamp is available with this message.</span></span> <span data-ttu-id="689c0-132">Pour les données d’entrée horodatées, vous devez utiliser les messages envoyés aux fonctions de rappel.</span><span class="sxs-lookup"><span data-stu-id="689c0-132">For time-stamped input data, you must use the messages that are sent to callback functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="689c0-133">Spécifications</span><span class="sxs-lookup"><span data-stu-id="689c0-133">Requirements</span></span>



| <span data-ttu-id="689c0-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="689c0-134">Requirement</span></span> | <span data-ttu-id="689c0-135">Value</span><span class="sxs-lookup"><span data-stu-id="689c0-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="689c0-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="689c0-136">Minimum supported client</span></span><br/> | <span data-ttu-id="689c0-137">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="689c0-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="689c0-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="689c0-138">Minimum supported server</span></span><br/> | <span data-ttu-id="689c0-139">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="689c0-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="689c0-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="689c0-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="689c0-141"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="689c0-141"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="689c0-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="689c0-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="689c0-143">Interface MIDI (Musical Instrument Digital Interface)</span><span class="sxs-lookup"><span data-stu-id="689c0-143">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="689c0-144">Messages MIDI</span><span class="sxs-lookup"><span data-stu-id="689c0-144">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

 





