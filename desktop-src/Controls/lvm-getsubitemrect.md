---
title: Message LVM_GETSUBITEMRECT (commctrl. h)
description: Récupère des informations sur le rectangle englobant d’un sous-élément dans un contrôle d’affichage de liste.
ms.assetid: 985876b2-6eb3-4c96-88ea-ddec67ef5b5a
keywords:
- LVM_GETSUBITEMRECT les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_GETSUBITEMRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd1184c52d60b86e008685b87c9f5555cf801b35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105490"
---
# <a name="lvm_getsubitemrect-message"></a><span data-ttu-id="5a090-104">\_Message GETSUBITEMRECT LVM</span><span class="sxs-lookup"><span data-stu-id="5a090-104">LVM\_GETSUBITEMRECT message</span></span>

<span data-ttu-id="5a090-105">Récupère des informations sur le rectangle englobant d’un sous-élément dans un contrôle d’affichage de liste.</span><span class="sxs-lookup"><span data-stu-id="5a090-105">Retrieves information about the bounding rectangle for a subitem in a list-view control.</span></span> <span data-ttu-id="5a090-106">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**\_ GetSubItemRect ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getsubitemrect) (recommandé).</span><span class="sxs-lookup"><span data-stu-id="5a090-106">You can send this message explicitly or by using the [**ListView\_GetSubItemRect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getsubitemrect) macro (recommended).</span></span> <span data-ttu-id="5a090-107">Ce message est destiné à être utilisé uniquement avec des contrôles d’affichage de liste qui utilisent le style de [**\_ rapport LVS**](list-view-window-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="5a090-107">This message is intended to be used only with list-view controls that use the [**LVS\_REPORT**](list-view-window-styles.md) style.</span></span>

## <a name="parameters"></a><span data-ttu-id="5a090-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5a090-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a090-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5a090-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5a090-110">Index de l’élément parent du sous-élément.</span><span class="sxs-lookup"><span data-stu-id="5a090-110">Index of the subitem's parent item.</span></span>

</dd> <dt>

<span data-ttu-id="5a090-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5a090-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5a090-112">Pointeur vers une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) qui recevra les informations de rectangle englobant du sous-élément.</span><span class="sxs-lookup"><span data-stu-id="5a090-112">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that will receive the subitem bounding rectangle information.</span></span> <span data-ttu-id="5a090-113">Ses membres doivent être initialisés conformément aux relations de membre/valeur suivantes :</span><span class="sxs-lookup"><span data-stu-id="5a090-113">Its members must be initialized according to the following member/value relationships:</span></span>



| <span data-ttu-id="5a090-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="5a090-114">Value</span></span>                                                                                                                             | <span data-ttu-id="5a090-115">Signification</span><span class="sxs-lookup"><span data-stu-id="5a090-115">Meaning</span></span>                                                                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span id="top"></span><span id="TOP"></span><dl> <span data-ttu-id="5a090-116"><dt>**Retour au début**</dt></span><span class="sxs-lookup"><span data-stu-id="5a090-116"><dt>**top**</dt></span></span> </dl>    | <span data-ttu-id="5a090-117">Index de base un du sous-élément.</span><span class="sxs-lookup"><span data-stu-id="5a090-117">The one-based index of the subitem.</span></span><br/>                                                                                    |
| <span id="left"></span><span id="LEFT"></span><dl> <span data-ttu-id="5a090-118"><dt>**gauche**</dt></span><span class="sxs-lookup"><span data-stu-id="5a090-118"><dt>**left**</dt></span></span> </dl> | <span data-ttu-id="5a090-119">Valeur de l’indicateur (consultez la section Notes).</span><span class="sxs-lookup"><span data-stu-id="5a090-119">Flag value (see remarks).</span></span> <span data-ttu-id="5a090-120">Indique la partie du sous-élément de vue de liste pour lequel récupérer le rectangle englobant.</span><span class="sxs-lookup"><span data-stu-id="5a090-120">Indicates the portion of the list-view subitem for which to retrieve the bounding rectangle.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a090-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5a090-121">Return value</span></span>

<span data-ttu-id="5a090-122">Retourne une valeur différente de zéro en cas de réussite, ou zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="5a090-122">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a090-123">Notes</span><span class="sxs-lookup"><span data-stu-id="5a090-123">Remarks</span></span>

<span data-ttu-id="5a090-124">Voici les valeurs d’indicateur qui peuvent être définies.</span><span class="sxs-lookup"><span data-stu-id="5a090-124">Following are the flag values that may be set.</span></span>



| <span data-ttu-id="5a090-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5a090-125">Requirement</span></span> | <span data-ttu-id="5a090-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="5a090-126">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a090-127">**Valeur de l’indicateur**</span><span class="sxs-lookup"><span data-stu-id="5a090-127">**Flag Value**</span></span> | <span data-ttu-id="5a090-128">**Signification**</span><span class="sxs-lookup"><span data-stu-id="5a090-128">**Meaning**</span></span>                                                                                                         |
| <span data-ttu-id="5a090-129">\_limites LVIR</span><span class="sxs-lookup"><span data-stu-id="5a090-129">LVIR\_BOUNDS</span></span>   | <span data-ttu-id="5a090-130">Retourne le rectangle englobant de l’élément entier, y compris l’icône et l’étiquette.</span><span class="sxs-lookup"><span data-stu-id="5a090-130">Returns the bounding rectangle of the entire item, including the icon and label.</span></span>                                    |
| <span data-ttu-id="5a090-131">\_icône LVIR</span><span class="sxs-lookup"><span data-stu-id="5a090-131">LVIR\_ICON</span></span>     | <span data-ttu-id="5a090-132">Retourne le rectangle englobant de l’icône ou de la petite icône.</span><span class="sxs-lookup"><span data-stu-id="5a090-132">Returns the bounding rectangle of the icon or small icon.</span></span>                                                           |
| <span data-ttu-id="5a090-133">\_étiquette LVIR</span><span class="sxs-lookup"><span data-stu-id="5a090-133">LVIR\_LABEL</span></span>    | <span data-ttu-id="5a090-134">Retourne le rectangle englobant de l’élément entier, y compris l’icône et l’étiquette.</span><span class="sxs-lookup"><span data-stu-id="5a090-134">Returns the bounding rectangle of the entire item, including the icon and label.</span></span> <span data-ttu-id="5a090-135">Cela est identique aux limites de LVIR \_ .</span><span class="sxs-lookup"><span data-stu-id="5a090-135">This is identical to LVIR\_BOUNDS.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="5a090-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5a090-136">Requirements</span></span>



| <span data-ttu-id="5a090-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5a090-137">Requirement</span></span> | <span data-ttu-id="5a090-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="5a090-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5a090-139">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5a090-139">Minimum supported client</span></span><br/> | <span data-ttu-id="5a090-140">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5a090-140">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5a090-141">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5a090-141">Minimum supported server</span></span><br/> | <span data-ttu-id="5a090-142">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5a090-142">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5a090-143">En-tête</span><span class="sxs-lookup"><span data-stu-id="5a090-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="5a090-144"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a090-144"><dt>Commctrl.h</dt></span></span> </dl> |



 

