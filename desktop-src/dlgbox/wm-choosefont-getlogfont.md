---
title: Message d’WM_CHOOSEFONT_GETLOGFONT (COMMDLG. h)
description: Une application envoie le \_ message WM CHOOSEFONT \_ GETLOGFONT à une boîte de dialogue de police pour récupérer des informations sur les sélections de polices d’utilisateur actuelles.
ms.assetid: afbf953a-13dd-409b-a988-f1426c8bbd31
keywords:
- Boîtes de dialogue de WM_CHOOSEFONT_GETLOGFONT message
topic_type:
- apiref
api_name:
- WM_CHOOSEFONT_GETLOGFONT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 696246d26c2b87e9b299844a9dc7e78d39ac632f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510987"
---
# <a name="wm_choosefont_getlogfont-message"></a><span data-ttu-id="8a49c-104">\_ \_ Message GETLOGFONT WM CHOOSEFONT</span><span class="sxs-lookup"><span data-stu-id="8a49c-104">WM\_CHOOSEFONT\_GETLOGFONT message</span></span>

<span data-ttu-id="8a49c-105">Une application envoie le message **WM \_ CHOOSEFONT \_ GETLOGFONT** à une boîte de dialogue de **police** pour récupérer des informations sur les sélections de polices d’utilisateur actuelles.</span><span class="sxs-lookup"><span data-stu-id="8a49c-105">An application sends the **WM\_CHOOSEFONT\_GETLOGFONT** message to a **Font** dialog box to retrieve information about the user's current font selections.</span></span>


```C++
#define WM_USER                        0x0400
#define WM_CHOOSEFONT_GETLOGFONT      (WM_USER + 1)
```



## <a name="parameters"></a><span data-ttu-id="8a49c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8a49c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a49c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8a49c-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8a49c-108">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="8a49c-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8a49c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8a49c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8a49c-110">Pointeur vers une structure [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) qui reçoit des informations sur les sélections de polices actuelles de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8a49c-110">A pointer to a [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure that receives information about the user's current font selections.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a49c-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8a49c-111">Return value</span></span>

<span data-ttu-id="8a49c-112">Ce message ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="8a49c-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8a49c-113">Notes</span><span class="sxs-lookup"><span data-stu-id="8a49c-113">Remarks</span></span>

<span data-ttu-id="8a49c-114">La fonction [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) crée une boîte de dialogue de **police** .</span><span class="sxs-lookup"><span data-stu-id="8a49c-114">The [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) function creates a **Font** dialog box.</span></span> <span data-ttu-id="8a49c-115">Lorsque l’utilisateur ferme la boîte de dialogue **police** , la fonction **ChooseFont** retourne des informations sur les sélections de police de l’utilisateur dans la structure [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) .</span><span class="sxs-lookup"><span data-stu-id="8a49c-115">When the user closes the **Font** dialog box, the **ChooseFont** function returns information about the user's font selections in the [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) structure.</span></span> <span data-ttu-id="8a49c-116">Le membre **lpLogFont** de la structure **CHOOSEFONT** est un pointeur vers une structure [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) .</span><span class="sxs-lookup"><span data-stu-id="8a49c-116">The **lpLogFont** member of the **CHOOSEFONT** structure is a pointer to a [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure.</span></span>

<span data-ttu-id="8a49c-117">Utilisez le message **WM \_ CHOOSEFONT \_ GETLOGFONT** pour obtenir des informations sur les sélections de polices d’utilisateur actuelles lorsque la boîte de dialogue **police** est ouverte.</span><span class="sxs-lookup"><span data-stu-id="8a49c-117">Use the **WM\_CHOOSEFONT\_GETLOGFONT** message to get information about the user's current font selections while the **Font** dialog box is open.</span></span> <span data-ttu-id="8a49c-118">Par exemple, si vous activez le bouton **appliquer** dans la boîte de dialogue **police** , envoyez le message pour obtenir les informations de police à appliquer à la sélection de texte actuelle.</span><span class="sxs-lookup"><span data-stu-id="8a49c-118">For example, if you enable the **Apply** button in the **Font** dialog box, send the message to get the font information to apply to the current text selection.</span></span>

<span data-ttu-id="8a49c-119">En règle générale, vous activez une procédure de hook [*CFHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc) pour traiter les messages de [**\_ commande WM**](/windows/desktop/menurc/wm-command) pour le bouton **appliquer** .</span><span class="sxs-lookup"><span data-stu-id="8a49c-119">Typically, you enable a [*CFHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc) hook procedure to process [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) messages for the **Apply** button.</span></span> <span data-ttu-id="8a49c-120">Quand l’utilisateur clique sur le bouton **apply** , la procédure de hook envoie le message **WM \_ CHOOSEFONT \_ GETLOGFONT** à la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="8a49c-120">When the user clicks the **Apply** button, the hook procedure sends the **WM\_CHOOSEFONT\_GETLOGFONT** message to the dialog box.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a49c-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8a49c-121">Requirements</span></span>



| <span data-ttu-id="8a49c-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8a49c-122">Requirement</span></span> | <span data-ttu-id="8a49c-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="8a49c-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a49c-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8a49c-124">Minimum supported client</span></span><br/> | <span data-ttu-id="8a49c-125">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8a49c-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="8a49c-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8a49c-126">Minimum supported server</span></span><br/> | <span data-ttu-id="8a49c-127">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8a49c-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8a49c-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="8a49c-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="8a49c-129"><dt>Commdlg. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8a49c-129"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a49c-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8a49c-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="8a49c-131">**Référence**</span><span class="sxs-lookup"><span data-stu-id="8a49c-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="8a49c-132">**CFHookProc**</span><span class="sxs-lookup"><span data-stu-id="8a49c-132">**CFHookProc**</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc)
</dt> <dt>

[<span data-ttu-id="8a49c-133">**ChooseFont**</span><span class="sxs-lookup"><span data-stu-id="8a49c-133">**ChooseFont**</span></span>](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

[<span data-ttu-id="8a49c-134">**CHOOSEFONT**</span><span class="sxs-lookup"><span data-stu-id="8a49c-134">**CHOOSEFONT**</span></span>](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

[<span data-ttu-id="8a49c-135">**WM, \_ commande**</span><span class="sxs-lookup"><span data-stu-id="8a49c-135">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> <dt>

<span data-ttu-id="8a49c-136">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="8a49c-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="8a49c-137">Bibliothèque de boîtes de dialogue communes</span><span class="sxs-lookup"><span data-stu-id="8a49c-137">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> <dt>

<span data-ttu-id="8a49c-138">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="8a49c-138">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="8a49c-139">**LOGFONT**</span><span class="sxs-lookup"><span data-stu-id="8a49c-139">**LOGFONT**</span></span>](/windows/win32/api/wingdi/ns-wingdi-logfonta)
</dt> </dl>

 

