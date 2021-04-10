---
title: Message DTM_GETMCSTYLE (commctrl. h)
description: Obtient le style d’un contrôle de sélecteur de date et d’heure (PAO). Envoyez ce message explicitement ou à l’aide de la \_ macro DateTime GetMonthCalStyle.
ms.assetid: 8983898f-e23a-4247-838c-56364f695429
keywords:
- DTM_GETMCSTYLE les contrôles de message Windows
topic_type:
- apiref
api_name:
- DTM_GETMCSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cae82d271d0e9aece54046527dfa3bedcef657f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942492"
---
# <a name="dtm_getmcstyle-message"></a><span data-ttu-id="fef4e-105">\_Message DTM GETMCSTYLE</span><span class="sxs-lookup"><span data-stu-id="fef4e-105">DTM\_GETMCSTYLE message</span></span>

<span data-ttu-id="fef4e-106">Obtient le style d’un contrôle de sélecteur de date et d’heure (PAO).</span><span class="sxs-lookup"><span data-stu-id="fef4e-106">Gets the style of a date and time picker (DTP) control.</span></span> <span data-ttu-id="fef4e-107">Envoyez ce message explicitement ou à l’aide de la macro [**DateTime \_ GetMonthCalStyle**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalstyle) .</span><span class="sxs-lookup"><span data-stu-id="fef4e-107">Send this message explicitly or by using the [**DateTime\_GetMonthCalStyle**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalstyle) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="fef4e-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fef4e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fef4e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fef4e-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fef4e-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="fef4e-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="fef4e-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fef4e-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="fef4e-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="fef4e-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fef4e-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fef4e-113">Return value</span></span>

<span data-ttu-id="fef4e-114">Retourne la valeur de style du contrôle.</span><span class="sxs-lookup"><span data-stu-id="fef4e-114">Returns the style value of the control.</span></span> <span data-ttu-id="fef4e-115">Pour plus d’informations, consultez [styles du contrôle Month Calendar](month-calendar-control-styles.md).</span><span class="sxs-lookup"><span data-stu-id="fef4e-115">For more information see [Month Calendar Control Styles](month-calendar-control-styles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fef4e-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fef4e-116">Requirements</span></span>



| <span data-ttu-id="fef4e-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fef4e-117">Requirement</span></span> | <span data-ttu-id="fef4e-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="fef4e-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fef4e-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fef4e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="fef4e-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fef4e-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fef4e-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fef4e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="fef4e-122">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fef4e-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fef4e-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="fef4e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="fef4e-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="fef4e-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





