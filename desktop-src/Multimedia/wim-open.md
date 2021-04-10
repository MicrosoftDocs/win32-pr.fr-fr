---
title: Message WIM_OPEN (mmsystem. h)
description: Le \_ message Wim Open est envoyé à une fonction de rappel d’entrée Waveform Audio quand un appareil d’entrée Waveform-Audio est ouvert.
ms.assetid: de18e6b2-ea28-46d9-812c-e6dac49838ee
keywords:
- Message WIM_OPEN Windows Multimedia
topic_type:
- apiref
api_name:
- WIM_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57c1661482149c90cf3f2bd6b10620cb32f380be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942685"
---
# <a name="wim_open-message"></a><span data-ttu-id="7762e-104">\_Message Wim ouvert</span><span class="sxs-lookup"><span data-stu-id="7762e-104">WIM\_OPEN message</span></span>

<span data-ttu-id="7762e-105">Le message **Wim \_ Open** est envoyé à une fonction de rappel d’entrée Waveform Audio quand un appareil d’entrée Waveform-Audio est ouvert.</span><span class="sxs-lookup"><span data-stu-id="7762e-105">The **WIM\_OPEN** message is sent to a waveform-audio input callback function when a waveform-audio input device is opened.</span></span>


```C++
WIM_OPEN 
dwParam1 = reserved 
dwParam2 = reserved 
```



## <a name="parameters"></a><span data-ttu-id="7762e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7762e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7762e-107"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="7762e-107"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span></span>
</dt> <dd>

<span data-ttu-id="7762e-108">Réservé doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="7762e-108">Reserved; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="7762e-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="7762e-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span></span>
</dt> <dd>

<span data-ttu-id="7762e-110">Réservé doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="7762e-110">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7762e-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="7762e-111">Return Value</span></span>

<span data-ttu-id="7762e-112">Ce message ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="7762e-112">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="7762e-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7762e-113">Requirements</span></span>



| <span data-ttu-id="7762e-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7762e-114">Requirement</span></span> | <span data-ttu-id="7762e-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="7762e-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7762e-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7762e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="7762e-117">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7762e-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="7762e-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7762e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="7762e-119">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7762e-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="7762e-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="7762e-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="7762e-121"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7762e-121"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7762e-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7762e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7762e-123">Sons Waveform</span><span class="sxs-lookup"><span data-stu-id="7762e-123">Waveform Audio</span></span>](waveform-audio.md)
</dt> <dt>

[<span data-ttu-id="7762e-124">Messages de forme d’onde</span><span class="sxs-lookup"><span data-stu-id="7762e-124">Waveform Messages</span></span>](waveform-messages.md)
</dt> </dl>

 

 





