---
title: Message EM_GETLINECOUNT (winuser. h)
description: Obtient le nombre de lignes dans un contrôle d’édition multiligne. Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.
ms.assetid: 9fe63c10-7395-4f98-a672-14960a70d14f
keywords:
- EM_GETLINECOUNT les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_GETLINECOUNT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15ffbeafb13850317faccb4be44571d81b0d7e36
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464543"
---
# <a name="em_getlinecount-message-winuserh"></a><span data-ttu-id="9fccc-105">Message EM_GETLINECOUNT (winuser. h)</span><span class="sxs-lookup"><span data-stu-id="9fccc-105">EM_GETLINECOUNT message (Winuser.h)</span></span>

<span data-ttu-id="9fccc-106">Obtient le nombre de lignes dans un contrôle d’édition multiligne.</span><span class="sxs-lookup"><span data-stu-id="9fccc-106">Gets the number of lines in a multiline edit control.</span></span> <span data-ttu-id="9fccc-107">Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.</span><span class="sxs-lookup"><span data-stu-id="9fccc-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="9fccc-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9fccc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9fccc-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9fccc-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9fccc-110">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="9fccc-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="9fccc-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9fccc-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9fccc-112">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="9fccc-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9fccc-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9fccc-113">Return value</span></span>

<span data-ttu-id="9fccc-114">La valeur de retour est un entier spécifiant le nombre total de lignes de texte dans le contrôle d’édition multiligne ou le contrôle Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="9fccc-114">The return value is an integer specifying the total number of text lines in the multiline edit control or rich edit control.</span></span> <span data-ttu-id="9fccc-115">Si le contrôle n’a pas de texte, la valeur de retour est 1.</span><span class="sxs-lookup"><span data-stu-id="9fccc-115">If the control has no text, the return value is 1.</span></span> <span data-ttu-id="9fccc-116">La valeur de retour ne sera jamais inférieure à 1.</span><span class="sxs-lookup"><span data-stu-id="9fccc-116">The return value will never be less than 1.</span></span>

## <a name="remarks"></a><span data-ttu-id="9fccc-117">Notes</span><span class="sxs-lookup"><span data-stu-id="9fccc-117">Remarks</span></span>

<span data-ttu-id="9fccc-118">Le message **em \_ GETLINECOUNT** récupère le nombre total de lignes de texte, pas seulement le nombre de lignes actuellement visibles.</span><span class="sxs-lookup"><span data-stu-id="9fccc-118">The **EM\_GETLINECOUNT** message retrieves the total number of text lines, not just the number of lines that are currently visible.</span></span>

<span data-ttu-id="9fccc-119">Si la fonctionnalité de retour automatique à la ligne est activée, le nombre de lignes peut changer lorsque les dimensions de la fenêtre d’édition changent.</span><span class="sxs-lookup"><span data-stu-id="9fccc-119">If the Wordwrap feature is enabled, the number of lines can change when the dimensions of the editing window change.</span></span>

<span data-ttu-id="9fccc-120">**Modification riche :** Pris en charge dans Microsoft Rich Edit 1,0 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="9fccc-120">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="9fccc-121">Pour plus d’informations sur la compatibilité des versions RichEdit avec les différentes versions du système, consultez [à propos des contrôles](about-rich-edit-controls.md)RichEdit.</span><span class="sxs-lookup"><span data-stu-id="9fccc-121">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9fccc-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9fccc-122">Requirements</span></span>



| <span data-ttu-id="9fccc-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9fccc-123">Requirement</span></span> | <span data-ttu-id="9fccc-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="9fccc-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9fccc-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9fccc-125">Minimum supported client</span></span><br/> | <span data-ttu-id="9fccc-126">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9fccc-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="9fccc-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9fccc-127">Minimum supported server</span></span><br/> | <span data-ttu-id="9fccc-128">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9fccc-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9fccc-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="9fccc-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="9fccc-130"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9fccc-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9fccc-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9fccc-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="9fccc-132">**Référence**</span><span class="sxs-lookup"><span data-stu-id="9fccc-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="9fccc-133">**\_GETLINE em**</span><span class="sxs-lookup"><span data-stu-id="9fccc-133">**EM\_GETLINE**</span></span>](em-getline.md)
</dt> <dt>

[<span data-ttu-id="9fccc-134">**\_LINELENGTH em**</span><span class="sxs-lookup"><span data-stu-id="9fccc-134">**EM\_LINELENGTH**</span></span>](em-linelength.md)
</dt> <dt>

[<span data-ttu-id="9fccc-135">**Modifier \_ GetLineCount**</span><span class="sxs-lookup"><span data-stu-id="9fccc-135">**Edit\_GetLineCount**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_getlinecount)
</dt> </dl>

 

 





