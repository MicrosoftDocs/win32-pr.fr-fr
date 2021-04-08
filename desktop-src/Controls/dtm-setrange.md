---
title: Message DTM_SETRANGE (commctrl. h)
description: Définit les heures système minimale et maximale autorisées pour un contrôle de sélecteur de dates et d’heures (PAO). Vous pouvez envoyer ce message explicitement ou utiliser la \_ macro DateTime SetRange.
ms.assetid: ef0f48f2-906e-4ae0-839d-177e0fb7f14e
keywords:
- DTM_SETRANGE les contrôles de message Windows
topic_type:
- apiref
api_name:
- DTM_SETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70578e7d468c6a0e54d1373af2d46e680afbbe5b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742557"
---
# <a name="dtm_setrange-message"></a><span data-ttu-id="6e888-105">\_Message DTM SEtrange</span><span class="sxs-lookup"><span data-stu-id="6e888-105">DTM\_SETRANGE message</span></span>

<span data-ttu-id="6e888-106">Définit les heures système minimale et maximale autorisées pour un contrôle de sélecteur de dates et d’heures (PAO).</span><span class="sxs-lookup"><span data-stu-id="6e888-106">Sets the minimum and maximum allowable system times for a date and time picker (DTP) control.</span></span> <span data-ttu-id="6e888-107">Vous pouvez envoyer ce message explicitement ou utiliser la macro [**DateTime \_ SetRange**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setrange) .</span><span class="sxs-lookup"><span data-stu-id="6e888-107">You can send this message explicitly or use the [**DateTime\_SetRange**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setrange) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="6e888-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6e888-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e888-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6e888-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6e888-110">Valeur qui spécifie les valeurs de plage valides.</span><span class="sxs-lookup"><span data-stu-id="6e888-110">A value specifying which range values are valid.</span></span> <span data-ttu-id="6e888-111">Ce paramètre peut être une combinaison des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="6e888-111">This parameter can be a combination of the following values:</span></span>



| <span data-ttu-id="6e888-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="6e888-112">Value</span></span>                                                                                                                                          | <span data-ttu-id="6e888-113">Signification</span><span class="sxs-lookup"><span data-stu-id="6e888-113">Meaning</span></span>                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GDTR_MIN"></span><span id="gdtr_min"></span><dl> <span data-ttu-id="6e888-114"><dt>**GDTR \_ min.**</dt></span><span class="sxs-lookup"><span data-stu-id="6e888-114"><dt>**GDTR\_MIN**</dt></span></span> </dl> | <span data-ttu-id="6e888-115">Le premier élément du tableau de la structure [**SystemTime**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) est valide et sera utilisé pour définir l’heure minimale autorisée du système.</span><span class="sxs-lookup"><span data-stu-id="6e888-115">The first element in the [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure array is valid and will be used to set the minimum allowable system time.</span></span><br/>  |
| <span id="GDTR_MAX"></span><span id="gdtr_max"></span><dl> <span data-ttu-id="6e888-116"><dt>**GDTR \_ Max**</dt></span><span class="sxs-lookup"><span data-stu-id="6e888-116"><dt>**GDTR\_MAX**</dt></span></span> </dl> | <span data-ttu-id="6e888-117">Le deuxième élément du tableau de la structure [**SystemTime**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) est valide et sera utilisé pour définir l’heure maximale autorisée du système.</span><span class="sxs-lookup"><span data-stu-id="6e888-117">The second element in the [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure array is valid and will be used to set the maximum allowable system time.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="6e888-118">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6e888-118">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6e888-119">Pointeur vers un tableau à deux éléments de structures [**SystemTime**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) .</span><span class="sxs-lookup"><span data-stu-id="6e888-119">A pointer to a two-element array of [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structures.</span></span> <span data-ttu-id="6e888-120">Le premier élément du tableau **SystemTime** contient l’heure minimale autorisée.</span><span class="sxs-lookup"><span data-stu-id="6e888-120">The first element of the **SYSTEMTIME** array contains the minimum allowable time.</span></span> <span data-ttu-id="6e888-121">Le deuxième élément du tableau **SystemTime** contient le temps maximum autorisé.</span><span class="sxs-lookup"><span data-stu-id="6e888-121">The second element of the **SYSTEMTIME** array contains the maximum allowable time.</span></span> <span data-ttu-id="6e888-122">Il n’est pas nécessaire de remplir un élément de tableau qui n’est pas spécifié dans le paramètre *wParam* .</span><span class="sxs-lookup"><span data-stu-id="6e888-122">It is not necessary to fill an array element that is not specified in the *wParam* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e888-123">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6e888-123">Return value</span></span>

<span data-ttu-id="6e888-124">Retourne une valeur différente de zéro en cas de réussite, ou zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="6e888-124">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="6e888-125">Notes</span><span class="sxs-lookup"><span data-stu-id="6e888-125">Remarks</span></span>

<span data-ttu-id="6e888-126">Le sélecteur de date et d’heure affiche uniquement les dates/heures qui se trouvent dans la plage spécifiée, ce qui empêche l’utilisateur de sélectionner une date et une heure situées en dehors de la plage.</span><span class="sxs-lookup"><span data-stu-id="6e888-126">The date and time picker displays only dates/times that fall within the specified range, preventing the user from selecting a date and time that falls outside the range.</span></span> <span data-ttu-id="6e888-127">Si le message [**DTM \_ SETSYSTEMTIME**](dtm-setsystemtime.md) spécifie une date et une heure qui se situent en dehors de la plage, l’opération échoue.</span><span class="sxs-lookup"><span data-stu-id="6e888-127">If the [**DTM\_SETSYSTEMTIME**](dtm-setsystemtime.md) message specifies a date and time that falls outside the range, it will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e888-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6e888-128">Requirements</span></span>



| <span data-ttu-id="6e888-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6e888-129">Requirement</span></span> | <span data-ttu-id="6e888-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="6e888-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6e888-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6e888-131">Minimum supported client</span></span><br/> | <span data-ttu-id="6e888-132">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6e888-132">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6e888-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6e888-133">Minimum supported server</span></span><br/> | <span data-ttu-id="6e888-134">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6e888-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6e888-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="6e888-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="6e888-136"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6e888-136"><dt>Commctrl.h</dt></span></span> </dl> |



 

