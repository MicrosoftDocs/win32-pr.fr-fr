---
title: Message MCM_SETMAXSELCOUNT (commctrl. h)
description: Définit le nombre maximal de jours pouvant être sélectionnés dans un contrôle Month Calendar. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro calendrier monthcal SetMaxSelCount.
ms.assetid: 190453ab-e53b-4db7-82c1-f9d50188ad39
keywords:
- MCM_SETMAXSELCOUNT les contrôles de message Windows
topic_type:
- apiref
api_name:
- MCM_SETMAXSELCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c67bcb7191bb20b9688c2fe1ffc2b458ecb7b8a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844270"
---
# <a name="mcm_setmaxselcount-message"></a><span data-ttu-id="66057-105">\_Message SETMAXSELCOUNT MCM</span><span class="sxs-lookup"><span data-stu-id="66057-105">MCM\_SETMAXSELCOUNT message</span></span>

<span data-ttu-id="66057-106">Définit le nombre maximal de jours pouvant être sélectionnés dans un contrôle Month Calendar.</span><span class="sxs-lookup"><span data-stu-id="66057-106">Sets the maximum number of days that can be selected in a month calendar control.</span></span> <span data-ttu-id="66057-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**calendrier monthcal \_ SetMaxSelCount**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setmaxselcount) .</span><span class="sxs-lookup"><span data-stu-id="66057-107">You can send this message explicitly or by using the [**MonthCal\_SetMaxSelCount**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setmaxselcount) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="66057-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="66057-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66057-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="66057-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="66057-110">Valeur de type **int** qui sera définie pour représenter le nombre maximal de jours pouvant être sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="66057-110">Value of type **int** that will be set to represent the maximum number of days that can be selected.</span></span>

</dd> <dt>

<span data-ttu-id="66057-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="66057-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="66057-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="66057-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66057-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="66057-113">Return value</span></span>

<span data-ttu-id="66057-114">Retourne une valeur différente de zéro en cas de réussite, ou zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="66057-114">Returns nonzero if successful, or zero otherwise.</span></span> <span data-ttu-id="66057-115">Ce message échouera s’il est appliqué à un contrôle Month Calendar qui n’utilise pas le style [**MCS \_ MultiSelect**](month-calendar-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="66057-115">This message will fail if applied to a month calendar control that does not use the [**MCS\_MULTISELECT**](month-calendar-control-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="66057-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="66057-116">Requirements</span></span>



| <span data-ttu-id="66057-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="66057-117">Requirement</span></span> | <span data-ttu-id="66057-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="66057-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="66057-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="66057-119">Minimum supported client</span></span><br/> | <span data-ttu-id="66057-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="66057-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="66057-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="66057-121">Minimum supported server</span></span><br/> | <span data-ttu-id="66057-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="66057-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="66057-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="66057-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="66057-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="66057-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





