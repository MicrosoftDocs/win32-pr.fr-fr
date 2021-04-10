---
title: Message MM_MIM_CLOSE (mmsystem. h)
description: Le \_ message de \_ fermeture MIM mm est envoyé à une fenêtre lorsqu’un périphérique d’entrée MIDI est fermé.
ms.assetid: 261021aa-4df6-44d8-aad3-5f98b1213459
keywords:
- Message MM_MIM_CLOSE Windows Multimedia
topic_type:
- apiref
api_name:
- MM_MIM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8ce511365b1faa49faefaf4ed25c5b8befb2288
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942432"
---
# <a name="mm_mim_close-message"></a><span data-ttu-id="fefe8-104">MM \_ \_ message de fermeture MIM</span><span class="sxs-lookup"><span data-stu-id="fefe8-104">MM\_MIM\_CLOSE message</span></span>

<span data-ttu-id="fefe8-105">Le message de **\_ \_ fermeture MIM mm** est envoyé à une fenêtre lorsqu’un périphérique d’entrée MIDI est fermé.</span><span class="sxs-lookup"><span data-stu-id="fefe8-105">The **MM\_MIM\_CLOSE** message is sent to a window when a MIDI input device is closed.</span></span>


```C++
MM_MIM_CLOSE 
wParam = (WPARAM) hInput 
lParam = reserved 
```



## <a name="parameters"></a><span data-ttu-id="fefe8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fefe8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fefe8-107"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*</span><span class="sxs-lookup"><span data-stu-id="fefe8-107"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*</span></span>
</dt> <dd>

<span data-ttu-id="fefe8-108">Handle vers l’appareil d’entrée MIDI qui a été fermé.</span><span class="sxs-lookup"><span data-stu-id="fefe8-108">Handle to the MIDI input device that was closed.</span></span>

</dd> <dt>

<span data-ttu-id="fefe8-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="fefe8-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="fefe8-110">Réservé n’utilisez pas.</span><span class="sxs-lookup"><span data-stu-id="fefe8-110">Reserved; do not use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fefe8-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="fefe8-111">Return Value</span></span>

<span data-ttu-id="fefe8-112">Ce message ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="fefe8-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fefe8-113">Notes</span><span class="sxs-lookup"><span data-stu-id="fefe8-113">Remarks</span></span>

<span data-ttu-id="fefe8-114">Le descripteur d’appareil n’est plus valide une fois que ce message a été envoyé.</span><span class="sxs-lookup"><span data-stu-id="fefe8-114">The device handle is no longer valid after this message has been sent.</span></span>

## <a name="requirements"></a><span data-ttu-id="fefe8-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fefe8-115">Requirements</span></span>



| <span data-ttu-id="fefe8-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fefe8-116">Requirement</span></span> | <span data-ttu-id="fefe8-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="fefe8-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fefe8-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fefe8-118">Minimum supported client</span></span><br/> | <span data-ttu-id="fefe8-119">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fefe8-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="fefe8-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fefe8-120">Minimum supported server</span></span><br/> | <span data-ttu-id="fefe8-121">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fefe8-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="fefe8-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="fefe8-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="fefe8-123"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fefe8-123"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fefe8-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fefe8-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fefe8-125">Interface MIDI (Musical Instrument Digital Interface)</span><span class="sxs-lookup"><span data-stu-id="fefe8-125">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="fefe8-126">Messages MIDI</span><span class="sxs-lookup"><span data-stu-id="fefe8-126">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

 





