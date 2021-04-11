---
title: Message MCIWNDM_GETPALETTE (VFW. h)
description: Le \_ message MCIWNDM GETPALETTE récupère un descripteur de la palette utilisée par un périphérique MCI. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro MCIWndGetPalette.
ms.assetid: f8426344-0fee-4419-9d8a-dcee26cb4c28
keywords:
- Message MCIWNDM_GETPALETTE Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_GETPALETTE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: faec3dd5d9c401d943fbc55ca58e452d3fb25497
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032468"
---
# <a name="mciwndm_getpalette-message"></a><span data-ttu-id="60e76-105">\_Message MCIWNDM GETPALETTE</span><span class="sxs-lookup"><span data-stu-id="60e76-105">MCIWNDM\_GETPALETTE message</span></span>

<span data-ttu-id="60e76-106">Le message **MCIWNDM \_ GETPALETTE** récupère un descripteur de la palette utilisée par un périphérique MCI.</span><span class="sxs-lookup"><span data-stu-id="60e76-106">The **MCIWNDM\_GETPALETTE** message retrieves a handle of the palette used by an MCI device.</span></span> <span data-ttu-id="60e76-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**MCIWndGetPalette**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpalette) .</span><span class="sxs-lookup"><span data-stu-id="60e76-107">You can send this message explicitly or by using the [**MCIWndGetPalette**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpalette) macro.</span></span>


```C++
MCIWNDM_GETPALETTE 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="60e76-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="60e76-108">Return Value</span></span>

<span data-ttu-id="60e76-109">Retourne le handle de la palette en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="60e76-109">Returns the handle of the palette if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="60e76-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="60e76-110">Requirements</span></span>



| <span data-ttu-id="60e76-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="60e76-111">Requirement</span></span> | <span data-ttu-id="60e76-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="60e76-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="60e76-113">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="60e76-113">Minimum supported client</span></span><br/> | <span data-ttu-id="60e76-114">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="60e76-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="60e76-115">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="60e76-115">Minimum supported server</span></span><br/> | <span data-ttu-id="60e76-116">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="60e76-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="60e76-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="60e76-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="60e76-118"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="60e76-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60e76-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="60e76-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60e76-120">**MCIWndGetPalette**</span><span class="sxs-lookup"><span data-stu-id="60e76-120">**MCIWndGetPalette**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpalette)
</dt> </dl>

 

 





