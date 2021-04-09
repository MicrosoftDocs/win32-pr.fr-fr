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
ms.openlocfilehash: aa8c015ba5e08302f7567fe8f474bedca74d3064
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032465"
---
# <a name="mm_mim_data-message"></a><span data-ttu-id="6999c-104">MM \_ \_ message de données MIM</span><span class="sxs-lookup"><span data-stu-id="6999c-104">MM\_MIM\_DATA message</span></span>

<span data-ttu-id="6999c-105">Le message de **\_ \_ données MIM mm** est envoyé à une fenêtre lorsqu’un message MIDI complet est reçu par un périphérique d’entrée MIDI.</span><span class="sxs-lookup"><span data-stu-id="6999c-105">The **MM\_MIM\_DATA** message is sent to a window when a complete MIDI message is received by a MIDI input device.</span></span>


```C++
MM_MIM_DATA 
wParam = (WPARAM) hInput 
lParam = (LPARAM) (DWORD) lMidiMessage 
```



## <a name="parameters"></a><span data-ttu-id="6999c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6999c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6999c-107"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*</span><span class="sxs-lookup"><span data-stu-id="6999c-107"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*</span></span>
</dt> <dd>

<span data-ttu-id="6999c-108">Handle vers l’appareil d’entrée MIDI qui a reçu le message MIDI.</span><span class="sxs-lookup"><span data-stu-id="6999c-108">Handle to the MIDI input device that received the MIDI message.</span></span>

</dd> <dt>

<span data-ttu-id="6999c-109"><span id="lMidiMessage"></span><span id="lmidimessage"></span><span id="LMIDIMESSAGE"></span>*lMidiMessage*</span><span class="sxs-lookup"><span data-stu-id="6999c-109"><span id="lMidiMessage"></span><span id="lmidimessage"></span><span id="LMIDIMESSAGE"></span>*lMidiMessage*</span></span>
</dt> <dd>

<span data-ttu-id="6999c-110">Message MIDI qui a été reçu.</span><span class="sxs-lookup"><span data-stu-id="6999c-110">MIDI message that was received.</span></span> <span data-ttu-id="6999c-111">Le message est empaqueté dans une valeur de mot double comme suit :</span><span class="sxs-lookup"><span data-stu-id="6999c-111">The message is packed into a doubleword value as follows:</span></span>



| <span data-ttu-id="6999c-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6999c-112">Requirement</span></span> | <span data-ttu-id="6999c-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="6999c-113">Value</span></span> |
|-----------|-----------------|-----------------------------------------------------|
| <span data-ttu-id="6999c-114">Mot haut</span><span class="sxs-lookup"><span data-stu-id="6999c-114">High word</span></span> | <span data-ttu-id="6999c-115">Octet de poids fort</span><span class="sxs-lookup"><span data-stu-id="6999c-115">High-order byte</span></span> | <span data-ttu-id="6999c-116">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="6999c-116">Not used.</span></span>                                           |
|           | <span data-ttu-id="6999c-117">Octet de poids faible</span><span class="sxs-lookup"><span data-stu-id="6999c-117">Low-order byte</span></span>  | <span data-ttu-id="6999c-118">Contient un deuxième octet de données MIDI (si nécessaire).</span><span class="sxs-lookup"><span data-stu-id="6999c-118">Contains a second byte of MIDI data (when needed).</span></span>  |
| <span data-ttu-id="6999c-119">Mot bas</span><span class="sxs-lookup"><span data-stu-id="6999c-119">Low word</span></span>  | <span data-ttu-id="6999c-120">Octet de poids fort</span><span class="sxs-lookup"><span data-stu-id="6999c-120">High-order byte</span></span> | <span data-ttu-id="6999c-121">Contient le premier octet des données MIDI (si nécessaire).</span><span class="sxs-lookup"><span data-stu-id="6999c-121">Contains the first byte of MIDI data (when needed).</span></span> |
|           | <span data-ttu-id="6999c-122">Octet de poids faible</span><span class="sxs-lookup"><span data-stu-id="6999c-122">Low-order byte</span></span>  | <span data-ttu-id="6999c-123">Contient l’État MIDI.</span><span class="sxs-lookup"><span data-stu-id="6999c-123">Contains the MIDI status.</span></span>                           |



 

<span data-ttu-id="6999c-124">Les deux octets de données MIDI sont facultatifs, en fonction de l’octet d’État MIDI.</span><span class="sxs-lookup"><span data-stu-id="6999c-124">The two MIDI data bytes are optional, depending on the MIDI status byte.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6999c-125">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="6999c-125">Return Value</span></span>

<span data-ttu-id="6999c-126">Ce message ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="6999c-126">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6999c-127">Notes</span><span class="sxs-lookup"><span data-stu-id="6999c-127">Remarks</span></span>

<span data-ttu-id="6999c-128">L’état d’exécution des messages MIDI reçus d’un port d’entrée MIDI est désactivé ; chaque message est développé pour inclure l’octet d’État MIDI.</span><span class="sxs-lookup"><span data-stu-id="6999c-128">MIDI messages received from a MIDI input port have running status disabled; each message is expanded to include the MIDI status byte.</span></span>

<span data-ttu-id="6999c-129">Ce message n’est pas envoyé lorsqu’un message MIDI système exclusif est reçu.</span><span class="sxs-lookup"><span data-stu-id="6999c-129">This message is not sent when a MIDI system-exclusive message is received.</span></span> <span data-ttu-id="6999c-130">Aucun horodatage n’est disponible avec ce message.</span><span class="sxs-lookup"><span data-stu-id="6999c-130">No time stamp is available with this message.</span></span> <span data-ttu-id="6999c-131">Pour les données d’entrée horodatées, vous devez utiliser les messages envoyés aux fonctions de rappel.</span><span class="sxs-lookup"><span data-stu-id="6999c-131">For time-stamped input data, you must use the messages that are sent to callback functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="6999c-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6999c-132">Requirements</span></span>



| <span data-ttu-id="6999c-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6999c-133">Requirement</span></span> | <span data-ttu-id="6999c-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="6999c-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6999c-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6999c-135">Minimum supported client</span></span><br/> | <span data-ttu-id="6999c-136">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6999c-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="6999c-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6999c-137">Minimum supported server</span></span><br/> | <span data-ttu-id="6999c-138">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6999c-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="6999c-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="6999c-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="6999c-140"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6999c-140"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6999c-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6999c-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6999c-142">Interface MIDI (Musical Instrument Digital Interface)</span><span class="sxs-lookup"><span data-stu-id="6999c-142">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="6999c-143">Messages MIDI</span><span class="sxs-lookup"><span data-stu-id="6999c-143">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

 





