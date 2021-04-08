---
title: Message MCIWNDM_CAN_EJECT (VFW. h)
description: Le MCIWNDM \_ peut \_ éjecter le message pour déterminer si un périphérique MCI peut éjecter son support. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro MCIWndCanEject.
ms.assetid: e9bd33c4-0ad8-4c0a-8b75-52011b58904d
keywords:
- Message MCIWNDM_CAN_EJECT Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_CAN_EJECT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00ba54c9263e23fdd9830be892e4559ae3755c07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743685"
---
# <a name="mciwndm_can_eject-message"></a><span data-ttu-id="c9785-105">MCIWNDM \_ peut \_ éjecter le message</span><span class="sxs-lookup"><span data-stu-id="c9785-105">MCIWNDM\_CAN\_EJECT message</span></span>

<span data-ttu-id="c9785-106">Le **MCIWNDM \_ peut \_ éjecter** le message pour déterminer si un périphérique MCI peut éjecter son support.</span><span class="sxs-lookup"><span data-stu-id="c9785-106">The **MCIWNDM\_CAN\_EJECT** message determines if an MCI device can eject its media.</span></span> <span data-ttu-id="c9785-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**MCIWndCanEject**](/windows/desktop/api/Vfw/nf-vfw-mciwndcaneject) .</span><span class="sxs-lookup"><span data-stu-id="c9785-107">You can send this message explicitly or by using the [**MCIWndCanEject**](/windows/desktop/api/Vfw/nf-vfw-mciwndcaneject) macro.</span></span>


```C++
MCIWNDM_CAN_EJECT 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="c9785-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="c9785-108">Return Value</span></span>

<span data-ttu-id="c9785-109">Retourne la **valeur true** si l’appareil peut éjecter son média ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="c9785-109">Returns **TRUE** if the device can eject its media or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9785-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c9785-110">Requirements</span></span>



| <span data-ttu-id="c9785-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c9785-111">Requirement</span></span> | <span data-ttu-id="c9785-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="c9785-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="c9785-113">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c9785-113">Minimum supported client</span></span><br/> | <span data-ttu-id="c9785-114">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c9785-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="c9785-115">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c9785-115">Minimum supported server</span></span><br/> | <span data-ttu-id="c9785-116">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c9785-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="c9785-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="c9785-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9785-118"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9785-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9785-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c9785-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9785-120">**MCIWndCanEject**</span><span class="sxs-lookup"><span data-stu-id="c9785-120">**MCIWndCanEject**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndcaneject)
</dt> </dl>

 

 





