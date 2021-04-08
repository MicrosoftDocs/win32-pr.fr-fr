---
description: Diffuser dans chaque fenêtre après un événement de modification de thème. Les exemples d’événements de changement de thème sont l’activation d’un thème, la désactivation d’un thème ou la transition d’un thème à un autre.
ms.assetid: 1a4051ac-cc6e-4520-ab66-d0a41a8a4c73
title: Message WM_THEMECHANGED (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bc15ab64126ff8972b858ef43ddd4d92cd62f58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751197"
---
# <a name="wm_themechanged-message"></a><span data-ttu-id="7df20-104">\_Message WM THEMECHANGED</span><span class="sxs-lookup"><span data-stu-id="7df20-104">WM\_THEMECHANGED message</span></span>

<span data-ttu-id="7df20-105">Diffuser dans chaque fenêtre après un événement de modification de thème.</span><span class="sxs-lookup"><span data-stu-id="7df20-105">Broadcast to every window following a theme change event.</span></span> <span data-ttu-id="7df20-106">Les exemples d’événements de changement de thème sont l’activation d’un thème, la désactivation d’un thème ou la transition d’un thème à un autre.</span><span class="sxs-lookup"><span data-stu-id="7df20-106">Examples of theme change events are the activation of a theme, the deactivation of a theme, or a transition from one theme to another.</span></span>


```C++
#define WM_THEMECHANGED                 0x031A
```



## <a name="parameters"></a><span data-ttu-id="7df20-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7df20-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7df20-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7df20-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7df20-109">Ce paramètre est réservé.</span><span class="sxs-lookup"><span data-stu-id="7df20-109">This parameter is reserved.</span></span>

</dd> <dt>

<span data-ttu-id="7df20-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7df20-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7df20-111">Ce paramètre est réservé.</span><span class="sxs-lookup"><span data-stu-id="7df20-111">This parameter is reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7df20-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7df20-112">Return value</span></span>

<span data-ttu-id="7df20-113">Type : **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="7df20-113">Type: **LRESULT**</span></span>

<span data-ttu-id="7df20-114">Si une application traite ce message, elle doit retourner la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="7df20-114">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="7df20-115">Notes</span><span class="sxs-lookup"><span data-stu-id="7df20-115">Remarks</span></span>

<span data-ttu-id="7df20-116">Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="7df20-116">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>

> [!Note]  
> <span data-ttu-id="7df20-117">Ce message est publié par le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="7df20-117">This message is posted by the operating system.</span></span> <span data-ttu-id="7df20-118">En général, les applications n’envoient pas ce message.</span><span class="sxs-lookup"><span data-stu-id="7df20-118">Applications typically do not send this message.</span></span>

 

<span data-ttu-id="7df20-119">Les thèmes sont des spécifications pour l’apparence des contrôles, afin que l’élément visuel d’un contrôle soit traité séparément de ses fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="7df20-119">Themes are specifications for the appearance of controls, so that the visual element of a control is treated separately from its functionality.</span></span>

<span data-ttu-id="7df20-120">Pour libérer un handle de thème existant, appelez [**CloseThemeData**](/windows/win32/api/uxtheme/nf-uxtheme-closethemedata).</span><span class="sxs-lookup"><span data-stu-id="7df20-120">To release an existing theme handle, call [**CloseThemeData**](/windows/win32/api/uxtheme/nf-uxtheme-closethemedata).</span></span> <span data-ttu-id="7df20-121">Pour acquérir un nouveau handle de thème, utilisez [**OpenThemeData**](/windows/win32/api/uxtheme/nf-uxtheme-openthemedata).</span><span class="sxs-lookup"><span data-stu-id="7df20-121">To acquire a new theme handle, use [**OpenThemeData**](/windows/win32/api/uxtheme/nf-uxtheme-openthemedata).</span></span>

<span data-ttu-id="7df20-122">À la suite de la diffusion **WM \_ THEMECHANGED** , les descripteurs de thème existants ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="7df20-122">Following the **WM\_THEMECHANGED** broadcast, any existing theme handles are invalid.</span></span> <span data-ttu-id="7df20-123">Une fenêtre sensible aux thèmes doit libérer et rouvrir l’un de ses descripteurs de thème préexistants lorsqu’elle reçoit le message **WM \_ THEMECHANGED** .</span><span class="sxs-lookup"><span data-stu-id="7df20-123">A theme-aware window should release and reopen any of its pre-existing theme handles when it receives the **WM\_THEMECHANGED** message.</span></span> <span data-ttu-id="7df20-124">Si la fonction [**OpenThemeData**](/windows/win32/api/uxtheme/nf-uxtheme-openthemedata) retourne la **valeur null**, la fenêtre doit être peinte sans thème.</span><span class="sxs-lookup"><span data-stu-id="7df20-124">If the [**OpenThemeData**](/windows/win32/api/uxtheme/nf-uxtheme-openthemedata) function returns **NULL**, the window should paint unthemed.</span></span>

## <a name="requirements"></a><span data-ttu-id="7df20-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7df20-125">Requirements</span></span>



| <span data-ttu-id="7df20-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7df20-126">Requirement</span></span> | <span data-ttu-id="7df20-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="7df20-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7df20-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7df20-128">Minimum supported client</span></span><br/> | <span data-ttu-id="7df20-129">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7df20-129">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="7df20-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7df20-130">Minimum supported server</span></span><br/> | <span data-ttu-id="7df20-131">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7df20-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7df20-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="7df20-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="7df20-133"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7df20-133"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7df20-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7df20-134">See also</span></span>

<dl> <dt>

<span data-ttu-id="7df20-135">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="7df20-135">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="7df20-136">**CloseThemeData**</span><span class="sxs-lookup"><span data-stu-id="7df20-136">**CloseThemeData**</span></span>](/windows/win32/api/uxtheme/nf-uxtheme-closethemedata)
</dt> <dt>

[<span data-ttu-id="7df20-137">**IsThemeActive**</span><span class="sxs-lookup"><span data-stu-id="7df20-137">**IsThemeActive**</span></span>](/windows/win32/api/uxtheme/nf-uxtheme-isthemeactive)
</dt> <dt>

[<span data-ttu-id="7df20-138">**OpenThemeData**</span><span class="sxs-lookup"><span data-stu-id="7df20-138">**OpenThemeData**</span></span>](/windows/win32/api/uxtheme/nf-uxtheme-openthemedata)
</dt> </dl>

 

 
