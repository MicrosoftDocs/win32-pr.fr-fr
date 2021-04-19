---
title: Styles du contrôle Month Calendar (CommCtrl. h)
description: Les constantes de style suivantes sont utilisées lors de la création de contrôles Month Calendar.
ms.assetid: 8d9b2239-fd13-4579-81a2-0385fd318e83
topic_type:
- apiref
api_name:
- MCS_DAYSTATE
- MCS_MULTISELECT
- MCS_WEEKNUMBERS
- MCS_NOTODAYCIRCLE
- MCS_NOTODAY
- MCS_NOTRAILINGDATES
- MCS_SHORTDAYSOFWEEK
- MCS_NOSELCHANGEONNAV
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45ccef4a3cc8e16851c0676b8b0dce8c53cfdd27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528094"
---
# <a name="month-calendar-control-styles"></a><span data-ttu-id="1519d-103">Styles du contrôle calendrier du mois</span><span class="sxs-lookup"><span data-stu-id="1519d-103">Month Calendar Control Styles</span></span>

<span data-ttu-id="1519d-104">Les constantes de style suivantes sont utilisées lors de la création de contrôles Month Calendar.</span><span class="sxs-lookup"><span data-stu-id="1519d-104">The following style constants are used when creating month calendar controls.</span></span>



| <span data-ttu-id="1519d-105">Constante</span><span class="sxs-lookup"><span data-stu-id="1519d-105">Constant</span></span>                                                                                                                                                                           | <span data-ttu-id="1519d-106">Description</span><span class="sxs-lookup"><span data-stu-id="1519d-106">Description</span></span>                                                                                                                                                                                                                                                                                                          |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MCS_DAYSTATE"></span><span id="mcs_daystate"></span><dl> <span data-ttu-id="1519d-107"><dt>**\_DAYSTATE MCS**</dt></span><span class="sxs-lookup"><span data-stu-id="1519d-107"><dt>**MCS\_DAYSTATE**</dt></span></span> </dl>                         | <span data-ttu-id="1519d-108">[Version 4,70](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="1519d-108">[Version 4.70](common-control-versions.md).</span></span> <span data-ttu-id="1519d-109">Le calendrier du mois envoie des notifications [ \_ GETDAYSTATE MCN](mcn-getdaystate.md) pour demander des informations sur les jours qui doivent s’afficher en gras.</span><span class="sxs-lookup"><span data-stu-id="1519d-109">The month calendar sends [MCN\_GETDAYSTATE](mcn-getdaystate.md) notifications to request information about which days should be displayed in bold.</span></span><br/>                                                                                                          |
| <span id="MCS_MULTISELECT"></span><span id="mcs_multiselect"></span><dl> <span data-ttu-id="1519d-110"><dt>**MCS \_ MULTIselect**</dt></span><span class="sxs-lookup"><span data-stu-id="1519d-110"><dt>**MCS\_MULTISELECT**</dt></span></span> </dl>                | <span data-ttu-id="1519d-111">[Version 4,70](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="1519d-111">[Version 4.70](common-control-versions.md).</span></span> <span data-ttu-id="1519d-112">Le calendrier du mois permet à l’utilisateur de sélectionner une plage de dates dans le contrôle.</span><span class="sxs-lookup"><span data-stu-id="1519d-112">The month calendar enables the user to select a range of dates within the control.</span></span> <span data-ttu-id="1519d-113">Par défaut, la plage maximale est d’une semaine.</span><span class="sxs-lookup"><span data-stu-id="1519d-113">By default, the maximum range is one week.</span></span> <span data-ttu-id="1519d-114">Vous pouvez modifier la plage maximale pouvant être sélectionnée à l’aide du message [**MCM \_ SETMAXSELCOUNT**](mcm-setmaxselcount.md) .</span><span class="sxs-lookup"><span data-stu-id="1519d-114">You can change the maximum range that can be selected by using the [**MCM\_SETMAXSELCOUNT**](mcm-setmaxselcount.md) message.</span></span> <br/> |
| <span id="MCS_WEEKNUMBERS"></span><span id="mcs_weeknumbers"></span><dl> <span data-ttu-id="1519d-115"><dt>**\_WEEKNUMBERS MCS**</dt></span><span class="sxs-lookup"><span data-stu-id="1519d-115"><dt>**MCS\_WEEKNUMBERS**</dt></span></span> </dl>                | <span data-ttu-id="1519d-116">[Version 4,70](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="1519d-116">[Version 4.70](common-control-versions.md).</span></span> <span data-ttu-id="1519d-117">Le contrôle Month Calendar affiche les numéros de semaine (1-52) à gauche de chaque ligne de jours.</span><span class="sxs-lookup"><span data-stu-id="1519d-117">The month calendar control displays week numbers (1-52) to the left of each row of days.</span></span> <span data-ttu-id="1519d-118">La semaine 1 est définie comme la première semaine qui contient au moins quatre jours.</span><span class="sxs-lookup"><span data-stu-id="1519d-118">Week 1 is defined as the first week that contains at least four days.</span></span> <br/>                                                                                              |
| <span id="MCS_NOTODAYCIRCLE"></span><span id="mcs_notodaycircle"></span><dl> <span data-ttu-id="1519d-119"><dt>**\_NOTODAYCIRCLE MCS**</dt></span><span class="sxs-lookup"><span data-stu-id="1519d-119"><dt>**MCS\_NOTODAYCIRCLE**</dt></span></span> </dl>          | <span data-ttu-id="1519d-120">[Version 4,70](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="1519d-120">[Version 4.70](common-control-versions.md).</span></span> <span data-ttu-id="1519d-121">Le contrôle Month Calendar n’entoure pas la date « today ».</span><span class="sxs-lookup"><span data-stu-id="1519d-121">The month calendar control does not circle the "today" date.</span></span> <br/>                                                                                                                                                                                                |
| <span id="MCS_NOTODAY"></span><span id="mcs_notoday"></span><dl> <span data-ttu-id="1519d-122"><dt>**MCS \_ NOaujourd’hui**</dt></span><span class="sxs-lookup"><span data-stu-id="1519d-122"><dt>**MCS\_NOTODAY**</dt></span></span> </dl>                            | <span data-ttu-id="1519d-123">[Version 4,70](common-control-versions.md). Le contrôle Month Calendar n’affiche pas la date « today » en bas du contrôle.</span><span class="sxs-lookup"><span data-stu-id="1519d-123">[Version 4.70](common-control-versions.md).The month calendar control does not display the "today" date at the bottom of the control.</span></span> <br/>                                                                                                                                                                   |
| <span id="MCS_NOTRAILINGDATES"></span><span id="mcs_notrailingdates"></span><dl> <span data-ttu-id="1519d-124"><dt>**\_NOTRAILINGDATES MCS**</dt></span><span class="sxs-lookup"><span data-stu-id="1519d-124"><dt>**MCS\_NOTRAILINGDATES**</dt></span></span> </dl>    | <span data-ttu-id="1519d-125">**Windows Vista.**</span><span class="sxs-lookup"><span data-stu-id="1519d-125">**Windows Vista.**</span></span> <span data-ttu-id="1519d-126">Les dates des mois précédents et suivants ne sont pas affichées dans le calendrier du mois en cours.</span><span class="sxs-lookup"><span data-stu-id="1519d-126">Dates from the previous and next months are not displayed in the current month's calendar.</span></span><br/>                                                                                                                                                                                              |
| <span id="MCS_SHORTDAYSOFWEEK"></span><span id="mcs_shortdaysofweek"></span><dl> <span data-ttu-id="1519d-127"><dt>**\_SHORTDAYSOFWEEK MCS**</dt></span><span class="sxs-lookup"><span data-stu-id="1519d-127"><dt>**MCS\_SHORTDAYSOFWEEK**</dt></span></span> </dl>    | <span data-ttu-id="1519d-128">**Windows Vista.**</span><span class="sxs-lookup"><span data-stu-id="1519d-128">**Windows Vista.**</span></span> <span data-ttu-id="1519d-129">Les noms de jours courts s’affichent dans l’en-tête.</span><span class="sxs-lookup"><span data-stu-id="1519d-129">Short day names are displayed in the header.</span></span><br/>                                                                                                                                                                                                                                            |
| <span id="MCS_NOSELCHANGEONNAV"></span><span id="mcs_noselchangeonnav"></span><dl> <span data-ttu-id="1519d-130"><dt>**\_NOSELCHANGEONNAV MCS**</dt></span><span class="sxs-lookup"><span data-stu-id="1519d-130"><dt>**MCS\_NOSELCHANGEONNAV**</dt></span></span> </dl> | <span data-ttu-id="1519d-131">**Windows Vista.**</span><span class="sxs-lookup"><span data-stu-id="1519d-131">**Windows Vista.**</span></span> <span data-ttu-id="1519d-132">La sélection n’est pas modifiée lorsque l’utilisateur navigue vers le haut ou vers le haut dans le calendrier.</span><span class="sxs-lookup"><span data-stu-id="1519d-132">The selection is not changed when the user navigates next or previous in the calendar.</span></span> <span data-ttu-id="1519d-133">Cela permet à l’utilisateur de sélectionner une plage supérieure à celle qui est visible.</span><span class="sxs-lookup"><span data-stu-id="1519d-133">This allows the user to select a range larger than is visible.</span></span><br/>                                                                                                                                  |



## <a name="requirements"></a><span data-ttu-id="1519d-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1519d-134">Requirements</span></span>



| <span data-ttu-id="1519d-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1519d-135">Requirement</span></span> | <span data-ttu-id="1519d-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="1519d-136">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1519d-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="1519d-137">Header</span></span><br/> | <dl> <span data-ttu-id="1519d-138"><dt>CommCtrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1519d-138"><dt>CommCtrl.h</dt></span></span> </dl> |



 

 





