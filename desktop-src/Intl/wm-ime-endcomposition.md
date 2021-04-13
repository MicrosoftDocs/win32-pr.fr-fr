---
description: Envoyé à une application lorsque l’IME termine la composition. Une fenêtre reçoit ce message par le biais de sa fonction WindowProc.
ms.assetid: d0f05524-4dfc-45b2-9476-6f1244190de5
title: Message WM_IME_ENDCOMPOSITION (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73ca9d1560810b22ae0d36010d2371e75b83a81c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318429"
---
# <a name="wm_ime_endcomposition-message"></a><span data-ttu-id="477d5-104">\_ \_ Message ENDCOMPOSITION de l’IME WM</span><span class="sxs-lookup"><span data-stu-id="477d5-104">WM\_IME\_ENDCOMPOSITION message</span></span>

<span data-ttu-id="477d5-105">Envoyé à une application lorsque l’IME termine la composition.</span><span class="sxs-lookup"><span data-stu-id="477d5-105">Sent to an application when the IME ends composition.</span></span> <span data-ttu-id="477d5-106">Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="477d5-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,      
  WM_IME_ENDCOMPOSITION,  
  WPARAM wParam,      
  LPARAM lParam             
);
```



## <a name="parameters"></a><span data-ttu-id="477d5-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="477d5-107">Parameters</span></span>

<span data-ttu-id="477d5-108">Ce message n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="477d5-108">This message has no parameters.</span></span>

<dl></dl>

## <a name="return-value"></a><span data-ttu-id="477d5-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="477d5-109">Return value</span></span>

<span data-ttu-id="477d5-110">Ce message n’a pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="477d5-110">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="477d5-111">Notes</span><span class="sxs-lookup"><span data-stu-id="477d5-111">Remarks</span></span>

<span data-ttu-id="477d5-112">Une application doit traiter ce message si elle affiche lui-même des caractères de composition.</span><span class="sxs-lookup"><span data-stu-id="477d5-112">An application should process this message if it displays composition characters itself.</span></span>

<span data-ttu-id="477d5-113">Si l’application a créé une fenêtre IME, elle doit transmettre ce message à cette fenêtre.</span><span class="sxs-lookup"><span data-stu-id="477d5-113">If the application has created an IME window, it should pass this message to that window.</span></span> <span data-ttu-id="477d5-114">La fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  traite ce message en le passant à la fenêtre IME par défaut.</span><span class="sxs-lookup"><span data-stu-id="477d5-114">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  function processes this message by passing it to the default IME window.</span></span>

## <a name="requirements"></a><span data-ttu-id="477d5-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="477d5-115">Requirements</span></span>



| <span data-ttu-id="477d5-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="477d5-116">Requirement</span></span> | <span data-ttu-id="477d5-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="477d5-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="477d5-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="477d5-118">Minimum supported client</span></span><br/> | <span data-ttu-id="477d5-119">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="477d5-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="477d5-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="477d5-120">Minimum supported server</span></span><br/> | <span data-ttu-id="477d5-121">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="477d5-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="477d5-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="477d5-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="477d5-123"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="477d5-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="477d5-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="477d5-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="477d5-125">Gestionnaire de méthode d’entrée</span><span class="sxs-lookup"><span data-stu-id="477d5-125">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="477d5-126">Messages du gestionnaire de méthode d’entrée</span><span class="sxs-lookup"><span data-stu-id="477d5-126">Input Method Manager Messages</span></span>](input-method-manager-messages.md)
</dt> </dl>

 

 
