---
title: Message EM_GETMODIFY (winuser. h)
description: Obtient l’état de l’indicateur de modification d’un contrôle d’édition. L’indicateur indique si le contenu du contrôle d’édition a été modifié. Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.
ms.assetid: 4229e2f2-3493-4721-8b52-8933c9dc0a77
keywords:
- EM_GETMODIFY les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_GETMODIFY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f8c525df061717255051c49abaa3bda88f317b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843205"
---
# <a name="em_getmodify-message"></a><span data-ttu-id="979ed-106">\_Message GETMODIFY em</span><span class="sxs-lookup"><span data-stu-id="979ed-106">EM\_GETMODIFY message</span></span>

<span data-ttu-id="979ed-107">Obtient l’état de l’indicateur de modification d’un contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="979ed-107">Gets the state of an edit control's modification flag.</span></span> <span data-ttu-id="979ed-108">L’indicateur indique si le contenu du contrôle d’édition a été modifié.</span><span class="sxs-lookup"><span data-stu-id="979ed-108">The flag indicates whether the contents of the edit control have been modified.</span></span> <span data-ttu-id="979ed-109">Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.</span><span class="sxs-lookup"><span data-stu-id="979ed-109">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="979ed-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="979ed-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="979ed-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="979ed-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="979ed-112">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="979ed-112">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="979ed-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="979ed-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="979ed-114">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="979ed-114">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="979ed-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="979ed-115">Return value</span></span>

<span data-ttu-id="979ed-116">Si le contenu du contrôle d’édition a été modifié, la valeur de retour est différente de zéro ; dans le cas contraire, il est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="979ed-116">If the contents of edit control have been modified, the return value is nonzero; otherwise, it is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="979ed-117">Notes</span><span class="sxs-lookup"><span data-stu-id="979ed-117">Remarks</span></span>

<span data-ttu-id="979ed-118">Le système efface automatiquement l’indicateur de modification à zéro lorsque le contrôle est créé.</span><span class="sxs-lookup"><span data-stu-id="979ed-118">The system automatically clears the modification flag to zero when the control is created.</span></span> <span data-ttu-id="979ed-119">Si l’utilisateur modifie le texte du contrôle, le système affecte à l’indicateur une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="979ed-119">If the user changes the control's text, the system sets the flag to nonzero.</span></span> <span data-ttu-id="979ed-120">Vous pouvez envoyer le [**message \_ SETMODIFY em**](em-setmodify.md) au contrôle Edit pour définir ou supprimer l’indicateur.</span><span class="sxs-lookup"><span data-stu-id="979ed-120">You can send the [**EM\_SETMODIFY**](em-setmodify.md) message to the edit control to set or clear the flag.</span></span>

<span data-ttu-id="979ed-121">**Modification riche :** Pris en charge dans Microsoft Rich Edit 1,0 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="979ed-121">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="979ed-122">Pour plus d’informations sur la compatibilité des versions RichEdit avec les différentes versions du système, consultez [à propos des contrôles](about-rich-edit-controls.md)RichEdit.</span><span class="sxs-lookup"><span data-stu-id="979ed-122">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="979ed-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="979ed-123">Requirements</span></span>



| <span data-ttu-id="979ed-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="979ed-124">Requirement</span></span> | <span data-ttu-id="979ed-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="979ed-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="979ed-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="979ed-126">Minimum supported client</span></span><br/> | <span data-ttu-id="979ed-127">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="979ed-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="979ed-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="979ed-128">Minimum supported server</span></span><br/> | <span data-ttu-id="979ed-129">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="979ed-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="979ed-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="979ed-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="979ed-131"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="979ed-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="979ed-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="979ed-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="979ed-133">**\_SETMODIFY em**</span><span class="sxs-lookup"><span data-stu-id="979ed-133">**EM\_SETMODIFY**</span></span>](em-setmodify.md)
</dt> </dl>

 

 





