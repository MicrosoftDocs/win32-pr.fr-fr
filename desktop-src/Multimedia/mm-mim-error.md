---
title: Message MM_MIM_ERROR (mmsystem. h)
description: Le \_ \_ message d’erreur de mm MIM est envoyé à une fenêtre lorsqu’un message MIDI non valide est reçu.
ms.assetid: 03760bfc-a4ef-48cd-97a9-1b93b56fc641
keywords:
- Message MM_MIM_ERROR Windows Multimedia
topic_type:
- apiref
api_name:
- MM_MIM_ERROR
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76b45988259601b40a804f9eb8acfbb085bddcda
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103033"
---
# <a name="mm_mim_error-message"></a><span data-ttu-id="db150-104">MM \_ \_ message d’erreur MIM</span><span class="sxs-lookup"><span data-stu-id="db150-104">MM\_MIM\_ERROR message</span></span>

<span data-ttu-id="db150-105">Le message d' **\_ \_ erreur de mm MIM** est envoyé à une fenêtre lorsqu’un message MIDI non valide est reçu.</span><span class="sxs-lookup"><span data-stu-id="db150-105">The **MM\_MIM\_ERROR** message is sent to a window when an invalid MIDI message is received.</span></span>


```C++
MM_MIM_ERROR 
wParam = (WPARAM) hInput 
lParam = (LPARAM) (DWORD) lMidiMessage 
```



## <a name="parameters"></a><span data-ttu-id="db150-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="db150-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db150-107"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*</span><span class="sxs-lookup"><span data-stu-id="db150-107"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*</span></span>
</dt> <dd>

<span data-ttu-id="db150-108">Handle vers l’appareil d’entrée MIDI qui a reçu le message non valide.</span><span class="sxs-lookup"><span data-stu-id="db150-108">Handle to the MIDI input device that received the invalid message.</span></span>

</dd> <dt>

<span data-ttu-id="db150-109"><span id="lMidiMessage"></span><span id="lmidimessage"></span><span id="LMIDIMESSAGE"></span>*lMidiMessage*</span><span class="sxs-lookup"><span data-stu-id="db150-109"><span id="lMidiMessage"></span><span id="lmidimessage"></span><span id="LMIDIMESSAGE"></span>*lMidiMessage*</span></span>
</dt> <dd>

<span data-ttu-id="db150-110">Message MIDI non valide.</span><span class="sxs-lookup"><span data-stu-id="db150-110">Invalid MIDI message.</span></span> <span data-ttu-id="db150-111">Le message est empaqueté dans une valeur **DWORD** avec le premier octet du message dans l’octet de poids faible.</span><span class="sxs-lookup"><span data-stu-id="db150-111">The message is packed into a **DWORD** value with the first byte of the message in the low-order byte.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db150-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="db150-112">Return Value</span></span>

<span data-ttu-id="db150-113">Ce message ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="db150-113">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="db150-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="db150-114">Requirements</span></span>



| <span data-ttu-id="db150-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="db150-115">Requirement</span></span> | <span data-ttu-id="db150-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="db150-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db150-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="db150-117">Minimum supported client</span></span><br/> | <span data-ttu-id="db150-118">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="db150-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="db150-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="db150-119">Minimum supported server</span></span><br/> | <span data-ttu-id="db150-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="db150-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="db150-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="db150-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="db150-122"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="db150-122"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db150-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="db150-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db150-124">Interface MIDI (Musical Instrument Digital Interface)</span><span class="sxs-lookup"><span data-stu-id="db150-124">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="db150-125">Messages MIDI</span><span class="sxs-lookup"><span data-stu-id="db150-125">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

 





