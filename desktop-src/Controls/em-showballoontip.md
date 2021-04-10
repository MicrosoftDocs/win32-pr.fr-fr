---
title: Message EM_SHOWBALLOONTIP (commctrl. h)
description: Le \_ message em SHOWBALLOONTIP affiche une info-bulle associée à un contrôle d’édition.
ms.assetid: 1e6915b7-4b61-43b2-be13-b89c72378a1a
keywords:
- EM_SHOWBALLOONTIP les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_SHOWBALLOONTIP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8fc0174752ab8214873da9478a0af435be76427
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104206"
---
# <a name="em_showballoontip-message"></a><span data-ttu-id="69928-104">\_Message SHOWBALLOONTIP em</span><span class="sxs-lookup"><span data-stu-id="69928-104">EM\_SHOWBALLOONTIP message</span></span>

<span data-ttu-id="69928-105">Le message **em \_ SHOWBALLOONTIP** affiche une info-bulle associée à un contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="69928-105">The **EM\_SHOWBALLOONTIP** message displays a balloon tip associated with an edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="69928-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="69928-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69928-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="69928-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="69928-108">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="69928-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="69928-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="69928-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="69928-110">Pointeur vers une structure [**EDITBALLOONTIP**](/windows/desktop/api/Commctrl/ns-commctrl-editballoontip) qui contient des informations sur l’info-bulle à afficher.</span><span class="sxs-lookup"><span data-stu-id="69928-110">A pointer to an [**EDITBALLOONTIP**](/windows/desktop/api/Commctrl/ns-commctrl-editballoontip) structure that contains information about the balloon tip to display.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69928-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="69928-111">Return value</span></span>

<span data-ttu-id="69928-112">Si le message est correctement exécuté, la méthode retourne la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="69928-112">If the message succeeds, it returns **TRUE**.</span></span> <span data-ttu-id="69928-113">Sinon, elle retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="69928-113">Otherwise it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="69928-114">Notes</span><span class="sxs-lookup"><span data-stu-id="69928-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="69928-115">Pour utiliser ce message, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0.</span><span class="sxs-lookup"><span data-stu-id="69928-115">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="69928-116">Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="69928-116">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="69928-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="69928-117">Requirements</span></span>



| <span data-ttu-id="69928-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="69928-118">Requirement</span></span> | <span data-ttu-id="69928-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="69928-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="69928-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="69928-120">Minimum supported client</span></span><br/> | <span data-ttu-id="69928-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="69928-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="69928-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="69928-122">Minimum supported server</span></span><br/> | <span data-ttu-id="69928-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="69928-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="69928-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="69928-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="69928-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="69928-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69928-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="69928-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="69928-127">**Référence**</span><span class="sxs-lookup"><span data-stu-id="69928-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="69928-128">**EDITBALLOONTIP**</span><span class="sxs-lookup"><span data-stu-id="69928-128">**EDITBALLOONTIP**</span></span>](/windows/desktop/api/Commctrl/ns-commctrl-editballoontip)
</dt> <dt>

[<span data-ttu-id="69928-129">**Modifier \_ ShowBalloonTip**</span><span class="sxs-lookup"><span data-stu-id="69928-129">**Edit\_ShowBalloonTip**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-edit_showballoontip)
</dt> </dl>

 

 





