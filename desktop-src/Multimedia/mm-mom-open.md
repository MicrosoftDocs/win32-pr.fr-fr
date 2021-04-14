---
title: Message MM_MOM_OPEN (mmsystem. h)
description: Le \_ \_ message Open MOM de mm est envoyé à une fenêtre lorsqu’un appareil de sortie MIDI est ouvert.
ms.assetid: 1374a07c-02fa-4b43-82df-cbd96302aec5
keywords:
- Message MM_MOM_OPEN Windows Multimedia
topic_type:
- apiref
api_name:
- MM_MOM_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2f676dccf532290ab2153b888c20fad7b19d98d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464215"
---
# <a name="mm_mom_open-message"></a><span data-ttu-id="e190f-104">MM \_ \_ message ouvert MOM</span><span class="sxs-lookup"><span data-stu-id="e190f-104">MM\_MOM\_OPEN message</span></span>

<span data-ttu-id="e190f-105">Le **message \_ \_ Open MOM de mm** est envoyé à une fenêtre lorsqu’un appareil de sortie MIDI est ouvert.</span><span class="sxs-lookup"><span data-stu-id="e190f-105">The **MM\_MOM\_OPEN** message is sent to a window when a MIDI output device is opened.</span></span>


```C++
MM_MOM_OPEN 
wParam = (WPARAM) hOutput 
lParam = reserved 
```



## <a name="parameters"></a><span data-ttu-id="e190f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e190f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e190f-107"><span id="hOutput"></span><span id="houtput"></span><span id="HOUTPUT"></span>*hOutput*</span><span class="sxs-lookup"><span data-stu-id="e190f-107"><span id="hOutput"></span><span id="houtput"></span><span id="HOUTPUT"></span>*hOutput*</span></span>
</dt> <dd>

<span data-ttu-id="e190f-108">Handle sur le périphérique de sortie MIDI.</span><span class="sxs-lookup"><span data-stu-id="e190f-108">Handle to the MIDI output device.</span></span>

</dd> <dt>

<span data-ttu-id="e190f-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="e190f-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="e190f-110">Réservé n’utilisez pas.</span><span class="sxs-lookup"><span data-stu-id="e190f-110">Reserved; do not use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e190f-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="e190f-111">Return Value</span></span>

<span data-ttu-id="e190f-112">Ce message ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="e190f-112">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="e190f-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e190f-113">Requirements</span></span>



| <span data-ttu-id="e190f-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e190f-114">Requirement</span></span> | <span data-ttu-id="e190f-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="e190f-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e190f-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e190f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e190f-117">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e190f-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="e190f-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e190f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e190f-119">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e190f-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="e190f-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="e190f-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="e190f-121"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e190f-121"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e190f-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e190f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e190f-123">Messages MIDI</span><span class="sxs-lookup"><span data-stu-id="e190f-123">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

 





