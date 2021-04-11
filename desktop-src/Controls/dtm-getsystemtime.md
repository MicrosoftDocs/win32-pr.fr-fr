---
title: Message DTM_GETSYSTEMTIME (commctrl. h)
description: Obtient l’heure actuellement sélectionnée à partir d’un contrôle de sélecteur de dates et d’heures (PAO) et la place dans une structure SYSTEMTIME spécifiée. Vous pouvez envoyer ce message de manière explicite ou utiliser la \_ macro DateTime GetSystemtime.
ms.assetid: 81c95187-109c-4b36-98ea-a2e77ce42d9a
keywords:
- DTM_GETSYSTEMTIME les contrôles de message Windows
topic_type:
- apiref
api_name:
- DTM_GETSYSTEMTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e14d8c998720cc987a03877e1918e97304bf769
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104842"
---
# <a name="dtm_getsystemtime-message"></a><span data-ttu-id="9b28c-105">\_Message DTM GETSYSTEMTIME</span><span class="sxs-lookup"><span data-stu-id="9b28c-105">DTM\_GETSYSTEMTIME message</span></span>

<span data-ttu-id="9b28c-106">Obtient l’heure actuellement sélectionnée à partir d’un contrôle de sélecteur de dates et d’heures (PAO) et la place dans une structure [**SystemTime**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) spécifiée.</span><span class="sxs-lookup"><span data-stu-id="9b28c-106">Gets the currently selected time from a date and time picker (DTP) control and places it in a specified [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure.</span></span> <span data-ttu-id="9b28c-107">Vous pouvez envoyer ce message de manière explicite ou utiliser la macro [**DateTime \_ GetSystemtime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getsystemtime) .</span><span class="sxs-lookup"><span data-stu-id="9b28c-107">You can send this message explicitly or use the [**DateTime\_GetSystemtime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getsystemtime) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="9b28c-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9b28c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b28c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9b28c-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="9b28c-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="9b28c-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="9b28c-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9b28c-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9b28c-112">Pointeur vers une structure [**SystemTime**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) .</span><span class="sxs-lookup"><span data-stu-id="9b28c-112">A pointer to a [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure.</span></span> <span data-ttu-id="9b28c-113">Si **DTM \_ GETSYSTEMTIME** retourne GDT \_ valide, cette structure contiendra l’heure actuellement sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="9b28c-113">If **DTM\_GETSYSTEMTIME** returns GDT\_VALID, this structure will contain the currently selected time.</span></span> <span data-ttu-id="9b28c-114">Dans le cas contraire, il ne contient pas d’informations valides.</span><span class="sxs-lookup"><span data-stu-id="9b28c-114">Otherwise, it will not contain valid information.</span></span> <span data-ttu-id="9b28c-115">Ce paramètre doit être un pointeur valide ; elle ne peut pas être **null**.</span><span class="sxs-lookup"><span data-stu-id="9b28c-115">This parameter must be a valid pointer; it cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b28c-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9b28c-116">Return value</span></span>

<span data-ttu-id="9b28c-117">Retourne GDT \_ valide si les informations d’heure ont été placées avec succès dans *lParam*.</span><span class="sxs-lookup"><span data-stu-id="9b28c-117">Returns GDT\_VALID if the time information was successfully placed in *lParam*.</span></span> <span data-ttu-id="9b28c-118">Retourne GDT \_ None si le contrôle a été défini sur le style [**DTS \_ SHOWNONE**](date-and-time-picker-control-styles.md) et que la case à cocher Control n’a pas été activée.</span><span class="sxs-lookup"><span data-stu-id="9b28c-118">Returns GDT\_NONE if the control was set to the [**DTS\_SHOWNONE**](date-and-time-picker-control-styles.md) style and the control check box was not selected.</span></span> <span data-ttu-id="9b28c-119">Retourne \_ une erreur GDT si une erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="9b28c-119">Returns GDT\_ERROR if an error occurs.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b28c-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9b28c-120">Requirements</span></span>



| <span data-ttu-id="9b28c-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9b28c-121">Requirement</span></span> | <span data-ttu-id="9b28c-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="9b28c-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9b28c-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9b28c-123">Minimum supported client</span></span><br/> | <span data-ttu-id="9b28c-124">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9b28c-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9b28c-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9b28c-125">Minimum supported server</span></span><br/> | <span data-ttu-id="9b28c-126">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9b28c-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9b28c-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="9b28c-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="9b28c-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9b28c-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

