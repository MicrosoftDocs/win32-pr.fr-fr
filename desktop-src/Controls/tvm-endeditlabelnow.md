---
title: Message TVM_ENDEDITLABELNOW (commctrl. h)
description: Termine la modification de l’étiquette d’un élément d’affichage d’arborescence. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro EndEditLabelNow TreeView.
ms.assetid: 68de2020-9311-4958-859a-de55f5e41fcf
keywords:
- TVM_ENDEDITLABELNOW les contrôles de message Windows
topic_type:
- apiref
api_name:
- TVM_ENDEDITLABELNOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f059be20560adeb8cbcb0c63a2555283f6b7051
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508449"
---
# <a name="tvm_endeditlabelnow-message"></a><span data-ttu-id="b4da2-105">TVM \_ ENDEDITLABELNOW message</span><span class="sxs-lookup"><span data-stu-id="b4da2-105">TVM\_ENDEDITLABELNOW message</span></span>

<span data-ttu-id="b4da2-106">Termine la modification de l’étiquette d’un élément d’affichage d’arborescence.</span><span class="sxs-lookup"><span data-stu-id="b4da2-106">Ends the editing of a tree-view item's label.</span></span> <span data-ttu-id="b4da2-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**\_ EndEditLabelNow TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_endeditlabelnow) .</span><span class="sxs-lookup"><span data-stu-id="b4da2-107">You can send this message explicitly or by using the [**TreeView\_EndEditLabelNow**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_endeditlabelnow) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="b4da2-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b4da2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4da2-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b4da2-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b4da2-110">Variable qui indique si la modification est annulée sans être enregistrée dans l’étiquette.</span><span class="sxs-lookup"><span data-stu-id="b4da2-110">Variable that indicates whether the editing is canceled without being saved to the label.</span></span> <span data-ttu-id="b4da2-111">Si ce paramètre a la **valeur true**, le système annule la modification sans enregistrer les modifications.</span><span class="sxs-lookup"><span data-stu-id="b4da2-111">If this parameter is **TRUE**, the system cancels editing without saving the changes.</span></span> <span data-ttu-id="b4da2-112">Dans le cas contraire, le système enregistre les modifications apportées à l’étiquette.</span><span class="sxs-lookup"><span data-stu-id="b4da2-112">Otherwise, the system saves the changes to the label.</span></span>

</dd> <dt>

<span data-ttu-id="b4da2-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b4da2-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="b4da2-114">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="b4da2-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4da2-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b4da2-115">Return value</span></span>

<span data-ttu-id="b4da2-116">Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="b4da2-116">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="b4da2-117">Notes</span><span class="sxs-lookup"><span data-stu-id="b4da2-117">Remarks</span></span>

<span data-ttu-id="b4da2-118">Ce message entraîne l’envoi du code de notification [TVN \_ ENDLABELEDIT](tvn-endlabeledit.md) à la fenêtre parente du contrôle Tree-View.</span><span class="sxs-lookup"><span data-stu-id="b4da2-118">This message causes the [TVN\_ENDLABELEDIT](tvn-endlabeledit.md) notification code to be sent to the parent window of the tree-view control.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4da2-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b4da2-119">Requirements</span></span>



| <span data-ttu-id="b4da2-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b4da2-120">Requirement</span></span> | <span data-ttu-id="b4da2-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="b4da2-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b4da2-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b4da2-122">Minimum supported client</span></span><br/> | <span data-ttu-id="b4da2-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b4da2-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b4da2-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b4da2-124">Minimum supported server</span></span><br/> | <span data-ttu-id="b4da2-125">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b4da2-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b4da2-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="b4da2-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="b4da2-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4da2-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





