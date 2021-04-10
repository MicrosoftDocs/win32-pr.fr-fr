---
title: Message DTM_SETMCSTYLE (commctrl. h)
description: Définit le style d’un contrôle de sélecteur de dates et d’heures (PAO). Envoyez ce message explicitement ou à l’aide de la \_ macro DateTime SetMonthCalStyle.
ms.assetid: 6b480a1e-c76e-4026-ab2a-5ec53df6fa28
keywords:
- DTM_SETMCSTYLE les contrôles de message Windows
topic_type:
- apiref
api_name:
- DTM_SETMCSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3691dfbd62847bc490c3a45e1d640d19b09cca6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104839"
---
# <a name="dtm_setmcstyle-message"></a><span data-ttu-id="c890c-105">\_Message DTM SETMCSTYLE</span><span class="sxs-lookup"><span data-stu-id="c890c-105">DTM\_SETMCSTYLE message</span></span>

<span data-ttu-id="c890c-106">Définit le style d’un contrôle de sélecteur de dates et d’heures (PAO).</span><span class="sxs-lookup"><span data-stu-id="c890c-106">Sets the style of a date and time picker (DTP) control.</span></span> <span data-ttu-id="c890c-107">Envoyez ce message explicitement ou à l’aide de la macro [**DateTime \_ SetMonthCalStyle**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalstyle) .</span><span class="sxs-lookup"><span data-stu-id="c890c-107">Send this message explicitly or by using the [**DateTime\_SetMonthCalStyle**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalstyle) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="c890c-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c890c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c890c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c890c-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c890c-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="c890c-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="c890c-111">*lParam* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c890c-111">*lParam* \[in\]</span></span>
</dt> <dd><span data-ttu-id="c890c-112">Valeur de style.</span><span class="sxs-lookup"><span data-stu-id="c890c-112">A style value.</span></span> <span data-ttu-id="c890c-113">Pour plus d’informations, consultez <a href="month-calendar-control-styles.md">styles du contrôle Month Calendar</a>.</span><span class="sxs-lookup"><span data-stu-id="c890c-113">For more information see <a href="month-calendar-control-styles.md">Month Calendar Control Styles</a>.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c890c-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c890c-114">Return value</span></span>

<span data-ttu-id="c890c-115">Retourne la valeur du style précédent.</span><span class="sxs-lookup"><span data-stu-id="c890c-115">Returns the value of the previous style.</span></span>

## <a name="requirements"></a><span data-ttu-id="c890c-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c890c-116">Requirements</span></span>



| <span data-ttu-id="c890c-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c890c-117">Requirement</span></span> | <span data-ttu-id="c890c-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="c890c-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c890c-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c890c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c890c-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c890c-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c890c-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c890c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c890c-122">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c890c-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c890c-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="c890c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c890c-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c890c-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





