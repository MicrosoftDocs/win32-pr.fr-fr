---
title: Message MOM_CLOSE (mmsystem. h)
description: Le \_ message de fermeture MOM est envoyé à une fonction de rappel de sortie MIDI lorsqu’un périphérique de sortie MIDI est fermé.
ms.assetid: 229b3701-16f1-4ec8-920e-cd8231561541
keywords:
- Message MOM_CLOSE Windows Multimedia
topic_type:
- apiref
api_name:
- MOM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68f173daa2fb104305979a72c9a14106175d7d20
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942746"
---
# <a name="mom_close-message"></a><span data-ttu-id="5cfb8-104">\_Message de fermeture MOM</span><span class="sxs-lookup"><span data-stu-id="5cfb8-104">MOM\_CLOSE message</span></span>

<span data-ttu-id="5cfb8-105">Le message de **\_ fermeture MOM** est envoyé à une fonction de rappel de sortie MIDI lorsqu’un périphérique de sortie MIDI est fermé.</span><span class="sxs-lookup"><span data-stu-id="5cfb8-105">The **MOM\_CLOSE** message is sent to a MIDI output callback function when a MIDI output device is closed.</span></span>


```C++
MOM_CLOSE 
dwParam1 = reserved 
dwParam2 = reserved 
```



## <a name="parameters"></a><span data-ttu-id="5cfb8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5cfb8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5cfb8-107"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="5cfb8-107"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span></span>
</dt> <dd>

<span data-ttu-id="5cfb8-108">Réservé n’utilisez pas.</span><span class="sxs-lookup"><span data-stu-id="5cfb8-108">Reserved; do not use.</span></span>

</dd> <dt>

<span data-ttu-id="5cfb8-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="5cfb8-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span></span>
</dt> <dd>

<span data-ttu-id="5cfb8-110">Réservé n’utilisez pas.</span><span class="sxs-lookup"><span data-stu-id="5cfb8-110">Reserved; do not use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5cfb8-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="5cfb8-111">Return Value</span></span>

<span data-ttu-id="5cfb8-112">Ce message ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="5cfb8-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5cfb8-113">Notes</span><span class="sxs-lookup"><span data-stu-id="5cfb8-113">Remarks</span></span>

<span data-ttu-id="5cfb8-114">Le descripteur d’appareil n’est plus valide une fois que ce message a été envoyé.</span><span class="sxs-lookup"><span data-stu-id="5cfb8-114">The device handle is no longer valid after this message has been sent.</span></span>

## <a name="requirements"></a><span data-ttu-id="5cfb8-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5cfb8-115">Requirements</span></span>



| <span data-ttu-id="5cfb8-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5cfb8-116">Requirement</span></span> | <span data-ttu-id="5cfb8-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="5cfb8-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5cfb8-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5cfb8-118">Minimum supported client</span></span><br/> | <span data-ttu-id="5cfb8-119">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5cfb8-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="5cfb8-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5cfb8-120">Minimum supported server</span></span><br/> | <span data-ttu-id="5cfb8-121">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5cfb8-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="5cfb8-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="5cfb8-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="5cfb8-123"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5cfb8-123"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5cfb8-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5cfb8-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5cfb8-125">Messages MIDI</span><span class="sxs-lookup"><span data-stu-id="5cfb8-125">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

 





