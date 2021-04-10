---
title: Message LVM_SETITEMSTATE (commctrl. h)
description: Modifie l’état d’un élément dans un contrôle List-View. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView SetItemState.
ms.assetid: aecd14dd-cfd0-4c7c-bddc-f65022de68c9
keywords:
- LVM_SETITEMSTATE les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_SETITEMSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2120d6d1d2cd3044368ebb343cdf0fe240d805c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103924"
---
# <a name="lvm_setitemstate-message"></a><span data-ttu-id="b5ac3-105">\_Message SETITEMSTATE LVM</span><span class="sxs-lookup"><span data-stu-id="b5ac3-105">LVM\_SETITEMSTATE message</span></span>

<span data-ttu-id="b5ac3-106">Modifie l’état d’un élément dans un contrôle List-View.</span><span class="sxs-lookup"><span data-stu-id="b5ac3-106">Changes the state of an item in a list-view control.</span></span> <span data-ttu-id="b5ac3-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ListView \_ SetItemState**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemstate) .</span><span class="sxs-lookup"><span data-stu-id="b5ac3-107">You can send this message explicitly or by using the [**ListView\_SetItemState**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemstate) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="b5ac3-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b5ac3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5ac3-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b5ac3-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b5ac3-110">Index de l’élément de vue de liste.</span><span class="sxs-lookup"><span data-stu-id="b5ac3-110">Index of the list-view item.</span></span> <span data-ttu-id="b5ac3-111">Si ce paramètre a la valeur-1, le changement d’État est appliqué à tous les éléments.</span><span class="sxs-lookup"><span data-stu-id="b5ac3-111">If this parameter is -1, then the state change is applied to all items.</span></span>

</dd> <dt>

<span data-ttu-id="b5ac3-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b5ac3-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b5ac3-113">Pointeur vers une structure [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) .</span><span class="sxs-lookup"><span data-stu-id="b5ac3-113">Pointer to an [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure.</span></span> <span data-ttu-id="b5ac3-114">Le membre **stateMask** spécifie les bits d’État à modifier, et le membre d' **État** contient les nouvelles valeurs pour ces bits.</span><span class="sxs-lookup"><span data-stu-id="b5ac3-114">The **stateMask** member specifies which state bits to change, and the **state** member contains the new values for those bits.</span></span> <span data-ttu-id="b5ac3-115">Les autres membres sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="b5ac3-115">The other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5ac3-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b5ac3-116">Return value</span></span>

<span data-ttu-id="b5ac3-117">Si vous envoyez ce message de manière explicite, il retourne **true** en cas de réussite ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="b5ac3-117">If you send this message explicitly, it returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5ac3-118">Notes</span><span class="sxs-lookup"><span data-stu-id="b5ac3-118">Remarks</span></span>

<span data-ttu-id="b5ac3-119">La valeur d’état d’un élément comprend un jeu d’indicateurs binaires qui indiquent l’état de l’élément.</span><span class="sxs-lookup"><span data-stu-id="b5ac3-119">An item's state value includes a set of bit flags that indicate the item's state.</span></span> <span data-ttu-id="b5ac3-120">La valeur d’État peut également inclure des index de liste d’images qui indiquent l’image d’état de l’élément et l’image de superposition.</span><span class="sxs-lookup"><span data-stu-id="b5ac3-120">The state value can also include image list indexes that indicate the item's state image and overlay image.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5ac3-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b5ac3-121">Requirements</span></span>



| <span data-ttu-id="b5ac3-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b5ac3-122">Requirement</span></span> | <span data-ttu-id="b5ac3-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="b5ac3-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b5ac3-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b5ac3-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b5ac3-125">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b5ac3-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b5ac3-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b5ac3-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b5ac3-127">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b5ac3-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b5ac3-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="b5ac3-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="b5ac3-129"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5ac3-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





