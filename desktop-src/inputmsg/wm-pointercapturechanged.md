---
title: Message WM_POINTERCAPTURECHANGED
description: Envoyé à une fenêtre qui perd la capture d’un pointeur d’entrée.
ms.assetid: 6eec37da-227c-4be1-bf0b-98704caa1322
keywords:
- WM_POINTERCAPTURECHANGED les messages d’entrée du message et les notifications
topic_type:
- apiref
api_name:
- WM_POINTERCAPTURECHANGED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 768dc81be57bb61a23acab7ebea450dba577d60a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106536919"
---
# <a name="wm_pointercapturechanged-message"></a><span data-ttu-id="15385-104">Message WM_POINTERCAPTURECHANGED</span><span class="sxs-lookup"><span data-stu-id="15385-104">WM_POINTERCAPTURECHANGED message</span></span>

<span data-ttu-id="15385-105">Envoyé à une fenêtre qui perd la capture d’un pointeur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="15385-105">Sent to a window that is losing capture of an input pointer.</span></span>

<span data-ttu-id="15385-106">Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="15385-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_POINTERCAPTURECHANGED           0x024C
```



## <a name="parameters"></a><span data-ttu-id="15385-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="15385-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15385-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="15385-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="15385-109">Contient des informations sur le pointeur d’entrée qui est perdu.</span><span class="sxs-lookup"><span data-stu-id="15385-109">Contains information about the input pointer that is being lost.</span></span> <span data-ttu-id="15385-110">Utilisez [**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api) pour récupérer l’ID du pointeur.</span><span class="sxs-lookup"><span data-stu-id="15385-110">Use [**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api) to get the pointer ID.</span></span>

</dd> <dt>

<span data-ttu-id="15385-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="15385-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="15385-112">Contient un handle vers la fenêtre qui capture le pointeur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="15385-112">Contains a handle to the window that is capturing the input pointer.</span></span> <span data-ttu-id="15385-113">Cette valeur peut être NULL si le pointeur n’est plus capturé par la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="15385-113">This value can be NULL if the pointer is no longer being captured by the window.</span></span>

<span data-ttu-id="15385-114">Si ce message est généré à partir du traitement interne, la valeur peut être le handle de la fenêtre qui reçoit le message.</span><span class="sxs-lookup"><span data-stu-id="15385-114">If this message is generated from internal processing, the value can be the handle of the window receiving the message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15385-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="15385-115">Return value</span></span>

<span data-ttu-id="15385-116">Si une application traite ce message, elle doit retourner la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="15385-116">If an application processes this message, it should return zero.</span></span>

<span data-ttu-id="15385-117">Si l’application ne traite pas ce message, elle doit appeler [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="15385-117">If the application does not process this message, it should call [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span>

## <a name="remarks"></a><span data-ttu-id="15385-118">Notes</span><span class="sxs-lookup"><span data-stu-id="15385-118">Remarks</span></span>

<span data-ttu-id="15385-119">Une fenêtre doit utiliser cette notification pour arrêter le traitement des messages suivants et lancer tout nettoyage requis pour la perte du pointeur.</span><span class="sxs-lookup"><span data-stu-id="15385-119">A window should use this notification to stop processing subsequent messages and initiate any cleanup required for the pointer being lost.</span></span> <span data-ttu-id="15385-120">Le traitement des mouvements associés au pointeur doit également être terminé (par exemple, en appelant [**StopInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-stopinteractioncontext)) et les contacts restants sont à nouveau associés à la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="15385-120">Processing of gestures associated with the pointer should also be terminated (for example, by calling [**StopInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-stopinteractioncontext)) and remaining contacts re-associated with the window.</span></span>

<span data-ttu-id="15385-121">En règle générale, si une fenêtre reçoit la notification **WM_POINTERCAPTURECHANGED** , aucune notification ultérieure relative au pointeur d’entrée n’est reçue.</span><span class="sxs-lookup"><span data-stu-id="15385-121">Typically, if a window receives the **WM_POINTERCAPTURECHANGED** notification, no subsequent notifications related to the input pointer are received.</span></span> <span data-ttu-id="15385-122">Pour cette raison, ne dépendez pas de notifications jumelées telles que [**WM_POINTERENTER**](wm-pointerenter.md) et [**WM_POINTERLEAVE**](wm-pointerleave.md).</span><span class="sxs-lookup"><span data-stu-id="15385-122">Because of this, do not depend on paired notifications such as [**WM_POINTERENTER**](wm-pointerenter.md) and [**WM_POINTERLEAVE**](wm-pointerleave.md).</span></span>

<span data-ttu-id="15385-123">**WM_POINTERCAPTURECHANGED** n’inclut pas les données [**POINTER_INFO**](/previous-versions/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="15385-123">**WM_POINTERCAPTURECHANGED** does not include [**POINTER_INFO**](/previous-versions/windows/desktop/api) data.</span></span> <span data-ttu-id="15385-124">À part l’indicateur [**POINTER_FLAG_CAPTURECHANGED**](pointer-flags-contants.md) défini, les données retournées par [**GetPointerInfo**](/previous-versions/windows/desktop/api) (ou toute variante) sont identiques à celles retournées avant la notification.</span><span class="sxs-lookup"><span data-stu-id="15385-124">Other than the [**POINTER_FLAG_CAPTURECHANGED**](pointer-flags-contants.md) flag being set, the data returned by [**GetPointerInfo**](/previous-versions/windows/desktop/api) (or any variant) is identical to that returned prior to the notification.</span></span>

<span data-ttu-id="15385-125">Si l’application ne traite pas cette notification, [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) peut générer un ou plusieurs messages [**WM_GESTURE**](../wintouch/wm-gesture.md) ou, si un mouvement n’est pas reconnu, **DefWindowProc** peut générer une entrée de souris.</span><span class="sxs-lookup"><span data-stu-id="15385-125">If the application does not process this notification, [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) may generate one or more [**WM_GESTURE**](../wintouch/wm-gesture.md) messages or, if a gesture is not recognized, **DefWindowProc** may generate mouse input.</span></span>

<span data-ttu-id="15385-126">Si une application consomme de manière sélective une entrée de pointeur et passe le reste à [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca), le comportement résultant n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="15385-126">If an application selectively consumes some pointer input and passes the rest to [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca), the resulting behavior is undefined.</span></span>

## <a name="requirements"></a><span data-ttu-id="15385-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="15385-127">Requirements</span></span>



| <span data-ttu-id="15385-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="15385-128">Requirement</span></span> | <span data-ttu-id="15385-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="15385-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15385-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="15385-130">Minimum supported client</span></span><br/> | <span data-ttu-id="15385-131">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="15385-131">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="15385-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="15385-132">Minimum supported server</span></span><br/> | <span data-ttu-id="15385-133">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="15385-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="15385-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="15385-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="15385-135"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="15385-135"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15385-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="15385-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15385-137">Messages</span><span class="sxs-lookup"><span data-stu-id="15385-137">Messages</span></span>](messages.md)
</dt> </dl>

 

