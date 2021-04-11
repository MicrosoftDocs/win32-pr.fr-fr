---
title: Message EM_GETSEL (winuser. h)
description: Obtient les positions des caractères de début et de fin (en TCHARs) de la sélection actuelle dans un contrôle d’édition. Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.
ms.assetid: cf12aaea-cfa7-4804-ae34-fd0992332288
keywords:
- EM_GETSEL les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_GETSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d28ba97c9043866c3e97c1c51389447498562455
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032800"
---
# <a name="em_getsel-message"></a><span data-ttu-id="71d65-105">\_Message GETSEL em</span><span class="sxs-lookup"><span data-stu-id="71d65-105">EM\_GETSEL message</span></span>

<span data-ttu-id="71d65-106">Obtient les positions des caractères de début et de fin (dans **TCHAR** s) de la sélection actuelle dans un contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="71d65-106">Gets the starting and ending character positions (in **TCHAR** s) of the current selection in an edit control.</span></span> <span data-ttu-id="71d65-107">Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.</span><span class="sxs-lookup"><span data-stu-id="71d65-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="71d65-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="71d65-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71d65-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="71d65-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="71d65-110">Pointeur vers une valeur **DWORD** qui reçoit la position de départ de la sélection.</span><span class="sxs-lookup"><span data-stu-id="71d65-110">A pointer to a **DWORD** value that receives the starting position of the selection.</span></span> <span data-ttu-id="71d65-111">Ce paramètre peut être **NULL**.</span><span class="sxs-lookup"><span data-stu-id="71d65-111">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="71d65-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="71d65-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="71d65-113">Pointeur vers une valeur **DWORD** qui reçoit la position du premier caractère non sélectionné après la fin de la sélection.</span><span class="sxs-lookup"><span data-stu-id="71d65-113">A pointer to a **DWORD** value that receives the position of the first unselected character after the end of the selection.</span></span> <span data-ttu-id="71d65-114">Ce paramètre peut être **NULL**.</span><span class="sxs-lookup"><span data-stu-id="71d65-114">This parameter can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71d65-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="71d65-115">Return value</span></span>

<span data-ttu-id="71d65-116">La valeur de retour est une valeur de base zéro avec la position de départ de la sélection dans le [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) et la position du premier **TCHAR** après le dernier **TCHAR** sélectionné dans le [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="71d65-116">The return value is a zero-based value with the starting position of the selection in the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) and the position of the first **TCHAR** after the last selected **TCHAR** in the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)).</span></span> <span data-ttu-id="71d65-117">Si l’une de ces valeurs dépasse 65 535, la valeur de retour est-1.</span><span class="sxs-lookup"><span data-stu-id="71d65-117">If either of these values exceeds 65,535, the return value is -1.</span></span>

<span data-ttu-id="71d65-118">Il est préférable d’utiliser les valeurs retournées dans *wParam* et *lParam* , car il s’agit de valeurs 32 bits complètes.</span><span class="sxs-lookup"><span data-stu-id="71d65-118">It is better to use the values returned in *wParam* and *lParam* because they are full 32-bit values.</span></span>

## <a name="remarks"></a><span data-ttu-id="71d65-119">Notes</span><span class="sxs-lookup"><span data-stu-id="71d65-119">Remarks</span></span>

<span data-ttu-id="71d65-120">S’il n’y a aucune sélection, les valeurs de début et de fin sont à la fois la position du signe insertion.</span><span class="sxs-lookup"><span data-stu-id="71d65-120">If there is no selection, the starting and ending values are both the position of the caret.</span></span>

<span data-ttu-id="71d65-121">**Contrôles RichEdit :** Vous pouvez également utiliser le [**message \_ EXGETSEL em**](em-exgetsel.md) pour récupérer les mêmes informations.</span><span class="sxs-lookup"><span data-stu-id="71d65-121">**Rich edit controls:** You can also use the [**EM\_EXGETSEL**](em-exgetsel.md) message to retrieve the same information.</span></span> <span data-ttu-id="71d65-122">**Em \_ EXGETSEL** retourne également les positions des caractères de début et de fin en tant que valeurs 32 bits.</span><span class="sxs-lookup"><span data-stu-id="71d65-122">**EM\_EXGETSEL** also returns starting and ending character positions as 32-bit values.</span></span>

<span data-ttu-id="71d65-123">**Modification riche :** Pris en charge dans Microsoft Rich Edit 1,0 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="71d65-123">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="71d65-124">Pour plus d’informations sur la compatibilité des versions RichEdit avec les différentes versions du système, consultez [à propos des contrôles](about-rich-edit-controls.md)RichEdit.</span><span class="sxs-lookup"><span data-stu-id="71d65-124">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="71d65-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="71d65-125">Requirements</span></span>



| <span data-ttu-id="71d65-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="71d65-126">Requirement</span></span> | <span data-ttu-id="71d65-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="71d65-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71d65-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="71d65-128">Minimum supported client</span></span><br/> | <span data-ttu-id="71d65-129">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="71d65-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="71d65-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="71d65-130">Minimum supported server</span></span><br/> | <span data-ttu-id="71d65-131">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="71d65-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="71d65-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="71d65-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="71d65-133"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="71d65-133"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71d65-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="71d65-134">See also</span></span>

<dl> <dt>

<span data-ttu-id="71d65-135">**Référence**</span><span class="sxs-lookup"><span data-stu-id="71d65-135">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="71d65-136">**\_EXGETSEL em**</span><span class="sxs-lookup"><span data-stu-id="71d65-136">**EM\_EXGETSEL**</span></span>](em-exgetsel.md)
</dt> <dt>

[<span data-ttu-id="71d65-137">**\_SETSEL em**</span><span class="sxs-lookup"><span data-stu-id="71d65-137">**EM\_SETSEL**</span></span>](em-setsel.md)
</dt> </dl>

 

