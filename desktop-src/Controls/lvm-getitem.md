---
title: Message LVM_GETITEM (commctrl. h)
description: Récupère une partie ou la totalité des attributs d’un élément d’affichage de liste. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView GetItem.
ms.assetid: 684ad96a-2c3b-4148-b66c-41f8322500bb
keywords:
- LVM_GETITEM les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_GETITEM
- LVM_GETITEMA
- LVM_GETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c19632567db5e37059b1b028a8ec1fc9385268cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742996"
---
# <a name="lvm_getitem-message"></a><span data-ttu-id="264e9-105">Message de LVM. \_</span><span class="sxs-lookup"><span data-stu-id="264e9-105">LVM\_GETITEM message</span></span>

<span data-ttu-id="264e9-106">Récupère une partie ou la totalité des attributs d’un élément d’affichage de liste.</span><span class="sxs-lookup"><span data-stu-id="264e9-106">Retrieves some or all of a list-view item's attributes.</span></span> <span data-ttu-id="264e9-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ListView \_ GetItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitem) .</span><span class="sxs-lookup"><span data-stu-id="264e9-107">You can send this message explicitly or by using the [**ListView\_GetItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="264e9-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="264e9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="264e9-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="264e9-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="264e9-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="264e9-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="264e9-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="264e9-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="264e9-112">Pointeur vers une structure [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) qui spécifie les informations pour récupérer et recevoir des informations sur l’élément de vue de liste.</span><span class="sxs-lookup"><span data-stu-id="264e9-112">Pointer to an [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure that specifies the information to retrieve and receives information about the list-view item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="264e9-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="264e9-113">Return value</span></span>

<span data-ttu-id="264e9-114">Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="264e9-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="264e9-115">Notes</span><span class="sxs-lookup"><span data-stu-id="264e9-115">Remarks</span></span>

<span data-ttu-id="264e9-116">Lorsque le **message \_ LVM de LVM** est envoyé, les membres **iItem** et **iSubItem** identifient l’élément ou le sous-élément pour lequel récupérer des informations et le membre **Mask** spécifie les attributs à récupérer.</span><span class="sxs-lookup"><span data-stu-id="264e9-116">When the **LVM\_GETITEM** message is sent, the **iItem** and **iSubItem** members identify the item or subitem to retrieve information about and the **mask** member specifies which attributes to retrieve.</span></span> <span data-ttu-id="264e9-117">Pour obtenir la liste des valeurs possibles, consultez la description de la structure [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) .</span><span class="sxs-lookup"><span data-stu-id="264e9-117">For a list of possible values, see the description of the [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure.</span></span>

<span data-ttu-id="264e9-118">Si l' \_ indicateur de texte LVIF est défini dans le membre **Mask** de la structure [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) , le membre **pszText** doit pointer vers une mémoire tampon valide et le membre **cchTextMax** doit avoir pour valeur le nombre de caractères de cette mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="264e9-118">If the LVIF\_TEXT flag is set in the **mask** member of the [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure, the **pszText** member must point to a valid buffer and the **cchTextMax** member must be set to the number of characters in that buffer.</span></span> <span data-ttu-id="264e9-119">Les applications ne doivent pas supposer que le texte sera nécessairement placé dans la mémoire tampon spécifiée.</span><span class="sxs-lookup"><span data-stu-id="264e9-119">Applications should not assume that the text will necessarily be placed in the specified buffer.</span></span> <span data-ttu-id="264e9-120">Le contrôle peut à la place modifier le membre **pszText** de la structure pour pointer vers le nouveau texte, au lieu de le placer dans la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="264e9-120">The control may instead change the **pszText** member of the structure to point to the new text, rather than place it in the buffer.</span></span>

<span data-ttu-id="264e9-121">Si le membre de **masque** spécifie la \_ valeur d’État LVIF, le membre **stateMask** doit spécifier les bits d’état d’élément à récupérer.</span><span class="sxs-lookup"><span data-stu-id="264e9-121">If the **mask** member specifies the LVIF\_STATE value, the **stateMask** member must specify the item state bits to retrieve.</span></span> <span data-ttu-id="264e9-122">Lors de la sortie, le membre d' **État** contient les valeurs des bits d’état spécifiés.</span><span class="sxs-lookup"><span data-stu-id="264e9-122">On output, the **state** member contains the values of the specified state bits.</span></span>

## <a name="requirements"></a><span data-ttu-id="264e9-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="264e9-123">Requirements</span></span>



| <span data-ttu-id="264e9-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="264e9-124">Requirement</span></span> | <span data-ttu-id="264e9-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="264e9-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="264e9-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="264e9-126">Minimum supported client</span></span><br/> | <span data-ttu-id="264e9-127">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="264e9-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="264e9-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="264e9-128">Minimum supported server</span></span><br/> | <span data-ttu-id="264e9-129">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="264e9-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="264e9-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="264e9-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="264e9-131"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="264e9-131"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="264e9-132">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="264e9-132">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="264e9-133">**LVM \_ GETITEMW** (Unicode) et **LVM \_ GETITEMA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="264e9-133">**LVM\_GETITEMW** (Unicode) and **LVM\_GETITEMA** (ANSI)</span></span><br/>                   |



 

 





