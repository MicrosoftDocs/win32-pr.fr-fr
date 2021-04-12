---
title: Message BCM_SETTEXTMARGIN (commctrl. h)
description: Le \_ message BCM SETTEXTMARGIN définit les marges de dessin du texte dans un contrôle Button.
ms.assetid: 0798b1c5-7db4-46c6-8881-4c847abc7460
keywords:
- BCM_SETTEXTMARGIN les contrôles de message Windows
topic_type:
- apiref
api_name:
- BCM_SETTEXTMARGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fb6653007c155a508ce4da899a7be0d8ff2ab2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465270"
---
# <a name="bcm_settextmargin-message"></a><span data-ttu-id="d33e4-104">\_Message SETTEXTMARGIN BCM</span><span class="sxs-lookup"><span data-stu-id="d33e4-104">BCM\_SETTEXTMARGIN message</span></span>

<span data-ttu-id="d33e4-105">Le message **BCM \_ SETTEXTMARGIN** définit les marges de dessin du texte dans un contrôle Button.</span><span class="sxs-lookup"><span data-stu-id="d33e4-105">The **BCM\_SETTEXTMARGIN** message sets the margins for drawing text in a button control.</span></span>

## <a name="parameters"></a><span data-ttu-id="d33e4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d33e4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d33e4-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d33e4-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d33e4-108">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="d33e4-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="d33e4-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d33e4-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d33e4-110">Pointeur vers une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) qui spécifie les marges à utiliser pour dessiner du texte.</span><span class="sxs-lookup"><span data-stu-id="d33e4-110">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that specifies the margins to use for drawing text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d33e4-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d33e4-111">Return value</span></span>

<span data-ttu-id="d33e4-112">Si le message est correctement exécuté, la méthode retourne la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="d33e4-112">If the message succeeds, it returns **TRUE**.</span></span> <span data-ttu-id="d33e4-113">Sinon, elle retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="d33e4-113">Otherwise it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="d33e4-114">Notes</span><span class="sxs-lookup"><span data-stu-id="d33e4-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d33e4-115">Pour utiliser ce message, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0.</span><span class="sxs-lookup"><span data-stu-id="d33e4-115">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="d33e4-116">Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="d33e4-116">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d33e4-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d33e4-117">Requirements</span></span>



| <span data-ttu-id="d33e4-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d33e4-118">Requirement</span></span> | <span data-ttu-id="d33e4-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="d33e4-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d33e4-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d33e4-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d33e4-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d33e4-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d33e4-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d33e4-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d33e4-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d33e4-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d33e4-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="d33e4-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d33e4-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d33e4-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d33e4-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d33e4-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="d33e4-127">**Référence**</span><span class="sxs-lookup"><span data-stu-id="d33e4-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d33e4-128">**Bouton \_ SetTextMargin**</span><span class="sxs-lookup"><span data-stu-id="d33e4-128">**Button\_SetTextMargin**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-button_settextmargin)
</dt> <dt>

<span data-ttu-id="d33e4-129">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="d33e4-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="d33e4-130">Boutons</span><span class="sxs-lookup"><span data-stu-id="d33e4-130">Buttons</span></span>](buttons.md)
</dt> </dl>

 

