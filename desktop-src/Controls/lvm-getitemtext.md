---
title: Message LVM_GETITEMTEXT (commctrl. h)
description: Récupère le texte d’un élément ou d’un sous-élément de vue de liste. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView GetItemText.
ms.assetid: 5711ed18-a766-4e7f-9e9d-b9203231b369
keywords:
- LVM_GETITEMTEXT les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_GETITEMTEXT
- LVM_GETITEMTEXTA
- LVM_GETITEMTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c71eec6b9dab4c649b11da5b24568eea816774ef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105502"
---
# <a name="lvm_getitemtext-message"></a><span data-ttu-id="3b7b3-105">\_Message GETITEMTEXT LVM</span><span class="sxs-lookup"><span data-stu-id="3b7b3-105">LVM\_GETITEMTEXT message</span></span>

<span data-ttu-id="3b7b3-106">Récupère le texte d’un élément ou d’un sous-élément de vue de liste.</span><span class="sxs-lookup"><span data-stu-id="3b7b3-106">Retrieves the text of a list-view item or subitem.</span></span> <span data-ttu-id="3b7b3-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ListView \_ GetItemText**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemtext) .</span><span class="sxs-lookup"><span data-stu-id="3b7b3-107">You can send this message explicitly or by using the [**ListView\_GetItemText**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemtext) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="3b7b3-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3b7b3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b7b3-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3b7b3-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3b7b3-110">Index de l’élément de vue de liste.</span><span class="sxs-lookup"><span data-stu-id="3b7b3-110">Index of the list-view item.</span></span>

</dd> <dt>

<span data-ttu-id="3b7b3-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3b7b3-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3b7b3-112">Pointeur vers une structure [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) .</span><span class="sxs-lookup"><span data-stu-id="3b7b3-112">Pointer to an [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure.</span></span> <span data-ttu-id="3b7b3-113">Pour récupérer le texte de l’élément, affectez à **iSubItem** la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="3b7b3-113">To retrieve the item text, set **iSubItem** to zero.</span></span> <span data-ttu-id="3b7b3-114">Pour récupérer le texte d’un sous-élément, définissez **iSubItem** sur l’index du sous-élément.</span><span class="sxs-lookup"><span data-stu-id="3b7b3-114">To retrieve the text of a subitem, set **iSubItem** to the subitem's index.</span></span> <span data-ttu-id="3b7b3-115">Le membre **pszText** pointe vers une mémoire tampon qui reçoit le texte.</span><span class="sxs-lookup"><span data-stu-id="3b7b3-115">The **pszText** member points to a buffer that receives the text.</span></span> <span data-ttu-id="3b7b3-116">Le membre **cchTextMax** spécifie le nombre de caractères dans la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="3b7b3-116">The **cchTextMax** member specifies the number of characters in the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b7b3-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3b7b3-117">Return value</span></span>

<span data-ttu-id="3b7b3-118">Si vous envoyez ce message de manière explicite, il retourne le nombre de caractères dans le membre **pszText** de la structure [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) .</span><span class="sxs-lookup"><span data-stu-id="3b7b3-118">If you send this message explicitly, it returns the number of characters in the **pszText** member of the [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b7b3-119">Notes</span><span class="sxs-lookup"><span data-stu-id="3b7b3-119">Remarks</span></span>

<span data-ttu-id="3b7b3-120">Vous pouvez également envoyer ce message en appelant la macro [**ListView \_ GetItemText**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemtext) .</span><span class="sxs-lookup"><span data-stu-id="3b7b3-120">You can also send this message by calling the [**ListView\_GetItemText**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemtext) macro.</span></span> <span data-ttu-id="3b7b3-121">Toutefois, cette macro ne retourne pas la longueur de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="3b7b3-121">However, this macro does not return the string length.</span></span>

<span data-ttu-id="3b7b3-122">**LVM \_ GETITEMTEXT** n’est pas pris en charge sous le style [**\_ OWNERDATA LVS**](list-view-window-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="3b7b3-122">**LVM\_GETITEMTEXT** is not supported under the [**LVS\_OWNERDATA**](list-view-window-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b7b3-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3b7b3-123">Requirements</span></span>



| <span data-ttu-id="3b7b3-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3b7b3-124">Requirement</span></span> | <span data-ttu-id="3b7b3-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="3b7b3-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3b7b3-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3b7b3-126">Minimum supported client</span></span><br/> | <span data-ttu-id="3b7b3-127">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3b7b3-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3b7b3-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3b7b3-128">Minimum supported server</span></span><br/> | <span data-ttu-id="3b7b3-129">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3b7b3-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3b7b3-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="3b7b3-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="3b7b3-131"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3b7b3-131"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="3b7b3-132">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="3b7b3-132">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="3b7b3-133">**LVM \_ GETITEMTEXTW** (Unicode) et **LVM \_ GETITEMTEXTA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="3b7b3-133">**LVM\_GETITEMTEXTW** (Unicode) and **LVM\_GETITEMTEXTA** (ANSI)</span></span><br/>           |



 

 





