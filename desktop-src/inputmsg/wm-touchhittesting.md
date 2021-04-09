---
title: Message WM_TOUCHHITTESTING
description: Envoyé à une fenêtre d’une commande tactile pour déterminer la cible tactile la plus probable.
ms.assetid: 741F9D67-A914-46CF-91A3-EF40447E7438
keywords:
- WM_TOUCHHITTESTING les messages d’entrée du message et les notifications
topic_type:
- apiref
api_name:
- WM_TOUCHHITTESTING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 83b6e564d692fb0223ec8871b99cefcb9fddf40b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104557"
---
# <a name="wm_touchhittesting-message"></a><span data-ttu-id="de1da-104">Message WM_TOUCHHITTESTING</span><span class="sxs-lookup"><span data-stu-id="de1da-104">WM_TOUCHHITTESTING message</span></span>

<span data-ttu-id="de1da-105">Envoyé à une fenêtre d’une commande tactile pour déterminer la cible tactile la plus probable.</span><span class="sxs-lookup"><span data-stu-id="de1da-105">Sent to a window on a touch down in order to determine the most probable touch target.</span></span>

> <span data-ttu-id="de1da-106">\[! Précieuse\]</span><span class="sxs-lookup"><span data-stu-id="de1da-106">\[!Important\]</span></span>  
> <span data-ttu-id="de1da-107">Les applications de bureau doivent prendre en charge DPI.</span><span class="sxs-lookup"><span data-stu-id="de1da-107">Desktop apps should be DPI aware.</span></span> <span data-ttu-id="de1da-108">Si votre application n’a pas de prise en charge DPI, les coordonnées d’écran contenues dans les messages de pointeur et les structures associées peuvent apparaître inexactes en raison de la virtualisation DPI.</span><span class="sxs-lookup"><span data-stu-id="de1da-108">If your app is not DPI aware, screen coordinates contained in pointer messages and related structures might appear inaccurate due to DPI virtualization.</span></span> <span data-ttu-id="de1da-109">La virtualisation PPP offre une prise en charge de la mise à l’échelle automatique aux applications qui ne prennent pas en charge la fonction PPP et est active par défaut (les utilisateurs peuvent la désactiver).</span><span class="sxs-lookup"><span data-stu-id="de1da-109">DPI virtualization provides automatic scaling support to applications that are not DPI aware and is active by default (users can turn it off).</span></span> <span data-ttu-id="de1da-110">Pour plus d’informations, consultez [écriture d’applications Win32 à haute résolution](/previous-versions//dd464660(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="de1da-110">For more information, see [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).</span></span>

 


```C++
#define WM_TOUCHHITTESTING       0x024D
```



## <a name="parameters"></a><span data-ttu-id="de1da-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="de1da-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de1da-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="de1da-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="de1da-113">Inutilisé.</span><span class="sxs-lookup"><span data-stu-id="de1da-113">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="de1da-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="de1da-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="de1da-115">Pointeur vers la structure [**TOUCH_HIT_TESTING_INPUT**](/windows/win32/api/winuser/ns-winuser-touch_hit_testing_input) qui contient les données tactiles de la zone de contact.</span><span class="sxs-lookup"><span data-stu-id="de1da-115">Pointer to the [**TOUCH_HIT_TESTING_INPUT**](/windows/win32/api/winuser/ns-winuser-touch_hit_testing_input) structure that holds the touch contact area data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de1da-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="de1da-116">Return value</span></span>

<span data-ttu-id="de1da-117">Si un ou plusieurs éléments se trouvent dans la zone de contact tactile, une application doit retourner le résultat de [**PackTouchHitTestingProximityEvaluation**](/windows/win32/api/winuser/nf-winuser-packtouchhittestingproximityevaluation).</span><span class="sxs-lookup"><span data-stu-id="de1da-117">If one or more elements are within the touch contact area, an application should return the result of [**PackTouchHitTestingProximityEvaluation**](/windows/win32/api/winuser/nf-winuser-packtouchhittestingproximityevaluation).</span></span>

<span data-ttu-id="de1da-118">Si aucun élément ne se trouve dans la zone tactile contact, une application doit définir la valeur de **score** dans [**TOUCH_HIT_TESTING_PROXIMITY_EVALUATION**](/windows/win32/api/winuser/ns-winuser-touch_hit_testing_proximity_evaluation) sur [**TOUCH_HIT_TESTING_PROXIMITY_FARTHEST**](/previous-versions/windows/desktop/input_touchhittest/hit-testing-scores) et appeler [**PACKTOUCHHITTESTINGPROXIMITYEVALUATION**](/windows/win32/api/winuser/nf-winuser-packtouchhittestingproximityevaluation) pour obtenir la valeur de retour LRESULT.</span><span class="sxs-lookup"><span data-stu-id="de1da-118">If no elements are within the touch contact area, an application should set the value of **score** in [**TOUCH_HIT_TESTING_PROXIMITY_EVALUATION**](/windows/win32/api/winuser/ns-winuser-touch_hit_testing_proximity_evaluation) to [**TOUCH_HIT_TESTING_PROXIMITY_FARTHEST**](/previous-versions/windows/desktop/input_touchhittest/hit-testing-scores) and call [**PackTouchHitTestingProximityEvaluation**](/windows/win32/api/winuser/nf-winuser-packtouchhittestingproximityevaluation) to get the LRESULT return value.</span></span>

<span data-ttu-id="de1da-119">Si l’application ne traite pas ce message, elle doit appeler [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="de1da-119">If the application does not process this message, it must call [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span>

## <a name="remarks"></a><span data-ttu-id="de1da-120">Notes</span><span class="sxs-lookup"><span data-stu-id="de1da-120">Remarks</span></span>

<span data-ttu-id="de1da-121">Ce message est envoyé aux fenêtres qui s’inscrivent via la fonction [**RegisterTouchHitTestingWindow**](/windows/win32/api/winuser/nf-winuser-registertouchhittestingwindow) .</span><span class="sxs-lookup"><span data-stu-id="de1da-121">This message is sent to windows that register through the [**RegisterTouchHitTestingWindow**](/windows/win32/api/winuser/nf-winuser-registertouchhittestingwindow) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="de1da-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="de1da-122">Requirements</span></span>



| <span data-ttu-id="de1da-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="de1da-123">Requirement</span></span> | <span data-ttu-id="de1da-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="de1da-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de1da-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="de1da-125">Minimum supported client</span></span><br/> | <span data-ttu-id="de1da-126">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="de1da-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="de1da-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="de1da-127">Minimum supported server</span></span><br/> | <span data-ttu-id="de1da-128">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="de1da-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="de1da-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="de1da-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="de1da-130"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="de1da-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de1da-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="de1da-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de1da-132">Messages</span><span class="sxs-lookup"><span data-stu-id="de1da-132">Messages</span></span>](messages.md)
</dt> <dt>

[<span data-ttu-id="de1da-133">**Scores de test d’atteinte tactile**</span><span class="sxs-lookup"><span data-stu-id="de1da-133">**Touch Hit Testing Scores**</span></span>](/previous-versions/windows/desktop/input_touchhittest/hit-testing-scores)
</dt> </dl>

 

