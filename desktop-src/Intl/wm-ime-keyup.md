---
description: Envoyé à une application par l’IME pour notifier l’application d’une version de clé et conserver l’ordre des messages. Une fenêtre reçoit ce message par le biais de sa fonction WindowProc.
ms.assetid: 652f951f-4e9f-407c-844c-b250b6a9e6f5
title: Message WM_IME_KEYUP (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e0eb6c6701510a373573ff6d85d5b50a8541b4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515036"
---
# <a name="wm_ime_keyup-message"></a><span data-ttu-id="8d5ef-104">\_Message de retouche de l’IME WM \_</span><span class="sxs-lookup"><span data-stu-id="8d5ef-104">WM\_IME\_KEYUP message</span></span>

<span data-ttu-id="8d5ef-105">Envoyé à une application par l’IME pour notifier l’application d’une version de clé et conserver l’ordre des messages.</span><span class="sxs-lookup"><span data-stu-id="8d5ef-105">Sent to an application by the IME to notify the application of a key release and to keep message order.</span></span> <span data-ttu-id="8d5ef-106">Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="8d5ef-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,       
  WM_IME_KEYUP,    
  WPARAM wParam,   
  LPARAM lParam    
);
```



## <a name="parameters"></a><span data-ttu-id="8d5ef-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8d5ef-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d5ef-108">*HWND*</span><span class="sxs-lookup"><span data-stu-id="8d5ef-108">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="8d5ef-109">Handle de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="8d5ef-109">A handle to window.</span></span>

</dd> <dt>

<span data-ttu-id="8d5ef-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8d5ef-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8d5ef-111">Code de clé virtuelle de la clé.</span><span class="sxs-lookup"><span data-stu-id="8d5ef-111">Virtual key code of the key.</span></span>

</dd> <dt>

<span data-ttu-id="8d5ef-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8d5ef-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8d5ef-113">Nombre de répétitions, code d’analyse, indicateur de clé étendue, code de contexte, indicateur d’état de clé précédent et indicateur d’état de transition, comme indiqué ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="8d5ef-113">Repeat count, scan code, extended key flag, context code, previous key state flag, and transition state flag, as shown below.</span></span>



| <span data-ttu-id="8d5ef-114">bit</span><span class="sxs-lookup"><span data-stu-id="8d5ef-114">Bit</span></span>   | <span data-ttu-id="8d5ef-115">Signification</span><span class="sxs-lookup"><span data-stu-id="8d5ef-115">Meaning</span></span>                                                                     |
|-------|-----------------------------------------------------------------------------|
| <span data-ttu-id="8d5ef-116">0-15</span><span class="sxs-lookup"><span data-stu-id="8d5ef-116">0-15</span></span>  | <span data-ttu-id="8d5ef-117">Nombre de répétitions.</span><span class="sxs-lookup"><span data-stu-id="8d5ef-117">Repeat count.</span></span> <span data-ttu-id="8d5ef-118">Cette valeur est toujours 1.</span><span class="sxs-lookup"><span data-stu-id="8d5ef-118">This value is always 1.</span></span>                                       |
| <span data-ttu-id="8d5ef-119">16-23</span><span class="sxs-lookup"><span data-stu-id="8d5ef-119">16-23</span></span> | <span data-ttu-id="8d5ef-120">Analyser le code.</span><span class="sxs-lookup"><span data-stu-id="8d5ef-120">Scan code.</span></span>                                                                  |
| <span data-ttu-id="8d5ef-121">24</span><span class="sxs-lookup"><span data-stu-id="8d5ef-121">24</span></span>    | <span data-ttu-id="8d5ef-122">Clé étendue.</span><span class="sxs-lookup"><span data-stu-id="8d5ef-122">Extended key.</span></span> <span data-ttu-id="8d5ef-123">Cette valeur est 1 s’il s’agit d’une clé étendue.</span><span class="sxs-lookup"><span data-stu-id="8d5ef-123">This value is 1 if it is an extended key.</span></span> <span data-ttu-id="8d5ef-124">Sinon, la valeur est 0.</span><span class="sxs-lookup"><span data-stu-id="8d5ef-124">Otherwise, it is 0.</span></span> |
| <span data-ttu-id="8d5ef-125">25-28</span><span class="sxs-lookup"><span data-stu-id="8d5ef-125">25-28</span></span> | <span data-ttu-id="8d5ef-126">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="8d5ef-126">Not used.</span></span>                                                                   |
| <span data-ttu-id="8d5ef-127">29</span><span class="sxs-lookup"><span data-stu-id="8d5ef-127">29</span></span>    | <span data-ttu-id="8d5ef-128">Code de contexte.</span><span class="sxs-lookup"><span data-stu-id="8d5ef-128">Context code.</span></span> <span data-ttu-id="8d5ef-129">Cette valeur est toujours 0.</span><span class="sxs-lookup"><span data-stu-id="8d5ef-129">This value is always 0.</span></span>                                       |
| <span data-ttu-id="8d5ef-130">30</span><span class="sxs-lookup"><span data-stu-id="8d5ef-130">30</span></span>    | <span data-ttu-id="8d5ef-131">État de la clé précédente.</span><span class="sxs-lookup"><span data-stu-id="8d5ef-131">Previous key state.</span></span> <span data-ttu-id="8d5ef-132">Cette valeur est toujours 1.</span><span class="sxs-lookup"><span data-stu-id="8d5ef-132">This value is always 1.</span></span>                                 |
| <span data-ttu-id="8d5ef-133">31</span><span class="sxs-lookup"><span data-stu-id="8d5ef-133">31</span></span>    | <span data-ttu-id="8d5ef-134">État de transition.</span><span class="sxs-lookup"><span data-stu-id="8d5ef-134">Transition state.</span></span> <span data-ttu-id="8d5ef-135">Cette valeur est toujours 1.</span><span class="sxs-lookup"><span data-stu-id="8d5ef-135">This value is always 1.</span></span>                                   |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d5ef-136">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8d5ef-136">Return value</span></span>

<span data-ttu-id="8d5ef-137">Une application doit retourner 0 si elle traite ce message.</span><span class="sxs-lookup"><span data-stu-id="8d5ef-137">An application should return 0 if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d5ef-138">Notes</span><span class="sxs-lookup"><span data-stu-id="8d5ef-138">Remarks</span></span>

<span data-ttu-id="8d5ef-139">Une application peut traiter ce message ou la passer à la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  pour générer un message [**WM \_ KEYUP**](../inputdev/wm-keyup.md) correspondant.</span><span class="sxs-lookup"><span data-stu-id="8d5ef-139">An application can process this message or pass it to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  function to generate a matching [**WM\_KEYUP**](../inputdev/wm-keyup.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d5ef-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8d5ef-140">Requirements</span></span>



| <span data-ttu-id="8d5ef-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8d5ef-141">Requirement</span></span> | <span data-ttu-id="8d5ef-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="8d5ef-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d5ef-143">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8d5ef-143">Minimum supported client</span></span><br/> | <span data-ttu-id="8d5ef-144">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8d5ef-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="8d5ef-145">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8d5ef-145">Minimum supported server</span></span><br/> | <span data-ttu-id="8d5ef-146">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8d5ef-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8d5ef-147">En-tête</span><span class="sxs-lookup"><span data-stu-id="8d5ef-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="8d5ef-148"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8d5ef-148"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d5ef-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8d5ef-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d5ef-150">Gestionnaire de méthode d’entrée</span><span class="sxs-lookup"><span data-stu-id="8d5ef-150">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="8d5ef-151">Messages du gestionnaire de méthode d’entrée</span><span class="sxs-lookup"><span data-stu-id="8d5ef-151">Input Method Manager Messages</span></span>](input-method-manager-messages.md)
</dt> </dl>

 

 
