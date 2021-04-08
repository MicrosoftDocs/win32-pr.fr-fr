---
title: Message d’WM_CHOOSEFONT_SETLOGFONT (COMMDLG. h)
description: Une application envoie le \_ message WM CHOOSEFONT \_ SETLOGFONT à une boîte de dialogue de police pour définir les informations de police logique actuelles.
ms.assetid: ad169eca-a3ae-45bd-90df-821a93a7a764
keywords:
- Boîtes de dialogue de WM_CHOOSEFONT_SETLOGFONT message
topic_type:
- apiref
api_name:
- WM_CHOOSEFONT_SETLOGFONT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6a588ebff7c8e56bb559a2cc9faa1d6290fbd8f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742581"
---
# <a name="wm_choosefont_setlogfont-message"></a><span data-ttu-id="28f90-104">\_ \_ Message SETLOGFONT WM CHOOSEFONT</span><span class="sxs-lookup"><span data-stu-id="28f90-104">WM\_CHOOSEFONT\_SETLOGFONT message</span></span>

<span data-ttu-id="28f90-105">Une application envoie le message **WM \_ CHOOSEFONT \_ SETLOGFONT** à une boîte de dialogue de **police** pour définir les informations de police logique actuelles.</span><span class="sxs-lookup"><span data-stu-id="28f90-105">An application sends the **WM\_CHOOSEFONT\_SETLOGFONT** message to a **Font** dialog box to set the current logical font information.</span></span>


```C++
#define WM_USER                        0x0400
#define WM_CHOOSEFONT_SETLOGFONT      (WM_USER + 101)
```



## <a name="parameters"></a><span data-ttu-id="28f90-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="28f90-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28f90-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="28f90-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="28f90-108">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="28f90-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="28f90-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="28f90-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="28f90-110">Pointeur vers une structure [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) qui contient des informations sur la police logique en cours.</span><span class="sxs-lookup"><span data-stu-id="28f90-110">A pointer to a [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure that contains information about the current logical font.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28f90-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="28f90-111">Return value</span></span>

<span data-ttu-id="28f90-112">Ce message n’a pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="28f90-112">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="28f90-113">Notes</span><span class="sxs-lookup"><span data-stu-id="28f90-113">Remarks</span></span>

<span data-ttu-id="28f90-114">Quand vous appelez la fonction [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) pour créer une boîte de dialogue de **police** , vous pouvez utiliser le membre **lpLogFont** de la structure [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) pour spécifier une structure [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) contenant les valeurs initiales de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="28f90-114">When you call the [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) function to create a **Font** dialog box, you can use the **lpLogFont** member of the [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) structure to specify a [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure containing initial values for the dialog box.</span></span> <span data-ttu-id="28f90-115">Utilisez le message **WM \_ CHOOSEFONT \_ SETLOGFONT** pour spécifier une structure **LOGFONT** avec des valeurs différentes lorsque la boîte de dialogue **police** est ouverte.</span><span class="sxs-lookup"><span data-stu-id="28f90-115">Use the **WM\_CHOOSEFONT\_SETLOGFONT** message to specify a **LOGFONT** structure with different values while the **Font** dialog box is open.</span></span>

<span data-ttu-id="28f90-116">En règle générale, vous envoyez le message **WM \_ CHOOSEFONT \_ SETLOGFONT** à partir d’une procédure de hook [**CFHookProc**](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc) .</span><span class="sxs-lookup"><span data-stu-id="28f90-116">Typically, you would send the **WM\_CHOOSEFONT\_SETLOGFONT** message from a [**CFHookProc**](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc) hook procedure.</span></span> <span data-ttu-id="28f90-117">La procédure de hook peut également envoyer les messages [**WM \_ CHOOSEFONT \_ GETLOGFONT**](wm-choosefont-getlogfont.md) et [**WM \_ CHOOSEFONT \_ SETFLAGS**](wm-choosefont-setflags.md) .</span><span class="sxs-lookup"><span data-stu-id="28f90-117">The hook procedure can also send the [**WM\_CHOOSEFONT\_GETLOGFONT**](wm-choosefont-getlogfont.md) and [**WM\_CHOOSEFONT\_SETFLAGS**](wm-choosefont-setflags.md) messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="28f90-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="28f90-118">Requirements</span></span>



| <span data-ttu-id="28f90-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="28f90-119">Requirement</span></span> | <span data-ttu-id="28f90-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="28f90-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28f90-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="28f90-121">Minimum supported client</span></span><br/> | <span data-ttu-id="28f90-122">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="28f90-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="28f90-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="28f90-123">Minimum supported server</span></span><br/> | <span data-ttu-id="28f90-124">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="28f90-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="28f90-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="28f90-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="28f90-126"><dt>Commdlg. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="28f90-126"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28f90-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="28f90-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="28f90-128">**Référence**</span><span class="sxs-lookup"><span data-stu-id="28f90-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="28f90-129">**CFHookProc**</span><span class="sxs-lookup"><span data-stu-id="28f90-129">**CFHookProc**</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc)
</dt> <dt>

[<span data-ttu-id="28f90-130">**ChooseFont**</span><span class="sxs-lookup"><span data-stu-id="28f90-130">**ChooseFont**</span></span>](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

[<span data-ttu-id="28f90-131">**CHOOSEFONT**</span><span class="sxs-lookup"><span data-stu-id="28f90-131">**CHOOSEFONT**</span></span>](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

[<span data-ttu-id="28f90-132">**\_CHOOSEFONT WM \_ GETLOGFONT**</span><span class="sxs-lookup"><span data-stu-id="28f90-132">**WM\_CHOOSEFONT\_GETLOGFONT**</span></span>](wm-choosefont-getlogfont.md)
</dt> <dt>

[<span data-ttu-id="28f90-133">**\_CHOOSEFONT WM \_ SETFLAGS**</span><span class="sxs-lookup"><span data-stu-id="28f90-133">**WM\_CHOOSEFONT\_SETFLAGS**</span></span>](wm-choosefont-setflags.md)
</dt> <dt>

<span data-ttu-id="28f90-134">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="28f90-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="28f90-135">Bibliothèque de boîtes de dialogue communes</span><span class="sxs-lookup"><span data-stu-id="28f90-135">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> <dt>

<span data-ttu-id="28f90-136">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="28f90-136">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="28f90-137">**LOGFONT**</span><span class="sxs-lookup"><span data-stu-id="28f90-137">**LOGFONT**</span></span>](/windows/win32/api/wingdi/ns-wingdi-logfonta)
</dt> </dl>

 

