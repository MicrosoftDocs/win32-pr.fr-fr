---
description: Envoyé à une application lorsque le système d’exploitation est sur le ou la modification de l’éditeur IME actuel. Une fenêtre reçoit ce message par le biais de sa fonction WindowProc.
ms.assetid: 5559b3ab-8d81-4f33-b0af-d05489371328
title: Message WM_IME_SELECT (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 940858e12c616b1d6281c23633b2f0f5e9657a9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515865"
---
# <a name="wm_ime_select-message"></a><span data-ttu-id="b1b6f-104">Message de sélection de l' \_ IME WM \_</span><span class="sxs-lookup"><span data-stu-id="b1b6f-104">WM\_IME\_SELECT message</span></span>

<span data-ttu-id="b1b6f-105">Envoyé à une application lorsque le système d’exploitation est sur le ou la modification de l’éditeur IME actuel.</span><span class="sxs-lookup"><span data-stu-id="b1b6f-105">Sent to an application when the operating system is about to change the current IME.</span></span> <span data-ttu-id="b1b6f-106">Une fenêtre reçoit ce message par le biais de sa fonction [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="b1b6f-106">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
 HWND  hwnd,       
 WM_IME_SELECT,   
 WPARAM wParam,   
 LPARAM lParam    
);
```



## <a name="parameters"></a><span data-ttu-id="b1b6f-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b1b6f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1b6f-108">*HWND*</span><span class="sxs-lookup"><span data-stu-id="b1b6f-108">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="b1b6f-109">Handle de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="b1b6f-109">A handle to window.</span></span>

</dd> <dt>

<span data-ttu-id="b1b6f-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b1b6f-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b1b6f-111">Indicateur de sélection.</span><span class="sxs-lookup"><span data-stu-id="b1b6f-111">Selection indicator.</span></span> <span data-ttu-id="b1b6f-112">Ce paramètre spécifie la **valeur true** si l’IME indiqué est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="b1b6f-112">This parameter specifies **TRUE** if the indicated IME is selected.</span></span> <span data-ttu-id="b1b6f-113">Le paramètre a la valeur **false** si l’IME spécifié n’est plus sélectionné.</span><span class="sxs-lookup"><span data-stu-id="b1b6f-113">The parameter is set to **FALSE** if the specified IME is no longer selected.</span></span>

</dd> <dt>

<span data-ttu-id="b1b6f-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b1b6f-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b1b6f-115">Identificateur de paramètres régionaux d’entrée associé à l’IME.</span><span class="sxs-lookup"><span data-stu-id="b1b6f-115">Input locale identifier associated with the IME.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1b6f-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b1b6f-116">Return value</span></span>

<span data-ttu-id="b1b6f-117">Ce message n’a pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="b1b6f-117">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b1b6f-118">Notes</span><span class="sxs-lookup"><span data-stu-id="b1b6f-118">Remarks</span></span>

<span data-ttu-id="b1b6f-119">Une application qui a créé une fenêtre IME doit transmettre ce message à cette fenêtre afin qu’il puisse récupérer le handle de la disposition du clavier vers l’IME nouvellement sélectionné.</span><span class="sxs-lookup"><span data-stu-id="b1b6f-119">An application that has created an IME window should pass this message to that window so that it can retrieve the keyboard layout handle to the newly selected IME.</span></span>

<span data-ttu-id="b1b6f-120">La fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  traite ce message en transmettant les informations à la fenêtre IME par défaut.</span><span class="sxs-lookup"><span data-stu-id="b1b6f-120">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  function processes this message by passing the information to the default IME window.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1b6f-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b1b6f-121">Requirements</span></span>



| <span data-ttu-id="b1b6f-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b1b6f-122">Requirement</span></span> | <span data-ttu-id="b1b6f-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="b1b6f-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1b6f-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b1b6f-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b1b6f-125">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b1b6f-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="b1b6f-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b1b6f-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b1b6f-127">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b1b6f-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b1b6f-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="b1b6f-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="b1b6f-129"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b1b6f-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1b6f-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b1b6f-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1b6f-131">Gestionnaire de méthode d’entrée</span><span class="sxs-lookup"><span data-stu-id="b1b6f-131">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="b1b6f-132">Messages du gestionnaire de méthode d’entrée</span><span class="sxs-lookup"><span data-stu-id="b1b6f-132">Input Method Manager Messages</span></span>](input-method-manager-messages.md)
</dt> </dl>

 

 
