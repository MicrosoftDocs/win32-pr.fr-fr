---
title: Message MCM_SETMONTHDELTA (commctrl. h)
description: Définit la vitesse de défilement pour un contrôle Month Calendar. La vitesse de défilement est le nombre de mois pendant lesquels le contrôle déplace son affichage lorsque l’utilisateur clique sur un bouton de défilement. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro calendrier monthcal SetMonthDelta.
ms.assetid: 2d01b95f-3be8-4548-80b5-ac01d3e49e9f
keywords:
- MCM_SETMONTHDELTA les contrôles de message Windows
topic_type:
- apiref
api_name:
- MCM_SETMONTHDELTA
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 123eddb55a7ee8ddf8e3f6d8136e9ee57dfc8681
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106513827"
---
# <a name="mcm_setmonthdelta-message"></a><span data-ttu-id="f567a-106">\_Message SETMONTHDELTA MCM</span><span class="sxs-lookup"><span data-stu-id="f567a-106">MCM\_SETMONTHDELTA message</span></span>

<span data-ttu-id="f567a-107">Définit la vitesse de défilement pour un contrôle Month Calendar.</span><span class="sxs-lookup"><span data-stu-id="f567a-107">Sets the scroll rate for a month calendar control.</span></span> <span data-ttu-id="f567a-108">La vitesse de défilement est le nombre de mois pendant lesquels le contrôle déplace son affichage lorsque l’utilisateur clique sur un bouton de défilement.</span><span class="sxs-lookup"><span data-stu-id="f567a-108">The scroll rate is the number of months that the control moves its display when the user clicks a scroll button.</span></span> <span data-ttu-id="f567a-109">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**calendrier monthcal \_ SetMonthDelta**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setmonthdelta) .</span><span class="sxs-lookup"><span data-stu-id="f567a-109">You can send this message explicitly or by using the [**MonthCal\_SetMonthDelta**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setmonthdelta) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="f567a-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f567a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f567a-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f567a-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f567a-112">Valeur représentant le nombre de mois à définir comme taux de défilement du contrôle.</span><span class="sxs-lookup"><span data-stu-id="f567a-112">Value representing the number of months to be set as the control's scroll rate.</span></span> <span data-ttu-id="f567a-113">Si cette valeur est égale à zéro, le delta du mois est rétabli à la valeur par défaut, qui est le nombre de mois affichés dans le contrôle.</span><span class="sxs-lookup"><span data-stu-id="f567a-113">If this value is zero, the month delta is reset to the default, which is the number of months displayed in the control.</span></span>

</dd> <dt>

<span data-ttu-id="f567a-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f567a-114">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="f567a-115">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="f567a-115">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f567a-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f567a-116">Return value</span></span>

<span data-ttu-id="f567a-117">Retourne une valeur INT qui représente la vitesse de défilement précédente.</span><span class="sxs-lookup"><span data-stu-id="f567a-117">Returns an INT value that represents the previous scroll rate.</span></span> <span data-ttu-id="f567a-118">Si la vitesse de défilement n’a pas été définie précédemment, la valeur de retour est zéro.</span><span class="sxs-lookup"><span data-stu-id="f567a-118">If the scroll rate was not previously set, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="f567a-119">Notes</span><span class="sxs-lookup"><span data-stu-id="f567a-119">Remarks</span></span>

<span data-ttu-id="f567a-120">Les touches PAGE précédente et PAGE suivante, VK \_ avant et VK \_ suivant, modifient le mois sélectionné d’une unité, quel que soit le nombre de mois affichés ou la valeur définie par **MCM \_ SETMONTHDELTA**.</span><span class="sxs-lookup"><span data-stu-id="f567a-120">The PAGE UP and PAGE DOWN keys, VK\_PRIOR and VK\_NEXT, change the selected month by one, regardless of the number of months displayed or the value set by **MCM\_SETMONTHDELTA**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f567a-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f567a-121">Requirements</span></span>



| <span data-ttu-id="f567a-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f567a-122">Requirement</span></span> | <span data-ttu-id="f567a-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="f567a-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f567a-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f567a-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f567a-125">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f567a-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f567a-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f567a-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f567a-127">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f567a-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f567a-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="f567a-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="f567a-129"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f567a-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





