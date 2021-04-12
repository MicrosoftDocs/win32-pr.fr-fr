---
title: Message EM_SETTABSTOPS (winuser. h)
description: Le \_ message em SETTABSTOPS définit les taquets de tabulation dans un contrôle d’édition multiligne.
ms.assetid: d6fe2828-4ae9-4652-ace0-2f71e146f777
keywords:
- EM_SETTABSTOPS les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_SETTABSTOPS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48d076dea415f169eff46101fd7cfe632d73d976
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104212"
---
# <a name="em_settabstops-message"></a><span data-ttu-id="330fa-104">\_Message SETTABSTOPS em</span><span class="sxs-lookup"><span data-stu-id="330fa-104">EM\_SETTABSTOPS message</span></span>

<span data-ttu-id="330fa-105">Le message **em \_ SETTABSTOPS** définit les taquets de tabulation dans un contrôle d’édition multiligne.</span><span class="sxs-lookup"><span data-stu-id="330fa-105">The **EM\_SETTABSTOPS** message sets the tab stops in a multiline edit control.</span></span> <span data-ttu-id="330fa-106">Lorsque du texte est copié dans le contrôle, tout caractère de tabulation dans le texte entraîne la génération de l’espace jusqu’au taquet de tabulation suivant.</span><span class="sxs-lookup"><span data-stu-id="330fa-106">When text is copied to the control, any tab character in the text causes space to be generated up to the next tab stop.</span></span>

<span data-ttu-id="330fa-107">Ce message est traité uniquement par les contrôles d’édition multiligne.</span><span class="sxs-lookup"><span data-stu-id="330fa-107">This message is processed only by multiline edit controls.</span></span> <span data-ttu-id="330fa-108">Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.</span><span class="sxs-lookup"><span data-stu-id="330fa-108">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="330fa-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="330fa-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="330fa-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="330fa-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="330fa-111">Nombre de taquets de tabulation contenus dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="330fa-111">The number of tab stops contained in the array.</span></span> <span data-ttu-id="330fa-112">Si ce paramètre est égal à zéro, le paramètre *lParam* est ignoré et les taquets de tabulation par défaut sont définis à chaque unité de modèle de boîte de dialogue 32.</span><span class="sxs-lookup"><span data-stu-id="330fa-112">If this parameter is zero, the *lParam* parameter is ignored and default tab stops are set at every 32 dialog template units.</span></span> <span data-ttu-id="330fa-113">Si ce paramètre a la valeur 1, les taquets de tabulation sont définis à toutes les *n* unités de modèle de boîte de dialogue, où *n* est la distance vers laquelle pointe le paramètre *lParam* .</span><span class="sxs-lookup"><span data-stu-id="330fa-113">If this parameter is 1, tab stops are set at every *n* dialog template units, where *n* is the distance pointed to by the *lParam* parameter.</span></span> <span data-ttu-id="330fa-114">Si ce paramètre est supérieur à 1, *lParam* est un pointeur vers un tableau de taquets de tabulation.</span><span class="sxs-lookup"><span data-stu-id="330fa-114">If this parameter is greater than 1, *lParam* is a pointer to an array of tab stops.</span></span>

</dd> <dt>

<span data-ttu-id="330fa-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="330fa-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="330fa-116">Pointeur vers un tableau d’entiers non signés qui spécifie les taquets de tabulation dans les unités du modèle de boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="330fa-116">A pointer to an array of unsigned integers specifying the tab stops, in dialog template units.</span></span> <span data-ttu-id="330fa-117">Si le paramètre *wParam* est 1, ce paramètre est un pointeur vers un entier non signé qui contient la distance entre tous les taquets de tabulation, dans les unités de modèle de boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="330fa-117">If the *wParam* parameter is 1, this parameter is a pointer to an unsigned integer containing the distance between all tab stops, in dialog template units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="330fa-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="330fa-118">Return value</span></span>

<span data-ttu-id="330fa-119">Si tous les onglets sont définis, la valeur de retour est **true**.</span><span class="sxs-lookup"><span data-stu-id="330fa-119">If all the tabs are set, the return value is **TRUE**.</span></span>

<span data-ttu-id="330fa-120">Si tous les onglets ne sont pas définis, la valeur de retour est **false**.</span><span class="sxs-lookup"><span data-stu-id="330fa-120">If all the tabs are not set, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="330fa-121">Notes</span><span class="sxs-lookup"><span data-stu-id="330fa-121">Remarks</span></span>

<span data-ttu-id="330fa-122">Le **message \_ SETTABSTOPS em** ne redessine pas automatiquement la fenêtre de contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="330fa-122">The **EM\_SETTABSTOPS** message does not automatically redraw the edit control window.</span></span> <span data-ttu-id="330fa-123">Si l’application modifie les taquets de tabulation pour le texte déjà présent dans le contrôle d’édition, elle doit appeler la fonction [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect) pour redessiner la fenêtre de contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="330fa-123">If the application is changing the tab stops for text already in the edit control, it should call the [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect) function to redraw the edit control window.</span></span>

<span data-ttu-id="330fa-124">Les valeurs spécifiées dans le tableau se trouvent dans les unités de modèle de boîte de dialogue, qui sont les unités indépendantes du périphérique utilisées dans les modèles de boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="330fa-124">The values specified in the array are in dialog template units, which are the device-independent units used in dialog box templates.</span></span> <span data-ttu-id="330fa-125">Pour convertir des mesures à partir d’unités de modèle de boîte de dialogue en unités d’écran (pixels), utilisez la fonction [**MapDialogRect**](/windows/desktop/api/winuser/nf-winuser-mapdialogrect) .</span><span class="sxs-lookup"><span data-stu-id="330fa-125">To convert measurements from dialog template units to screen units (pixels), use the [**MapDialogRect**](/windows/desktop/api/winuser/nf-winuser-mapdialogrect) function.</span></span>

<span data-ttu-id="330fa-126">**Modification riche :** Pris en charge dans Microsoft Rich Edit 3,0 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="330fa-126">**Rich Edit:** Supported in Microsoft Rich Edit 3.0 and later.</span></span> <span data-ttu-id="330fa-127">Un contrôle RichEdit peut avoir le nombre maximal de taquets de tabulation spécifiés par les \_ taquets de tabulation Max \_ .</span><span class="sxs-lookup"><span data-stu-id="330fa-127">A rich edit control can have the maximum number of tab stops specified by MAX\_TAB\_STOPS.</span></span> <span data-ttu-id="330fa-128">Pour plus d’informations sur la compatibilité des versions RichEdit avec les différentes versions du système, consultez [à propos des contrôles](about-rich-edit-controls.md)RichEdit.</span><span class="sxs-lookup"><span data-stu-id="330fa-128">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="330fa-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="330fa-129">Requirements</span></span>



| <span data-ttu-id="330fa-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="330fa-130">Requirement</span></span> | <span data-ttu-id="330fa-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="330fa-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="330fa-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="330fa-132">Minimum supported client</span></span><br/> | <span data-ttu-id="330fa-133">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="330fa-133">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="330fa-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="330fa-134">Minimum supported server</span></span><br/> | <span data-ttu-id="330fa-135">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="330fa-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="330fa-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="330fa-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="330fa-137"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="330fa-137"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="330fa-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="330fa-138">See also</span></span>

<dl> <dt>

<span data-ttu-id="330fa-139">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="330fa-139">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="330fa-140">**InvalidateRect**</span><span class="sxs-lookup"><span data-stu-id="330fa-140">**InvalidateRect**</span></span>](/windows/desktop/api/winuser/nf-winuser-invalidaterect)
</dt> <dt>

[<span data-ttu-id="330fa-141">**MapDialogRect**</span><span class="sxs-lookup"><span data-stu-id="330fa-141">**MapDialogRect**</span></span>](/windows/desktop/api/winuser/nf-winuser-mapdialogrect)
</dt> </dl>

 

