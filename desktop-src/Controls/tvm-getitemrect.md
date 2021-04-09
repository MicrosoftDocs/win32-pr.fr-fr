---
title: Message TVM_GETITEMRECT (commctrl. h)
description: Récupère le rectangle englobant d’un élément d’arborescence et indique si l’élément est visible. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro GetItemRect TreeView.
ms.assetid: f2d7d7b1-cfe7-4361-bd90-e3e99dbcd99c
keywords:
- TVM_GETITEMRECT les contrôles de message Windows
topic_type:
- apiref
api_name:
- TVM_GETITEMRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebdf4d73fb83ddbd8e9e682f11ee1f5ecfbd5153
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103461"
---
# <a name="tvm_getitemrect-message"></a><span data-ttu-id="4e7ea-105">TVM \_ GETITEMRECT message</span><span class="sxs-lookup"><span data-stu-id="4e7ea-105">TVM\_GETITEMRECT message</span></span>

<span data-ttu-id="4e7ea-106">Récupère le rectangle englobant d’un élément d’arborescence et indique si l’élément est visible.</span><span class="sxs-lookup"><span data-stu-id="4e7ea-106">Retrieves the bounding rectangle for a tree-view item and indicates whether the item is visible.</span></span> <span data-ttu-id="4e7ea-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**\_ GetItemRect TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitemrect) .</span><span class="sxs-lookup"><span data-stu-id="4e7ea-107">You can send this message explicitly or by using the [**TreeView\_GetItemRect**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitemrect) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="4e7ea-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4e7ea-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e7ea-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4e7ea-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4e7ea-110">Valeur spécifiant la partie de l’élément dont le rectangle englobant doit être récupéré.</span><span class="sxs-lookup"><span data-stu-id="4e7ea-110">Value specifying the portion of the item for which to retrieve the bounding rectangle.</span></span> <span data-ttu-id="4e7ea-111">Si ce paramètre a la **valeur true**, le rectangle englobant comprend uniquement le texte de l’élément.</span><span class="sxs-lookup"><span data-stu-id="4e7ea-111">If this parameter is **TRUE**, the bounding rectangle includes only the text of the item.</span></span> <span data-ttu-id="4e7ea-112">Dans le cas contraire, il comprend la ligne entière occupée par l’élément dans le contrôle Tree-View.</span><span class="sxs-lookup"><span data-stu-id="4e7ea-112">Otherwise, it includes the entire line that the item occupies in the tree-view control.</span></span>

</dd> <dt>

<span data-ttu-id="4e7ea-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4e7ea-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4e7ea-114">Pointeur vers une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) qui, lors de l’envoi du message, contient le handle de l’élément pour lequel récupérer le rectangle.</span><span class="sxs-lookup"><span data-stu-id="4e7ea-114">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that, when sending the message, contains the handle of the item to retrieve the rectangle for.</span></span> <span data-ttu-id="4e7ea-115">Consultez l’exemple ci-dessous pour plus d’informations sur la façon de placer le descripteur d’élément dans ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="4e7ea-115">See the example below for more information on how to place the item handle in this parameter.</span></span> <span data-ttu-id="4e7ea-116">Après avoir retourné le message, ce paramètre contient le rectangle englobant.</span><span class="sxs-lookup"><span data-stu-id="4e7ea-116">After returning from the message, this parameter contains the bounding rectangle.</span></span> <span data-ttu-id="4e7ea-117">Les coordonnées sont relatives au coin supérieur gauche du contrôle Tree-View.</span><span class="sxs-lookup"><span data-stu-id="4e7ea-117">The coordinates are relative to the upper-left corner of the tree-view control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e7ea-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4e7ea-118">Return value</span></span>

<span data-ttu-id="4e7ea-119">Si l’élément est visible et que le rectangle englobant a été récupéré avec succès, la valeur de retour est **true**.</span><span class="sxs-lookup"><span data-stu-id="4e7ea-119">If the item is visible and the bounding rectangle was successfully retrieved, the return value is **TRUE**.</span></span> <span data-ttu-id="4e7ea-120">Dans le cas contraire, le message retourne la **valeur false** et ne récupère pas le rectangle englobant.</span><span class="sxs-lookup"><span data-stu-id="4e7ea-120">Otherwise, the message returns **FALSE** and does not retrieve the bounding rectangle.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e7ea-121">Notes</span><span class="sxs-lookup"><span data-stu-id="4e7ea-121">Remarks</span></span>

<span data-ttu-id="4e7ea-122">Lors de l’envoi de ce message, le paramètre *lParam* contient le handle de l’élément pour lequel le rectangle est récupéré.</span><span class="sxs-lookup"><span data-stu-id="4e7ea-122">When sending this message, the *lParam* parameter contains the handle of the item that the rectangle is being retrieved for.</span></span> <span data-ttu-id="4e7ea-123">Le descripteur est placé dans *lParam* comme indiqué dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="4e7ea-123">The handle is placed in *lParam* as shown in the following example:</span></span>


```
RECT rc;

*(HTREEITEM*)&rc = hTreeItem;

SendMessage(hwndTreeView, TVM_GETITEMRECT, FALSE, (LPARAM)&rc);
```



## <a name="requirements"></a><span data-ttu-id="4e7ea-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4e7ea-124">Requirements</span></span>



| <span data-ttu-id="4e7ea-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4e7ea-125">Requirement</span></span> | <span data-ttu-id="4e7ea-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="4e7ea-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4e7ea-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4e7ea-127">Minimum supported client</span></span><br/> | <span data-ttu-id="4e7ea-128">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4e7ea-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4e7ea-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4e7ea-129">Minimum supported server</span></span><br/> | <span data-ttu-id="4e7ea-130">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4e7ea-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4e7ea-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="4e7ea-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="4e7ea-132"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4e7ea-132"><dt>Commctrl.h</dt></span></span> </dl> |



 

