---
title: Message TVM_GETITEM (commctrl. h)
description: Récupère une partie ou la totalité des attributs d’un élément d’affichage d’arborescence. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro TreeView GetItem.
ms.assetid: e26ec000-967d-46de-8f71-6ebc36fefe5e
keywords:
- TVM_GETITEM les contrôles de message Windows
topic_type:
- apiref
api_name:
- TVM_GETITEM
- TVM_GETITEMA
- TVM_GETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dff96f4721a3c50eda54792b2b1c003cd808bf11
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106573"
---
# <a name="tvm_getitem-message"></a><span data-ttu-id="b277f-105">TVM ( \_ message GETITEM)</span><span class="sxs-lookup"><span data-stu-id="b277f-105">TVM\_GETITEM message</span></span>

<span data-ttu-id="b277f-106">Récupère une partie ou la totalité des attributs d’un élément d’affichage d’arborescence.</span><span class="sxs-lookup"><span data-stu-id="b277f-106">Retrieves some or all of a tree-view item's attributes.</span></span> <span data-ttu-id="b277f-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**TreeView \_ GetItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitem) .</span><span class="sxs-lookup"><span data-stu-id="b277f-107">You can send this message explicitly or by using the [**TreeView\_GetItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="b277f-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b277f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b277f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b277f-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="b277f-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="b277f-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="b277f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b277f-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b277f-112">Pointeur vers une structure [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) qui spécifie les informations pour récupérer et recevoir des informations sur l’élément.</span><span class="sxs-lookup"><span data-stu-id="b277f-112">Pointer to a [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure that specifies the information to retrieve and receives information about the item.</span></span> <span data-ttu-id="b277f-113">Avec la [version 4,71](common-control-versions.md) et les versions ultérieures, vous pouvez utiliser une structure [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) à la place.</span><span class="sxs-lookup"><span data-stu-id="b277f-113">With [version 4.71](common-control-versions.md) and later, you can use a [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) structure instead.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b277f-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b277f-114">Return value</span></span>

<span data-ttu-id="b277f-115">Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="b277f-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="b277f-116">Notes</span><span class="sxs-lookup"><span data-stu-id="b277f-116">Remarks</span></span>

<span data-ttu-id="b277f-117">Lorsque le message est envoyé, le membre **hitem** de la structure [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) ou [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) identifie l’élément sur lequel les informations doivent être récupérées, et le membre **Mask** spécifie les attributs à récupérer.</span><span class="sxs-lookup"><span data-stu-id="b277f-117">When the message is sent, the **hItem** member of the [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) or [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) structure identifies the item to retrieve information about, and the **mask** member specifies the attributes to retrieve.</span></span>

<span data-ttu-id="b277f-118">Si l' \_ indicateur de texte TVIF est défini dans le membre **Mask** de la structure [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) ou [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) , le membre **pszText** doit pointer vers une mémoire tampon valide et le membre **cchTextMax** doit avoir pour valeur le nombre de caractères de cette mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="b277f-118">If the TVIF\_TEXT flag is set in the **mask** member of the [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) or [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) structure, the **pszText** member must point to a valid buffer and the **cchTextMax** member must be set to the number of characters in that buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="b277f-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b277f-119">Requirements</span></span>



| <span data-ttu-id="b277f-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b277f-120">Requirement</span></span> | <span data-ttu-id="b277f-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="b277f-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b277f-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b277f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="b277f-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b277f-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b277f-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b277f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="b277f-125">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b277f-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b277f-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="b277f-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="b277f-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b277f-127"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="b277f-128">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="b277f-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="b277f-129">**TVM \_ GETITEMW** (Unicode) et **TVM \_ GETITEMA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="b277f-129">**TVM\_GETITEMW** (Unicode) and **TVM\_GETITEMA** (ANSI)</span></span><br/>                   |



 

 





