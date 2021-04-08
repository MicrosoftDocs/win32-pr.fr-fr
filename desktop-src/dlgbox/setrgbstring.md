---
title: Message SETRGBSTRING (COMMDLG. h)
description: La procédure de raccordement d’une boîte de dialogue de couleur, CCHookProc, peut envoyer le message SETRGBSTRING Registered à la boîte de dialogue pour définir la sélection de couleur actuelle.
ms.assetid: 02d36248-be75-4552-853f-6ac3ec034ebe
keywords:
- Boîtes de dialogue de message SETRGBSTRING
topic_type:
- apiref
api_name:
- SETRGBSTRING
- SETRGBSTRINGA
- SETRGBSTRINGW
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dea5489aaa6fafcaa19a97a44d81fd85abb178d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742588"
---
# <a name="setrgbstring-message"></a><span data-ttu-id="54fdf-104">Message SETRGBSTRING</span><span class="sxs-lookup"><span data-stu-id="54fdf-104">SETRGBSTRING message</span></span>

<span data-ttu-id="54fdf-105">La procédure de raccordement d’une boîte de dialogue de **couleur** , [*CCHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpcchookproc), peut envoyer le message **SETRGBSTRING** Registered à la boîte de dialogue pour définir la sélection de couleur actuelle.</span><span class="sxs-lookup"><span data-stu-id="54fdf-105">The hook procedure of a **Color** dialog box, [*CCHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpcchookproc), can send the **SETRGBSTRING** registered message to the dialog box to set the current color selection.</span></span>


```C++
#define SETRGBSTRING TEXT("commdlg_SetRGBColor")
```



## <a name="parameters"></a><span data-ttu-id="54fdf-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="54fdf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54fdf-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="54fdf-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="54fdf-108">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="54fdf-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="54fdf-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="54fdf-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="54fdf-110">Valeur RVB de la couleur à sélectionner dans la boîte de dialogue **couleur** .</span><span class="sxs-lookup"><span data-stu-id="54fdf-110">The RGB value of the color to select in the **Color** dialog box.</span></span> <span data-ttu-id="54fdf-111">Vous pouvez utiliser la macro [**RGB**](/windows/desktop/api/wingdi/nf-wingdi-rgb) pour spécifier les intensités rouge, verte et bleue d’une valeur de couleur RVB.</span><span class="sxs-lookup"><span data-stu-id="54fdf-111">You can use the [**RGB**](/windows/desktop/api/wingdi/nf-wingdi-rgb) macro to specify the red, green, and blue intensities of an RGB color value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54fdf-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="54fdf-112">Return value</span></span>

<span data-ttu-id="54fdf-113">Ce message n’a pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="54fdf-113">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="54fdf-114">Notes</span><span class="sxs-lookup"><span data-stu-id="54fdf-114">Remarks</span></span>

<span data-ttu-id="54fdf-115">Si *lParam* correspond à l’une des couleurs de base ou à l’une des 16 couleurs personnalisées, la procédure de la boîte de dialogue sélectionne cette couleur.</span><span class="sxs-lookup"><span data-stu-id="54fdf-115">If *lParam* matches one of the basic colors or one of the 16 custom colors, the dialog box procedure selects that color.</span></span> <span data-ttu-id="54fdf-116">La procédure de boîte de dialogue met également à jour tous les contrôles dans l’extension de couleur personnalisée de la boîte de dialogue **couleur** , s’il est ouvert.</span><span class="sxs-lookup"><span data-stu-id="54fdf-116">The dialog box procedure also updates all the controls in the custom color extension of the **Color** dialog box, if it is open.</span></span>

<span data-ttu-id="54fdf-117">Si *lParam* ne correspond pas à une couleur de base ou personnalisée, la procédure de boîte de dialogue ne change pas la sélection de couleur actuelle, mais elle met à jour les contrôles de couleur personnalisés, s’ils sont visibles.</span><span class="sxs-lookup"><span data-stu-id="54fdf-117">If *lParam* does not match a basic or custom color, the dialog box procedure does not change the current color selection, but it does update the custom color controls, if they are visible.</span></span>

## <a name="examples"></a><span data-ttu-id="54fdf-118">Exemples</span><span class="sxs-lookup"><span data-stu-id="54fdf-118">Examples</span></span>

<span data-ttu-id="54fdf-119">L’exemple de code suivant obtient l’identificateur de message **SETRGBSTRING** , puis définit la sélection de couleur sur bleu.</span><span class="sxs-lookup"><span data-stu-id="54fdf-119">The following sample code gets the **SETRGBSTRING** message identifier and then sets the color selection to blue.</span></span>


```
UINT uiSetRGB;

uiSetRGB = RegisterWindowMessage(SETRGBSTRING);

SendMessage(hdlg, uiSetRGB, 0, (LPARAM) RGB(0, 0, 255)); 
```



## <a name="requirements"></a><span data-ttu-id="54fdf-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="54fdf-120">Requirements</span></span>



| <span data-ttu-id="54fdf-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="54fdf-121">Requirement</span></span> | <span data-ttu-id="54fdf-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="54fdf-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54fdf-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="54fdf-123">Minimum supported client</span></span><br/> | <span data-ttu-id="54fdf-124">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="54fdf-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="54fdf-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="54fdf-125">Minimum supported server</span></span><br/> | <span data-ttu-id="54fdf-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="54fdf-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="54fdf-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="54fdf-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="54fdf-128"><dt>Commdlg. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="54fdf-128"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="54fdf-129">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="54fdf-129">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="54fdf-130">**SETRGBSTRINGW** (Unicode) et **SETRGBSTRINGA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="54fdf-130">**SETRGBSTRINGW** (Unicode) and **SETRGBSTRINGA** (ANSI)</span></span><br/>                                      |



## <a name="see-also"></a><span data-ttu-id="54fdf-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="54fdf-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="54fdf-132">**Référence**</span><span class="sxs-lookup"><span data-stu-id="54fdf-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="54fdf-133">**RegisterWindowMessage**</span><span class="sxs-lookup"><span data-stu-id="54fdf-133">**RegisterWindowMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

[<span data-ttu-id="54fdf-134">**RGB**</span><span class="sxs-lookup"><span data-stu-id="54fdf-134">**RGB**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-rgb)
</dt> <dt>

[<span data-ttu-id="54fdf-135">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="54fdf-135">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

<span data-ttu-id="54fdf-136">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="54fdf-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="54fdf-137">Bibliothèque de boîtes de dialogue communes</span><span class="sxs-lookup"><span data-stu-id="54fdf-137">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

