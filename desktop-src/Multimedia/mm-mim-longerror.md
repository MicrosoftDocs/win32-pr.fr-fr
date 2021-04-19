---
title: Message MM_MIM_LONGERROR (mmsystem. h)
description: Le \_ message mm MIM \_ LONGERROR est envoyé à une fenêtre lorsqu’un message System-exclusive midi non valide ou incomplet est reçu.
ms.assetid: 2de4c2f8-2ded-4994-934c-6e72c95637b2
keywords:
- Message MM_MIM_LONGERROR Windows Multimedia
topic_type:
- apiref
api_name:
- MM_MIM_LONGERROR
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e274faca26a90a5cd3b3915a7e8e1ed27bcfd77
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510349"
---
# <a name="mm_mim_longerror-message"></a><span data-ttu-id="e13ad-104">MM \_ \_ message LONGERROR MIM</span><span class="sxs-lookup"><span data-stu-id="e13ad-104">MM\_MIM\_LONGERROR message</span></span>

<span data-ttu-id="e13ad-105">Le message **mm \_ MIM \_ LONGERROR** est envoyé à une fenêtre lorsqu’un message System-exclusive midi non valide ou incomplet est reçu.</span><span class="sxs-lookup"><span data-stu-id="e13ad-105">The **MM\_MIM\_LONGERROR** message is sent to a window when an invalid or incomplete MIDI system-exclusive message is received.</span></span>


```C++
MM_MIM_LONGERROR 
wParam = (WPARAM) hInput 
lParam = (LPARAM) lpMidiHdr 
```



## <a name="parameters"></a><span data-ttu-id="e13ad-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e13ad-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e13ad-107"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*</span><span class="sxs-lookup"><span data-stu-id="e13ad-107"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*</span></span>
</dt> <dd>

<span data-ttu-id="e13ad-108">Handle vers l’appareil d’entrée MIDI qui a reçu le message non valide.</span><span class="sxs-lookup"><span data-stu-id="e13ad-108">Handle to the MIDI input device that received the invalid message.</span></span>

</dd> <dt>

<span data-ttu-id="e13ad-109"><span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*</span><span class="sxs-lookup"><span data-stu-id="e13ad-109"><span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*</span></span>
</dt> <dd>

<span data-ttu-id="e13ad-110">Pointeur vers une structure [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) identifiant la mémoire tampon contenant le message non valide.</span><span class="sxs-lookup"><span data-stu-id="e13ad-110">Pointer to a [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure identifying the buffer containing the invalid message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e13ad-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="e13ad-111">Return Value</span></span>

<span data-ttu-id="e13ad-112">Ce message ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="e13ad-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e13ad-113">Notes</span><span class="sxs-lookup"><span data-stu-id="e13ad-113">Remarks</span></span>

<span data-ttu-id="e13ad-114">La mémoire tampon retournée n’est peut-être pas pleine.</span><span class="sxs-lookup"><span data-stu-id="e13ad-114">The returned buffer might not be full.</span></span> <span data-ttu-id="e13ad-115">Pour déterminer le nombre d’octets enregistrés dans la mémoire tampon retournée, utilisez le membre **dwBytesRecorded** de la structure [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) spécifiée par *lpMidiHdr*.</span><span class="sxs-lookup"><span data-stu-id="e13ad-115">To determine the number of bytes recorded into the returned buffer, use the **dwBytesRecorded** member of the [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure specified by *lpMidiHdr*.</span></span>

## <a name="requirements"></a><span data-ttu-id="e13ad-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e13ad-116">Requirements</span></span>



| <span data-ttu-id="e13ad-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e13ad-117">Requirement</span></span> | <span data-ttu-id="e13ad-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="e13ad-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e13ad-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e13ad-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e13ad-120">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e13ad-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="e13ad-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e13ad-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e13ad-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e13ad-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="e13ad-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="e13ad-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e13ad-124"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e13ad-124"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e13ad-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e13ad-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e13ad-126">Interface MIDI (Musical Instrument Digital Interface)</span><span class="sxs-lookup"><span data-stu-id="e13ad-126">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="e13ad-127">Messages MIDI</span><span class="sxs-lookup"><span data-stu-id="e13ad-127">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

