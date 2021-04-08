---
title: Message MM_MIM_OPEN (mmsystem. h)
description: Le \_ \_ message d’ouverture MIM mm est envoyé à une fenêtre lorsqu’un périphérique d’entrée MIDI est ouvert.
ms.assetid: 8dfc24a0-0ab8-4f49-954f-0c0a55fa28bc
keywords:
- Message MM_MIM_OPEN Windows Multimedia
topic_type:
- apiref
api_name:
- MM_MIM_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7d87e391336b948d0c784048baeffa7bba88b29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843041"
---
# <a name="mm_mim_open-message"></a><span data-ttu-id="fe4f5-104">MM \_ \_ message ouvert MIM</span><span class="sxs-lookup"><span data-stu-id="fe4f5-104">MM\_MIM\_OPEN message</span></span>

<span data-ttu-id="fe4f5-105">Le message d' **\_ \_ ouverture MIM mm** est envoyé à une fenêtre lorsqu’un périphérique d’entrée MIDI est ouvert.</span><span class="sxs-lookup"><span data-stu-id="fe4f5-105">The **MM\_MIM\_OPEN** message is sent to a window when a MIDI input device is opened.</span></span>


```C++
MM_MIM_OPEN 
wParam = (WPARAM) hInput 
lParam = reserved 
```



## <a name="parameters"></a><span data-ttu-id="fe4f5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fe4f5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe4f5-107"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*</span><span class="sxs-lookup"><span data-stu-id="fe4f5-107"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*</span></span>
</dt> <dd>

<span data-ttu-id="fe4f5-108">Handle vers l’appareil d’entrée MIDI qui a été ouvert.</span><span class="sxs-lookup"><span data-stu-id="fe4f5-108">Handle to the MIDI input device that was opened.</span></span>

</dd> <dt>

<span data-ttu-id="fe4f5-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="fe4f5-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="fe4f5-110">Réservé n’utilisez pas.</span><span class="sxs-lookup"><span data-stu-id="fe4f5-110">Reserved; do not use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe4f5-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="fe4f5-111">Return Value</span></span>

<span data-ttu-id="fe4f5-112">Ce message ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="fe4f5-112">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe4f5-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fe4f5-113">Requirements</span></span>



| <span data-ttu-id="fe4f5-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fe4f5-114">Requirement</span></span> | <span data-ttu-id="fe4f5-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="fe4f5-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe4f5-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fe4f5-116">Minimum supported client</span></span><br/> | <span data-ttu-id="fe4f5-117">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fe4f5-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="fe4f5-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fe4f5-118">Minimum supported server</span></span><br/> | <span data-ttu-id="fe4f5-119">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fe4f5-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="fe4f5-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="fe4f5-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe4f5-121"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fe4f5-121"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe4f5-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fe4f5-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe4f5-123">Interface MIDI (Musical Instrument Digital Interface)</span><span class="sxs-lookup"><span data-stu-id="fe4f5-123">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="fe4f5-124">Messages MIDI</span><span class="sxs-lookup"><span data-stu-id="fe4f5-124">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

 





