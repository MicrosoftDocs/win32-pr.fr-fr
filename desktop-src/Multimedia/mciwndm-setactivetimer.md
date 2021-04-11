---
title: Message MCIWNDM_SETACTIVETIMER (VFW. h)
description: Le \_ message MCIWNDM SETACTIVETIMER définit la période de mise à jour utilisée par MCIWnd pour mettre à jour le TrackBar dans la fenêtre MCIWnd, mettre à jour les informations de position affichées dans la barre de titre de la fenêtre et envoyer des messages de notification à la fenêtre parente lorsque la fenêtre MCIWnd est active. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro MCIWndSetActiveTimer.
ms.assetid: a30c0091-d9bb-44a3-a7b0-d1be30adcd9c
keywords:
- Message MCIWNDM_SETACTIVETIMER Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_SETACTIVETIMER
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1924a991f0627009a8e622c8f8be086b2e045635
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104713"
---
# <a name="mciwndm_setactivetimer-message"></a><span data-ttu-id="80634-105">\_Message MCIWNDM SETACTIVETIMER</span><span class="sxs-lookup"><span data-stu-id="80634-105">MCIWNDM\_SETACTIVETIMER message</span></span>

<span data-ttu-id="80634-106">Le message **MCIWNDM \_ SETACTIVETIMER** définit la période de mise à jour utilisée par MCIWnd pour mettre à jour le TrackBar dans la fenêtre MCIWnd, mettre à jour les informations de position affichées dans la barre de titre de la fenêtre et envoyer des messages de notification à la fenêtre parente lorsque la fenêtre MCIWnd est active.</span><span class="sxs-lookup"><span data-stu-id="80634-106">The **MCIWNDM\_SETACTIVETIMER** message sets the update period used by MCIWnd to update the trackbar in the MCIWnd window, update position information displayed in the window title bar, and send notification messages to the parent window when the MCIWnd window is active.</span></span> <span data-ttu-id="80634-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**MCIWndSetActiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetactivetimer) .</span><span class="sxs-lookup"><span data-stu-id="80634-107">You can send this message explicitly or by using the [**MCIWndSetActiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetactivetimer) macro.</span></span>


```C++
MCIWNDM_SETACTIVETIMER 
wParam = (WPARAM) (UINT) active; 
lParam = 0L; 
```



## <a name="parameters"></a><span data-ttu-id="80634-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="80634-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80634-109"><span id="active"></span><span id="ACTIVE"></span>*proactive*</span><span class="sxs-lookup"><span data-stu-id="80634-109"><span id="active"></span><span id="ACTIVE"></span>*active*</span></span>
</dt> <dd>

<span data-ttu-id="80634-110">Période de mise à jour, en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="80634-110">Update period, in milliseconds.</span></span> <span data-ttu-id="80634-111">La valeur par défaut est 500 millisecondes.</span><span class="sxs-lookup"><span data-stu-id="80634-111">The default is 500 milliseconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80634-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="80634-112">Return Value</span></span>

<span data-ttu-id="80634-113">Ce message ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="80634-113">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="80634-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="80634-114">Requirements</span></span>



| <span data-ttu-id="80634-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="80634-115">Requirement</span></span> | <span data-ttu-id="80634-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="80634-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="80634-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="80634-117">Minimum supported client</span></span><br/> | <span data-ttu-id="80634-118">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="80634-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="80634-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="80634-119">Minimum supported server</span></span><br/> | <span data-ttu-id="80634-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="80634-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="80634-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="80634-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="80634-122"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="80634-122"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80634-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="80634-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80634-124">**MCIWndSetActiveTimer**</span><span class="sxs-lookup"><span data-stu-id="80634-124">**MCIWndSetActiveTimer**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndsetactivetimer)
</dt> </dl>

 

 





