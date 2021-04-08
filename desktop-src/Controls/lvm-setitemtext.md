---
title: Message LVM_SETITEMTEXT (commctrl. h)
description: Modifie le texte d’un élément ou d’un sous-élément de vue de liste. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView SetItemText.
ms.assetid: 1a9c7e4d-78e0-44c7-bf4f-d0fc7a0049f3
keywords:
- LVM_SETITEMTEXT les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_SETITEMTEXT
- LVM_SETITEMTEXTA
- LVM_SETITEMTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d326e48047325fc9aff2c6607da6d7d377965adf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843665"
---
# <a name="lvm_setitemtext-message"></a><span data-ttu-id="7ac3e-105">\_Message SETITEMTEXT LVM</span><span class="sxs-lookup"><span data-stu-id="7ac3e-105">LVM\_SETITEMTEXT message</span></span>

<span data-ttu-id="7ac3e-106">Modifie le texte d’un élément ou d’un sous-élément de vue de liste.</span><span class="sxs-lookup"><span data-stu-id="7ac3e-106">Changes the text of a list-view item or subitem.</span></span> <span data-ttu-id="7ac3e-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ListView \_ SetItemText**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemtext) .</span><span class="sxs-lookup"><span data-stu-id="7ac3e-107">You can send this message explicitly or by using the [**ListView\_SetItemText**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemtext) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="7ac3e-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7ac3e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ac3e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7ac3e-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7ac3e-110">Index de base zéro de l’élément de vue de liste.</span><span class="sxs-lookup"><span data-stu-id="7ac3e-110">Zero-based index of the list-view item.</span></span>

</dd> <dt>

<span data-ttu-id="7ac3e-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7ac3e-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7ac3e-112">Pointeur vers une structure [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) .</span><span class="sxs-lookup"><span data-stu-id="7ac3e-112">Pointer to an [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure.</span></span> <span data-ttu-id="7ac3e-113">Le membre **iSubItem** est l’index du sous-élément, ou il peut être égal à zéro pour définir l’étiquette de l’élément.</span><span class="sxs-lookup"><span data-stu-id="7ac3e-113">The **iSubItem** member is the index of the subitem, or it can be zero to set the item label.</span></span> <span data-ttu-id="7ac3e-114">Le membre **pszText** est l’adresse d’une chaîne se terminant par un caractère null qui contient le nouveau texte ; elle peut également avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="7ac3e-114">The **pszText** member is the address of a null-terminated string containing the new text; it can also be **NULL**.</span></span> <span data-ttu-id="7ac3e-115">Le membre **pszText** peut également être LPSTR \_ TEXTCALLBACK pour indiquer un élément de rappel pour lequel la fenêtre parente stocke le texte.</span><span class="sxs-lookup"><span data-stu-id="7ac3e-115">The **pszText** member can also be LPSTR\_TEXTCALLBACK to indicate a callback item for which the parent window stores the text.</span></span> <span data-ttu-id="7ac3e-116">Dans ce cas, le contrôle List-View envoie au parent un code de notification [**LVN \_ GETDISPINFO**](lvn-getdispinfo.md) lorsqu’il a besoin du texte.</span><span class="sxs-lookup"><span data-stu-id="7ac3e-116">In this case, the list-view control sends the parent an [**LVN\_GETDISPINFO**](lvn-getdispinfo.md) notification code when it needs the text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ac3e-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7ac3e-117">Return value</span></span>

<span data-ttu-id="7ac3e-118">Si vous envoyez ce message de manière explicite, il retourne **true** en cas de réussite ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="7ac3e-118">If you send this message explicitly, it returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ac3e-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7ac3e-119">Requirements</span></span>



| <span data-ttu-id="7ac3e-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7ac3e-120">Requirement</span></span> | <span data-ttu-id="7ac3e-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="7ac3e-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7ac3e-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7ac3e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="7ac3e-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7ac3e-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7ac3e-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7ac3e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="7ac3e-125">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7ac3e-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7ac3e-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="7ac3e-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ac3e-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ac3e-127"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="7ac3e-128">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="7ac3e-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="7ac3e-129">**LVM \_ SETITEMTEXTW** (Unicode) et **LVM \_ SETITEMTEXTA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="7ac3e-129">**LVM\_SETITEMTEXTW** (Unicode) and **LVM\_SETITEMTEXTA** (ANSI)</span></span><br/>           |



 

 





