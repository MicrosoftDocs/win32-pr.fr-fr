---
title: Message TCM_SETCURFOCUS (commctrl. h)
description: Définit le focus sur un onglet spécifié dans un contrôle onglet. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro TabCtrl SetCurFocus.
ms.assetid: bcbd5f26-b54e-492b-aff3-357b8ae23969
keywords:
- TCM_SETCURFOCUS les contrôles de message Windows
topic_type:
- apiref
api_name:
- TCM_SETCURFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abe566d1e1b3cc7d257c4756fe123423fc344a7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942157"
---
# <a name="tcm_setcurfocus-message"></a><span data-ttu-id="e7c11-105">\_Message SETCURFOCUS TCM</span><span class="sxs-lookup"><span data-stu-id="e7c11-105">TCM\_SETCURFOCUS message</span></span>

<span data-ttu-id="e7c11-106">Définit le focus sur un onglet spécifié dans un contrôle onglet.</span><span class="sxs-lookup"><span data-stu-id="e7c11-106">Sets the focus to a specified tab in a tab control.</span></span> <span data-ttu-id="e7c11-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**TabCtrl \_ SetCurFocus**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setcurfocus) .</span><span class="sxs-lookup"><span data-stu-id="e7c11-107">You can send this message explicitly or by using the [**TabCtrl\_SetCurFocus**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setcurfocus) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="e7c11-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e7c11-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7c11-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e7c11-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e7c11-110">Index de l’onglet qui obtient le focus.</span><span class="sxs-lookup"><span data-stu-id="e7c11-110">Index of the tab that gets the focus.</span></span>

</dd> <dt>

<span data-ttu-id="e7c11-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e7c11-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="e7c11-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="e7c11-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7c11-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e7c11-113">Return value</span></span>

<span data-ttu-id="e7c11-114">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="e7c11-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7c11-115">Notes</span><span class="sxs-lookup"><span data-stu-id="e7c11-115">Remarks</span></span>

<span data-ttu-id="e7c11-116">Si le contrôle onglet a le style de [**\_ boutons TCS**](tab-control-styles.md) (mode bouton), l’onglet avec le focus peut être différent de l’onglet sélectionné. Par exemple, lorsqu’un onglet est sélectionné, l’utilisateur peut appuyer sur les touches de direction pour définir le focus sur un autre onglet sans modifier l’onglet sélectionné. En mode bouton, **TCM \_ SETCURFOCUS** définit le focus d’entrée sur le bouton associé à l’onglet spécifié, mais il ne modifie pas l’onglet sélectionné.</span><span class="sxs-lookup"><span data-stu-id="e7c11-116">If the tab control has the [**TCS\_BUTTONS**](tab-control-styles.md) style (button mode), the tab with the focus may be different from the selected tab. For example, when a tab is selected, the user can press the arrow keys to set the focus to a different tab without changing the selected tab. In button mode, **TCM\_SETCURFOCUS** sets the input focus to the button associated with the specified tab, but it does not change the selected tab.</span></span>

<span data-ttu-id="e7c11-117">Si le contrôle onglet n’a pas le style de [**\_ boutons TCS**](tab-control-styles.md) , le fait de modifier le focus modifie également l’onglet sélectionné. Dans ce cas, le contrôle onglet envoie les codes de notification [TCN \_ SELCHANGING](tcn-selchanging.md) et [TCN \_ selChange](tcn-selchange.md) à sa fenêtre parente.</span><span class="sxs-lookup"><span data-stu-id="e7c11-117">If the tab control does not have the [**TCS\_BUTTONS**](tab-control-styles.md) style, changing the focus also changes the selected tab. In this case, the tab control sends the [TCN\_SELCHANGING](tcn-selchanging.md) and [TCN\_SELCHANGE](tcn-selchange.md) notification codes to its parent window.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7c11-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e7c11-118">Requirements</span></span>



| <span data-ttu-id="e7c11-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e7c11-119">Requirement</span></span> | <span data-ttu-id="e7c11-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="e7c11-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e7c11-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e7c11-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e7c11-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e7c11-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e7c11-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e7c11-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e7c11-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e7c11-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e7c11-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="e7c11-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7c11-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7c11-126"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7c11-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e7c11-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7c11-128">**\_GETCURFOCUS TCM**</span><span class="sxs-lookup"><span data-stu-id="e7c11-128">**TCM\_GETCURFOCUS**</span></span>](tcm-getcurfocus.md)
</dt> </dl>

 

 





