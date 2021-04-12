---
title: Message EM_POSFROMCHAR (winuser. h)
description: Récupère les coordonnées de la zone cliente d’un caractère spécifié dans un contrôle d’édition. Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.
ms.assetid: a32532fa-976f-4c19-ac6e-29e5614fc410
keywords:
- EM_POSFROMCHAR les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_POSFROMCHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d98968873ad006b2e91cf3add2429bf7630fae1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508710"
---
# <a name="em_posfromchar-message"></a><span data-ttu-id="91143-105">\_Message POSFROMCHAR em</span><span class="sxs-lookup"><span data-stu-id="91143-105">EM\_POSFROMCHAR message</span></span>

<span data-ttu-id="91143-106">Récupère les coordonnées de la zone cliente d’un caractère spécifié dans un contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="91143-106">Retrieves the client area coordinates of a specified character in an edit control.</span></span> <span data-ttu-id="91143-107">Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.</span><span class="sxs-lookup"><span data-stu-id="91143-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="91143-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="91143-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91143-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="91143-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="91143-110">**Édition enrichie 1,0 et 3,0 :** Pointeur vers une structure [**pointer**](/previous-versions//dd162807(v=vs.85)) qui reçoit les coordonnées de la zone cliente du caractère.</span><span class="sxs-lookup"><span data-stu-id="91143-110">**Rich Edit 1.0 and 3.0:** A pointer to a [**POINTL**](/previous-versions//dd162807(v=vs.85)) structure that receives the client area coordinates of the character.</span></span> <span data-ttu-id="91143-111">Les coordonnées sont exprimées en unités d’écran et sont relatives au coin supérieur gauche de la zone cliente du contrôle.</span><span class="sxs-lookup"><span data-stu-id="91143-111">The coordinates are in screen units and are relative to the upper-left corner of the control's client area.</span></span>

<span data-ttu-id="91143-112">**Edit Controls et Rich edit 2,0 :** Index de base zéro du caractère.</span><span class="sxs-lookup"><span data-stu-id="91143-112">**Edit controls and Rich Edit 2.0:** The zero-based index of the character.</span></span>

</dd> <dt>

<span data-ttu-id="91143-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="91143-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="91143-114">**Édition enrichie 1,0 et 3,0 :** Index de base zéro du caractère.</span><span class="sxs-lookup"><span data-stu-id="91143-114">**Rich Edit 1.0 and 3.0:** The zero-based index of the character.</span></span>

<span data-ttu-id="91143-115">**Edit Controls et Rich edit 2,0 :** Ce paramètre n’est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="91143-115">**Edit controls and Rich Edit 2.0:** This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91143-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="91143-116">Return value</span></span>

<span data-ttu-id="91143-117">**Édition enrichie 1,0 et 3,0 :** La valeur de retour n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="91143-117">**Rich Edit 1.0 and 3.0:** The return value is not used.</span></span>

<span data-ttu-id="91143-118">**Edit Controls et Rich edit 2,0 :** La valeur de retour contient les coordonnées de la zone cliente du caractère.</span><span class="sxs-lookup"><span data-stu-id="91143-118">**Edit controls and Rich Edit 2.0:** The return value contains the client area coordinates of the character.</span></span> <span data-ttu-id="91143-119">Le [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contient la coordonnée horizontale et le [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) contient la coordonnée verticale.</span><span class="sxs-lookup"><span data-stu-id="91143-119">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the horizontal coordinate and the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) contains the vertical coordinate.</span></span>

## <a name="remarks"></a><span data-ttu-id="91143-120">Notes</span><span class="sxs-lookup"><span data-stu-id="91143-120">Remarks</span></span>

<span data-ttu-id="91143-121">Une coordonnée retournée peut être une valeur négative si le caractère spécifié n’est pas affiché dans la zone cliente du contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="91143-121">A returned coordinate can be a negative value if the specified character is not displayed in the edit control's client area.</span></span> <span data-ttu-id="91143-122">Les coordonnées sont tronquées en valeurs entières.</span><span class="sxs-lookup"><span data-stu-id="91143-122">The coordinates are truncated to integer values.</span></span>

<span data-ttu-id="91143-123">Si le caractère est un délimiteur de ligne, les coordonnées retournées indiquent un point situé juste après le dernier caractère visible dans la ligne.</span><span class="sxs-lookup"><span data-stu-id="91143-123">If the character is a line delimiter, the returned coordinates indicate a point just beyond the last visible character in the line.</span></span> <span data-ttu-id="91143-124">Si l’index spécifié est supérieur à l’index du dernier caractère du contrôle, le contrôle retourne-1.</span><span class="sxs-lookup"><span data-stu-id="91143-124">If the specified index is greater than the index of the last character in the control, the control returns -1.</span></span>

<span data-ttu-id="91143-125">**Édition enrichie 3,0 et versions ultérieures :** Pour la compatibilité descendante, Microsoft Rich Edit 3,0 prend en charge la syntaxe utilisée par Microsoft Rich Edit 2,0.</span><span class="sxs-lookup"><span data-stu-id="91143-125">**Rich Edit 3.0 and later:** For backward compatibility, Microsoft Rich Edit 3.0 supports the syntax used by Microsoft Rich Edit 2.0.</span></span> <span data-ttu-id="91143-126">Si Microsoft Rich Edit 3,0 détecte que *wParam* n’est pas un pointeur [**pointer**](/previous-versions//dd162807(v=vs.85)) valide, il suppose que le message a été envoyé à l’aide de la syntaxe Microsoft Rich Edit 2,0.</span><span class="sxs-lookup"><span data-stu-id="91143-126">If Microsoft Rich Edit 3.0 detects that *wParam* is not a valid [**POINTL**](/previous-versions//dd162807(v=vs.85)) pointer, it assumes the message was sent using the Microsoft Rich Edit 2.0 syntax.</span></span> <span data-ttu-id="91143-127">Dans ce cas, elle utilise la valeur de retour pour retourner les coordonnées.</span><span class="sxs-lookup"><span data-stu-id="91143-127">In this case, it uses the return value to return the coordinates.</span></span>

<span data-ttu-id="91143-128">**Modification riche :** Pris en charge dans Microsoft Rich Edit 1,0 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="91143-128">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="91143-129">Pour plus d’informations sur la compatibilité des versions RichEdit avec les différentes versions du système, consultez [à propos des contrôles](about-rich-edit-controls.md)RichEdit.</span><span class="sxs-lookup"><span data-stu-id="91143-129">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="91143-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="91143-130">Requirements</span></span>



| <span data-ttu-id="91143-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="91143-131">Requirement</span></span> | <span data-ttu-id="91143-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="91143-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91143-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="91143-133">Minimum supported client</span></span><br/> | <span data-ttu-id="91143-134">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="91143-134">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="91143-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="91143-135">Minimum supported server</span></span><br/> | <span data-ttu-id="91143-136">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="91143-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="91143-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="91143-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="91143-138"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="91143-138"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91143-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="91143-139">See also</span></span>

<dl> <dt>

<span data-ttu-id="91143-140">**Référence**</span><span class="sxs-lookup"><span data-stu-id="91143-140">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="91143-141">**\_CHARFROMPOS em**</span><span class="sxs-lookup"><span data-stu-id="91143-141">**EM\_CHARFROMPOS**</span></span>](em-charfrompos.md)
</dt> <dt>

<span data-ttu-id="91143-142">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="91143-142">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="91143-143">[**POINTer**](/previous-versions//dd162807(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="91143-143">[**POINTL**](/previous-versions//dd162807(v=vs.85))</span></span>
</dt> </dl>

 

