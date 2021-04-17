---
title: Message MCIWNDM_GETSPEED (VFW. h)
description: Le \_ message MCIWNDM GETSPEED récupère la vitesse de lecture d’un périphérique MCI. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro MCIWndGetSpeed.
ms.assetid: d10a8f88-e85e-449b-8655-bb0832031d59
keywords:
- Message MCIWNDM_GETSPEED Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_GETSPEED
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c84a8ebb3e97d4543f68f3a237add8eed7706ae2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466782"
---
# <a name="mciwndm_getspeed-message"></a><span data-ttu-id="48611-105">\_Message MCIWNDM GETSPEED</span><span class="sxs-lookup"><span data-stu-id="48611-105">MCIWNDM\_GETSPEED message</span></span>

<span data-ttu-id="48611-106">Le message **MCIWNDM \_ GETSPEED** récupère la vitesse de lecture d’un périphérique MCI.</span><span class="sxs-lookup"><span data-stu-id="48611-106">The **MCIWNDM\_GETSPEED** message retrieves the playback speed of an MCI device.</span></span> <span data-ttu-id="48611-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**MCIWndGetSpeed**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetspeed) .</span><span class="sxs-lookup"><span data-stu-id="48611-107">You can send this message explicitly or by using the [**MCIWndGetSpeed**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetspeed) macro.</span></span>


```C++
MCIWNDM_GETSPEED 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="48611-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="48611-108">Return Value</span></span>

<span data-ttu-id="48611-109">Retourne la vitesse de lecture en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="48611-109">Returns the playback speed if successful.</span></span> <span data-ttu-id="48611-110">La valeur de la vitesse normale est 1000.</span><span class="sxs-lookup"><span data-stu-id="48611-110">The value for normal speed is 1000.</span></span> <span data-ttu-id="48611-111">Des valeurs plus élevées indiquent des vitesses supérieures, les valeurs inférieures indiquent des vitesses plus basses.</span><span class="sxs-lookup"><span data-stu-id="48611-111">Larger values indicate faster speeds, smaller values indicate slower speeds.</span></span>

## <a name="requirements"></a><span data-ttu-id="48611-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="48611-112">Requirements</span></span>



| <span data-ttu-id="48611-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="48611-113">Requirement</span></span> | <span data-ttu-id="48611-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="48611-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="48611-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="48611-115">Minimum supported client</span></span><br/> | <span data-ttu-id="48611-116">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="48611-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="48611-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="48611-117">Minimum supported server</span></span><br/> | <span data-ttu-id="48611-118">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="48611-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="48611-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="48611-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="48611-120"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="48611-120"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48611-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="48611-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48611-122">**MCIWndGetSpeed**</span><span class="sxs-lookup"><span data-stu-id="48611-122">**MCIWndGetSpeed**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetspeed)
</dt> </dl>

 

 





