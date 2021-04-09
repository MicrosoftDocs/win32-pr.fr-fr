---
title: Message EM_SETRECTNP (winuser. h)
description: Définit le rectangle de mise en forme d’un contrôle d’édition multiligne.
ms.assetid: 1ab497ca-023f-4c26-b92d-b441a0d7b90c
keywords:
- EM_SETRECTNP les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_SETRECTNP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e017bd4737c843c2452382918d71ef63345917cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942661"
---
# <a name="em_setrectnp-message"></a><span data-ttu-id="d3f84-104">\_Message SETRECTNP em</span><span class="sxs-lookup"><span data-stu-id="d3f84-104">EM\_SETRECTNP message</span></span>

<span data-ttu-id="d3f84-105">Définit le [rectangle de mise en forme](about-edit-controls.md) d’un contrôle d’édition multiligne.</span><span class="sxs-lookup"><span data-stu-id="d3f84-105">Sets the [formatting rectangle](about-edit-controls.md) of a multiline edit control.</span></span> <span data-ttu-id="d3f84-106">Le **message em \_ SETRECTNP** est identique au message [**em \_ SETRECT**](em-setrect.md) , sauf que **em \_ SETRECTNP** ne redessine *pas* la fenêtre de contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="d3f84-106">The **EM\_SETRECTNP** message is identical to the [**EM\_SETRECT**](em-setrect.md) message, except that **EM\_SETRECTNP** does *not* redraw the edit control window.</span></span>

<span data-ttu-id="d3f84-107">Le rectangle de mise en forme est le rectangle de limitation dans lequel le contrôle dessine le texte.</span><span class="sxs-lookup"><span data-stu-id="d3f84-107">The formatting rectangle is the limiting rectangle into which the control draws the text.</span></span> <span data-ttu-id="d3f84-108">Le rectangle de limitation est indépendant de la taille de la fenêtre de contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="d3f84-108">The limiting rectangle is independent of the size of the edit control window.</span></span>

<span data-ttu-id="d3f84-109">Ce message est traité uniquement par les contrôles d’édition multiligne.</span><span class="sxs-lookup"><span data-stu-id="d3f84-109">This message is processed only by multiline edit controls.</span></span> <span data-ttu-id="d3f84-110">Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.</span><span class="sxs-lookup"><span data-stu-id="d3f84-110">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="d3f84-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d3f84-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3f84-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d3f84-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d3f84-113">**Édition enrichie 3,0 et versions ultérieures :** Indique si le nouveau rectangle contient des coordonnées absolues ou relatives.</span><span class="sxs-lookup"><span data-stu-id="d3f84-113">**Rich Edit 3.0 and later:** Indicates whether the new rectangle contains absolute or relative coordinates.</span></span> <span data-ttu-id="d3f84-114">La valeur zéro indique des coordonnées absolues.</span><span class="sxs-lookup"><span data-stu-id="d3f84-114">A value of zero indicates absolute coordinates.</span></span> <span data-ttu-id="d3f84-115">La valeur 1 indique des décalages par rapport au rectangle de mise en forme actuel.</span><span class="sxs-lookup"><span data-stu-id="d3f84-115">A value of 1 indicates offsets relative to the current formatting rectangle.</span></span> <span data-ttu-id="d3f84-116">(Les décalages peuvent être positifs ou négatifs.)</span><span class="sxs-lookup"><span data-stu-id="d3f84-116">(The offsets can be positive or negative.)</span></span>

<span data-ttu-id="d3f84-117">**Contrôles d’édition :** Ce paramètre n’est pas utilisé et doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="d3f84-117">**Edit controls:** This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="d3f84-118">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d3f84-118">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d3f84-119">Pointeur vers une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) qui spécifie les nouvelles dimensions du rectangle.</span><span class="sxs-lookup"><span data-stu-id="d3f84-119">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that specifies the new dimensions of the rectangle.</span></span> <span data-ttu-id="d3f84-120">Si ce paramètre a la **valeur null**, le rectangle de mise en forme est défini sur ses valeurs par défaut.</span><span class="sxs-lookup"><span data-stu-id="d3f84-120">If this parameter is **NULL**, the formatting rectangle is set to its default values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3f84-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d3f84-121">Return value</span></span>

<span data-ttu-id="d3f84-122">Ce message ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="d3f84-122">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d3f84-123">Notes</span><span class="sxs-lookup"><span data-stu-id="d3f84-123">Remarks</span></span>

<span data-ttu-id="d3f84-124">**Modification riche :** Pris en charge dans Microsoft Rich Edit 3,0 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="d3f84-124">**Rich Edit:** Supported in Microsoft Rich Edit 3.0 and later.</span></span> <span data-ttu-id="d3f84-125">Pour plus d’informations sur la compatibilité des versions RichEdit avec les différentes versions du système, consultez [à propos des contrôles](about-rich-edit-controls.md)RichEdit.</span><span class="sxs-lookup"><span data-stu-id="d3f84-125">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d3f84-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d3f84-126">Requirements</span></span>



| <span data-ttu-id="d3f84-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d3f84-127">Requirement</span></span> | <span data-ttu-id="d3f84-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="d3f84-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3f84-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d3f84-129">Minimum supported client</span></span><br/> | <span data-ttu-id="d3f84-130">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d3f84-130">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d3f84-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d3f84-131">Minimum supported server</span></span><br/> | <span data-ttu-id="d3f84-132">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d3f84-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d3f84-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="d3f84-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3f84-134"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d3f84-134"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3f84-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d3f84-135">See also</span></span>

<dl> <dt>

<span data-ttu-id="d3f84-136">**Référence**</span><span class="sxs-lookup"><span data-stu-id="d3f84-136">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d3f84-137">**\_SETRECT em**</span><span class="sxs-lookup"><span data-stu-id="d3f84-137">**EM\_SETRECT**</span></span>](em-setrect.md)
</dt> <dt>

<span data-ttu-id="d3f84-138">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="d3f84-138">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="d3f84-139">[**RECTANGULAIRE**](/previous-versions//dd162897(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d3f84-139">[**RECT**](/previous-versions//dd162897(v=vs.85))</span></span>
</dt> </dl>

 

