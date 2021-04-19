---
description: Envoyé avant le message WM \_ Create lorsqu’une fenêtre est créée pour la première fois.
ms.assetid: 5dd0eda3-83a6-4077-a7a3-e371c9413b0f
title: Message WM_NCCREATE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8757cbdeba49d54f6e5d842a5b40c7f7ae61cac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106539094"
---
# <a name="wm_nccreate-message"></a><span data-ttu-id="44a68-103">\_Message WM NCCREATE</span><span class="sxs-lookup"><span data-stu-id="44a68-103">WM\_NCCREATE message</span></span>

<span data-ttu-id="44a68-104">Envoyé avant le message [**WM \_ Create**](wm-create.md) lorsqu’une fenêtre est créée pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="44a68-104">Sent prior to the [**WM\_CREATE**](wm-create.md) message when a window is first created.</span></span>

<span data-ttu-id="44a68-105">Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="44a68-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_NCCREATE                     0x0081
```



## <a name="parameters"></a><span data-ttu-id="44a68-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="44a68-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44a68-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="44a68-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="44a68-108">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="44a68-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="44a68-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="44a68-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="44a68-110">Pointeur vers la structure [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) qui contient des informations sur la fenêtre en cours de création.</span><span class="sxs-lookup"><span data-stu-id="44a68-110">A pointer to the [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) structure that contains information about the window being created.</span></span> <span data-ttu-id="44a68-111">Les membres de **CREATESTRUCT** sont identiques aux paramètres de la fonction [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) .</span><span class="sxs-lookup"><span data-stu-id="44a68-111">The members of **CREATESTRUCT** are identical to the parameters of the [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44a68-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="44a68-112">Return value</span></span>

<span data-ttu-id="44a68-113">Type : **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="44a68-113">Type: **LRESULT**</span></span>

<span data-ttu-id="44a68-114">Si une application traite ce message, elle doit retourner la **valeur true** pour poursuivre la création de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="44a68-114">If an application processes this message, it should return **TRUE** to continue creation of the window.</span></span> <span data-ttu-id="44a68-115">Si l’application retourne la **valeur false**, la fonction [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) ou [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) retourne un handle **null** .</span><span class="sxs-lookup"><span data-stu-id="44a68-115">If the application returns **FALSE**, the [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) or [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) function will return a **NULL** handle.</span></span>

## <a name="requirements"></a><span data-ttu-id="44a68-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="44a68-116">Requirements</span></span>



| <span data-ttu-id="44a68-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="44a68-117">Requirement</span></span> | <span data-ttu-id="44a68-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="44a68-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44a68-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="44a68-119">Minimum supported client</span></span><br/> | <span data-ttu-id="44a68-120">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="44a68-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="44a68-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="44a68-121">Minimum supported server</span></span><br/> | <span data-ttu-id="44a68-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="44a68-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="44a68-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="44a68-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="44a68-124"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="44a68-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44a68-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="44a68-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="44a68-126">**Référence**</span><span class="sxs-lookup"><span data-stu-id="44a68-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="44a68-127">**CreateWindow**</span><span class="sxs-lookup"><span data-stu-id="44a68-127">**CreateWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-createwindowa)
</dt> <dt>

[<span data-ttu-id="44a68-128">**CreateWindowEx**</span><span class="sxs-lookup"><span data-stu-id="44a68-128">**CreateWindowEx**</span></span>](/windows/win32/api/winuser/nf-winuser-createwindowexa)
</dt> <dt>

[<span data-ttu-id="44a68-129">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="44a68-129">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="44a68-130">**CREATESTRUCT**</span><span class="sxs-lookup"><span data-stu-id="44a68-130">**CREATESTRUCT**</span></span>](/windows/win32/api/winuser/ns-winuser-createstructa)
</dt> <dt>

[<span data-ttu-id="44a68-131">**création de WM \_**</span><span class="sxs-lookup"><span data-stu-id="44a68-131">**WM\_CREATE**</span></span>](wm-create.md)
</dt> <dt>

<span data-ttu-id="44a68-132">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="44a68-132">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="44a68-133">Windows</span><span class="sxs-lookup"><span data-stu-id="44a68-133">Windows</span></span>](windows.md)
</dt> </dl>

 

 
