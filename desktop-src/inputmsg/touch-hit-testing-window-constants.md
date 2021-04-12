---
title: Constantes de la fenêtre test d’atteinte tactile
description: Indique comment les messages pour le test d’atteinte tactile sont traités par les fenêtres qui sont inscrites via la fonction RegisterTouchHitTestingWindow.
ms.assetid: CC6CCD0B-882F-4DA7-B886-D4BD18D6060C
topic_type:
- apiref
api_name:
- TOUCH_HIT_TESTING_DEFAULT
- TOUCH_HIT_TESTING_CLIENT
- TOUCH_HIT_TESTING_NONE
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 46d577e03eaf918e4f2ea40aae30a2ab5112b630
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385032"
---
# <a name="touch-hit-testing-window-constants"></a><span data-ttu-id="b8b2b-103">Constantes de la fenêtre test d’atteinte tactile</span><span class="sxs-lookup"><span data-stu-id="b8b2b-103">Touch Hit Testing Window Constants</span></span>

<span data-ttu-id="b8b2b-104">Indique comment les messages pour le test d’atteinte tactile sont traités par les fenêtres qui sont inscrites via la fonction [**RegisterTouchHitTestingWindow**](/windows/win32/api/winuser/nf-winuser-registertouchhittestingwindow) .</span><span class="sxs-lookup"><span data-stu-id="b8b2b-104">Indicates how messages for touch hit testing are processed by windows that are registered through the [**RegisterTouchHitTestingWindow**](/windows/win32/api/winuser/nf-winuser-registertouchhittestingwindow) function.</span></span>



| <span data-ttu-id="b8b2b-105">Constante/valeur</span><span class="sxs-lookup"><span data-stu-id="b8b2b-105">Constant/value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="b8b2b-106">Description</span><span class="sxs-lookup"><span data-stu-id="b8b2b-106">Description</span></span>                                                                                                                            |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TOUCH_HIT_TESTING_DEFAULT"></span><span id="touch_hit_testing_default"></span><dl> <span data-ttu-id="b8b2b-107"><dt>**TOUCH_HIT_TESTING_DEFAULT**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="b8b2b-107"><dt>**TOUCH_HIT_TESTING_DEFAULT**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="b8b2b-108">[**WM_TOUCHHITTESTING**](wm-touchhittesting.md) messages ne sont pas envoyés à la fenêtre cible, mais sont envoyés aux fenêtres enfants.</span><span class="sxs-lookup"><span data-stu-id="b8b2b-108">[**WM_TOUCHHITTESTING**](wm-touchhittesting.md) messages are not sent to the target window but are sent to child windows.</span></span><br/> |
| <span id="TOUCH_HIT_TESTING_CLIENT"></span><span id="touch_hit_testing_client"></span><dl> <span data-ttu-id="b8b2b-109"><dt>**TOUCH_HIT_TESTING_CLIENT**</dt> <dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="b8b2b-109"><dt>**TOUCH_HIT_TESTING_CLIENT**</dt> <dt>1 (0x1)</dt></span></span> </dl>    | <span data-ttu-id="b8b2b-110">[**WM_TOUCHHITTESTING**](wm-touchhittesting.md) messages sont envoyés à la fenêtre cible.</span><span class="sxs-lookup"><span data-stu-id="b8b2b-110">[**WM_TOUCHHITTESTING**](wm-touchhittesting.md) messages are sent to the target window.</span></span><br/>                                   |
| <span id="TOUCH_HIT_TESTING_NONE"></span><span id="touch_hit_testing_none"></span><dl> <span data-ttu-id="b8b2b-111"><dt>**TOUCH_HIT_TESTING_NONE**</dt> <dt>2 (0X2)</dt></span><span class="sxs-lookup"><span data-stu-id="b8b2b-111"><dt>**TOUCH_HIT_TESTING_NONE**</dt> <dt>2 (0x2)</dt></span></span> </dl>          | <span data-ttu-id="b8b2b-112">[**WM_TOUCHHITTESTING**](wm-touchhittesting.md) messages ne sont pas envoyés à la fenêtre cible ou aux fenêtres enfants.</span><span class="sxs-lookup"><span data-stu-id="b8b2b-112">[**WM_TOUCHHITTESTING**](wm-touchhittesting.md) messages are not sent to the target window or child windows.</span></span><br/>              |



## <a name="requirements"></a><span data-ttu-id="b8b2b-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b8b2b-113">Requirements</span></span>



| <span data-ttu-id="b8b2b-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b8b2b-114">Requirement</span></span> | <span data-ttu-id="b8b2b-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="b8b2b-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b8b2b-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b8b2b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="b8b2b-117">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b8b2b-117">Windows 8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="b8b2b-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b8b2b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="b8b2b-119">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b8b2b-119">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="b8b2b-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="b8b2b-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8b2b-121"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="b8b2b-121"><dt>Winuser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8b2b-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b8b2b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8b2b-123">Constantes</span><span class="sxs-lookup"><span data-stu-id="b8b2b-123">Constants</span></span>](constants.md)
</dt> <dt>

[<span data-ttu-id="b8b2b-124">**POINTER_INFO**</span><span class="sxs-lookup"><span data-stu-id="b8b2b-124">**POINTER_INFO**</span></span>](/previous-versions/windows/desktop/api)
</dt> </dl>

 

