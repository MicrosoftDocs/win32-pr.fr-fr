---
title: Message LVM_ARRANGE (commctrl. h)
description: Organise les éléments en mode icône. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro organiser ListView.
ms.assetid: f7dbcdd2-3cc9-4bae-827e-8bac3b49486c
keywords:
- LVM_ARRANGE les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_ARRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a1b6a081cf963a649329951358ea4c972f200f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102909"
---
# <a name="lvm_arrange-message"></a><span data-ttu-id="748dc-105">\_Message d’organisation LVM</span><span class="sxs-lookup"><span data-stu-id="748dc-105">LVM\_ARRANGE message</span></span>

<span data-ttu-id="748dc-106">Organise les éléments en mode icône.</span><span class="sxs-lookup"><span data-stu-id="748dc-106">Arranges items in icon view.</span></span> <span data-ttu-id="748dc-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**\_ organiser ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_arrange) .</span><span class="sxs-lookup"><span data-stu-id="748dc-107">You can send this message explicitly or by using the [**ListView\_Arrange**](/windows/desktop/api/Commctrl/nf-commctrl-listview_arrange) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="748dc-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="748dc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="748dc-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="748dc-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="748dc-110">L’une des valeurs suivantes qui spécifient l’alignement :</span><span class="sxs-lookup"><span data-stu-id="748dc-110">One of the following values that specifies alignment:</span></span>



| <span data-ttu-id="748dc-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="748dc-111">Value</span></span>                                                                                                                                                            | <span data-ttu-id="748dc-112">Signification</span><span class="sxs-lookup"><span data-stu-id="748dc-112">Meaning</span></span>                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| <span id="LVA_ALIGNLEFT"></span><span id="lva_alignleft"></span><dl> <span data-ttu-id="748dc-113"><dt>**LVA \_ ALIGNLEFT**</dt></span><span class="sxs-lookup"><span data-stu-id="748dc-113"><dt>**LVA\_ALIGNLEFT**</dt></span></span> </dl>    | <span data-ttu-id="748dc-114">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="748dc-114">Not implemented.</span></span> <span data-ttu-id="748dc-115">Appliquez le [**style \_ ALIGNLEFT LVS**](list-view-window-styles.md) à la place.</span><span class="sxs-lookup"><span data-stu-id="748dc-115">Apply the [**LVS\_ALIGNLEFT**](list-view-window-styles.md) style instead.</span></span><br/> |
| <span id="LVA_ALIGNTOP"></span><span id="lva_aligntop"></span><dl> <span data-ttu-id="748dc-116"><dt>**LVA \_ ALIGNTOP**</dt></span><span class="sxs-lookup"><span data-stu-id="748dc-116"><dt>**LVA\_ALIGNTOP**</dt></span></span> </dl>       | <span data-ttu-id="748dc-117">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="748dc-117">Not implemented.</span></span> <span data-ttu-id="748dc-118">Appliquez le style [**LVS \_ ALIGNTOP**](list-view-window-styles.md) à la place.</span><span class="sxs-lookup"><span data-stu-id="748dc-118">Apply the [**LVS\_ALIGNTOP**](list-view-window-styles.md) style instead.</span></span><br/>   |
| <span id="LVA_DEFAULT"></span><span id="lva_default"></span><dl> <span data-ttu-id="748dc-119"><dt>**LVA \_ par défaut**</dt></span><span class="sxs-lookup"><span data-stu-id="748dc-119"><dt>**LVA\_DEFAULT**</dt></span></span> </dl>          | <span data-ttu-id="748dc-120">Aligne les éléments selon les styles d’alignement actuels du contrôle List-View (valeur par défaut).</span><span class="sxs-lookup"><span data-stu-id="748dc-120">Aligns items according to the list-view control's current alignment styles (the default value).</span></span><br/>           |
| <span id="LVA_SNAPTOGRID"></span><span id="lva_snaptogrid"></span><dl> <span data-ttu-id="748dc-121"><dt>**LVA \_ SNAPTOGRID**</dt></span><span class="sxs-lookup"><span data-stu-id="748dc-121"><dt>**LVA\_SNAPTOGRID**</dt></span></span> </dl> | <span data-ttu-id="748dc-122">Aligne toutes les icônes à la position de grille la plus proche.</span><span class="sxs-lookup"><span data-stu-id="748dc-122">Snaps all icons to the nearest grid position.</span></span><br/>                                                             |



 

</dd> <dt>

<span data-ttu-id="748dc-123">*lParam*</span><span class="sxs-lookup"><span data-stu-id="748dc-123">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="748dc-124">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="748dc-124">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="748dc-125">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="748dc-125">Return value</span></span>

<span data-ttu-id="748dc-126">Retourne la **valeur true** en cas de réussite ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="748dc-126">Returns **TRUE** if successful; otherwise, **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="748dc-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="748dc-127">Requirements</span></span>



| <span data-ttu-id="748dc-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="748dc-128">Requirement</span></span> | <span data-ttu-id="748dc-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="748dc-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="748dc-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="748dc-130">Minimum supported client</span></span><br/> | <span data-ttu-id="748dc-131">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="748dc-131">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="748dc-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="748dc-132">Minimum supported server</span></span><br/> | <span data-ttu-id="748dc-133">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="748dc-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="748dc-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="748dc-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="748dc-135"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="748dc-135"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





