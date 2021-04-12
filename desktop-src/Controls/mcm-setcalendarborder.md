---
title: Message MCM_SETCALENDARBORDER (commctrl. h)
description: Définit la taille de la bordure, en pixels. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro calendrier monthcal SetCalendarBorder.
ms.assetid: 2a64a08f-a1fb-47a8-8f09-725807e87a03
keywords:
- MCM_SETCALENDARBORDER les contrôles de message Windows
topic_type:
- apiref
api_name:
- MCM_SETCALENDARBORDER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09b870346e8d8b475833657dd83141ba1fe11715
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465247"
---
# <a name="mcm_setcalendarborder-message"></a><span data-ttu-id="b69e7-105">\_Message SETCALENDARBORDER MCM</span><span class="sxs-lookup"><span data-stu-id="b69e7-105">MCM\_SETCALENDARBORDER message</span></span>

<span data-ttu-id="b69e7-106">Définit la taille de la bordure, en pixels.</span><span class="sxs-lookup"><span data-stu-id="b69e7-106">Sets the size of the border, in pixels.</span></span> <span data-ttu-id="b69e7-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**calendrier monthcal \_ SetCalendarBorder**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcalendarborder) .</span><span class="sxs-lookup"><span data-stu-id="b69e7-107">You can send this message explicitly or by using the [**MonthCal\_SetCalendarBorder**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcalendarborder) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="b69e7-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b69e7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b69e7-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b69e7-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b69e7-110">Si la **valeur est true**, la taille de la bordure est définie sur le nombre de pixels que le *lParam* spécifie.</span><span class="sxs-lookup"><span data-stu-id="b69e7-110">If **TRUE**, then the border size is set to the number of pixels that *lParam* specifies.</span></span> <span data-ttu-id="b69e7-111">Si la valeur est **false**, la taille de la bordure est réinitialisée à la valeur par défaut spécifiée par le thème, ou zéro si les thèmes ne sont pas utilisés.</span><span class="sxs-lookup"><span data-stu-id="b69e7-111">If **FALSE**, then the border size is reset to the default value specified by the theme, or zero if themes are not being used.</span></span>

</dd> <dt>

<span data-ttu-id="b69e7-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b69e7-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b69e7-113">Nombre de pixels de la taille de la bordure.</span><span class="sxs-lookup"><span data-stu-id="b69e7-113">Number of pixels of the border size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b69e7-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b69e7-114">Return value</span></span>

<span data-ttu-id="b69e7-115">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="b69e7-115">Not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="b69e7-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b69e7-116">Requirements</span></span>



| <span data-ttu-id="b69e7-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b69e7-117">Requirement</span></span> | <span data-ttu-id="b69e7-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="b69e7-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b69e7-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b69e7-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b69e7-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b69e7-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b69e7-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b69e7-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b69e7-122">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b69e7-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b69e7-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="b69e7-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b69e7-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b69e7-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





