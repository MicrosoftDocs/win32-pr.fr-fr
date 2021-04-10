---
title: Message EM_SETREADONLY (winuser. h)
description: Définit ou supprime le style en lecture seule (ES \_ ReadOnly) d’un contrôle d’édition. Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.
ms.assetid: a10b3f57-0e67-4a0f-89f3-9c8ebd1514f8
keywords:
- EM_SETREADONLY les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_SETREADONLY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0b224e11212077703ab62ab6a180875672c879e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103553"
---
# <a name="em_setreadonly-message"></a><span data-ttu-id="ad195-105">\_Message SETREADONLY em</span><span class="sxs-lookup"><span data-stu-id="ad195-105">EM\_SETREADONLY message</span></span>

<span data-ttu-id="ad195-106">Définit ou supprime le style en lecture seule ([**es \_ ReadOnly**](edit-control-styles.md)) d’un contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="ad195-106">Sets or removes the read-only style ([**ES\_READONLY**](edit-control-styles.md)) of an edit control.</span></span> <span data-ttu-id="ad195-107">Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.</span><span class="sxs-lookup"><span data-stu-id="ad195-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="ad195-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ad195-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad195-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ad195-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ad195-110">Spécifie s’il faut définir ou supprimer le style [**es \_ ReadOnly**](edit-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="ad195-110">Specifies whether to set or remove the [**ES\_READONLY**](edit-control-styles.md) style.</span></span> <span data-ttu-id="ad195-111">La valeur **true** définit le style **es \_ ReadOnly** ; la valeur **false** supprime le style **es \_ ReadOnly** .</span><span class="sxs-lookup"><span data-stu-id="ad195-111">A value of **TRUE** sets the **ES\_READONLY** style; a value of **FALSE** removes the **ES\_READONLY** style.</span></span>

</dd> <dt>

<span data-ttu-id="ad195-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ad195-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ad195-113">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="ad195-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad195-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ad195-114">Return value</span></span>

<span data-ttu-id="ad195-115">Si l’opération a échoué, la valeur de retour est différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="ad195-115">If the operation succeeds, the return value is nonzero.</span></span>

<span data-ttu-id="ad195-116">Si l’opération échoue, la valeur de retour est zéro.</span><span class="sxs-lookup"><span data-stu-id="ad195-116">If the operation fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad195-117">Notes</span><span class="sxs-lookup"><span data-stu-id="ad195-117">Remarks</span></span>

<span data-ttu-id="ad195-118">Lorsqu’un contrôle d’édition a le style [**es \_ ReadOnly**](edit-control-styles.md) , l’utilisateur ne peut pas modifier le texte dans le contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="ad195-118">When an edit control has the [**ES\_READONLY**](edit-control-styles.md) style, the user cannot change the text within the edit control.</span></span>

<span data-ttu-id="ad195-119">Pour déterminer si un contrôle d’édition a le style [**es \_ ReadOnly**](edit-control-styles.md) , utilisez la fonction [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) avec l' \_ indicateur de style GWL.</span><span class="sxs-lookup"><span data-stu-id="ad195-119">To determine whether an edit control has the [**ES\_READONLY**](edit-control-styles.md) style, use the [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) function with the GWL\_STYLE flag.</span></span>

<span data-ttu-id="ad195-120">**Modification riche :** Pris en charge dans Microsoft Rich Edit 1,0 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="ad195-120">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="ad195-121">Pour plus d’informations sur la compatibilité des versions RichEdit avec les différentes versions du système, consultez [à propos des contrôles](about-rich-edit-controls.md)RichEdit.</span><span class="sxs-lookup"><span data-stu-id="ad195-121">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ad195-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ad195-122">Requirements</span></span>



| <span data-ttu-id="ad195-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ad195-123">Requirement</span></span> | <span data-ttu-id="ad195-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="ad195-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad195-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ad195-125">Minimum supported client</span></span><br/> | <span data-ttu-id="ad195-126">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ad195-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ad195-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ad195-127">Minimum supported server</span></span><br/> | <span data-ttu-id="ad195-128">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ad195-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ad195-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="ad195-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="ad195-130"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ad195-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad195-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ad195-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad195-132">**GetWindowLong**</span><span class="sxs-lookup"><span data-stu-id="ad195-132">**GetWindowLong**</span></span>](/windows/desktop/api/winuser/nf-winuser-getwindowlonga)
</dt> </dl>

 

