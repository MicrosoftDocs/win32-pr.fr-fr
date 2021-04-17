---
title: Message MIM_CLOSE (mmsystem. h)
description: Le \_ message de fermeture MIM est envoyé à une fonction de rappel d’entrée MIDI lorsqu’un périphérique d’entrée MIDI est fermé.
ms.assetid: c19ecd3a-c3a5-4f17-9d44-d0d71eefcb15
keywords:
- Message MIM_CLOSE Windows Multimedia
topic_type:
- apiref
api_name:
- MIM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5549d9bef1e802b0b34ab6437b1386519a25d349
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508329"
---
# <a name="mim_close-message"></a><span data-ttu-id="b3c36-104">\_Message de fermeture MIM</span><span class="sxs-lookup"><span data-stu-id="b3c36-104">MIM\_CLOSE message</span></span>

<span data-ttu-id="b3c36-105">Le message de **\_ fermeture MIM** est envoyé à une fonction de rappel d’entrée MIDI lorsqu’un périphérique d’entrée MIDI est fermé.</span><span class="sxs-lookup"><span data-stu-id="b3c36-105">The **MIM\_CLOSE** message is sent to a MIDI input callback function when a MIDI input device is closed.</span></span>


```C++
MIM_CLOSE 
dwParam1 = reserved 
dwParam2 = reserved 
```



## <a name="parameters"></a><span data-ttu-id="b3c36-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b3c36-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3c36-107"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="b3c36-107"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span></span>
</dt> <dd>

<span data-ttu-id="b3c36-108">Réservé n’utilisez pas.</span><span class="sxs-lookup"><span data-stu-id="b3c36-108">Reserved; do not use.</span></span>

</dd> <dt>

<span data-ttu-id="b3c36-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="b3c36-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span></span>
</dt> <dd>

<span data-ttu-id="b3c36-110">Réservé n’utilisez pas.</span><span class="sxs-lookup"><span data-stu-id="b3c36-110">Reserved; do not use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3c36-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b3c36-111">Return Value</span></span>

<span data-ttu-id="b3c36-112">Ce message ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="b3c36-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3c36-113">Notes</span><span class="sxs-lookup"><span data-stu-id="b3c36-113">Remarks</span></span>

<span data-ttu-id="b3c36-114">Le descripteur d’appareil n’est plus valide une fois que ce message a été envoyé.</span><span class="sxs-lookup"><span data-stu-id="b3c36-114">The device handle is no longer valid after this message has been sent.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3c36-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b3c36-115">Requirements</span></span>



| <span data-ttu-id="b3c36-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b3c36-116">Requirement</span></span> | <span data-ttu-id="b3c36-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="b3c36-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3c36-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b3c36-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b3c36-119">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b3c36-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="b3c36-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b3c36-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b3c36-121">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b3c36-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="b3c36-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="b3c36-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="b3c36-123"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b3c36-123"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3c36-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b3c36-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3c36-125">Interface MIDI (Musical Instrument Digital Interface)</span><span class="sxs-lookup"><span data-stu-id="b3c36-125">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="b3c36-126">Messages MIDI</span><span class="sxs-lookup"><span data-stu-id="b3c36-126">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

 





