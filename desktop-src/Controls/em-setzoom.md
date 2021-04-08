---
title: Message EM_SETZOOM (RichEdit. h)
description: Définit le facteur de zoom. Le ratio doit être une valeur comprise entre 1/64 et 64. Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.
ms.assetid: 6cdec5b8-4ce7-4fd5-8083-4daa63d17f63
keywords:
- EM_SETZOOM les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_SETZOOM
api_location:
- Richedit.h
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d38630f27afcfc0ed29e3ccc3129e2dea22d4ac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843802"
---
# <a name="em_setzoom-message"></a><span data-ttu-id="05a61-106">\_Message SETZOOM em</span><span class="sxs-lookup"><span data-stu-id="05a61-106">EM\_SETZOOM message</span></span>

<span data-ttu-id="05a61-107">Définit le taux de zoom pour un contrôle d’édition multiligne ou un contrôle RichEdit.</span><span class="sxs-lookup"><span data-stu-id="05a61-107">Sets the zoom ratio for a multiline edit control or a rich edit control.</span></span> <span data-ttu-id="05a61-108">Le ratio doit être une valeur comprise entre 1/64 et 64.</span><span class="sxs-lookup"><span data-stu-id="05a61-108">The ratio must be a value between 1/64 and 64.</span></span> <span data-ttu-id="05a61-109">Le contrôle d’édition doit avoir le jeu de styles étendus **es \_ ex \_ zoomable** . pour que ce message ait un effet, consultez [modifier les styles étendus de contrôle](edit-control-window-extended-styles.md).</span><span class="sxs-lookup"><span data-stu-id="05a61-109">The edit control needs to have the **ES\_EX\_ZOOMABLE** extended style set, for this message to have an effect, see [Edit Control Extended Styles](edit-control-window-extended-styles.md).</span></span>

## <a name="parameters"></a><span data-ttu-id="05a61-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="05a61-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05a61-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="05a61-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="05a61-112">Numérateur du rapport de zoom.</span><span class="sxs-lookup"><span data-stu-id="05a61-112">Numerator of the zoom ratio.</span></span>

</dd> <dt>

<span data-ttu-id="05a61-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="05a61-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="05a61-114">Dénominateur du rapport de zoom.</span><span class="sxs-lookup"><span data-stu-id="05a61-114">Denominator of the zoom ratio.</span></span> <span data-ttu-id="05a61-115">Ces paramètres peuvent avoir les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="05a61-115">These parameters can have the following values.</span></span>



| <span data-ttu-id="05a61-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="05a61-116">Value</span></span>                                                                                                                                                                                                                                                              | <span data-ttu-id="05a61-117">Signification</span><span class="sxs-lookup"><span data-stu-id="05a61-117">Meaning</span></span>                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Both_0"></span><span id="both_0"></span><span id="BOTH_0"></span><dl> <span data-ttu-id="05a61-118"><dt>**Les deux**</dt></span><span class="sxs-lookup"><span data-stu-id="05a61-118"><dt>**Both 0**</dt></span></span> </dl>                                                                                                   | <span data-ttu-id="05a61-119">Désactive le zoom à l’aide du **message \_ SETZOOM em** (le zoom peut encore se produire à l’aide de [**TxGetExtent**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txgetextent)).</span><span class="sxs-lookup"><span data-stu-id="05a61-119">Turns off zooming by using the **EM\_SETZOOM** message (zooming may still occur using [**TxGetExtent**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txgetextent)).</span></span><br/> |
| <span id="1_64____wParam___lParam____64"></span><span id="1_64____wparam___lparam____64"></span><span id="1_64____WPARAM___LPARAM____64"></span><dl> <span data-ttu-id="05a61-120"><dt>**1/64 < (wParam/lParam) < 64**</dt></span><span class="sxs-lookup"><span data-stu-id="05a61-120"><dt>**1/64 < (wParam / lParam) < 64**</dt></span></span> </dl> | <span data-ttu-id="05a61-121">Zooms affichés par le numérateur/dénominateur du rapport de zoom</span><span class="sxs-lookup"><span data-stu-id="05a61-121">Zooms display by the zoom ratio numerator/denominator</span></span><br/>                                                                                |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05a61-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="05a61-122">Return value</span></span>

<span data-ttu-id="05a61-123">Si le nouveau paramètre de zoom est accepté, la valeur de retour est **true**.</span><span class="sxs-lookup"><span data-stu-id="05a61-123">If the new zoom setting is accepted, the return value is **TRUE**.</span></span>

<span data-ttu-id="05a61-124">Si le nouveau paramètre de zoom n’est pas accepté, la valeur de retour est **false**.</span><span class="sxs-lookup"><span data-stu-id="05a61-124">If the new zoom setting is not accepted, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="05a61-125">Notes</span><span class="sxs-lookup"><span data-stu-id="05a61-125">Remarks</span></span>

<span data-ttu-id="05a61-126">**Modifier :** Pris en charge dans Windows 10 1809 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="05a61-126">**Edit:** Supported in Windows 10 1809 and later.</span></span> <span data-ttu-id="05a61-127">Le contrôle d’édition doit avoir le jeu de styles étendus **es \_ ex \_ zoomable** . pour que ce message ait un effet, consultez [modifier les styles étendus de contrôle](edit-control-window-extended-styles.md).</span><span class="sxs-lookup"><span data-stu-id="05a61-127">The edit control needs to have the **ES\_EX\_ZOOMABLE** extended style set, for this message to have an effect, see [Edit Control Extended Styles](edit-control-window-extended-styles.md).</span></span> <span data-ttu-id="05a61-128">Pour plus d’informations sur le contrôle d’édition, consultez [modifier des contrôles](about-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="05a61-128">For information about the edit control, see [Edit Controls](about-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="05a61-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="05a61-129">Requirements</span></span>



| <span data-ttu-id="05a61-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="05a61-130">Requirement</span></span> | <span data-ttu-id="05a61-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="05a61-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="05a61-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="05a61-132">Minimum supported client</span></span><br/> | <span data-ttu-id="05a61-133">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="05a61-133">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="05a61-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="05a61-134">Minimum supported server</span></span><br/> | <span data-ttu-id="05a61-135">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="05a61-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="05a61-136">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="05a61-136">Redistributable</span></span><br/>          | <span data-ttu-id="05a61-137">Édition enrichie 3,0</span><span class="sxs-lookup"><span data-stu-id="05a61-137">Rich Edit 3.0</span></span><br/>                                                              |
| <span data-ttu-id="05a61-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="05a61-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="05a61-139"><dt>RichEdit. h/commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="05a61-139"><dt>Richedit.h/Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05a61-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="05a61-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05a61-141">**\_GETZOOM em**</span><span class="sxs-lookup"><span data-stu-id="05a61-141">**EM\_GETZOOM**</span></span>](em-getzoom.md)
</dt> </dl>

 

 





