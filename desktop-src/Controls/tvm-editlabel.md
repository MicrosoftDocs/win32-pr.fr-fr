---
title: Message TVM_EDITLABEL (commctrl. h)
description: Commence la modification sur place du texte de l’élément spécifié, en remplaçant le texte de l’élément par un contrôle d’édition sur une seule ligne qui contient le texte.
ms.assetid: ae844cbf-fa43-4f91-90cc-688f44bf77a5
keywords:
- TVM_EDITLABEL les contrôles de message Windows
topic_type:
- apiref
api_name:
- TVM_EDITLABEL
- TVM_EDITLABELA
- TVM_EDITLABELW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3608c3f959c45571d9bc085518b763cf505180ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941942"
---
# <a name="tvm_editlabel-message"></a><span data-ttu-id="e8743-104">TVM \_ EDITLABEL message</span><span class="sxs-lookup"><span data-stu-id="e8743-104">TVM\_EDITLABEL message</span></span>

<span data-ttu-id="e8743-105">Commence la modification sur place du texte de l’élément spécifié, en remplaçant le texte de l’élément par un contrôle d’édition sur une seule ligne qui contient le texte.</span><span class="sxs-lookup"><span data-stu-id="e8743-105">Begins in-place editing of the specified item's text, replacing the text of the item with a single-line edit control containing the text.</span></span> <span data-ttu-id="e8743-106">Ce message sélectionne et concentre implicitement l’élément spécifié.</span><span class="sxs-lookup"><span data-stu-id="e8743-106">This message implicitly selects and focuses the specified item.</span></span> <span data-ttu-id="e8743-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**\_ EditLabel TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_editlabel) .</span><span class="sxs-lookup"><span data-stu-id="e8743-107">You can send this message explicitly or by using the [**TreeView\_EditLabel**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_editlabel) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="e8743-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e8743-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8743-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e8743-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="e8743-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="e8743-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="e8743-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e8743-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e8743-112">Handle de l’élément à modifier.</span><span class="sxs-lookup"><span data-stu-id="e8743-112">Handle to the item to edit.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8743-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e8743-113">Return value</span></span>

<span data-ttu-id="e8743-114">Retourne le handle du contrôle d’édition utilisé pour modifier le texte de l’élément en cas de réussite, ou **null** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="e8743-114">Returns the handle to the edit control used to edit the item text if successful, or **NULL** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8743-115">Notes</span><span class="sxs-lookup"><span data-stu-id="e8743-115">Remarks</span></span>

<span data-ttu-id="e8743-116">Ce message envoie un code de notification [TVN \_ BEGINLABELEDIT](tvn-beginlabeledit.md) au parent du contrôle Tree-View.</span><span class="sxs-lookup"><span data-stu-id="e8743-116">This message sends a [TVN\_BEGINLABELEDIT](tvn-beginlabeledit.md) notification code to the parent of the tree-view control.</span></span>

<span data-ttu-id="e8743-117">Lorsque l’utilisateur termine ou annule la modification, le contrôle d’édition est détruit et le descripteur n’est plus valide.</span><span class="sxs-lookup"><span data-stu-id="e8743-117">When the user completes or cancels editing, the edit control is destroyed and the handle is no longer valid.</span></span> <span data-ttu-id="e8743-118">Vous pouvez sous-définir le contrôle d’édition, mais ne le détruisez pas.</span><span class="sxs-lookup"><span data-stu-id="e8743-118">You can subclass the edit control, but do not destroy it.</span></span>

<span data-ttu-id="e8743-119">Le contrôle doit avoir le focus avant d’envoyer ce message au contrôle.</span><span class="sxs-lookup"><span data-stu-id="e8743-119">The control must have the focus before you send this message to the control.</span></span> <span data-ttu-id="e8743-120">Le focus peut être défini à l’aide de la fonction [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) .</span><span class="sxs-lookup"><span data-stu-id="e8743-120">Focus can be set using the [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8743-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e8743-121">Requirements</span></span>



| <span data-ttu-id="e8743-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e8743-122">Requirement</span></span> | <span data-ttu-id="e8743-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="e8743-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e8743-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e8743-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e8743-125">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e8743-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e8743-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e8743-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e8743-127">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e8743-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e8743-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="e8743-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8743-129"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8743-129"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="e8743-130">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="e8743-130">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="e8743-131">**TVM \_ EDITLABELW** (Unicode) et **TVM \_ EDITLABELA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="e8743-131">**TVM\_EDITLABELW** (Unicode) and **TVM\_EDITLABELA** (ANSI)</span></span><br/>               |



 

