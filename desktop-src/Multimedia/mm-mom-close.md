---
title: Message MM_MOM_CLOSE (mmsystem. h)
description: Le message de fermeture de MM \_ MOM \_ est envoyé à une fenêtre lorsqu’un périphérique de sortie MIDI est fermé.
ms.assetid: 4829bbe5-5103-4354-88a7-37def22e926e
keywords:
- Message MM_MOM_CLOSE Windows Multimedia
topic_type:
- apiref
api_name:
- MM_MOM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ae55cbca7c5effc146dee0c5ef9be67469a9201
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464498"
---
# <a name="mm_mom_close-message"></a><span data-ttu-id="8bb34-104">Message de fermeture de \_ MOM mm \_</span><span class="sxs-lookup"><span data-stu-id="8bb34-104">MM\_MOM\_CLOSE message</span></span>

<span data-ttu-id="8bb34-105">Le message de **\_ \_ fermeture de mm MOM** est envoyé à une fenêtre lorsqu’un périphérique de sortie MIDI est fermé.</span><span class="sxs-lookup"><span data-stu-id="8bb34-105">The **MM\_MOM\_CLOSE** message is sent to a window when a MIDI output device is closed.</span></span>


```C++
MM_MOM_CLOSE 
wParam = (WPARAM) hOutput 
lParam = reserved 
```



## <a name="parameters"></a><span data-ttu-id="8bb34-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8bb34-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8bb34-107"><span id="hOutput"></span><span id="houtput"></span><span id="HOUTPUT"></span>*hOutput*</span><span class="sxs-lookup"><span data-stu-id="8bb34-107"><span id="hOutput"></span><span id="houtput"></span><span id="HOUTPUT"></span>*hOutput*</span></span>
</dt> <dd>

<span data-ttu-id="8bb34-108">Handle sur le périphérique de sortie MIDI.</span><span class="sxs-lookup"><span data-stu-id="8bb34-108">Handle to the MIDI output device.</span></span>

</dd> <dt>

<span data-ttu-id="8bb34-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="8bb34-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="8bb34-110">Réservé n’utilisez pas.</span><span class="sxs-lookup"><span data-stu-id="8bb34-110">Reserved; do not use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8bb34-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="8bb34-111">Return Value</span></span>

<span data-ttu-id="8bb34-112">Ce message ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="8bb34-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8bb34-113">Notes</span><span class="sxs-lookup"><span data-stu-id="8bb34-113">Remarks</span></span>

<span data-ttu-id="8bb34-114">Le descripteur d’appareil n’est plus valide une fois que ce message a été envoyé.</span><span class="sxs-lookup"><span data-stu-id="8bb34-114">The device handle is no longer valid after this message has been sent.</span></span>

## <a name="requirements"></a><span data-ttu-id="8bb34-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8bb34-115">Requirements</span></span>



| <span data-ttu-id="8bb34-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8bb34-116">Requirement</span></span> | <span data-ttu-id="8bb34-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="8bb34-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8bb34-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8bb34-118">Minimum supported client</span></span><br/> | <span data-ttu-id="8bb34-119">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8bb34-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="8bb34-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8bb34-120">Minimum supported server</span></span><br/> | <span data-ttu-id="8bb34-121">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8bb34-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="8bb34-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="8bb34-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="8bb34-123"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8bb34-123"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8bb34-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8bb34-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8bb34-125">Messages MIDI</span><span class="sxs-lookup"><span data-stu-id="8bb34-125">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

 





