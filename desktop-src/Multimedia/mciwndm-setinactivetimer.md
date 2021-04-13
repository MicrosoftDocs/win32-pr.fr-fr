---
title: Message MCIWNDM_SETINACTIVETIMER (VFW. h)
description: Le \_ message MCIWNDM SETINACTIVETIMER définit la période de mise à jour utilisée par MCIWnd pour mettre à jour le TrackBar dans la fenêtre MCIWnd, mettre à jour les informations de position affichées dans la barre de titre de la fenêtre et envoyer des messages de notification à la fenêtre parente lorsque la fenêtre MCIWnd est inactive. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro MCIWndSetInactiveTimer.
ms.assetid: 8900c372-0493-4a63-a027-ef6ecf8f8254
keywords:
- Message MCIWNDM_SETINACTIVETIMER Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_SETINACTIVETIMER
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba4504d84b254dfb67616568f5f97bba8e3bc2e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508890"
---
# <a name="mciwndm_setinactivetimer-message"></a><span data-ttu-id="fa825-105">\_Message MCIWNDM SETINACTIVETIMER</span><span class="sxs-lookup"><span data-stu-id="fa825-105">MCIWNDM\_SETINACTIVETIMER message</span></span>

<span data-ttu-id="fa825-106">Le message **MCIWNDM \_ SETINACTIVETIMER** définit la période de mise à jour utilisée par MCIWnd pour mettre à jour le TrackBar dans la fenêtre MCIWnd, mettre à jour les informations de position affichées dans la barre de titre de la fenêtre et envoyer des messages de notification à la fenêtre parente lorsque la fenêtre MCIWnd est inactive.</span><span class="sxs-lookup"><span data-stu-id="fa825-106">The **MCIWNDM\_SETINACTIVETIMER** message sets the update period used by MCIWnd to update the trackbar in the MCIWnd window, update position information displayed in the window title bar, and send notification messages to the parent window when the MCIWnd window is inactive.</span></span> <span data-ttu-id="fa825-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**MCIWndSetInactiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetinactivetimer) .</span><span class="sxs-lookup"><span data-stu-id="fa825-107">You can send this message explicitly or by using the [**MCIWndSetInactiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetinactivetimer) macro.</span></span>


```C++
MCIWNDM_SETINACTIVETIMER 
wParam = (WPARAM) (UINT) inactive; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="fa825-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fa825-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa825-109"><span id="inactive"></span><span id="INACTIVE"></span>*inactive*</span><span class="sxs-lookup"><span data-stu-id="fa825-109"><span id="inactive"></span><span id="INACTIVE"></span>*inactive*</span></span>
</dt> <dd>

<span data-ttu-id="fa825-110">Période de mise à jour, en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="fa825-110">Update period, in milliseconds.</span></span> <span data-ttu-id="fa825-111">La valeur par défaut est 2000 millisecondes.</span><span class="sxs-lookup"><span data-stu-id="fa825-111">The default is 2000 milliseconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa825-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="fa825-112">Return Value</span></span>

<span data-ttu-id="fa825-113">Ce message ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="fa825-113">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa825-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fa825-114">Requirements</span></span>



| <span data-ttu-id="fa825-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fa825-115">Requirement</span></span> | <span data-ttu-id="fa825-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="fa825-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="fa825-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fa825-117">Minimum supported client</span></span><br/> | <span data-ttu-id="fa825-118">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fa825-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="fa825-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fa825-119">Minimum supported server</span></span><br/> | <span data-ttu-id="fa825-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fa825-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="fa825-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="fa825-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa825-122"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="fa825-122"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa825-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fa825-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa825-124">**MCIWndSetInactiveTimer**</span><span class="sxs-lookup"><span data-stu-id="fa825-124">**MCIWndSetInactiveTimer**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndsetinactivetimer)
</dt> </dl>

 

 





