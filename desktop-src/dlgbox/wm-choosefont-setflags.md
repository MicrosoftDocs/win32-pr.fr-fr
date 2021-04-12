---
title: Message d’WM_CHOOSEFONT_SETFLAGS (COMMDLG. h)
description: Une application envoie le \_ message WM CHOOSEFONT \_ SETFLAGS à une boîte de dialogue de police pour définir les options d’affichage de la boîte de dialogue.
ms.assetid: 945ebc07-440d-4466-8255-ad344bdc568a
keywords:
- Boîtes de dialogue de WM_CHOOSEFONT_SETFLAGS message
topic_type:
- apiref
api_name:
- WM_CHOOSEFONT_SETFLAGS
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f7abf436311f8a3868b1471c2a10a7ee2e4a3b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104881"
---
# <a name="wm_choosefont_setflags-message"></a><span data-ttu-id="6524d-104">\_ \_ Message SETFLAGS WM CHOOSEFONT</span><span class="sxs-lookup"><span data-stu-id="6524d-104">WM\_CHOOSEFONT\_SETFLAGS message</span></span>

<span data-ttu-id="6524d-105">Une application envoie le message **WM \_ CHOOSEFONT \_ SETFLAGS** à une boîte de dialogue de **police** pour définir les options d’affichage de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="6524d-105">An application sends the **WM\_CHOOSEFONT\_SETFLAGS** message to a **Font** dialog box to set the display options for the dialog box.</span></span>


```C++
#define WM_USER                        0x0400
#define WM_CHOOSEFONT_SETFLAGS        (WM_USER + 102)
```



## <a name="parameters"></a><span data-ttu-id="6524d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6524d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6524d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6524d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6524d-108">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="6524d-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="6524d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6524d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6524d-110">Pointeur vers une structure [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) qui contient de nouveaux paramètres dans le membre **Flags** .</span><span class="sxs-lookup"><span data-stu-id="6524d-110">A pointer to a [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) structure that contains new settings in the **Flags** member.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6524d-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6524d-111">Return value</span></span>

<span data-ttu-id="6524d-112">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="6524d-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6524d-113">Notes</span><span class="sxs-lookup"><span data-stu-id="6524d-113">Remarks</span></span>

<span data-ttu-id="6524d-114">La fonction [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) crée une boîte de dialogue de **police** et utilise une structure [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) pour spécifier les valeurs initiales du membre **Flags** .</span><span class="sxs-lookup"><span data-stu-id="6524d-114">The [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) function creates a **Font** dialog box and uses a [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) structure to specify the initial values for the **Flags** member.</span></span> <span data-ttu-id="6524d-115">Utilisez le **message \_ \_ SETFLAGS WM CHOOSEFONT** pour spécifier des valeurs différentes pour le membre **Flags** lorsque la boîte de dialogue **police** est ouverte.</span><span class="sxs-lookup"><span data-stu-id="6524d-115">Use the **WM\_CHOOSEFONT\_SETFLAGS** message to specify different values for the **Flags** member while the **Font** dialog box is open.</span></span>

<span data-ttu-id="6524d-116">En règle générale, vous devez envoyer le message **WM \_ CHOOSEFONT \_ SETFLAGS** à partir d’une procédure de hook [**CFHookProc**](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc) .</span><span class="sxs-lookup"><span data-stu-id="6524d-116">Typically, you should send the **WM\_CHOOSEFONT\_SETFLAGS** message from a [**CFHookProc**](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc) hook procedure.</span></span>

## <a name="requirements"></a><span data-ttu-id="6524d-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6524d-117">Requirements</span></span>



| <span data-ttu-id="6524d-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6524d-118">Requirement</span></span> | <span data-ttu-id="6524d-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="6524d-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6524d-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6524d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6524d-121">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6524d-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="6524d-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6524d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6524d-123">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6524d-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6524d-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="6524d-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="6524d-125"><dt>Commdlg. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6524d-125"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6524d-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6524d-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="6524d-127">**Référence**</span><span class="sxs-lookup"><span data-stu-id="6524d-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="6524d-128">**CFHookProc**</span><span class="sxs-lookup"><span data-stu-id="6524d-128">**CFHookProc**</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc)
</dt> <dt>

[<span data-ttu-id="6524d-129">**ChooseFont**</span><span class="sxs-lookup"><span data-stu-id="6524d-129">**ChooseFont**</span></span>](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

[<span data-ttu-id="6524d-130">**CHOOSEFONT**</span><span class="sxs-lookup"><span data-stu-id="6524d-130">**CHOOSEFONT**</span></span>](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

<span data-ttu-id="6524d-131">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="6524d-131">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="6524d-132">Bibliothèque de boîtes de dialogue communes</span><span class="sxs-lookup"><span data-stu-id="6524d-132">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

