---
description: Envoyé à une application par l’IME pour notifier l’application d’une pression de touche et conserver l’ordre des messages. Une fenêtre reçoit ce message par le biais de sa fonction WindowProc.
ms.assetid: db7075fb-b3d4-4d32-a0db-096d17d67c72
title: Message WM_IME_KEYDOWN (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3089af3c839f70e7f55895ae13158e7b2240605
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201475"
---
# <a name="wm_ime_keydown-message"></a><span data-ttu-id="1292c-104">\_Message de \_ keyversion de l’IME WM</span><span class="sxs-lookup"><span data-stu-id="1292c-104">WM\_IME\_KEYDOWN message</span></span>

<span data-ttu-id="1292c-105">Envoyé à une application par l’IME pour notifier l’application d’une pression de touche et conserver l’ordre des messages.</span><span class="sxs-lookup"><span data-stu-id="1292c-105">Sent to an application by the IME to notify the application of a key press and to keep message order.</span></span> <span data-ttu-id="1292c-106">Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="1292c-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,        
  WM_IME_KEYDOWN,  
  WPARAM wParam, 
  LPARAM lParam      
);
```



## <a name="parameters"></a><span data-ttu-id="1292c-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1292c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1292c-108">*HWND*</span><span class="sxs-lookup"><span data-stu-id="1292c-108">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="1292c-109">Handle de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="1292c-109">A handle to window.</span></span>

</dd> <dt>

<span data-ttu-id="1292c-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1292c-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1292c-111">Code de clé virtuelle de la clé.</span><span class="sxs-lookup"><span data-stu-id="1292c-111">Virtual key code of the key.</span></span>

</dd> <dt>

<span data-ttu-id="1292c-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1292c-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1292c-113">Le tableau suivant indique le nombre de répétitions, l’analyse du code, l’indicateur de clé étendu, le code de contexte, l’indicateur d’état de la clé précédente et l’indicateur d’état de transition.</span><span class="sxs-lookup"><span data-stu-id="1292c-113">Repeat count, scan code, extended key flag, context code, previous key state flag, and transition state flag, as shown in the following table.</span></span>



| <span data-ttu-id="1292c-114">bit</span><span class="sxs-lookup"><span data-stu-id="1292c-114">Bit</span></span>   | <span data-ttu-id="1292c-115">Signification</span><span class="sxs-lookup"><span data-stu-id="1292c-115">Meaning</span></span>                                                                     |
|-------|-----------------------------------------------------------------------------|
| <span data-ttu-id="1292c-116">0-15</span><span class="sxs-lookup"><span data-stu-id="1292c-116">0-15</span></span>  | <span data-ttu-id="1292c-117">Nombre de répétitions.</span><span class="sxs-lookup"><span data-stu-id="1292c-117">Repeat count.</span></span>                                                               |
| <span data-ttu-id="1292c-118">16-23</span><span class="sxs-lookup"><span data-stu-id="1292c-118">16-23</span></span> | <span data-ttu-id="1292c-119">Analyser le code.</span><span class="sxs-lookup"><span data-stu-id="1292c-119">Scan code.</span></span>                                                                  |
| <span data-ttu-id="1292c-120">24</span><span class="sxs-lookup"><span data-stu-id="1292c-120">24</span></span>    | <span data-ttu-id="1292c-121">Clé étendue.</span><span class="sxs-lookup"><span data-stu-id="1292c-121">Extended key.</span></span> <span data-ttu-id="1292c-122">Cette valeur est 1 s’il s’agit d’une clé étendue.</span><span class="sxs-lookup"><span data-stu-id="1292c-122">This value is 1 if it is an extended key.</span></span> <span data-ttu-id="1292c-123">Sinon, la valeur est 0.</span><span class="sxs-lookup"><span data-stu-id="1292c-123">Otherwise, it is 0.</span></span> |
| <span data-ttu-id="1292c-124">25-28</span><span class="sxs-lookup"><span data-stu-id="1292c-124">25-28</span></span> | <span data-ttu-id="1292c-125">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="1292c-125">Not used.</span></span>                                                                   |
| <span data-ttu-id="1292c-126">29</span><span class="sxs-lookup"><span data-stu-id="1292c-126">29</span></span>    | <span data-ttu-id="1292c-127">Code de contexte.</span><span class="sxs-lookup"><span data-stu-id="1292c-127">Context code.</span></span> <span data-ttu-id="1292c-128">Cette valeur est toujours 0.</span><span class="sxs-lookup"><span data-stu-id="1292c-128">This value is always 0.</span></span>                                       |
| <span data-ttu-id="1292c-129">30</span><span class="sxs-lookup"><span data-stu-id="1292c-129">30</span></span>    | <span data-ttu-id="1292c-130">État de la clé précédente.</span><span class="sxs-lookup"><span data-stu-id="1292c-130">Previous key state.</span></span> <span data-ttu-id="1292c-131">Cette valeur est 1 si la touche est enfoncée ou 0 si elle est active.</span><span class="sxs-lookup"><span data-stu-id="1292c-131">This value is 1 if the key is down or 0 if it is up.</span></span>    |
| <span data-ttu-id="1292c-132">31</span><span class="sxs-lookup"><span data-stu-id="1292c-132">31</span></span>    | <span data-ttu-id="1292c-133">État de transition.</span><span class="sxs-lookup"><span data-stu-id="1292c-133">Transition state.</span></span> <span data-ttu-id="1292c-134">Cette valeur est toujours 0.</span><span class="sxs-lookup"><span data-stu-id="1292c-134">This value is always 0.</span></span>                                   |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1292c-135">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1292c-135">Return value</span></span>

<span data-ttu-id="1292c-136">Une application doit retourner 0 si elle traite ce message.</span><span class="sxs-lookup"><span data-stu-id="1292c-136">An application should return 0 if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="1292c-137">Notes</span><span class="sxs-lookup"><span data-stu-id="1292c-137">Remarks</span></span>

<span data-ttu-id="1292c-138">Une application peut traiter ce message ou la passer à la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  pour générer un message [**de \_ keyversion WM**](../inputdev/wm-keydown.md) correspondant.</span><span class="sxs-lookup"><span data-stu-id="1292c-138">An application can process this message or pass it to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  function to generate a matching [**WM\_KEYDOWN**](../inputdev/wm-keydown.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="1292c-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1292c-139">Requirements</span></span>



| <span data-ttu-id="1292c-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1292c-140">Requirement</span></span> | <span data-ttu-id="1292c-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="1292c-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1292c-142">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1292c-142">Minimum supported client</span></span><br/> | <span data-ttu-id="1292c-143">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1292c-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="1292c-144">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1292c-144">Minimum supported server</span></span><br/> | <span data-ttu-id="1292c-145">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1292c-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1292c-146">En-tête</span><span class="sxs-lookup"><span data-stu-id="1292c-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="1292c-147"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1292c-147"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1292c-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1292c-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1292c-149">Gestionnaire de méthode d’entrée</span><span class="sxs-lookup"><span data-stu-id="1292c-149">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="1292c-150">Messages du gestionnaire de méthode d’entrée</span><span class="sxs-lookup"><span data-stu-id="1292c-150">Input Method Manager Messages</span></span>](input-method-manager-messages.md)
</dt> </dl>

 

 
