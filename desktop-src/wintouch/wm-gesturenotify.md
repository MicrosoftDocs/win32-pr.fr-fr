---
title: Message WM_GESTURENOTIFY (winuser. h)
description: Vous donne la possibilité de définir la configuration du geste.
ms.assetid: 83c23928-86ce-421d-bb84-5c41a770bf60
keywords:
- WM_GESTURENOTIFY message Windows tactile
topic_type:
- apiref
api_name:
- WM_GESTURENOTIFY
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e900e4b607760df16938080a49f97a3ab0cf2ed
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104530"
---
# <a name="wm_gesturenotify-message"></a><span data-ttu-id="506ea-104">\_Message WM GESTURENOTIFY</span><span class="sxs-lookup"><span data-stu-id="506ea-104">WM\_GESTURENOTIFY message</span></span>

<span data-ttu-id="506ea-105">Vous donne la possibilité de définir la configuration du geste.</span><span class="sxs-lookup"><span data-stu-id="506ea-105">Gives you a chance to set the gesture configuration.</span></span>

## <a name="parameters"></a><span data-ttu-id="506ea-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="506ea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="506ea-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="506ea-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="506ea-108">Inutilisé.</span><span class="sxs-lookup"><span data-stu-id="506ea-108">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="506ea-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="506ea-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="506ea-110">Pointeur vers un [**GESTURENOTIFYSTRUCT**](/windows/win32/api/winuser/ns-winuser-gesturenotifystruct).</span><span class="sxs-lookup"><span data-stu-id="506ea-110">A pointer to a [**GESTURENOTIFYSTRUCT**](/windows/win32/api/winuser/ns-winuser-gesturenotifystruct).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="506ea-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="506ea-111">Return value</span></span>

<span data-ttu-id="506ea-112">Une valeur doit être retournée à partir de [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="506ea-112">A value should be returned from [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span>

## <a name="remarks"></a><span data-ttu-id="506ea-113">Notes</span><span class="sxs-lookup"><span data-stu-id="506ea-113">Remarks</span></span>

<span data-ttu-id="506ea-114">Lorsque le message **WM \_ GESTURENOTIFY** est reçu, l’application peut utiliser [**SetGestureConfig**](/windows/desktop/api/winuser/nf-winuser-setgestureconfig) pour spécifier les gestes à recevoir.</span><span class="sxs-lookup"><span data-stu-id="506ea-114">When the **WM\_GESTURENOTIFY** message is received, the application can use [**SetGestureConfig**](/windows/desktop/api/winuser/nf-winuser-setgestureconfig) to specify the gestures to receive.</span></span> <span data-ttu-id="506ea-115">Ce message doit toujours être propagé à l’aide de la fonction [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) .</span><span class="sxs-lookup"><span data-stu-id="506ea-115">This message should always be bubbled up using the [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) function.</span></span>

> [!Note]  
> <span data-ttu-id="506ea-116">Le fait de gérer le message **WM \_ GESTURENOTIFY** modifie la configuration du geste pour la durée de vie de la fenêtre, pas seulement pour le mouvement suivant.</span><span class="sxs-lookup"><span data-stu-id="506ea-116">Handling the **WM\_GESTURENOTIFY** message will change the gesture configuration for the lifetime of the Window, not just for the next gesture.</span></span>

 

## <a name="examples"></a><span data-ttu-id="506ea-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="506ea-117">Examples</span></span>

<span data-ttu-id="506ea-118">L’exemple suivant montre comment activer tous les mouvements.</span><span class="sxs-lookup"><span data-stu-id="506ea-118">The following example shows how to enable all gestures.</span></span> <span data-ttu-id="506ea-119">Pour plus d’exemples, consultez [**SetGestureConfig**](/windows/desktop/api/winuser/nf-winuser-setgestureconfig).</span><span class="sxs-lookup"><span data-stu-id="506ea-119">For more examples, see [**SetGestureConfig**](/windows/desktop/api/winuser/nf-winuser-setgestureconfig).</span></span>


```C++
    switch (message)
    {
    case WM_GESTURENOTIFY:
        GESTURECONFIG gc = {0,GC_ALLGESTURES,0};
        BOOL bResult = SetGestureConfig(hWnd,0,1,&gc,sizeof(GESTURECONFIG));
            
        if(!bResult)
        {
            // an error
        }
        return DefWindowProc(hWnd, WM_GESTURENOTIFY, wParam, lParam);
    }
      
```



## <a name="requirements"></a><span data-ttu-id="506ea-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="506ea-120">Requirements</span></span>



| <span data-ttu-id="506ea-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="506ea-121">Requirement</span></span> | <span data-ttu-id="506ea-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="506ea-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="506ea-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="506ea-123">Minimum supported client</span></span><br/> | <span data-ttu-id="506ea-124">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="506ea-124">Windows 7 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="506ea-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="506ea-125">Minimum supported server</span></span><br/> | <span data-ttu-id="506ea-126">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="506ea-126">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                  |
| <span data-ttu-id="506ea-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="506ea-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="506ea-128"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="506ea-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="506ea-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="506ea-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="506ea-130">Notifications</span><span class="sxs-lookup"><span data-stu-id="506ea-130">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="506ea-131">Guide de programmation des gestes tactiles Windows</span><span class="sxs-lookup"><span data-stu-id="506ea-131">Windows Touch Gestures Programming Guide</span></span>](guide-multi-touch-gestures.md)
</dt> <dt>

[<span data-ttu-id="506ea-132">**GESTURENOTIFYSTRUCT**</span><span class="sxs-lookup"><span data-stu-id="506ea-132">**GESTURENOTIFYSTRUCT**</span></span>](/windows/win32/api/winuser/ns-winuser-gesturenotifystruct)
</dt> <dt>

[<span data-ttu-id="506ea-133">**SetGestureConfig**</span><span class="sxs-lookup"><span data-stu-id="506ea-133">**SetGestureConfig**</span></span>](/windows/desktop/api/winuser/nf-winuser-setgestureconfig)
</dt> </dl>

 

