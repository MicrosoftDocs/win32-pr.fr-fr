---
title: Message MCIWNDM_GETINACTIVETIMER (VFW. h)
description: Le \_ message MCIWNDM GETINACTIVETIMER récupère la période de mise à jour utilisée lorsque la fenêtre MCIWnd est la fenêtre inactive. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro MCIWndGetInactiveTimer.
ms.assetid: 84e00d2f-2cf8-4b6b-a8cb-7eb320754783
keywords:
- Message MCIWNDM_GETINACTIVETIMER Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_GETINACTIVETIMER
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a270aeffdee59b7749aa87a0e711204960d74d7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512363"
---
# <a name="mciwndm_getinactivetimer-message"></a><span data-ttu-id="ff74e-105">\_Message MCIWNDM GETINACTIVETIMER</span><span class="sxs-lookup"><span data-stu-id="ff74e-105">MCIWNDM\_GETINACTIVETIMER message</span></span>

<span data-ttu-id="ff74e-106">Le message **MCIWNDM \_ GETINACTIVETIMER** récupère la période de mise à jour utilisée lorsque la fenêtre MCIWnd est la fenêtre inactive.</span><span class="sxs-lookup"><span data-stu-id="ff74e-106">The **MCIWNDM\_GETINACTIVETIMER** message retrieves the update period used when the MCIWnd window is the inactive window.</span></span> <span data-ttu-id="ff74e-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**MCIWndGetInactiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetinactivetimer) .</span><span class="sxs-lookup"><span data-stu-id="ff74e-107">You can send this message explicitly or by using the [**MCIWndGetInactiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetinactivetimer) macro.</span></span>


```C++
MCIWNDM_GETINACTIVETIMER 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="ff74e-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ff74e-108">Return Value</span></span>

<span data-ttu-id="ff74e-109">Retourne la période de mise à jour, en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="ff74e-109">Returns the update period, in milliseconds.</span></span> <span data-ttu-id="ff74e-110">La valeur par défaut est 2000 millisecondes.</span><span class="sxs-lookup"><span data-stu-id="ff74e-110">The default value is 2000 milliseconds.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff74e-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ff74e-111">Requirements</span></span>



| <span data-ttu-id="ff74e-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ff74e-112">Requirement</span></span> | <span data-ttu-id="ff74e-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="ff74e-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ff74e-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ff74e-114">Minimum supported client</span></span><br/> | <span data-ttu-id="ff74e-115">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ff74e-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="ff74e-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ff74e-116">Minimum supported server</span></span><br/> | <span data-ttu-id="ff74e-117">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ff74e-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="ff74e-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="ff74e-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="ff74e-119"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="ff74e-119"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff74e-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ff74e-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff74e-121">**MCIWndGetInactiveTimer**</span><span class="sxs-lookup"><span data-stu-id="ff74e-121">**MCIWndGetInactiveTimer**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetinactivetimer)
</dt> </dl>

 

 





