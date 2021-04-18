---
title: Message PGM_SETBUTTONSIZE (commctrl. h)
description: Définit la taille actuelle du bouton pour le contrôle de pagineur. Vous pouvez envoyer ce message de manière explicite ou utiliser la macro de radiomessagerie \_ SetButtonSize.
ms.assetid: b31960f8-87c2-4209-8213-df75ac883e11
keywords:
- PGM_SETBUTTONSIZE les contrôles de message Windows
topic_type:
- apiref
api_name:
- PGM_SETBUTTONSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ecf8c164ed960675c1a68be36acfe0eff40f972f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508486"
---
# <a name="pgm_setbuttonsize-message"></a><span data-ttu-id="e734e-105">\_Message SETBUTTONSIZE PGM</span><span class="sxs-lookup"><span data-stu-id="e734e-105">PGM\_SETBUTTONSIZE message</span></span>

<span data-ttu-id="e734e-106">Définit la taille actuelle du bouton pour le contrôle de pagineur.</span><span class="sxs-lookup"><span data-stu-id="e734e-106">Sets the current button size for the pager control.</span></span> <span data-ttu-id="e734e-107">Vous pouvez envoyer ce message de manière explicite ou utiliser la macro de [**radiomessagerie \_ SetButtonSize**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setbuttonsize) .</span><span class="sxs-lookup"><span data-stu-id="e734e-107">You can send this message explicitly or use the [**Pager\_SetButtonSize**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setbuttonsize) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="e734e-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e734e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e734e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e734e-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="e734e-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="e734e-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="e734e-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e734e-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e734e-112">Valeur de type **int** qui contient la nouvelle taille de bouton, en pixels.</span><span class="sxs-lookup"><span data-stu-id="e734e-112">Value of type **int** that contains the new button size, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e734e-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e734e-113">Return value</span></span>

<span data-ttu-id="e734e-114">Retourne une valeur **int** qui contient la taille de bouton précédente, en pixels.</span><span class="sxs-lookup"><span data-stu-id="e734e-114">Returns an **int** value that contains the previous button size, in pixels.</span></span>

## <a name="remarks"></a><span data-ttu-id="e734e-115">Notes</span><span class="sxs-lookup"><span data-stu-id="e734e-115">Remarks</span></span>

<span data-ttu-id="e734e-116">Si le contrôle de pagineur a le style [**PG \_ horiment**](pager-control-styles.md) , la taille du bouton détermine la largeur des boutons du pagineur.</span><span class="sxs-lookup"><span data-stu-id="e734e-116">If the pager control has the [**PGS\_HORZ**](pager-control-styles.md) style, the button size determines the width of the pager buttons.</span></span> <span data-ttu-id="e734e-117">Si le contrôle de pagineur a le style [**PG \_ vert**](pager-control-styles.md) , la taille du bouton détermine la hauteur des boutons du pagineur.</span><span class="sxs-lookup"><span data-stu-id="e734e-117">If the pager control has the [**PGS\_VERT**](pager-control-styles.md) style, the button size determines the height of the pager buttons.</span></span> <span data-ttu-id="e734e-118">Par défaut, le contrôle pager définit sa taille de bouton sur trois-quarts de la largeur de la barre de défilement.</span><span class="sxs-lookup"><span data-stu-id="e734e-118">By default, the pager control sets its button size to three-fourths of the width of the scroll bar.</span></span>

<span data-ttu-id="e734e-119">La taille minimale du bouton du pagineur est actuellement de 12 pixels.</span><span class="sxs-lookup"><span data-stu-id="e734e-119">There is a minimum size to the pager button, currently 12 pixels.</span></span> <span data-ttu-id="e734e-120">Toutefois, cela peut changer par conséquent, vous ne devez pas dépendre de cette valeur.</span><span class="sxs-lookup"><span data-stu-id="e734e-120">However, this can change so you should not depend on this value.</span></span>

## <a name="requirements"></a><span data-ttu-id="e734e-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e734e-121">Requirements</span></span>



| <span data-ttu-id="e734e-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e734e-122">Requirement</span></span> | <span data-ttu-id="e734e-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="e734e-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e734e-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e734e-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e734e-125">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e734e-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e734e-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e734e-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e734e-127">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e734e-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e734e-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="e734e-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="e734e-129"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e734e-129"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e734e-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e734e-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e734e-131">**\_GETBUTTONSIZE PGM**</span><span class="sxs-lookup"><span data-stu-id="e734e-131">**PGM\_GETBUTTONSIZE**</span></span>](pgm-getbuttonsize.md)
</dt> </dl>

 

 





