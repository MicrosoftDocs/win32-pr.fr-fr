---
title: Message MOM_OPEN (mmsystem. h)
description: Le \_ message MOM Open est envoyé à une fonction de rappel de sortie MIDI lorsqu’un périphérique de sortie MIDI est ouvert.
ms.assetid: f3360482-7d16-419c-b5d1-0dd3a6e3c690
keywords:
- Message MOM_OPEN Windows Multimedia
topic_type:
- apiref
api_name:
- MOM_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24072aad6bff9ce192460c2c8525da4506f32746
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743364"
---
# <a name="mom_open-message"></a><span data-ttu-id="ff288-104">\_Message MOM ouvert</span><span class="sxs-lookup"><span data-stu-id="ff288-104">MOM\_OPEN message</span></span>

<span data-ttu-id="ff288-105">Le message **MOM \_ Open** est envoyé à une fonction de rappel de sortie MIDI lorsqu’un périphérique de sortie MIDI est ouvert.</span><span class="sxs-lookup"><span data-stu-id="ff288-105">The **MOM\_OPEN** message is sent to a MIDI output callback function when a MIDI output device is opened.</span></span>


```C++
MOM_OPEN 
dwParam1 = reserved 
dwParam2 = reserved 
```



## <a name="parameters"></a><span data-ttu-id="ff288-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ff288-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff288-107"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="ff288-107"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span></span>
</dt> <dd>

<span data-ttu-id="ff288-108">Réservé n’utilisez pas.</span><span class="sxs-lookup"><span data-stu-id="ff288-108">Reserved; do not use.</span></span>

</dd> <dt>

<span data-ttu-id="ff288-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="ff288-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span></span>
</dt> <dd>

<span data-ttu-id="ff288-110">Réservé n’utilisez pas.</span><span class="sxs-lookup"><span data-stu-id="ff288-110">Reserved; do not use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff288-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ff288-111">Return Value</span></span>

<span data-ttu-id="ff288-112">Ce message ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="ff288-112">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff288-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ff288-113">Requirements</span></span>



| <span data-ttu-id="ff288-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ff288-114">Requirement</span></span> | <span data-ttu-id="ff288-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="ff288-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff288-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ff288-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ff288-117">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ff288-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="ff288-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ff288-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ff288-119">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ff288-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="ff288-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="ff288-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="ff288-121"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ff288-121"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff288-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ff288-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff288-123">Messages MIDI</span><span class="sxs-lookup"><span data-stu-id="ff288-123">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

 





