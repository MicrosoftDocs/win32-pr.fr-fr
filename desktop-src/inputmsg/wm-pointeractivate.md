---
title: Message WM_POINTERACTIVATE
description: Envoyé à une fenêtre inactive lorsqu’un pointeur principal génère un WM_POINTERDOWN sur la fenêtre.
ms.assetid: 4eec37da-227c-4be1-bf0b-99704caa1322
keywords:
- WM_POINTERACTIVATE les messages d’entrée du message et les notifications
topic_type:
- apiref
api_name:
- WM_POINTERACTIVATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: b9bda11b5cb7a27f7744df6e20890a125a66bd88
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509933"
---
# <a name="wm_pointeractivate-message"></a><span data-ttu-id="be4a1-104">Message WM_POINTERACTIVATE</span><span class="sxs-lookup"><span data-stu-id="be4a1-104">WM_POINTERACTIVATE message</span></span>

<span data-ttu-id="be4a1-105">Envoyé à une fenêtre inactive lorsqu’un pointeur principal génère un [**WM_POINTERDOWN**](wm-pointerdown.md) sur la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="be4a1-105">Sent to an inactive window when a primary pointer generates a [**WM_POINTERDOWN**](wm-pointerdown.md) over the window.</span></span> <span data-ttu-id="be4a1-106">Tant que le message reste non géré, il se déplace vers le haut de la chaîne de la fenêtre parente jusqu’à ce qu’il atteigne la fenêtre de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="be4a1-106">As long as the message remains unhandled, it travels up the parent window chain until it is reaches the top-level window.</span></span> <span data-ttu-id="be4a1-107">Les applications peuvent répondre à ce message pour spécifier s’ils souhaitent être activés.</span><span class="sxs-lookup"><span data-stu-id="be4a1-107">Applications can respond to this message to specify whether they wish to be activated.</span></span>

<span data-ttu-id="be4a1-108">Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="be4a1-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_POINTERACTIVATE             0x024B
```



## <a name="parameters"></a><span data-ttu-id="be4a1-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="be4a1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be4a1-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="be4a1-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="be4a1-111">Contient l’identificateur du pointeur et des informations supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="be4a1-111">Contains the pointer identifier and additional information.</span></span> <span data-ttu-id="be4a1-112">Utilisez les macros suivantes pour récupérer ces informations.</span><span class="sxs-lookup"><span data-stu-id="be4a1-112">Use the following macros to retrieve this information.</span></span>

<span data-ttu-id="be4a1-113">[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam) : identificateur de pointeur</span><span class="sxs-lookup"><span data-stu-id="be4a1-113">[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): pointer identifier</span></span>

<span data-ttu-id="be4a1-114">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))(wParam) : valeur de test de positionnement retournée par le traitement du message de [**WM_NCHITTEST**](../inputdev/wm-nchittest.md) .</span><span class="sxs-lookup"><span data-stu-id="be4a1-114">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))(wParam): hit-test value returned from processing the [**WM_NCHITTEST**](../inputdev/wm-nchittest.md) message.</span></span>

</dd> <dt>

<span data-ttu-id="be4a1-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="be4a1-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="be4a1-116">Contient le handle de la fenêtre de niveau supérieur de la fenêtre en cours d’activation.</span><span class="sxs-lookup"><span data-stu-id="be4a1-116">Contains the handle to the top-level window of the window being activated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be4a1-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="be4a1-117">Return value</span></span>

<span data-ttu-id="be4a1-118">Si une application traite ce message, elle doit retourner l’une des valeurs décrites dans la section Notes.</span><span class="sxs-lookup"><span data-stu-id="be4a1-118">If an application processes this message, it should return one of the values described in the Remarks section.</span></span>

<span data-ttu-id="be4a1-119">Si l’application ne traite pas ce message, elle doit appeler [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="be4a1-119">If the application does not process this message, it should call [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span>

## <a name="remarks"></a><span data-ttu-id="be4a1-120">Notes</span><span class="sxs-lookup"><span data-stu-id="be4a1-120">Remarks</span></span>

<span data-ttu-id="be4a1-121">Une application peut gérer ce message et retourner l’une des valeurs suivantes pour déterminer comment le système traite l’activation et l’entrée d’activation :</span><span class="sxs-lookup"><span data-stu-id="be4a1-121">An application can handle this message and return one of the following values to determine how the system processes the activation and the activating input:</span></span>

-   <span data-ttu-id="be4a1-122">PA_ACTIVATE</span><span class="sxs-lookup"><span data-stu-id="be4a1-122">PA_ACTIVATE</span></span>
-   <span data-ttu-id="be4a1-123">PA_NOACTIVATE</span><span class="sxs-lookup"><span data-stu-id="be4a1-123">PA_NOACTIVATE</span></span>

<span data-ttu-id="be4a1-124">Il est important de noter que, lorsque l’utilisateur interagit avec le système avec plusieurs pointeurs simultanés, l’opportunité d’activation que le message **WM_POINTERACTIVATE** représente est disponible pour les applications uniquement pour le premier de ces pointeurs.</span><span class="sxs-lookup"><span data-stu-id="be4a1-124">It is important to note that, when the user is interacting with the system with multiple simultaneous pointers, the activation opportunity that the **WM_POINTERACTIVATE** message represents is available to applications only for the first of those pointers.</span></span> <span data-ttu-id="be4a1-125">Les applications doivent donc être conscientes qu’elles peuvent toujours recevoir des entrées des pointeurs alors qu’elles sont inactives.</span><span class="sxs-lookup"><span data-stu-id="be4a1-125">Applications should, therefore, be aware that they may still receive input from pointers while they are inactive.</span></span>

<span data-ttu-id="be4a1-126">Si l’application ne gère pas ce message, [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) transmet le message à la fenêtre parente.</span><span class="sxs-lookup"><span data-stu-id="be4a1-126">If the application does not handle this message, [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) passes the message to the parent window.</span></span>

## <a name="requirements"></a><span data-ttu-id="be4a1-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="be4a1-127">Requirements</span></span>



| <span data-ttu-id="be4a1-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="be4a1-128">Requirement</span></span> | <span data-ttu-id="be4a1-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="be4a1-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be4a1-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="be4a1-130">Minimum supported client</span></span><br/> | <span data-ttu-id="be4a1-131">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="be4a1-131">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="be4a1-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="be4a1-132">Minimum supported server</span></span><br/> | <span data-ttu-id="be4a1-133">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="be4a1-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="be4a1-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="be4a1-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="be4a1-135"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="be4a1-135"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be4a1-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="be4a1-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be4a1-137">Messages</span><span class="sxs-lookup"><span data-stu-id="be4a1-137">Messages</span></span>](messages.md)
</dt> </dl>

 

