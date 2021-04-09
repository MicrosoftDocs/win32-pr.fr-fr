---
title: Message MCM_GETMONTHDELTA (commctrl. h)
description: Récupère la vitesse de défilement pour un contrôle Month Calendar. La vitesse de défilement est le nombre de mois pendant lesquels le contrôle déplace son affichage lorsque l’utilisateur clique sur un bouton de défilement. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro calendrier monthcal GetMonthDelta.
ms.assetid: 6db02993-b22c-430f-8928-8bd5768b2151
keywords:
- MCM_GETMONTHDELTA les contrôles de message Windows
topic_type:
- apiref
api_name:
- MCM_GETMONTHDELTA
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01eaa40b930e6317cc2be6b674f0cea58115ae40
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106660"
---
# <a name="mcm_getmonthdelta-message"></a><span data-ttu-id="97c40-106">\_Message GETMONTHDELTA MCM</span><span class="sxs-lookup"><span data-stu-id="97c40-106">MCM\_GETMONTHDELTA message</span></span>

<span data-ttu-id="97c40-107">Récupère la vitesse de défilement pour un contrôle Month Calendar.</span><span class="sxs-lookup"><span data-stu-id="97c40-107">Retrieves the scroll rate for a month calendar control.</span></span> <span data-ttu-id="97c40-108">La vitesse de défilement est le nombre de mois pendant lesquels le contrôle déplace son affichage lorsque l’utilisateur clique sur un bouton de défilement.</span><span class="sxs-lookup"><span data-stu-id="97c40-108">The scroll rate is the number of months that the control moves its display when the user clicks a scroll button.</span></span> <span data-ttu-id="97c40-109">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**calendrier monthcal \_ GetMonthDelta**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getmonthdelta) .</span><span class="sxs-lookup"><span data-stu-id="97c40-109">You can send this message explicitly or by using the [**MonthCal\_GetMonthDelta**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getmonthdelta) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="97c40-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="97c40-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97c40-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="97c40-111">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="97c40-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="97c40-112">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="97c40-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="97c40-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="97c40-114">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="97c40-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97c40-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="97c40-115">Return value</span></span>

<span data-ttu-id="97c40-116">Si le delta du mois a été défini précédemment à l’aide du message [**MCM \_ SETMONTHDELTA**](mcm-setmonthdelta.md) , retourne une valeur int qui représente la vitesse de défilement actuelle du calendrier du mois.</span><span class="sxs-lookup"><span data-stu-id="97c40-116">If the month delta was previously set using the [**MCM\_SETMONTHDELTA**](mcm-setmonthdelta.md) message, returns an INT value that represents the month calendar's current scroll rate.</span></span> <span data-ttu-id="97c40-117">Si le delta du mois n’a pas été défini précédemment à l’aide du message **MCM \_ SETMONTHDELTA** ou si le delta du mois a été réinitialisé à la valeur par défaut, retourne une valeur int qui représente le nombre actuel de mois visibles.</span><span class="sxs-lookup"><span data-stu-id="97c40-117">If the month delta was not previously set using the **MCM\_SETMONTHDELTA** message, or the month delta was reset to the default, returns an INT value that represents the current number of months visible.</span></span>

## <a name="requirements"></a><span data-ttu-id="97c40-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="97c40-118">Requirements</span></span>



| <span data-ttu-id="97c40-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="97c40-119">Requirement</span></span> | <span data-ttu-id="97c40-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="97c40-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="97c40-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="97c40-121">Minimum supported client</span></span><br/> | <span data-ttu-id="97c40-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="97c40-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="97c40-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="97c40-123">Minimum supported server</span></span><br/> | <span data-ttu-id="97c40-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="97c40-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="97c40-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="97c40-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="97c40-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="97c40-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





