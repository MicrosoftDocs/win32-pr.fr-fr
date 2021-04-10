---
title: Message MM_MOM_POSITIONCB (mmsystem. h)
description: Le \_ message de \_ POSITIONCB MOM mm est envoyé à une fenêtre lorsqu’un \_ \_ événement de rappel MEVT F est atteint dans le flux de sortie MIDI.
ms.assetid: afd2ba4c-ff6a-4e47-a7e8-a0da62650963
keywords:
- Message MM_MOM_POSITIONCB Windows Multimedia
topic_type:
- apiref
api_name:
- MM_MOM_POSITIONCB
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e86fd6f34ab44d307bbbb0e5fc9fd61d083ccda4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941731"
---
# <a name="mm_mom_positioncb-message"></a><span data-ttu-id="38ce7-104">\_Message POSITIONCB MOM de mm \_</span><span class="sxs-lookup"><span data-stu-id="38ce7-104">MM\_MOM\_POSITIONCB message</span></span>

<span data-ttu-id="38ce7-105">Le message de **\_ \_ POSITIONCB MOM mm** est envoyé à une fenêtre lorsqu’un \_ \_ événement de rappel MEVT F est atteint dans le flux de sortie MIDI.</span><span class="sxs-lookup"><span data-stu-id="38ce7-105">The **MM\_MOM\_POSITIONCB** message is sent to a window when an MEVT\_F\_CALLBACK event is reached in the MIDI output stream.</span></span>


```C++
MM_MOM_POSITIONCB 
wParam = (WPARAM) lpMidiHdr 
lParam = reserved 
```



## <a name="parameters"></a><span data-ttu-id="38ce7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="38ce7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38ce7-107"><span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*</span><span class="sxs-lookup"><span data-stu-id="38ce7-107"><span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*</span></span>
</dt> <dd>

<span data-ttu-id="38ce7-108">Pointeur vers une structure [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) qui identifie l’événement qui a provoqué le rappel.</span><span class="sxs-lookup"><span data-stu-id="38ce7-108">Pointer to a [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure that identifies the event that caused the callback.</span></span> <span data-ttu-id="38ce7-109">Le membre **dwOffset** donne le décalage de l’événement.</span><span class="sxs-lookup"><span data-stu-id="38ce7-109">The **dwOffset** member gives the offset of the event.</span></span>

</dd> <dt>

<span data-ttu-id="38ce7-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="38ce7-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="38ce7-111">Réservé n’utilisez pas.</span><span class="sxs-lookup"><span data-stu-id="38ce7-111">Reserved; do not use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38ce7-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="38ce7-112">Return Value</span></span>

<span data-ttu-id="38ce7-113">Ce message ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="38ce7-113">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="38ce7-114">Notes</span><span class="sxs-lookup"><span data-stu-id="38ce7-114">Remarks</span></span>

<span data-ttu-id="38ce7-115">La lecture de la mémoire tampon de flux continue même pendant l’exécution de la fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="38ce7-115">Playback of the stream buffer continues even while the callback function is executing.</span></span> <span data-ttu-id="38ce7-116">Les événements qui se trouvent après l' \_ \_ événement de rappel MEVT F dans la mémoire tampon sont planifiés et envoyés à temps, quel que soit le temps passé dans la fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="38ce7-116">Any events after the MEVT\_F\_CALLBACK event in the buffer will be scheduled and sent on time regardless of how much time is spent in the callback function.</span></span>

<span data-ttu-id="38ce7-117">Si les rappels de position sont générés plus rapidement que votre application ne peut les traiter, le membre **dwOffset** de la structure [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) peut faire référence à un événement que votre application n’a pas encore traitée.</span><span class="sxs-lookup"><span data-stu-id="38ce7-117">If position callbacks are being generated more quickly than your application can process them, the **dwOffset** member of the [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure might refer to an event your application has not yet processed.</span></span>

## <a name="requirements"></a><span data-ttu-id="38ce7-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="38ce7-118">Requirements</span></span>



| <span data-ttu-id="38ce7-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="38ce7-119">Requirement</span></span> | <span data-ttu-id="38ce7-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="38ce7-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38ce7-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="38ce7-121">Minimum supported client</span></span><br/> | <span data-ttu-id="38ce7-122">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="38ce7-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="38ce7-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="38ce7-123">Minimum supported server</span></span><br/> | <span data-ttu-id="38ce7-124">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="38ce7-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="38ce7-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="38ce7-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="38ce7-126"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="38ce7-126"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38ce7-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="38ce7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38ce7-128">Messages MIDI</span><span class="sxs-lookup"><span data-stu-id="38ce7-128">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

