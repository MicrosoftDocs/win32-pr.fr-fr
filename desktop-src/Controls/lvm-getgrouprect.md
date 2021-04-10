---
title: Message LVM_GETGROUPRECT (commctrl. h)
description: Obtient le rectangle pour un groupe spécifié. Envoyez ce message explicitement ou à l’aide de la \_ macro ListView GetGroupRect.
ms.assetid: 9441a6c5-11d8-4f52-80dd-1b60befd9b9d
keywords:
- LVM_GETGROUPRECT les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_GETGROUPRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab2cbdfb1ec6e670e7b5d333694f3a1ca56d287b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941713"
---
# <a name="lvm_getgrouprect-message"></a><span data-ttu-id="34f47-105">\_Message GETGROUPRECT LVM</span><span class="sxs-lookup"><span data-stu-id="34f47-105">LVM\_GETGROUPRECT message</span></span>

<span data-ttu-id="34f47-106">Obtient le rectangle pour un groupe spécifié.</span><span class="sxs-lookup"><span data-stu-id="34f47-106">Gets the rectangle for a specified group.</span></span> <span data-ttu-id="34f47-107">Envoyez ce message explicitement ou à l’aide de la macro [**ListView \_ GetGroupRect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getgrouprect) .</span><span class="sxs-lookup"><span data-stu-id="34f47-107">Send this message explicitly or by using the [**ListView\_GetGroupRect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getgrouprect) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="34f47-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="34f47-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34f47-109">*wParam* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="34f47-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34f47-110">Spécifie le groupe par **iGroupId** (voir structure [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) ).</span><span class="sxs-lookup"><span data-stu-id="34f47-110">Specifies the group by **iGroupId** (see [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) structure).</span></span>

</dd> <dt>

<span data-ttu-id="34f47-111">*lParam* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="34f47-111">*lParam* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="34f47-112">Pointeur vers une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) pour recevoir des informations sur le groupe spécifié par *wParam*.</span><span class="sxs-lookup"><span data-stu-id="34f47-112">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure to receive information on the group specified by *wParam*.</span></span> <span data-ttu-id="34f47-113">Le récepteur de messages est chargé de définir les membres de structure avec les informations relatives au groupe spécifié par *wParam*.</span><span class="sxs-lookup"><span data-stu-id="34f47-113">The message receiver is responsible for setting the structure members with information for the group specified by *wParam*.</span></span>

<span data-ttu-id="34f47-114">Le processus appelant est chargé d’allouer de la mémoire pour la structure.</span><span class="sxs-lookup"><span data-stu-id="34f47-114">The calling process is responsible for allocating memory for the structure.</span></span> <span data-ttu-id="34f47-115">Définissez le membre **supérieur** du [**Rect**](/previous-versions//dd162897(v=vs.85)) sur l’un des indicateurs suivants pour spécifier les coordonnées du rectangle à récupérer.</span><span class="sxs-lookup"><span data-stu-id="34f47-115">Set the **top** member of the [**RECT**](/previous-versions//dd162897(v=vs.85)) to one of the following flags to specify the coordinates of the rectangle to get.</span></span>



| <span data-ttu-id="34f47-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="34f47-116">Value</span></span>                                                                                                                                                                  | <span data-ttu-id="34f47-117">Signification</span><span class="sxs-lookup"><span data-stu-id="34f47-117">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LVGGR_GROUP"></span><span id="lvggr_group"></span><dl> <span data-ttu-id="34f47-118"><dt>**\_groupe LVGGR**</dt></span><span class="sxs-lookup"><span data-stu-id="34f47-118"><dt>**LVGGR\_GROUP**</dt></span></span> </dl>                | <span data-ttu-id="34f47-119">Coordonnées de l’ensemble du groupe développé.</span><span class="sxs-lookup"><span data-stu-id="34f47-119">Coordinates of the entire expanded group.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="LVGGR_HEADER"></span><span id="lvggr_header"></span><dl> <span data-ttu-id="34f47-120"><dt>**\_en-tête LVGGR**</dt></span><span class="sxs-lookup"><span data-stu-id="34f47-120"><dt>**LVGGR\_HEADER**</dt></span></span> </dl>             | <span data-ttu-id="34f47-121">Coordonnées de l’en-tête uniquement (groupe réduit).</span><span class="sxs-lookup"><span data-stu-id="34f47-121">Coordinates of the header only (collapsed group).</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="LVGGR_LABEL"></span><span id="lvggr_label"></span><dl> <span data-ttu-id="34f47-122"><dt>**\_étiquette LVGGR**</dt></span><span class="sxs-lookup"><span data-stu-id="34f47-122"><dt>**LVGGR\_LABEL**</dt></span></span> </dl>                | <span data-ttu-id="34f47-123">Coordonnées de l’étiquette uniquement.</span><span class="sxs-lookup"><span data-stu-id="34f47-123">Coordinates of the label only.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="LVGGR_SUBSETLINK"></span><span id="lvggr_subsetlink"></span><dl> <span data-ttu-id="34f47-124"><dt>**LVGGR \_ SUBSETLINK**</dt></span><span class="sxs-lookup"><span data-stu-id="34f47-124"><dt>**LVGGR\_SUBSETLINK**</dt></span></span> </dl> | <span data-ttu-id="34f47-125">Coordonnées du lien du sous-ensemble uniquement (sous-ensemble de balises).</span><span class="sxs-lookup"><span data-stu-id="34f47-125">Coordinates of the subset link only (markup subset).</span></span> <span data-ttu-id="34f47-126">Un contrôle List-View peut limiter le nombre d’éléments visibles affichés dans chaque groupe.</span><span class="sxs-lookup"><span data-stu-id="34f47-126">A list-view control can limit the number of visible items displayed in each group.</span></span> <span data-ttu-id="34f47-127">Un lien est présenté à l’utilisateur pour permettre à l’utilisateur de développer le groupe.</span><span class="sxs-lookup"><span data-stu-id="34f47-127">A link is presented to the user to allow the user to expand the group.</span></span> <span data-ttu-id="34f47-128">Cet indicateur retourne le rectangle englobant du lien du sous-ensemble si le groupe est un sous-ensemble (État du groupe de LVGS \_ sous-ensemble, consultez structure [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup), **État** du membre).</span><span class="sxs-lookup"><span data-stu-id="34f47-128">This flag will return the bounding rectangle of the subset link if the group is a subset (group state of LVGS\_SUBSETED, see structure [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup), member **state**).</span></span> <span data-ttu-id="34f47-129">Cet indicateur est fourni afin que les applications d’accessibilité puissent localiser le lien.</span><span class="sxs-lookup"><span data-stu-id="34f47-129">This flag is provided so that accessibility applications can located the link.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34f47-130">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="34f47-130">Return value</span></span>

<span data-ttu-id="34f47-131">Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="34f47-131">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="34f47-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="34f47-132">Requirements</span></span>



| <span data-ttu-id="34f47-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="34f47-133">Requirement</span></span> | <span data-ttu-id="34f47-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="34f47-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="34f47-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="34f47-135">Minimum supported client</span></span><br/> | <span data-ttu-id="34f47-136">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="34f47-136">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="34f47-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="34f47-137">Minimum supported server</span></span><br/> | <span data-ttu-id="34f47-138">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="34f47-138">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="34f47-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="34f47-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="34f47-140"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="34f47-140"><dt>Commctrl.h</dt></span></span> </dl> |



 

