---
title: Message WOM_OPEN (mmsystem. h)
description: Le \_ message WOM Open est envoyé à une fonction de rappel de sortie Waveform Audio lorsqu’un appareil de sortie Waveform-Audio est ouvert.
ms.assetid: 7fa175d3-7c07-4ca0-a0bd-4526fbc24f8d
keywords:
- Message WOM_OPEN Windows Multimedia
topic_type:
- apiref
api_name:
- WOM_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3cfca721019b28a5bf039e8c56c75892d85bd5e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102836"
---
# <a name="wom_open-message"></a><span data-ttu-id="66e62-104">WOM \_ ouvrir le message</span><span class="sxs-lookup"><span data-stu-id="66e62-104">WOM\_OPEN message</span></span>

<span data-ttu-id="66e62-105">Le message **WOM \_ Open** est envoyé à une fonction de rappel de sortie Waveform Audio lorsqu’un appareil de sortie Waveform-Audio est ouvert.</span><span class="sxs-lookup"><span data-stu-id="66e62-105">The **WOM\_OPEN** message is sent to a waveform-audio output callback function when a waveform-audio output device is opened.</span></span>


```C++
WOM_OPEN 
dwParam1 = reserved 
dwParam2 = reserved 
```



## <a name="parameters"></a><span data-ttu-id="66e62-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="66e62-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66e62-107"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="66e62-107"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span></span>
</dt> <dd>

<span data-ttu-id="66e62-108">Réservé doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="66e62-108">Reserved; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="66e62-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="66e62-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span></span>
</dt> <dd>

<span data-ttu-id="66e62-110">Réservé doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="66e62-110">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66e62-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="66e62-111">Return Value</span></span>

<span data-ttu-id="66e62-112">Ce message ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="66e62-112">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="66e62-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="66e62-113">Requirements</span></span>



| <span data-ttu-id="66e62-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="66e62-114">Requirement</span></span> | <span data-ttu-id="66e62-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="66e62-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66e62-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="66e62-116">Minimum supported client</span></span><br/> | <span data-ttu-id="66e62-117">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="66e62-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="66e62-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="66e62-118">Minimum supported server</span></span><br/> | <span data-ttu-id="66e62-119">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="66e62-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="66e62-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="66e62-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="66e62-121"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="66e62-121"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66e62-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="66e62-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66e62-123">Sons Waveform</span><span class="sxs-lookup"><span data-stu-id="66e62-123">Waveform Audio</span></span>](waveform-audio.md)
</dt> <dt>

[<span data-ttu-id="66e62-124">Messages de forme d’onde</span><span class="sxs-lookup"><span data-stu-id="66e62-124">Waveform Messages</span></span>](waveform-messages.md)
</dt> </dl>

 

 





