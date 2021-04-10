---
title: Message MCIWNDM_SETSPEED (VFW. h)
description: Le \_ message MCIWNDM SETSPEED définit la vitesse de lecture d’un périphérique MCI. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro MCIWndSetSpeed.
ms.assetid: 7658dd25-dc68-4bd1-b995-df06b509be16
keywords:
- Message MCIWNDM_SETSPEED Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_SETSPEED
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 282bb3a2e135b674605be55aaccaa455d30edbcc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942433"
---
# <a name="mciwndm_setspeed-message"></a><span data-ttu-id="5a3f2-105">\_Message MCIWNDM SETSPEED</span><span class="sxs-lookup"><span data-stu-id="5a3f2-105">MCIWNDM\_SETSPEED message</span></span>

<span data-ttu-id="5a3f2-106">Le message **MCIWNDM \_ SETSPEED** définit la vitesse de lecture d’un périphérique MCI.</span><span class="sxs-lookup"><span data-stu-id="5a3f2-106">The **MCIWNDM\_SETSPEED** message sets the playback speed of an MCI device.</span></span> <span data-ttu-id="5a3f2-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**MCIWndSetSpeed**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetspeed) .</span><span class="sxs-lookup"><span data-stu-id="5a3f2-107">You can send this message explicitly or by using the [**MCIWndSetSpeed**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetspeed) macro.</span></span>


```C++
MCIWNDM_SETSPEED 
wParam = 0; 
lParam = (LPARAM) (UINT) iSpeed; 
```



## <a name="parameters"></a><span data-ttu-id="5a3f2-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5a3f2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a3f2-109"><span id="iSpeed"></span><span id="ispeed"></span><span id="ISPEED"></span>*iSpeed*</span><span class="sxs-lookup"><span data-stu-id="5a3f2-109"><span id="iSpeed"></span><span id="ispeed"></span><span id="ISPEED"></span>*iSpeed*</span></span>
</dt> <dd>

<span data-ttu-id="5a3f2-110">Vitesse de lecture.</span><span class="sxs-lookup"><span data-stu-id="5a3f2-110">Playback speed.</span></span> <span data-ttu-id="5a3f2-111">Spécifiez 1000 pour la vitesse normale, des valeurs plus élevées pour des vitesses plus rapides et des valeurs plus petites pour des vitesses plus lentes.</span><span class="sxs-lookup"><span data-stu-id="5a3f2-111">Specify 1000 for normal speed, larger values for faster speeds, and smaller values for slower speeds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a3f2-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="5a3f2-112">Return Value</span></span>

<span data-ttu-id="5a3f2-113">Retourne zéro en cas de réussite ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="5a3f2-113">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a3f2-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5a3f2-114">Requirements</span></span>



| <span data-ttu-id="5a3f2-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5a3f2-115">Requirement</span></span> | <span data-ttu-id="5a3f2-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="5a3f2-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="5a3f2-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5a3f2-117">Minimum supported client</span></span><br/> | <span data-ttu-id="5a3f2-118">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5a3f2-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="5a3f2-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5a3f2-119">Minimum supported server</span></span><br/> | <span data-ttu-id="5a3f2-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5a3f2-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="5a3f2-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="5a3f2-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="5a3f2-122"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a3f2-122"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a3f2-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5a3f2-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a3f2-124">**MCIWndSetSpeed**</span><span class="sxs-lookup"><span data-stu-id="5a3f2-124">**MCIWndSetSpeed**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndsetspeed)
</dt> </dl>

 

 





