---
title: Message MCIWNDM_SETPALETTE (VFW. h)
description: Le \_ message MCIWNDM SETPALETTE envoie un descripteur de palette au périphérique MCI associé à la fenêtre MCIWnd. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro MCIWndSetPalette.
ms.assetid: d2399cb7-d83c-465c-b02f-e6a016c28ae3
keywords:
- Message MCIWNDM_SETPALETTE Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_SETPALETTE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba7e354082de4fc15f4179555a8b635b9426af90
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466050"
---
# <a name="mciwndm_setpalette-message"></a><span data-ttu-id="aa976-105">\_Message MCIWNDM SETPALETTE</span><span class="sxs-lookup"><span data-stu-id="aa976-105">MCIWNDM\_SETPALETTE message</span></span>

<span data-ttu-id="aa976-106">Le message **MCIWNDM \_ SETPALETTE** envoie un descripteur de palette au périphérique MCI associé à la fenêtre MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="aa976-106">The **MCIWNDM\_SETPALETTE** message sends a palette handle to the MCI device associated with the MCIWnd window.</span></span> <span data-ttu-id="aa976-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**MCIWndSetPalette**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetpalette) .</span><span class="sxs-lookup"><span data-stu-id="aa976-107">You can send this message explicitly or by using the [**MCIWndSetPalette**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetpalette) macro.</span></span>


```C++
MCIWNDM_SETPALETTE 
wParam = (WPARAM) (HPALETTE) hpal; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="aa976-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="aa976-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa976-109"><span id="hpal"></span><span id="HPAL"></span>*hpal*</span><span class="sxs-lookup"><span data-stu-id="aa976-109"><span id="hpal"></span><span id="HPAL"></span>*hpal*</span></span>
</dt> <dd>

<span data-ttu-id="aa976-110">Handle de palette.</span><span class="sxs-lookup"><span data-stu-id="aa976-110">Palette handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa976-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="aa976-111">Return Value</span></span>

<span data-ttu-id="aa976-112">Retourne zéro en cas de réussite ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="aa976-112">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa976-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="aa976-113">Requirements</span></span>



| <span data-ttu-id="aa976-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="aa976-114">Requirement</span></span> | <span data-ttu-id="aa976-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="aa976-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="aa976-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aa976-116">Minimum supported client</span></span><br/> | <span data-ttu-id="aa976-117">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="aa976-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="aa976-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aa976-118">Minimum supported server</span></span><br/> | <span data-ttu-id="aa976-119">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="aa976-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="aa976-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="aa976-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="aa976-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="aa976-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa976-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aa976-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa976-123">**MCIWndSetPalette**</span><span class="sxs-lookup"><span data-stu-id="aa976-123">**MCIWndSetPalette**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndsetpalette)
</dt> </dl>

 

 





