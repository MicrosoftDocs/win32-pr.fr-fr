---
title: Message MCIWNDM_GETACTIVETIMER (VFW. h)
description: Le \_ message MCIWNDM GETACTIVETIMER récupère la période de mise à jour utilisée lorsque la fenêtre MCIWnd est la fenêtre active. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro MCIWndGetActiveTimer.
ms.assetid: f9e6f9ed-75fd-4e45-ad92-79a82d8d572c
keywords:
- Message MCIWNDM_GETACTIVETIMER Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_GETACTIVETIMER
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cb86fc2940c8bd5d82c004754b81e5389ada892
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106531"
---
# <a name="mciwndm_getactivetimer-message"></a><span data-ttu-id="806f7-105">\_Message MCIWNDM GETACTIVETIMER</span><span class="sxs-lookup"><span data-stu-id="806f7-105">MCIWNDM\_GETACTIVETIMER message</span></span>

<span data-ttu-id="806f7-106">Le message **MCIWNDM \_ GETACTIVETIMER** récupère la période de mise à jour utilisée lorsque la fenêtre MCIWnd est la fenêtre active.</span><span class="sxs-lookup"><span data-stu-id="806f7-106">The **MCIWNDM\_GETACTIVETIMER** message retrieves the update period used when the MCIWnd window is the active window.</span></span> <span data-ttu-id="806f7-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**MCIWndGetActiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetactivetimer) .</span><span class="sxs-lookup"><span data-stu-id="806f7-107">You can send this message explicitly or by using the [**MCIWndGetActiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetactivetimer) macro.</span></span>


```C++
MCIWNDM_GETACTIVETIMER 
wParam = 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="806f7-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="806f7-108">Return Value</span></span>

<span data-ttu-id="806f7-109">Retourne la période de mise à jour en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="806f7-109">Returns the update period in milliseconds.</span></span> <span data-ttu-id="806f7-110">La valeur par défaut est 500 millisecondes.</span><span class="sxs-lookup"><span data-stu-id="806f7-110">The default is 500 milliseconds.</span></span>

## <a name="requirements"></a><span data-ttu-id="806f7-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="806f7-111">Requirements</span></span>



| <span data-ttu-id="806f7-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="806f7-112">Requirement</span></span> | <span data-ttu-id="806f7-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="806f7-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="806f7-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="806f7-114">Minimum supported client</span></span><br/> | <span data-ttu-id="806f7-115">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="806f7-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="806f7-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="806f7-116">Minimum supported server</span></span><br/> | <span data-ttu-id="806f7-117">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="806f7-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="806f7-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="806f7-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="806f7-119"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="806f7-119"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="806f7-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="806f7-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="806f7-121">**MCIWndGetActiveTimer**</span><span class="sxs-lookup"><span data-stu-id="806f7-121">**MCIWndGetActiveTimer**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetactivetimer)
</dt> </dl>

 

 





