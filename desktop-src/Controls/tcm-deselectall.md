---
title: Message TCM_DESELECTALL (commctrl. h)
description: Réinitialise des éléments dans un contrôle onglet, en effaçant tous ceux qui ont été définis sur l' \_ État TCIS BUTTONPRESSED. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro TabCtrl DeselectAll.
ms.assetid: cc2e5131-3c1b-473a-a0ca-274a2d39a2f1
keywords:
- TCM_DESELECTALL les contrôles de message Windows
topic_type:
- apiref
api_name:
- TCM_DESELECTALL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f606538075a9163d8b8dc8328b5585b51b769aa5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105748"
---
# <a name="tcm_deselectall-message"></a><span data-ttu-id="04232-105">\_Message DESELECTALL TCM</span><span class="sxs-lookup"><span data-stu-id="04232-105">TCM\_DESELECTALL message</span></span>

<span data-ttu-id="04232-106">Réinitialise des éléments dans un contrôle onglet, en effaçant tous ceux qui ont été définis sur l’état [**TCIS \_ BUTTONPRESSED**](tab-control-item-states.md) .</span><span class="sxs-lookup"><span data-stu-id="04232-106">Resets items in a tab control, clearing any that were set to the [**TCIS\_BUTTONPRESSED**](tab-control-item-states.md) state.</span></span> <span data-ttu-id="04232-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**TabCtrl \_ DeselectAll**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_deselectall) .</span><span class="sxs-lookup"><span data-stu-id="04232-107">You can send this message explicitly or by using the [**TabCtrl\_DeselectAll**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_deselectall) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="04232-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="04232-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04232-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="04232-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="04232-110">Indicateur qui spécifie la portée de la désélection de l’élément.</span><span class="sxs-lookup"><span data-stu-id="04232-110">Flag that specifies the scope of the item deselection.</span></span> <span data-ttu-id="04232-111">Si ce paramètre est défini sur **false**, tous les éléments d’onglet sont réinitialisés.</span><span class="sxs-lookup"><span data-stu-id="04232-111">If this parameter is set to **FALSE**, all tab items will be reset.</span></span> <span data-ttu-id="04232-112">S’il est défini sur **true**, tous les éléments d’onglet, à l’exception de celui qui est actuellement sélectionné, sont réinitialisés.</span><span class="sxs-lookup"><span data-stu-id="04232-112">If it is set to **TRUE**, then all tab items except for the one currently selected will be reset.</span></span>

</dd> <dt>

<span data-ttu-id="04232-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="04232-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="04232-114">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="04232-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04232-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="04232-115">Return value</span></span>

<span data-ttu-id="04232-116">La valeur de retour de ce message n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="04232-116">The return value for this message is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="04232-117">Notes</span><span class="sxs-lookup"><span data-stu-id="04232-117">Remarks</span></span>

<span data-ttu-id="04232-118">Ce message est significatif uniquement si l’indicateur de style de [**\_ boutons TCS**](tab-control-styles.md) a été défini.</span><span class="sxs-lookup"><span data-stu-id="04232-118">This message is only meaningful if the [**TCS\_BUTTONS**](tab-control-styles.md) style flag has been set.</span></span>

## <a name="requirements"></a><span data-ttu-id="04232-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="04232-119">Requirements</span></span>



| <span data-ttu-id="04232-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="04232-120">Requirement</span></span> | <span data-ttu-id="04232-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="04232-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="04232-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="04232-122">Minimum supported client</span></span><br/> | <span data-ttu-id="04232-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="04232-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="04232-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="04232-124">Minimum supported server</span></span><br/> | <span data-ttu-id="04232-125">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="04232-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="04232-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="04232-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="04232-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="04232-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





