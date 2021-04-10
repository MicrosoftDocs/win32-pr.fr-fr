---
title: Message MCIWNDM_CAN_WINDOW (VFW. h)
description: Le \_ message de fenêtre MCIWNDM peut \_ déterminer si un périphérique MCI prend en charge les commandes MCI orientées fenêtre. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro MCIWndCanWindow.
ms.assetid: bf89c096-1272-441e-9334-2b4215dbc979
keywords:
- Message MCIWNDM_CAN_WINDOW Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_CAN_WINDOW
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d638b61093483b6e834b57af1d5c892d77d0f1d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942006"
---
# <a name="mciwndm_can_window-message"></a><span data-ttu-id="cbdf8-105">MCIWNDM \_ peut être un \_ message de fenêtre</span><span class="sxs-lookup"><span data-stu-id="cbdf8-105">MCIWNDM\_CAN\_WINDOW message</span></span>

<span data-ttu-id="cbdf8-106">Le message de **\_ \_ fenêtre MCIWNDM peut** déterminer si un périphérique MCI prend en charge les commandes MCI orientées fenêtre.</span><span class="sxs-lookup"><span data-stu-id="cbdf8-106">The **MCIWNDM\_CAN\_WINDOW** message determines if an MCI device supports window-oriented MCI commands.</span></span> <span data-ttu-id="cbdf8-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**MCIWndCanWindow**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanwindow) .</span><span class="sxs-lookup"><span data-stu-id="cbdf8-107">You can send this message explicitly or by using the [**MCIWndCanWindow**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanwindow) macro.</span></span>


```C++
MCIWNDM_CAN_WINDOW 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="cbdf8-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="cbdf8-108">Return Value</span></span>

<span data-ttu-id="cbdf8-109">Retourne la **valeur true** si l’appareil prend en charge les commandes MCI orientées fenêtre ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="cbdf8-109">Returns **TRUE** if the device supports window-oriented MCI commands or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="cbdf8-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cbdf8-110">Requirements</span></span>



| <span data-ttu-id="cbdf8-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cbdf8-111">Requirement</span></span> | <span data-ttu-id="cbdf8-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="cbdf8-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="cbdf8-113">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cbdf8-113">Minimum supported client</span></span><br/> | <span data-ttu-id="cbdf8-114">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cbdf8-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="cbdf8-115">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cbdf8-115">Minimum supported server</span></span><br/> | <span data-ttu-id="cbdf8-116">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cbdf8-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="cbdf8-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="cbdf8-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="cbdf8-118"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="cbdf8-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cbdf8-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cbdf8-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbdf8-120">**MCIWndCanWindow**</span><span class="sxs-lookup"><span data-stu-id="cbdf8-120">**MCIWndCanWindow**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndcanwindow)
</dt> </dl>

 

 





