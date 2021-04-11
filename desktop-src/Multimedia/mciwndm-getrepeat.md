---
title: Message MCIWNDM_GETREPEAT (VFW. h)
description: Le \_ message MCIWNDM GETREPEAT détermine si la lecture continue a été activée. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro MCIWndGetRepeat.
ms.assetid: 6d644117-e705-421f-b45f-9f0e833e6bc8
keywords:
- Message MCIWNDM_GETREPEAT Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_GETREPEAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef47dc4f639c7aa34f7a00341e6ad2e19be909d1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103049"
---
# <a name="mciwndm_getrepeat-message"></a><span data-ttu-id="94063-105">\_Message MCIWNDM GETREPEAT</span><span class="sxs-lookup"><span data-stu-id="94063-105">MCIWNDM\_GETREPEAT message</span></span>

<span data-ttu-id="94063-106">Le message **MCIWNDM \_ GETREPEAT** détermine si la lecture continue a été activée.</span><span class="sxs-lookup"><span data-stu-id="94063-106">The **MCIWNDM\_GETREPEAT** message determines if continuous playback has been activated.</span></span> <span data-ttu-id="94063-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**MCIWndGetRepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetrepeat) .</span><span class="sxs-lookup"><span data-stu-id="94063-107">You can send this message explicitly or by using the [**MCIWndGetRepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetrepeat) macro.</span></span>


```C++
MCIWNDM_GETREPEAT 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="94063-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="94063-108">Return Value</span></span>

<span data-ttu-id="94063-109">Retourne la **valeur true** si la lecture continue est activée ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="94063-109">Returns **TRUE** if continuous playback is activated or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="94063-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="94063-110">Requirements</span></span>



| <span data-ttu-id="94063-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="94063-111">Requirement</span></span> | <span data-ttu-id="94063-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="94063-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="94063-113">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="94063-113">Minimum supported client</span></span><br/> | <span data-ttu-id="94063-114">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="94063-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="94063-115">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="94063-115">Minimum supported server</span></span><br/> | <span data-ttu-id="94063-116">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="94063-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="94063-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="94063-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="94063-118"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="94063-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94063-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="94063-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94063-120">**MCIWndGetRepeat**</span><span class="sxs-lookup"><span data-stu-id="94063-120">**MCIWndGetRepeat**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetrepeat)
</dt> </dl>

 

 





