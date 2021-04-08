---
title: Message LVM_GETITEMRECT (commctrl. h)
description: Récupère le rectangle englobant pour l’intégralité ou une partie d’un élément dans l’affichage actuel. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView GetItemRect.
ms.assetid: 7ce74b65-3360-42b4-9889-d90aefe2d284
keywords:
- LVM_GETITEMRECT les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_GETITEMRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd0915c9afc16f13ac8f36a639524fb5af6e8082
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033142"
---
# <a name="lvm_getitemrect-message"></a><span data-ttu-id="ef019-105">\_Message GETITEMRECT LVM</span><span class="sxs-lookup"><span data-stu-id="ef019-105">LVM\_GETITEMRECT message</span></span>

<span data-ttu-id="ef019-106">Récupère le rectangle englobant pour l’intégralité ou une partie d’un élément dans l’affichage actuel.</span><span class="sxs-lookup"><span data-stu-id="ef019-106">Retrieves the bounding rectangle for all or part of an item in the current view.</span></span> <span data-ttu-id="ef019-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ListView \_ GetItemRect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemrect) .</span><span class="sxs-lookup"><span data-stu-id="ef019-107">You can send this message explicitly or by using the [**ListView\_GetItemRect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemrect) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="ef019-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ef019-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef019-109">*wParam* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ef019-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef019-110">Index de l’élément de vue de liste.</span><span class="sxs-lookup"><span data-stu-id="ef019-110">Index of the list-view item.</span></span>

</dd> <dt>

<span data-ttu-id="ef019-111">*lParam* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="ef019-111">*lParam* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ef019-112">Pointeur vers une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) qui reçoit le rectangle englobant.</span><span class="sxs-lookup"><span data-stu-id="ef019-112">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that receives the bounding rectangle.</span></span> <span data-ttu-id="ef019-113">Lorsque le message est envoyé, le membre de **gauche** de cette structure est utilisé pour spécifier la partie de l’élément de vue de liste à partir de laquelle récupérer le rectangle englobant.</span><span class="sxs-lookup"><span data-stu-id="ef019-113">When the message is sent, the **left** member of this structure is used to specify the portion of the list-view item from which to retrieve the bounding rectangle.</span></span> <span data-ttu-id="ef019-114">Elle doit être définie sur l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="ef019-114">It must be set to one of the following values:</span></span>



| <span data-ttu-id="ef019-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="ef019-115">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="ef019-116">Signification</span><span class="sxs-lookup"><span data-stu-id="ef019-116">Meaning</span></span>                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span id="LVIR_BOUNDS"></span><span id="lvir_bounds"></span><dl> <span data-ttu-id="ef019-117"><dt>**\_limites LVIR**</dt></span><span class="sxs-lookup"><span data-stu-id="ef019-117"><dt>**LVIR\_BOUNDS**</dt></span></span> </dl>                   | <span data-ttu-id="ef019-118">Retourne le rectangle englobant de l’élément entier, y compris l’icône et l’étiquette.</span><span class="sxs-lookup"><span data-stu-id="ef019-118">Returns the bounding rectangle of the entire item, including the icon and label.</span></span><br/>                     |
| <span id="LVIR_ICON"></span><span id="lvir_icon"></span><dl> <span data-ttu-id="ef019-119"><dt>**\_icône LVIR**</dt></span><span class="sxs-lookup"><span data-stu-id="ef019-119"><dt>**LVIR\_ICON**</dt></span></span> </dl>                         | <span data-ttu-id="ef019-120">Retourne le rectangle englobant de l’icône ou de la petite icône.</span><span class="sxs-lookup"><span data-stu-id="ef019-120">Returns the bounding rectangle of the icon or small icon.</span></span><br/>                                            |
| <span id="LVIR_LABEL"></span><span id="lvir_label"></span><dl> <span data-ttu-id="ef019-121"><dt>**\_étiquette LVIR**</dt></span><span class="sxs-lookup"><span data-stu-id="ef019-121"><dt>**LVIR\_LABEL**</dt></span></span> </dl>                      | <span data-ttu-id="ef019-122">Retourne le rectangle englobant du texte de l’élément.</span><span class="sxs-lookup"><span data-stu-id="ef019-122">Returns the bounding rectangle of the item text.</span></span><br/>                                                     |
| <span id="LVIR_SELECTBOUNDS"></span><span id="lvir_selectbounds"></span><dl> <span data-ttu-id="ef019-123"><dt>**LVIR \_ SELECTBOUNDS**</dt></span><span class="sxs-lookup"><span data-stu-id="ef019-123"><dt>**LVIR\_SELECTBOUNDS**</dt></span></span> </dl> | <span data-ttu-id="ef019-124">Retourne l’Union des rectangles de l’icône LVIR et de l' \_ \_ étiquette LVIR, mais exclut les colonnes de la vue rapport.</span><span class="sxs-lookup"><span data-stu-id="ef019-124">Returns the union of the LVIR\_ICON and LVIR\_LABEL rectangles, but excludes columns in report view.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef019-125">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ef019-125">Return value</span></span>

<span data-ttu-id="ef019-126">Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="ef019-126">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef019-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ef019-127">Requirements</span></span>



| <span data-ttu-id="ef019-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ef019-128">Requirement</span></span> | <span data-ttu-id="ef019-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="ef019-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ef019-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ef019-130">Minimum supported client</span></span><br/> | <span data-ttu-id="ef019-131">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ef019-131">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ef019-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ef019-132">Minimum supported server</span></span><br/> | <span data-ttu-id="ef019-133">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ef019-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ef019-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="ef019-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef019-135"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef019-135"><dt>Commctrl.h</dt></span></span> </dl> |



 

