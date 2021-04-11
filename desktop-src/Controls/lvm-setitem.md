---
title: Message LVM_SETITEM (commctrl. h)
description: Définit tout ou partie des attributs d’un élément d’affichage de liste. Vous pouvez également envoyer \_ des SETITEM LVM pour définir le texte d’un sous-élément. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView SetItem.
ms.assetid: f1189b5d-bce7-4569-b4b9-bd750d7ef505
keywords:
- LVM_SETITEM les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_SETITEM
- LVM_SETITEMA
- LVM_SETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 623339c3d1ecc7a74cf20b5e52fb621666391bd5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032623"
---
# <a name="lvm_setitem-message"></a><span data-ttu-id="74453-106">\_Message SETITEM LVM</span><span class="sxs-lookup"><span data-stu-id="74453-106">LVM\_SETITEM message</span></span>

<span data-ttu-id="74453-107">Définit tout ou partie des attributs d’un élément d’affichage de liste.</span><span class="sxs-lookup"><span data-stu-id="74453-107">Sets some or all of a list-view item's attributes.</span></span> <span data-ttu-id="74453-108">Vous pouvez également envoyer \_ des SETITEM LVM pour définir le texte d’un sous-élément.</span><span class="sxs-lookup"><span data-stu-id="74453-108">You can also send LVM\_SETITEM to set the text of a subitem.</span></span> <span data-ttu-id="74453-109">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ListView \_ SetItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitem) .</span><span class="sxs-lookup"><span data-stu-id="74453-109">You can send this message explicitly or by using the [**ListView\_SetItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="74453-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="74453-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74453-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="74453-111">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="74453-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="74453-112">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="74453-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="74453-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="74453-114">Pointeur vers une structure [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) qui contient les nouveaux attributs d’élément.</span><span class="sxs-lookup"><span data-stu-id="74453-114">Pointer to an [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure that contains the new item attributes.</span></span> <span data-ttu-id="74453-115">Les membres **iItem** et **iSubItem** identifient l’élément ou le sous-élément, et le membre **Mask** spécifie les attributs à définir.</span><span class="sxs-lookup"><span data-stu-id="74453-115">The **iItem** and **iSubItem** members identify the item or subitem, and the **mask** member specifies which attributes to set.</span></span> <span data-ttu-id="74453-116">Si le membre de **masque** spécifie la \_ valeur de texte LVIF, le membre **pszText** est l’adresse d’une chaîne terminée par le caractère null et le membre **cchTextMax** est ignoré.</span><span class="sxs-lookup"><span data-stu-id="74453-116">If the **mask** member specifies the LVIF\_TEXT value, the **pszText** member is the address of a null-terminated string and the **cchTextMax** member is ignored.</span></span> <span data-ttu-id="74453-117">Si le membre de **masque** spécifie la \_ valeur d’État LVIF, le membre **stateMask** spécifie les États à modifier et le membre d' **État** contient les valeurs de ces États.</span><span class="sxs-lookup"><span data-stu-id="74453-117">If the **mask** member specifies the LVIF\_STATE value, the **stateMask** member specifies which item states to change and the **state** member contains the values for those states.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74453-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="74453-118">Return value</span></span>

<span data-ttu-id="74453-119">Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="74453-119">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="74453-120">Notes</span><span class="sxs-lookup"><span data-stu-id="74453-120">Remarks</span></span>

<span data-ttu-id="74453-121">Pour définir les attributs d’un élément de vue de liste, définissez le membre **iItem** de la structure [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) sur l’index de l’élément et définissez le membre **iSubItem** sur zéro.</span><span class="sxs-lookup"><span data-stu-id="74453-121">To set the attributes of a list-view item, set the **iItem** member of the [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure to the index of the item, and set the **iSubItem** member to zero.</span></span> <span data-ttu-id="74453-122">Pour un élément, vous pouvez définir les membres **State**, **pszText**, **IImage** et **lParam** de la structure **LVITEM** .</span><span class="sxs-lookup"><span data-stu-id="74453-122">For an item, you can set the **state**, **pszText**, **iImage**, and **lParam** members of the **LVITEM** structure.</span></span>

<span data-ttu-id="74453-123">Pour définir le texte d’un sous-élément, définissez les membres **iItem** et **iSubItem** pour indiquer le sous-élément spécifique, puis utilisez le membre **pszText** pour spécifier le texte.</span><span class="sxs-lookup"><span data-stu-id="74453-123">To set the text of a subitem, set the **iItem** and **iSubItem** members to indicate the specific subitem, and use the **pszText** member to specify the text.</span></span> <span data-ttu-id="74453-124">Vous pouvez également utiliser la macro [**ListView \_ SetItemText**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemtext) pour définir le texte d’un sous-élément.</span><span class="sxs-lookup"><span data-stu-id="74453-124">Alternatively, you can use the [**ListView\_SetItemText**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemtext) macro to set the text of a subitem.</span></span> <span data-ttu-id="74453-125">Vous ne pouvez pas définir les membres **State** ou **lParam** pour les sous-éléments, car les sous-éléments ne possèdent pas ces attributs.</span><span class="sxs-lookup"><span data-stu-id="74453-125">You cannot set the **state** or **lParam** members for subitems because subitems do not have these attributes.</span></span> <span data-ttu-id="74453-126">Dans la version 4,70 et les versions ultérieures, vous pouvez définir le membre **IImage** pour les sous-éléments.</span><span class="sxs-lookup"><span data-stu-id="74453-126">In version 4.70 and later, you can set the **iImage** member for subitems.</span></span> <span data-ttu-id="74453-127">L’image de sous-élément sera affichée si le contrôle List-View a le style étendu [**LVS \_ ex \_ SUBITEMIMAGES**](extended-list-view-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="74453-127">The subitem image will be displayed if the list-view control has the [**LVS\_EX\_SUBITEMIMAGES**](extended-list-view-styles.md) extended style.</span></span> <span data-ttu-id="74453-128">Les versions précédentes ignorent l’image de sous-élément.</span><span class="sxs-lookup"><span data-stu-id="74453-128">Previous versions will ignore the subitem image.</span></span>

## <a name="requirements"></a><span data-ttu-id="74453-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="74453-129">Requirements</span></span>



| <span data-ttu-id="74453-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="74453-130">Requirement</span></span> | <span data-ttu-id="74453-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="74453-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="74453-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="74453-132">Minimum supported client</span></span><br/> | <span data-ttu-id="74453-133">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="74453-133">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="74453-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="74453-134">Minimum supported server</span></span><br/> | <span data-ttu-id="74453-135">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="74453-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="74453-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="74453-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="74453-137"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="74453-137"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="74453-138">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="74453-138">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="74453-139">**LVM \_ SETITEMW** (Unicode) et **LVM \_ SETITEMA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="74453-139">**LVM\_SETITEMW** (Unicode) and **LVM\_SETITEMA** (ANSI)</span></span><br/>                   |



 

 





