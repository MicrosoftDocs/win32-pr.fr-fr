---
title: Message TCM_SETEXTENDEDSTYLE (commctrl. h)
description: Définit les styles étendus que le contrôle onglet utilisera. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro TabCtrl SetExtendedStyle.
ms.assetid: 96ccebe1-2836-4198-8cd7-858401562c21
keywords:
- TCM_SETEXTENDEDSTYLE les contrôles de message Windows
topic_type:
- apiref
api_name:
- TCM_SETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4c789b45eaae6cb3b1bc4fed6f216ec5010b463
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032882"
---
# <a name="tcm_setextendedstyle-message"></a><span data-ttu-id="c7d79-105">\_Message SETEXTENDEDSTYLE TCM</span><span class="sxs-lookup"><span data-stu-id="c7d79-105">TCM\_SETEXTENDEDSTYLE message</span></span>

<span data-ttu-id="c7d79-106">Définit les styles étendus que le contrôle onglet utilisera.</span><span class="sxs-lookup"><span data-stu-id="c7d79-106">Sets the extended styles that the tab control will use.</span></span> <span data-ttu-id="c7d79-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**TabCtrl \_ SetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setextendedstyle) .</span><span class="sxs-lookup"><span data-stu-id="c7d79-107">You can send this message explicitly or by using the [**TabCtrl\_SetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setextendedstyle) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="c7d79-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c7d79-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7d79-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c7d79-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c7d79-110">Valeur **DWORD** qui indique les styles de *lParam* à affecter.</span><span class="sxs-lookup"><span data-stu-id="c7d79-110">A **DWORD** value that indicates which styles in *lParam* are to be affected.</span></span> <span data-ttu-id="c7d79-111">Seuls les styles étendus dans *wParam* seront modifiés.</span><span class="sxs-lookup"><span data-stu-id="c7d79-111">Only the extended styles in *wParam* will be changed.</span></span> <span data-ttu-id="c7d79-112">Tous les autres styles seront conservés tels quels.</span><span class="sxs-lookup"><span data-stu-id="c7d79-112">All other styles will be maintained as they are.</span></span> <span data-ttu-id="c7d79-113">Si ce paramètre est égal à zéro, tous les styles de *lParam* sont affectés.</span><span class="sxs-lookup"><span data-stu-id="c7d79-113">If this parameter is zero, then all of the styles in *lParam* will be affected.</span></span>

</dd> <dt>

<span data-ttu-id="c7d79-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c7d79-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c7d79-115">Valeur qui spécifie les styles du contrôle onglet étendu.</span><span class="sxs-lookup"><span data-stu-id="c7d79-115">Value specifying the extended tab control styles.</span></span> <span data-ttu-id="c7d79-116">Cette valeur est une combinaison de [styles étendus](tab-control-extended-styles.md)de contrôle d’onglet.</span><span class="sxs-lookup"><span data-stu-id="c7d79-116">This value is a combination of tab control [extended styles](tab-control-extended-styles.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7d79-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c7d79-117">Return value</span></span>

<span data-ttu-id="c7d79-118">Retourne une valeur **DWORD** qui contient les styles étendus du contrôle onglet précédent.</span><span class="sxs-lookup"><span data-stu-id="c7d79-118">Returns a **DWORD** value that contains the previous tab control extended styles.</span></span>

## <a name="remarks"></a><span data-ttu-id="c7d79-119">Notes</span><span class="sxs-lookup"><span data-stu-id="c7d79-119">Remarks</span></span>

<span data-ttu-id="c7d79-120">Le paramètre *wParam* vous permet de modifier un ou plusieurs styles étendus sans avoir à récupérer d’abord les styles existants.</span><span class="sxs-lookup"><span data-stu-id="c7d79-120">The *wParam* parameter allows you to modify one or more extended styles without having to retrieve the existing styles first.</span></span> <span data-ttu-id="c7d79-121">Par exemple, si vous transmettez des [**TCS \_ ex \_ FLATSEPARATORS**](tab-control-extended-styles.md) pour *wParam* et 0 pour *lParam*, le style **TCS \_ ex \_ FLATSEPARATORS** est effacé, mais tous les autres styles restent les mêmes.</span><span class="sxs-lookup"><span data-stu-id="c7d79-121">For example, if you pass [**TCS\_EX\_FLATSEPARATORS**](tab-control-extended-styles.md) for *wParam* and 0 for *lParam*, the **TCS\_EX\_FLATSEPARATORS** style will be cleared, but all other styles will remain the same.</span></span>

<span data-ttu-id="c7d79-122">Pour des raisons de compatibilité descendante, la macro [**TabCtrl \_ SetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setextendedstyle) n’a pas été mise à jour pour utiliser *dwExMask*.</span><span class="sxs-lookup"><span data-stu-id="c7d79-122">For backward compatibility reasons, the [**TabCtrl\_SetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setextendedstyle) macro has not been updated to use *dwExMask*.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7d79-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c7d79-123">Requirements</span></span>



| <span data-ttu-id="c7d79-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c7d79-124">Requirement</span></span> | <span data-ttu-id="c7d79-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="c7d79-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c7d79-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c7d79-126">Minimum supported client</span></span><br/> | <span data-ttu-id="c7d79-127">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c7d79-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c7d79-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c7d79-128">Minimum supported server</span></span><br/> | <span data-ttu-id="c7d79-129">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c7d79-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c7d79-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="c7d79-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7d79-131"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c7d79-131"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7d79-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c7d79-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7d79-133">**\_GETEXTENDEDSTYLE TCM**</span><span class="sxs-lookup"><span data-stu-id="c7d79-133">**TCM\_GETEXTENDEDSTYLE**</span></span>](tcm-getextendedstyle.md)
</dt> </dl>

 

 





