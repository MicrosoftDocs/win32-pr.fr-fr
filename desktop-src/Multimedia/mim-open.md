---
title: Message MIM_OPEN (mmsystem. h)
description: Le \_ message MIM Open est envoyé à une fonction de rappel d’entrée MIDI lorsqu’un périphérique d’entrée MIDI est ouvert.
ms.assetid: c7a8b856-aedd-457d-8a21-0ec2e9303960
keywords:
- Message MIM_OPEN Windows Multimedia
topic_type:
- apiref
api_name:
- MIM_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49fcfd05ef7702fbc7bf3108365e49660071ae9a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104383979"
---
# <a name="mim_open-message"></a><span data-ttu-id="0a36a-104">\_Message MIM ouvert</span><span class="sxs-lookup"><span data-stu-id="0a36a-104">MIM\_OPEN message</span></span>

<span data-ttu-id="0a36a-105">Le message **MIM \_ Open** est envoyé à une fonction de rappel d’entrée MIDI lorsqu’un périphérique d’entrée MIDI est ouvert.</span><span class="sxs-lookup"><span data-stu-id="0a36a-105">The **MIM\_OPEN** message is sent to a MIDI input callback function when a MIDI input device is opened.</span></span>


```C++
MIM_OPEN 
dwParam1 = reserved 
dwParam2 = reserved 
```



## <a name="parameters"></a><span data-ttu-id="0a36a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0a36a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a36a-107"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="0a36a-107"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span></span>
</dt> <dd>

<span data-ttu-id="0a36a-108">Réservé n’utilisez pas.</span><span class="sxs-lookup"><span data-stu-id="0a36a-108">Reserved; do not use.</span></span>

</dd> <dt>

<span data-ttu-id="0a36a-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="0a36a-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span></span>
</dt> <dd>

<span data-ttu-id="0a36a-110">Réservé n’utilisez pas.</span><span class="sxs-lookup"><span data-stu-id="0a36a-110">Reserved; do not use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a36a-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="0a36a-111">Return Value</span></span>

<span data-ttu-id="0a36a-112">Ce message ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="0a36a-112">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a36a-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0a36a-113">Requirements</span></span>



| <span data-ttu-id="0a36a-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0a36a-114">Requirement</span></span> | <span data-ttu-id="0a36a-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="0a36a-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a36a-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0a36a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="0a36a-117">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0a36a-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="0a36a-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0a36a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="0a36a-119">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0a36a-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="0a36a-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="0a36a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="0a36a-121"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0a36a-121"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a36a-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0a36a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a36a-123">Interface MIDI (Musical Instrument Digital Interface)</span><span class="sxs-lookup"><span data-stu-id="0a36a-123">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="0a36a-124">Messages MIDI</span><span class="sxs-lookup"><span data-stu-id="0a36a-124">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

 





