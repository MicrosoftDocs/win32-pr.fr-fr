---
title: Message EM_SETMODIFY (winuser. h)
description: Définit ou efface l’indicateur de modification d’un contrôle d’édition. L’indicateur de modification indique si le texte du contrôle d’édition a été modifié. Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.
ms.assetid: 9393f03e-0719-458b-8122-616df738c417
keywords:
- EM_SETMODIFY les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_SETMODIFY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 591b57dbc5441e96c1c6d3963172864713ed939f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843809"
---
# <a name="em_setmodify-message"></a><span data-ttu-id="21f43-106">\_Message SETMODIFY em</span><span class="sxs-lookup"><span data-stu-id="21f43-106">EM\_SETMODIFY message</span></span>

<span data-ttu-id="21f43-107">Définit ou efface l’indicateur de modification d’un contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="21f43-107">Sets or clears the modification flag for an edit control.</span></span> <span data-ttu-id="21f43-108">L’indicateur de modification indique si le texte du contrôle d’édition a été modifié.</span><span class="sxs-lookup"><span data-stu-id="21f43-108">The modification flag indicates whether the text within the edit control has been modified.</span></span> <span data-ttu-id="21f43-109">Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.</span><span class="sxs-lookup"><span data-stu-id="21f43-109">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="21f43-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="21f43-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21f43-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="21f43-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="21f43-112">Nouvelle valeur de l’indicateur de modification.</span><span class="sxs-lookup"><span data-stu-id="21f43-112">The new value for the modification flag.</span></span> <span data-ttu-id="21f43-113">La valeur **true** indique que le texte a été modifié et la valeur **false** indique qu’il n’a pas été modifié.</span><span class="sxs-lookup"><span data-stu-id="21f43-113">A value of **TRUE** indicates the text has been modified, and a value of **FALSE** indicates it has not been modified.</span></span>

</dd> <dt>

<span data-ttu-id="21f43-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="21f43-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="21f43-115">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="21f43-115">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21f43-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="21f43-116">Return value</span></span>

<span data-ttu-id="21f43-117">Ce message ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="21f43-117">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="21f43-118">Notes</span><span class="sxs-lookup"><span data-stu-id="21f43-118">Remarks</span></span>

<span data-ttu-id="21f43-119">Le système efface automatiquement l’indicateur de modification à zéro lorsque le contrôle est créé.</span><span class="sxs-lookup"><span data-stu-id="21f43-119">The system automatically clears the modification flag to zero when the control is created.</span></span> <span data-ttu-id="21f43-120">Si l’utilisateur modifie le texte du contrôle, le système affecte à l’indicateur une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="21f43-120">If the user changes the control's text, the system sets the flag to nonzero.</span></span> <span data-ttu-id="21f43-121">Vous pouvez envoyer le [**message \_ GETMODIFY em**](em-getmodify.md) au contrôle d’édition pour récupérer l’état actuel de l’indicateur.</span><span class="sxs-lookup"><span data-stu-id="21f43-121">You can send the [**EM\_GETMODIFY**](em-getmodify.md) message to the edit control to retrieve the current state of the flag.</span></span>

<span data-ttu-id="21f43-122">**Édition enrichie 1,0 :** Les objets créés sans l’indicateur **REO \_ Dynamics** sont verrouillés dans leurs étendues lorsque l’indicateur de modification est défini sur **false**.</span><span class="sxs-lookup"><span data-stu-id="21f43-122">**Rich Edit 1.0:** Objects created without the **REO\_DYNAMICSIZE** flag will lock in their extents when the modify flag is set to **FALSE**.</span></span>

<span data-ttu-id="21f43-123">**Modification riche :** Pris en charge dans Microsoft Rich Edit 1,0 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="21f43-123">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="21f43-124">Pour plus d’informations sur la compatibilité des versions RichEdit avec les différentes versions du système, consultez [à propos des contrôles](about-rich-edit-controls.md)RichEdit.</span><span class="sxs-lookup"><span data-stu-id="21f43-124">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="21f43-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="21f43-125">Requirements</span></span>



| <span data-ttu-id="21f43-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="21f43-126">Requirement</span></span> | <span data-ttu-id="21f43-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="21f43-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="21f43-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="21f43-128">Minimum supported client</span></span><br/> | <span data-ttu-id="21f43-129">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="21f43-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="21f43-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="21f43-130">Minimum supported server</span></span><br/> | <span data-ttu-id="21f43-131">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="21f43-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="21f43-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="21f43-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="21f43-133"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="21f43-133"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21f43-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="21f43-134">See also</span></span>

<dl> <dt>

<span data-ttu-id="21f43-135">**Référence**</span><span class="sxs-lookup"><span data-stu-id="21f43-135">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="21f43-136">**\_GETMODIFY em**</span><span class="sxs-lookup"><span data-stu-id="21f43-136">**EM\_GETMODIFY**</span></span>](em-getmodify.md)
</dt> <dt>

[<span data-ttu-id="21f43-137">**Réobjet**</span><span class="sxs-lookup"><span data-stu-id="21f43-137">**REOBJECT**</span></span>](/windows/desktop/api/Richole/ns-richole-reobject)
</dt> </dl>

 

 





