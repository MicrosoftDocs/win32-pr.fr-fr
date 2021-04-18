---
title: Message LVM_INSERTITEM (commctrl. h)
description: Insère un nouvel élément dans un contrôle List-View. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView InsertItem.
ms.assetid: ac283e81-5b9f-4a90-acdb-fd7813c9cb84
keywords:
- LVM_INSERTITEM les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_INSERTITEM
- LVM_INSERTITEMA
- LVM_INSERTITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 467c6b595e307dc16f87e40da858ff8b120fb3f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512600"
---
# <a name="lvm_insertitem-message"></a><span data-ttu-id="2b732-105">\_Message INSERTITEM LVM</span><span class="sxs-lookup"><span data-stu-id="2b732-105">LVM\_INSERTITEM message</span></span>

<span data-ttu-id="2b732-106">Insère un nouvel élément dans un contrôle List-View.</span><span class="sxs-lookup"><span data-stu-id="2b732-106">Inserts a new item in a list-view control.</span></span> <span data-ttu-id="2b732-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ListView \_ InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertitem) .</span><span class="sxs-lookup"><span data-stu-id="2b732-107">You can send this message explicitly or by using the [**ListView\_InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="2b732-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2b732-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b732-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2b732-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="2b732-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="2b732-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="2b732-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2b732-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2b732-112">Pointeur vers une structure [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) qui spécifie les attributs de l’élément de vue de liste.</span><span class="sxs-lookup"><span data-stu-id="2b732-112">Pointer to an [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure that specifies the attributes of the list-view item.</span></span> <span data-ttu-id="2b732-113">Utilisez le membre **iItem** pour spécifier l’index de base zéro auquel le nouvel élément doit être inséré.</span><span class="sxs-lookup"><span data-stu-id="2b732-113">Use the **iItem** member to specify the zero-based index at which the new item should be inserted.</span></span> <span data-ttu-id="2b732-114">Si cette valeur est supérieure au nombre d’éléments actuellement contenus dans le ListView, le nouvel élément est ajouté à la fin de la liste et reçoit l’index correct.</span><span class="sxs-lookup"><span data-stu-id="2b732-114">If this value is greater than the number of items currently contained by the listview, the new item will be appended to the end of the list and assigned the correct index.</span></span> <span data-ttu-id="2b732-115">Examinez la valeur de retour du message pour déterminer l’index réel affecté à l’élément.</span><span class="sxs-lookup"><span data-stu-id="2b732-115">Examine the message's return value to determine the actual index assigned to the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b732-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2b732-116">Return value</span></span>

<span data-ttu-id="2b732-117">Retourne l’index du nouvel élément en cas de réussite, ou-1 dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="2b732-117">Returns the index of the new item if successful, or -1 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b732-118">Notes</span><span class="sxs-lookup"><span data-stu-id="2b732-118">Remarks</span></span>

<span data-ttu-id="2b732-119">Vous ne pouvez pas utiliser [**ListView \_ InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertitem) ou **LVM \_ InsertItem** pour insérer des sous-éléments.</span><span class="sxs-lookup"><span data-stu-id="2b732-119">You cannot use [**ListView\_InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertitem) or **LVM\_INSERTITEM** to insert subitems.</span></span> <span data-ttu-id="2b732-120">Le membre **iSubItem** de la structure [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="2b732-120">The **iSubItem** member of the [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure must be zero.</span></span> <span data-ttu-id="2b732-121">Pour plus d’informations sur la définition des sous-éléments, consultez [**\_ SETITEM LVM**](lvm-setitem.md) .</span><span class="sxs-lookup"><span data-stu-id="2b732-121">See [**LVM\_SETITEM**](lvm-setitem.md) for information on setting subitems.</span></span>

<span data-ttu-id="2b732-122">Si un contrôle List-View a le style [**LVS \_ ex \_ checkboxs**](extended-list-view-styles.md) défini, toute valeur placée dans les bits 12 à 15 du membre **State** de la structure [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) sera ignorée.</span><span class="sxs-lookup"><span data-stu-id="2b732-122">If a list-view control has the [**LVS\_EX\_CHECKBOXES**](extended-list-view-styles.md) style set, any value placed in bits 12 through 15 of the **state** member of the [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure will be ignored.</span></span> <span data-ttu-id="2b732-123">Lorsqu’un élément est ajouté avec cet ensemble de styles, il est toujours défini sur l’état désactivé.</span><span class="sxs-lookup"><span data-stu-id="2b732-123">When an item is added with this style set, it will always be set to the unchecked state.</span></span>

<span data-ttu-id="2b732-124">Si un contrôle List-View a le style de fenêtre [**LVS \_ SORTASCENDING**](list-view-window-styles.md) ou [**LVS \_ SORTDESCENDING**](list-view-window-styles.md) , un **message \_ INSERTITEM de LVM** échoue si vous essayez d’insérer un élément dont \_ la valeur de LPSTR TEXTCALLBACK est la valeur de son membre **pszText** .</span><span class="sxs-lookup"><span data-stu-id="2b732-124">If a list-view control has either the [**LVS\_SORTASCENDING**](list-view-window-styles.md) or [**LVS\_SORTDESCENDING**](list-view-window-styles.md) window style, an **LVM\_INSERTITEM** message will fail if you try to insert an item that has LPSTR\_TEXTCALLBACK as the value for its **pszText** member.</span></span>

<span data-ttu-id="2b732-125">Le **message \_ INSERTITEM du LVM** insère le nouvel élément à la position appropriée dans l’ordre de tri si les conditions suivantes sont respectées :</span><span class="sxs-lookup"><span data-stu-id="2b732-125">The **LVM\_INSERTITEM** message will insert the new item in the proper position in the sort order if the following conditions hold:</span></span>

-   <span data-ttu-id="2b732-126">Vous utilisez l’un des styles LVS \_ SORTXXX.</span><span class="sxs-lookup"><span data-stu-id="2b732-126">You are using one of the LVS\_SORTXXX styles.</span></span>
-   <span data-ttu-id="2b732-127">Vous n’utilisez pas le style [**LVS \_ OwnerDraw**](list-view-window-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="2b732-127">You are not using the [**LVS\_OWNERDRAW**](list-view-window-styles.md) style.</span></span>
-   <span data-ttu-id="2b732-128">Le membre **pszText** de la structure vers laquelle pointe **pItem** n’a pas la valeur LPSTR \_ TEXTCALLBACK.</span><span class="sxs-lookup"><span data-stu-id="2b732-128">The **pszText** member of the structure pointed to by **pitem** is not set to LPSTR\_TEXTCALLBACK.</span></span>

<span data-ttu-id="2b732-129">Si la structure [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) ne contient pas LVIF \_ GROUPID dans le membre **Mask** , la valeur du membre **iGroupId** est I \_ GROUPIDCALLBACK par défaut.</span><span class="sxs-lookup"><span data-stu-id="2b732-129">If the [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure does not contain LVIF\_GROUPID in the **mask** member, the value of the **iGroupId** member is I\_GROUPIDCALLBACK by default.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b732-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2b732-130">Requirements</span></span>



| <span data-ttu-id="2b732-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2b732-131">Requirement</span></span> | <span data-ttu-id="2b732-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="2b732-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2b732-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2b732-133">Minimum supported client</span></span><br/> | <span data-ttu-id="2b732-134">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2b732-134">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2b732-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2b732-135">Minimum supported server</span></span><br/> | <span data-ttu-id="2b732-136">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2b732-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2b732-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="2b732-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="2b732-138"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2b732-138"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="2b732-139">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="2b732-139">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="2b732-140">**LVM \_ INSERTITEMW** (Unicode) et **LVM \_ INSERTITEMA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="2b732-140">**LVM\_INSERTITEMW** (Unicode) and **LVM\_INSERTITEMA** (ANSI)</span></span><br/>             |



 

 





