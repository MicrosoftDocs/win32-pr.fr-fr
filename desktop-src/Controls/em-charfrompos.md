---
title: Message EM_CHARFROMPOS (winuser. h)
description: Obtient des informations sur le caractère le plus proche d’un point spécifié dans la zone cliente d’un contrôle d’édition. Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.
ms.assetid: fe9f96f2-5b3c-4039-befd-5e9a456ba32d
keywords:
- EM_CHARFROMPOS les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_CHARFROMPOS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1156d69c012faa0141726c00ab880d954fe2857
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465902"
---
# <a name="em_charfrompos-message"></a><span data-ttu-id="fc97a-105">\_Message CHARFROMPOS em</span><span class="sxs-lookup"><span data-stu-id="fc97a-105">EM\_CHARFROMPOS message</span></span>

<span data-ttu-id="fc97a-106">Obtient des informations sur le caractère le plus proche d’un point spécifié dans la zone cliente d’un contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="fc97a-106">Gets information about the character closest to a specified point in the client area of an edit control.</span></span> <span data-ttu-id="fc97a-107">Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.</span><span class="sxs-lookup"><span data-stu-id="fc97a-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="fc97a-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fc97a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc97a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fc97a-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fc97a-110">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="fc97a-110">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="fc97a-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fc97a-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fc97a-112">Coordonnées d’un point dans la zone cliente du contrôle.</span><span class="sxs-lookup"><span data-stu-id="fc97a-112">The coordinates of a point in the control's client area.</span></span> <span data-ttu-id="fc97a-113">Les coordonnées sont exprimées en unités d’écran et sont relatives au coin supérieur gauche de la zone cliente du contrôle.</span><span class="sxs-lookup"><span data-stu-id="fc97a-113">The coordinates are in screen units and are relative to the upper-left corner of the control's client area.</span></span>

<span data-ttu-id="fc97a-114">**Contrôles RichEdit :** Pointeur vers une structure de [**pointeurs**](/previous-versions//dd162807(v=vs.85)) qui contient les coordonnées horizontales et verticales.</span><span class="sxs-lookup"><span data-stu-id="fc97a-114">**Rich edit controls:** A pointer to a [**POINTL**](/previous-versions//dd162807(v=vs.85)) structure that contains the horizontal and vertical coordinates.</span></span>

<span data-ttu-id="fc97a-115">**Contrôles d’édition :** [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contient la coordonnée horizontale.</span><span class="sxs-lookup"><span data-stu-id="fc97a-115">**Edit controls:** The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the horizontal coordinate.</span></span> <span data-ttu-id="fc97a-116">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) contient la coordonnée verticale.</span><span class="sxs-lookup"><span data-stu-id="fc97a-116">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) contains the vertical coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc97a-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fc97a-117">Return value</span></span>

<span data-ttu-id="fc97a-118">**Contrôles RichEdit :** La valeur de retour spécifie l’index de caractère de base zéro du caractère le plus proche du point spécifié.</span><span class="sxs-lookup"><span data-stu-id="fc97a-118">**Rich edit controls:** The return value specifies the zero-based character index of the character nearest the specified point.</span></span> <span data-ttu-id="fc97a-119">La valeur de retour indique le dernier caractère dans le contrôle d’édition si le point spécifié est au-delà du dernier caractère dans le contrôle.</span><span class="sxs-lookup"><span data-stu-id="fc97a-119">The return value indicates the last character in the edit control if the specified point is beyond the last character in the control.</span></span>

<span data-ttu-id="fc97a-120">**Contrôles d’édition :** [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) spécifie l’index de base zéro du caractère le plus proche du point spécifié.</span><span class="sxs-lookup"><span data-stu-id="fc97a-120">**Edit controls:** The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the zero-based index of the character nearest the specified point.</span></span> <span data-ttu-id="fc97a-121">Cet index est relatif au début du contrôle, et non au début de la ligne.</span><span class="sxs-lookup"><span data-stu-id="fc97a-121">This index is relative to the beginning of the control, not the beginning of the line.</span></span> <span data-ttu-id="fc97a-122">Si le point spécifié est au-delà du dernier caractère du contrôle d’édition, la valeur de retour indique le dernier caractère dans le contrôle.</span><span class="sxs-lookup"><span data-stu-id="fc97a-122">If the specified point is beyond the last character in the edit control, the return value indicates the last character in the control.</span></span> <span data-ttu-id="fc97a-123">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) spécifie l’index de base zéro de la ligne qui contient le caractère.</span><span class="sxs-lookup"><span data-stu-id="fc97a-123">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the zero-based index of the line that contains the character.</span></span> <span data-ttu-id="fc97a-124">Pour les contrôles d’édition sur une seule ligne, cette valeur est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="fc97a-124">For single-line edit controls, this value is zero.</span></span> <span data-ttu-id="fc97a-125">L’index indique le séparateur de lignes si le point spécifié est au-delà du dernier caractère visible d’une ligne.</span><span class="sxs-lookup"><span data-stu-id="fc97a-125">The index indicates the line delimiter if the specified point is beyond the last visible character in a line.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc97a-126">Notes</span><span class="sxs-lookup"><span data-stu-id="fc97a-126">Remarks</span></span>

<span data-ttu-id="fc97a-127">**Modification riche :** Pris en charge dans Microsoft Rich Edit 1,0 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="fc97a-127">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="fc97a-128">Pour plus d’informations sur la compatibilité des versions RichEdit avec les différentes versions du système, consultez [à propos des contrôles](about-rich-edit-controls.md)RichEdit.</span><span class="sxs-lookup"><span data-stu-id="fc97a-128">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

<span data-ttu-id="fc97a-129">Si un point est passé à **em \_ CHARFROMPOS** comme *lParam* et que le point se trouve en dehors des limites du contrôle d’édition, la *LRESULT* est (65535, 65535).</span><span class="sxs-lookup"><span data-stu-id="fc97a-129">If a point is passed to **EM\_CHARFROMPOS** as the *lParam* and the point is outside the bounds of the edit control, then the *lResult* is (65535, 65535).</span></span>

## <a name="requirements"></a><span data-ttu-id="fc97a-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fc97a-130">Requirements</span></span>



| <span data-ttu-id="fc97a-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fc97a-131">Requirement</span></span> | <span data-ttu-id="fc97a-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="fc97a-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc97a-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fc97a-133">Minimum supported client</span></span><br/> | <span data-ttu-id="fc97a-134">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fc97a-134">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="fc97a-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fc97a-135">Minimum supported server</span></span><br/> | <span data-ttu-id="fc97a-136">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fc97a-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="fc97a-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="fc97a-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="fc97a-138"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fc97a-138"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc97a-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fc97a-139">See also</span></span>

<dl> <dt>

<span data-ttu-id="fc97a-140">**Référence**</span><span class="sxs-lookup"><span data-stu-id="fc97a-140">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="fc97a-141">**\_POSFROMCHAR em**</span><span class="sxs-lookup"><span data-stu-id="fc97a-141">**EM\_POSFROMCHAR**</span></span>](em-posfromchar.md)
</dt> <dt>

<span data-ttu-id="fc97a-142">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="fc97a-142">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="fc97a-143">**MAKELPARAM**</span><span class="sxs-lookup"><span data-stu-id="fc97a-143">**MAKELPARAM**</span></span>](/windows/desktop/api/winuser/nf-winuser-makelparam)
</dt> <dt>

<span data-ttu-id="fc97a-144">[**POINTer**](/previous-versions//dd162807(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fc97a-144">[**POINTL**](/previous-versions//dd162807(v=vs.85))</span></span>
</dt> </dl>

 

