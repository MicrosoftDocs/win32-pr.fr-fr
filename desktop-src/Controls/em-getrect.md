---
title: Message EM_GETRECT (winuser. h)
description: Obtient le rectangle de mise en forme d’un contrôle d’édition.
ms.assetid: eef0150d-9b7a-4247-acbf-6fea2efd1dc3
keywords:
- EM_GETRECT les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_GETRECT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a8192fd4c3aa7fbe953a36217f6b1408f055d8d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843706"
---
# <a name="em_getrect-message"></a><span data-ttu-id="859de-104">\_Message GETRECT em</span><span class="sxs-lookup"><span data-stu-id="859de-104">EM\_GETRECT message</span></span>

<span data-ttu-id="859de-105">Obtient le [rectangle de mise en forme](about-edit-controls.md) d’un contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="859de-105">Gets the [formatting rectangle](about-edit-controls.md) of an edit control.</span></span> <span data-ttu-id="859de-106">Le rectangle de mise en forme est le rectangle de limitation dans lequel le contrôle dessine le texte.</span><span class="sxs-lookup"><span data-stu-id="859de-106">The formatting rectangle is the limiting rectangle into which the control draws the text.</span></span> <span data-ttu-id="859de-107">Le rectangle de limitation est indépendant de la taille de la fenêtre Modifier-contrôle.</span><span class="sxs-lookup"><span data-stu-id="859de-107">The limiting rectangle is independent of the size of the edit-control window.</span></span> <span data-ttu-id="859de-108">Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.</span><span class="sxs-lookup"><span data-stu-id="859de-108">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="859de-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="859de-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="859de-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="859de-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="859de-111">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="859de-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="859de-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="859de-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="859de-113">Pointeur vers une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) qui reçoit le rectangle de mise en forme.</span><span class="sxs-lookup"><span data-stu-id="859de-113">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that receives the formatting rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="859de-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="859de-114">Return value</span></span>

<span data-ttu-id="859de-115">La valeur de retour n’est pas significative.</span><span class="sxs-lookup"><span data-stu-id="859de-115">The return value is not meaningful.</span></span>

## <a name="remarks"></a><span data-ttu-id="859de-116">Notes</span><span class="sxs-lookup"><span data-stu-id="859de-116">Remarks</span></span>

<span data-ttu-id="859de-117">Vous pouvez modifier le rectangle de mise en forme d’un contrôle d’édition multiligne à l’aide des messages [**em \_ SETRECT**](em-setrect.md) et [**em \_ SETRECTNP**](em-setrectnp.md) .</span><span class="sxs-lookup"><span data-stu-id="859de-117">You can modify the formatting rectangle of a multiline edit control by using the [**EM\_SETRECT**](em-setrect.md) and [**EM\_SETRECTNP**](em-setrectnp.md) messages.</span></span>

<span data-ttu-id="859de-118">Dans certaines conditions, **em \_ GETRECT** peut ne pas retourner les valeurs exactes pour lesquelles [**em \_ SETRECT**](em-setrect.md) ou [**em \_ SETRECTNP**](em-setrectnp.md) est approximativement correct, mais il peut être décalé de quelques pixels.</span><span class="sxs-lookup"><span data-stu-id="859de-118">Under certain conditions, **EM\_GETRECT** might not return the exact values that [**EM\_SETRECT**](em-setrect.md) or [**EM\_SETRECTNP**](em-setrectnp.md) set it will be approximately correct, but it can be off by a few pixels.</span></span>

<span data-ttu-id="859de-119">**Modification riche :** Pris en charge dans Microsoft Rich Edit 1,0 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="859de-119">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="859de-120">Le rectangle de mise en forme n’inclut pas la barre de sélection, qui est une zone non marquée à gauche de chaque paragraphe.</span><span class="sxs-lookup"><span data-stu-id="859de-120">The formatting rectangle does not include the selection bar, which is an unmarked area to the left of each paragraph.</span></span> <span data-ttu-id="859de-121">Lorsque vous cliquez sur cette option, la barre de sélection sélectionne la ligne.</span><span class="sxs-lookup"><span data-stu-id="859de-121">When clicked, the selection bar selects the line.</span></span> <span data-ttu-id="859de-122">Pour plus d’informations sur la compatibilité des versions RichEdit avec les différentes versions du système, consultez [à propos des contrôles](about-rich-edit-controls.md)RichEdit.</span><span class="sxs-lookup"><span data-stu-id="859de-122">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="859de-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="859de-123">Requirements</span></span>



| <span data-ttu-id="859de-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="859de-124">Requirement</span></span> | <span data-ttu-id="859de-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="859de-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="859de-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="859de-126">Minimum supported client</span></span><br/> | <span data-ttu-id="859de-127">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="859de-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="859de-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="859de-128">Minimum supported server</span></span><br/> | <span data-ttu-id="859de-129">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="859de-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="859de-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="859de-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="859de-131"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="859de-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="859de-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="859de-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="859de-133">**Référence**</span><span class="sxs-lookup"><span data-stu-id="859de-133">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="859de-134">**\_SETRECT em**</span><span class="sxs-lookup"><span data-stu-id="859de-134">**EM\_SETRECT**</span></span>](em-setrect.md)
</dt> <dt>

[<span data-ttu-id="859de-135">**\_SETRECTNP em**</span><span class="sxs-lookup"><span data-stu-id="859de-135">**EM\_SETRECTNP**</span></span>](em-setrectnp.md)
</dt> <dt>

<span data-ttu-id="859de-136">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="859de-136">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="859de-137">[**RECTANGULAIRE**](/previous-versions//dd162897(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="859de-137">[**RECT**](/previous-versions//dd162897(v=vs.85))</span></span>
</dt> </dl>

 

