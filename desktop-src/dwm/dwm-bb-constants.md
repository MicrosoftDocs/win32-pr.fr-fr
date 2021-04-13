---
title: Brouilleur de DWM derrière les constantes (dwmapi. h)
description: Indicateurs utilisés par la \_ structure DWM BLURBEHIND pour indiquer les membres qui contiennent des informations valides.
ms.assetid: d6dd552c-1f3b-4f16-8705-f5016ed55d9e
topic_type:
- apiref
api_name:
- DWM_BB_ENABLE
- DWM_BB_BLURREGION
- DWM_BB_TRANSITIONONMAXIMIZED
api_location:
- Dwmapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbe08e0315d4c4b906cdb897ac7ad5dd34d50fbf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508810"
---
# <a name="dwm-blur-behind-constants"></a><span data-ttu-id="2165e-103">Brouilleur de DWM derrière les constantes</span><span class="sxs-lookup"><span data-stu-id="2165e-103">DWM Blur Behind Constants</span></span>

<span data-ttu-id="2165e-104">Indicateurs utilisés par la structure [**DWM \_ BLURBEHIND**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_blurbehind) pour indiquer les membres qui contiennent des informations valides.</span><span class="sxs-lookup"><span data-stu-id="2165e-104">Flags used by the [**DWM\_BLURBEHIND**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_blurbehind) structure to indicate which of its members contain valid information.</span></span>

<dl> <dt>

<span data-ttu-id="2165e-105"><span id="DWM_BB_ENABLE"></span><span id="dwm_bb_enable"></span>**DWM \_ BB \_ activé**</span><span class="sxs-lookup"><span data-stu-id="2165e-105"><span id="DWM_BB_ENABLE"></span><span id="dwm_bb_enable"></span>**DWM\_BB\_ENABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2165e-106">0x00000001</span><span class="sxs-lookup"><span data-stu-id="2165e-106">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="2165e-107">Une valeur a été spécifiée pour le membre **fEnable** .</span><span class="sxs-lookup"><span data-stu-id="2165e-107">A value for the **fEnable** member has been specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2165e-108"><span id="DWM_BB_BLURREGION"></span><span id="dwm_bb_blurregion"></span>**DWM \_ BB \_ BLURREGION**</span><span class="sxs-lookup"><span data-stu-id="2165e-108"><span id="DWM_BB_BLURREGION"></span><span id="dwm_bb_blurregion"></span>**DWM\_BB\_BLURREGION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2165e-109">0x00000002</span><span class="sxs-lookup"><span data-stu-id="2165e-109">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="2165e-110">Une valeur a été spécifiée pour le membre **hRgnBlur** .</span><span class="sxs-lookup"><span data-stu-id="2165e-110">A value for the **hRgnBlur** member has been specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2165e-111"><span id="DWM_BB_TRANSITIONONMAXIMIZED"></span><span id="dwm_bb_transitiononmaximized"></span>**DWM \_ BB \_ TRANSITIONONMAXIMIZED**</span><span class="sxs-lookup"><span data-stu-id="2165e-111"><span id="DWM_BB_TRANSITIONONMAXIMIZED"></span><span id="dwm_bb_transitiononmaximized"></span>**DWM\_BB\_TRANSITIONONMAXIMIZED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2165e-112">0x00000004</span><span class="sxs-lookup"><span data-stu-id="2165e-112">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="2165e-113">Une valeur a été spécifiée pour le membre **fTransitionOnMaximized** .</span><span class="sxs-lookup"><span data-stu-id="2165e-113">A value for the **fTransitionOnMaximized** member has been specified.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2165e-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2165e-114">Requirements</span></span>



| <span data-ttu-id="2165e-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2165e-115">Requirement</span></span> | <span data-ttu-id="2165e-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="2165e-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="2165e-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2165e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="2165e-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2165e-118">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="2165e-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2165e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="2165e-120">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2165e-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="2165e-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="2165e-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="2165e-122"><dt>Dwmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="2165e-122"><dt>Dwmapi.h</dt></span></span> </dl> |



 

 





