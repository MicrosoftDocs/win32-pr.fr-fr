---
title: Message MM_WIM_OPEN (mmsystem. h)
description: Le \_ \_ message d’ouverture Wim mm est envoyé à une fenêtre quand un appareil d’entrée Waveform-Audio est ouvert.
ms.assetid: 4c646f58-c324-467e-871b-8fc36d5b89bc
keywords:
- Message MM_WIM_OPEN Windows Multimedia
topic_type:
- apiref
api_name:
- MM_WIM_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64ff028dcd9dc851d94699ef5cb75707429ba149
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033259"
---
# <a name="mm_wim_open-message"></a><span data-ttu-id="1c58d-104">MM \_ \_ message ouvert Wim</span><span class="sxs-lookup"><span data-stu-id="1c58d-104">MM\_WIM\_OPEN message</span></span>

<span data-ttu-id="1c58d-105">Le message d' **\_ \_ ouverture Wim mm** est envoyé à une fenêtre quand un appareil d’entrée Waveform-Audio est ouvert.</span><span class="sxs-lookup"><span data-stu-id="1c58d-105">The **MM\_WIM\_OPEN** message is sent to a window when a waveform-audio input device is opened.</span></span>


```C++
MM_WIM_OPEN 
wParam = (WPARAM) hInputDev 
lParam = reserved 
```



## <a name="parameters"></a><span data-ttu-id="1c58d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1c58d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c58d-107"><span id="hInputDev"></span><span id="hinputdev"></span><span id="HINPUTDEV"></span>*hInputDev*</span><span class="sxs-lookup"><span data-stu-id="1c58d-107"><span id="hInputDev"></span><span id="hinputdev"></span><span id="HINPUTDEV"></span>*hInputDev*</span></span>
</dt> <dd>

<span data-ttu-id="1c58d-108">Handle de l’appareil qui a été ouvert.</span><span class="sxs-lookup"><span data-stu-id="1c58d-108">Handle to the device that was opened.</span></span>

</dd> <dt>

<span data-ttu-id="1c58d-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="1c58d-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="1c58d-110">Réservé doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="1c58d-110">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c58d-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="1c58d-111">Return Value</span></span>

<span data-ttu-id="1c58d-112">Ce message ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="1c58d-112">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c58d-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1c58d-113">Requirements</span></span>



| <span data-ttu-id="1c58d-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1c58d-114">Requirement</span></span> | <span data-ttu-id="1c58d-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="1c58d-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c58d-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1c58d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="1c58d-117">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1c58d-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="1c58d-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1c58d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="1c58d-119">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1c58d-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="1c58d-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="1c58d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="1c58d-121"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1c58d-121"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c58d-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1c58d-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c58d-123">Sons Waveform</span><span class="sxs-lookup"><span data-stu-id="1c58d-123">Waveform Audio</span></span>](waveform-audio.md)
</dt> <dt>

[<span data-ttu-id="1c58d-124">Messages de forme d’onde</span><span class="sxs-lookup"><span data-stu-id="1c58d-124">Waveform Messages</span></span>](waveform-messages.md)
</dt> </dl>

 

 





