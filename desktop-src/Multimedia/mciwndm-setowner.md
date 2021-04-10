---
title: Message MCIWNDM_SETOWNER (VFW. h)
description: Le \_ message MCIWNDM de la conlocalité définit la fenêtre de réception des messages de notification associés à la fenêtre MCIWnd. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro MCIWndSetOwner.
ms.assetid: c2d0f9d5-bf60-4036-a613-65ba1ed83110
keywords:
- Message MCIWNDM_SETOWNER Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_SETOWNER
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3989632e83a65cda5e805bd91da3f502ca387d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104719"
---
# <a name="mciwndm_setowner-message"></a><span data-ttu-id="08847-105">\_Message MCIWNDM</span><span class="sxs-lookup"><span data-stu-id="08847-105">MCIWNDM\_SETOWNER message</span></span>

<span data-ttu-id="08847-106">Le message MCIWNDM de la **\_ conlocalité** définit la fenêtre de réception des messages de notification associés à la fenêtre MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="08847-106">The **MCIWNDM\_SETOWNER** message sets the window to receive notification messages associated with the MCIWnd window.</span></span> <span data-ttu-id="08847-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**MCIWndSetOwner**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetowner) .</span><span class="sxs-lookup"><span data-stu-id="08847-107">You can send this message explicitly or by using the [**MCIWndSetOwner**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetowner) macro.</span></span>


```C++
MCIWNDM_SETOWNER 
wParam = (WPARAM) hwndP; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="08847-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="08847-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08847-109"><span id="hwndP"></span><span id="hwndp"></span><span id="HWNDP"></span>*hwndP*</span><span class="sxs-lookup"><span data-stu-id="08847-109"><span id="hwndP"></span><span id="hwndp"></span><span id="HWNDP"></span>*hwndP*</span></span>
</dt> <dd>

<span data-ttu-id="08847-110">Handle de la fenêtre pour recevoir les messages de notification.</span><span class="sxs-lookup"><span data-stu-id="08847-110">Handle to the window to receive the notification messages.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08847-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="08847-111">Return Value</span></span>

<span data-ttu-id="08847-112">Retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="08847-112">Returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="08847-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="08847-113">Requirements</span></span>



| <span data-ttu-id="08847-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="08847-114">Requirement</span></span> | <span data-ttu-id="08847-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="08847-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="08847-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="08847-116">Minimum supported client</span></span><br/> | <span data-ttu-id="08847-117">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="08847-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="08847-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="08847-118">Minimum supported server</span></span><br/> | <span data-ttu-id="08847-119">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="08847-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="08847-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="08847-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="08847-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="08847-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08847-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="08847-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08847-123">**MCIWndSetOwner**</span><span class="sxs-lookup"><span data-stu-id="08847-123">**MCIWndSetOwner**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndsetowner)
</dt> </dl>

 

 





