---
title: Message LVM_GETITEMINDEXRECT (commctrl. h)
description: Récupère le rectangle englobant pour l’intégralité ou une partie d’un sous-élément dans l’affichage actuel d’un contrôle List View. Envoyez ce message explicitement ou à l’aide de la \_ macro ListView GetItemIndexRect.
ms.assetid: 17704d24-c029-4d41-b198-04d1e78698e0
keywords:
- LVM_GETITEMINDEXRECT les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_GETITEMINDEXRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31ccd114713326c4796ca69f56fc2c38daf145db
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466511"
---
# <a name="lvm_getitemindexrect-message"></a><span data-ttu-id="b1fad-105">\_Message GETITEMINDEXRECT LVM</span><span class="sxs-lookup"><span data-stu-id="b1fad-105">LVM\_GETITEMINDEXRECT message</span></span>

<span data-ttu-id="b1fad-106">Récupère le rectangle englobant pour l’intégralité ou une partie d’un sous-élément dans l’affichage actuel d’un contrôle List View.</span><span class="sxs-lookup"><span data-stu-id="b1fad-106">Retrieves the bounding rectangle for all or part of a subitem in the current view of a list-view control.</span></span> <span data-ttu-id="b1fad-107">Envoyez ce message explicitement ou à l’aide de la macro [**ListView \_ GetItemIndexRect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemindexrect) .</span><span class="sxs-lookup"><span data-stu-id="b1fad-107">Send this message explicitly or by using the [**ListView\_GetItemIndexRect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemindexrect) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="b1fad-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b1fad-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1fad-109">*wParam* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b1fad-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1fad-110">Pointeur vers une structure [**LVITEMINDEX**](/windows/win32/api/commctrl/ns-commctrl-lvitemindex) pour l’élément parent du sous-élément.</span><span class="sxs-lookup"><span data-stu-id="b1fad-110">A pointer to a [**LVITEMINDEX**](/windows/win32/api/commctrl/ns-commctrl-lvitemindex) structure for the parent item of the subitem.</span></span> <span data-ttu-id="b1fad-111">Le processus appelant est responsable de l’allocation de cette structure et de la définition de ses membres.</span><span class="sxs-lookup"><span data-stu-id="b1fad-111">The calling process is responsible for allocating this structure and setting its members.</span></span> <span data-ttu-id="b1fad-112">*wParam* ne doit pas être **null**.</span><span class="sxs-lookup"><span data-stu-id="b1fad-112">*wParam* must not be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b1fad-113">*lParam* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="b1fad-113">*lParam* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b1fad-114">Pointeur vers une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) pour recevoir les coordonnées.</span><span class="sxs-lookup"><span data-stu-id="b1fad-114">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure to receive the coordinates.</span></span> <span data-ttu-id="b1fad-115">Le processus appelant est chargé d’allouer cette structure.</span><span class="sxs-lookup"><span data-stu-id="b1fad-115">The calling process is responsible for allocating this structure.</span></span> <span data-ttu-id="b1fad-116">*lParam* ne doit pas avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="b1fad-116">*lParam* must not be **NULL**.</span></span> <span data-ttu-id="b1fad-117">Définissez le membre **supérieur** sur l’index du sous-élément.</span><span class="sxs-lookup"><span data-stu-id="b1fad-117">Set the **top** member to the index of the subitem.</span></span> <span data-ttu-id="b1fad-118">Définissez le membre de **gauche** sur l’une des valeurs suivantes, indiquant la partie du sous-élément pour laquelle le rectangle englobant doit être récupéré.</span><span class="sxs-lookup"><span data-stu-id="b1fad-118">Set the **left** member to one of the following values, indicating the part of the subitem for which the bounding rectangle is to be retrieved.</span></span>



| <span data-ttu-id="b1fad-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="b1fad-119">Value</span></span>                                                                                                                                                   | <span data-ttu-id="b1fad-120">Signification</span><span class="sxs-lookup"><span data-stu-id="b1fad-120">Meaning</span></span>                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="LVIR_BOUNDS"></span><span id="lvir_bounds"></span><dl> <span data-ttu-id="b1fad-121"><dt>**\_limites LVIR**</dt></span><span class="sxs-lookup"><span data-stu-id="b1fad-121"><dt>**LVIR\_BOUNDS**</dt></span></span> </dl> | <span data-ttu-id="b1fad-122">Retourne le rectangle englobant du sous-élément entier, y compris l’icône et l’étiquette.</span><span class="sxs-lookup"><span data-stu-id="b1fad-122">Returns the bounding rectangle of the entire subitem, including the icon and label.</span></span><br/> |
| <span id="LVIR_ICON"></span><span id="lvir_icon"></span><dl> <span data-ttu-id="b1fad-123"><dt>**\_icône LVIR**</dt></span><span class="sxs-lookup"><span data-stu-id="b1fad-123"><dt>**LVIR\_ICON**</dt></span></span> </dl>       | <span data-ttu-id="b1fad-124">Retourne le rectangle englobant de l’icône ou de la petite icône du sous-élément.</span><span class="sxs-lookup"><span data-stu-id="b1fad-124">Returns the bounding rectangle of the icon or small icon of the subitem.</span></span><br/>            |
| <span id="LVIR_LABEL"></span><span id="lvir_label"></span><dl> <span data-ttu-id="b1fad-125"><dt>**\_étiquette LVIR**</dt></span><span class="sxs-lookup"><span data-stu-id="b1fad-125"><dt>**LVIR\_LABEL**</dt></span></span> </dl>    | <span data-ttu-id="b1fad-126">Retourne le rectangle englobant du texte du sous-élément.</span><span class="sxs-lookup"><span data-stu-id="b1fad-126">Returns the bounding rectangle of the subitem text.</span></span><br/>                                 |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1fad-127">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b1fad-127">Return value</span></span>

<span data-ttu-id="b1fad-128">Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="b1fad-128">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1fad-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b1fad-129">Requirements</span></span>



| <span data-ttu-id="b1fad-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b1fad-130">Requirement</span></span> | <span data-ttu-id="b1fad-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="b1fad-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b1fad-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b1fad-132">Minimum supported client</span></span><br/> | <span data-ttu-id="b1fad-133">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b1fad-133">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b1fad-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b1fad-134">Minimum supported server</span></span><br/> | <span data-ttu-id="b1fad-135">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b1fad-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b1fad-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="b1fad-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="b1fad-137"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b1fad-137"><dt>Commctrl.h</dt></span></span> </dl> |



 

