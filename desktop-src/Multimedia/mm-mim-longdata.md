---
title: Message MM_MIM_LONGDATA (mmsystem. h)
description: Le \_ message mm MIM \_ LONGDATA est envoyé à une fenêtre lors de la réception d’un message MIDI système exclusif complet ou lorsqu’une mémoire tampon a été remplie avec des données système exclusives.
ms.assetid: 72b9eade-4224-436f-bfef-32204eaf51ae
keywords:
- Message MM_MIM_LONGDATA Windows Multimedia
topic_type:
- apiref
api_name:
- MM_MIM_LONGDATA
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25bf1900ef2e9394b9d8772747eba873f8d607f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105904"
---
# <a name="mm_mim_longdata-message"></a><span data-ttu-id="be149-104">MM \_ \_ message LONGDATA MIM</span><span class="sxs-lookup"><span data-stu-id="be149-104">MM\_MIM\_LONGDATA message</span></span>

<span data-ttu-id="be149-105">Le message **mm \_ MIM \_ LONGDATA** est envoyé à une fenêtre lors de la réception d’un message MIDI système exclusif complet ou lorsqu’une mémoire tampon a été remplie avec des données système exclusives.</span><span class="sxs-lookup"><span data-stu-id="be149-105">The **MM\_MIM\_LONGDATA** message is sent to a window when either a complete MIDI system-exclusive message is received or when a buffer has been filled with system-exclusive data.</span></span>


```C++
MM_MIM_LONGDATA 
wParam = (WPARAM) hInput 
lParam = (LPARAM) lpMidiHdr 
```



## <a name="parameters"></a><span data-ttu-id="be149-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="be149-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be149-107"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*</span><span class="sxs-lookup"><span data-stu-id="be149-107"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*</span></span>
</dt> <dd>

<span data-ttu-id="be149-108">Handle vers l’appareil d’entrée MIDI qui a reçu les données.</span><span class="sxs-lookup"><span data-stu-id="be149-108">Handle to the MIDI input device that received the data.</span></span>

</dd> <dt>

<span data-ttu-id="be149-109"><span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*</span><span class="sxs-lookup"><span data-stu-id="be149-109"><span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*</span></span>
</dt> <dd>

<span data-ttu-id="be149-110">Pointeur vers une structure [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) identifiant la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="be149-110">Pointer to a [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure identifying the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be149-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="be149-111">Return Value</span></span>

<span data-ttu-id="be149-112">Ce message ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="be149-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="be149-113">Notes</span><span class="sxs-lookup"><span data-stu-id="be149-113">Remarks</span></span>

<span data-ttu-id="be149-114">La mémoire tampon retournée n’est peut-être pas pleine.</span><span class="sxs-lookup"><span data-stu-id="be149-114">The returned buffer might not be full.</span></span> <span data-ttu-id="be149-115">Pour déterminer le nombre d’octets enregistrés dans la mémoire tampon retournée, utilisez le membre **dwBytesRecorded** de la structure [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) vers laquelle pointe *lpMidiHdr*.</span><span class="sxs-lookup"><span data-stu-id="be149-115">To determine the number of bytes recorded into the returned buffer, use the **dwBytesRecorded** member of the [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure pointed to by *lpMidiHdr*.</span></span>

<span data-ttu-id="be149-116">Aucun horodatage n’est disponible avec ce message.</span><span class="sxs-lookup"><span data-stu-id="be149-116">No time stamp is available with this message.</span></span> <span data-ttu-id="be149-117">Pour les données d’entrée horodatées, vous devez utiliser les messages envoyés aux fonctions de rappel.</span><span class="sxs-lookup"><span data-stu-id="be149-117">For time-stamped input data, you must use the messages that are sent to callback functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="be149-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="be149-118">Requirements</span></span>



| <span data-ttu-id="be149-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="be149-119">Requirement</span></span> | <span data-ttu-id="be149-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="be149-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be149-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="be149-121">Minimum supported client</span></span><br/> | <span data-ttu-id="be149-122">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="be149-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="be149-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="be149-123">Minimum supported server</span></span><br/> | <span data-ttu-id="be149-124">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="be149-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="be149-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="be149-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="be149-126"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="be149-126"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be149-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="be149-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be149-128">Interface MIDI (Musical Instrument Digital Interface)</span><span class="sxs-lookup"><span data-stu-id="be149-128">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="be149-129">Messages MIDI</span><span class="sxs-lookup"><span data-stu-id="be149-129">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

