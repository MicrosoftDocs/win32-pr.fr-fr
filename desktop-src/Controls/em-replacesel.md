---
title: Message EM_REPLACESEL (winuser. h)
description: Remplace le texte sélectionné dans un contrôle d’édition ou un contrôle RichEdit par le texte spécifié.
ms.assetid: 525e6f5a-f52f-4bab-bc76-caa484729897
keywords:
- EM_REPLACESEL les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_REPLACESEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d9745b870a310626a6cbbbddbef118a63c64479
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106270"
---
# <a name="em_replacesel-message"></a><span data-ttu-id="c4575-104">\_Message REPLACESEL em</span><span class="sxs-lookup"><span data-stu-id="c4575-104">EM\_REPLACESEL message</span></span>

<span data-ttu-id="c4575-105">Remplace le texte sélectionné dans un contrôle d’édition ou un contrôle RichEdit par le texte spécifié.</span><span class="sxs-lookup"><span data-stu-id="c4575-105">Replaces the selected text in an edit control or a rich edit control with the specified text.</span></span>

## <a name="parameters"></a><span data-ttu-id="c4575-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c4575-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4575-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c4575-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c4575-108">Spécifie si l’opération de remplacement peut être annulée.</span><span class="sxs-lookup"><span data-stu-id="c4575-108">Specifies whether the replacement operation can be undone.</span></span> <span data-ttu-id="c4575-109">Si la **valeur est true**, l’opération peut être annulée.</span><span class="sxs-lookup"><span data-stu-id="c4575-109">If this is **TRUE**, the operation can be undone.</span></span> <span data-ttu-id="c4575-110">Si la **valeur est false** , l’opération ne peut pas être annulée.</span><span class="sxs-lookup"><span data-stu-id="c4575-110">If this is **FALSE** , the operation cannot be undone.</span></span>

</dd> <dt>

<span data-ttu-id="c4575-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c4575-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c4575-112">Pointeur vers une chaîne se terminant par un caractère null qui contient le texte de remplacement.</span><span class="sxs-lookup"><span data-stu-id="c4575-112">A pointer to a null-terminated string containing the replacement text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4575-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c4575-113">Return value</span></span>

<span data-ttu-id="c4575-114">Ce message ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="c4575-114">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c4575-115">Notes</span><span class="sxs-lookup"><span data-stu-id="c4575-115">Remarks</span></span>

<span data-ttu-id="c4575-116">Utilisez le message **em \_ REPLACESEL** pour remplacer uniquement une partie du texte dans un contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="c4575-116">Use the **EM\_REPLACESEL** message to replace only a portion of the text in an edit control.</span></span> <span data-ttu-id="c4575-117">Pour remplacer tout le texte, utilisez le message [**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext) .</span><span class="sxs-lookup"><span data-stu-id="c4575-117">To replace all of the text, use the [**WM\_SETTEXT**](/windows/desktop/winmsg/wm-settext) message.</span></span>

<span data-ttu-id="c4575-118">Si aucune sélection n’est effectuée, le texte de remplacement est inséré au niveau du signe insertion.</span><span class="sxs-lookup"><span data-stu-id="c4575-118">If there is no selection, the replacement text is inserted at the caret.</span></span>

<span data-ttu-id="c4575-119">**Modification riche :** Pris en charge dans Microsoft Rich Edit 1,0 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="c4575-119">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="c4575-120">Pour plus d’informations sur la compatibilité des versions RichEdit avec les différentes versions du système, consultez [à propos des contrôles](about-rich-edit-controls.md)RichEdit.</span><span class="sxs-lookup"><span data-stu-id="c4575-120">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

<span data-ttu-id="c4575-121">Dans un contrôle Rich Edit, le texte de remplacement prend la mise en forme du caractère au point d’insertion ou, s’il existe une sélection, du premier caractère de la sélection.</span><span class="sxs-lookup"><span data-stu-id="c4575-121">In a rich edit control, the replacement text takes the formatting of the character at the caret or, if there is a selection, of the first character in the selection.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4575-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c4575-122">Requirements</span></span>



| <span data-ttu-id="c4575-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c4575-123">Requirement</span></span> | <span data-ttu-id="c4575-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="c4575-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4575-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c4575-125">Minimum supported client</span></span><br/> | <span data-ttu-id="c4575-126">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c4575-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c4575-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c4575-127">Minimum supported server</span></span><br/> | <span data-ttu-id="c4575-128">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c4575-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c4575-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="c4575-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="c4575-130"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c4575-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4575-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c4575-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4575-132">**WM, \_ SETTEXT**</span><span class="sxs-lookup"><span data-stu-id="c4575-132">**WM\_SETTEXT**</span></span>](/windows/desktop/winmsg/wm-settext)
</dt> </dl>

 

