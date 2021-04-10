---
title: Message TVM_SETINDENT (commctrl. h)
description: Définit la largeur du retrait pour un contrôle d’arborescence et redessine le contrôle pour refléter la nouvelle largeur. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro SetIndent TreeView.
ms.assetid: 377da8fe-c8e6-479b-a283-f1811cbc3e58
keywords:
- TVM_SETINDENT les contrôles de message Windows
topic_type:
- apiref
api_name:
- TVM_SETINDENT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f85263c7c4330a692dc08949870a0eaa92f2b22c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104179"
---
# <a name="tvm_setindent-message"></a><span data-ttu-id="dd719-105">TVM \_ SETINDENT message</span><span class="sxs-lookup"><span data-stu-id="dd719-105">TVM\_SETINDENT message</span></span>

<span data-ttu-id="dd719-106">Définit la largeur du retrait pour un contrôle d’arborescence et redessine le contrôle pour refléter la nouvelle largeur.</span><span class="sxs-lookup"><span data-stu-id="dd719-106">Sets the width of indentation for a tree-view control and redraws the control to reflect the new width.</span></span> <span data-ttu-id="dd719-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**\_ SetIndent TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setindent) .</span><span class="sxs-lookup"><span data-stu-id="dd719-107">You can send this message explicitly or by using the [**TreeView\_SetIndent**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setindent) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="dd719-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dd719-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd719-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="dd719-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dd719-110">Largeur, en pixels, de la mise en retrait.</span><span class="sxs-lookup"><span data-stu-id="dd719-110">Width, in pixels, of the indentation.</span></span> <span data-ttu-id="dd719-111">Si ce paramètre est inférieur à la largeur minimale définie par le système, la nouvelle largeur est définie sur la valeur minimale définie par le système.</span><span class="sxs-lookup"><span data-stu-id="dd719-111">If this parameter is less than the system-defined minimum width, the new width is set to the system-defined minimum.</span></span>

</dd> <dt>

<span data-ttu-id="dd719-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="dd719-112">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="dd719-113">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="dd719-113">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd719-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dd719-114">Return value</span></span>

<span data-ttu-id="dd719-115">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="dd719-115">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="dd719-116">Notes</span><span class="sxs-lookup"><span data-stu-id="dd719-116">Remarks</span></span>

<span data-ttu-id="dd719-117">La valeur de mise en retrait minimale définie par le système est généralement de cinq pixels, mais elle n’est pas fixe.</span><span class="sxs-lookup"><span data-stu-id="dd719-117">The system-defined minimum indent value is typically five pixels, but it is not fixed.</span></span> <span data-ttu-id="dd719-118">Pour récupérer la valeur exacte du retrait minimal sur un système particulier, envoyez un message de **TVM \_ SETINDENT** avec *wParam* défini à zéro.</span><span class="sxs-lookup"><span data-stu-id="dd719-118">To retrieve the exact value of the minimum indent on a particular system, send a **TVM\_SETINDENT** message with *wParam* set to zero.</span></span> <span data-ttu-id="dd719-119">Envoyez ensuite un message [**TVM \_ GETINDENT**](tvm-getindent.md) pour récupérer la valeur de retrait minimale.</span><span class="sxs-lookup"><span data-stu-id="dd719-119">Then send a [**TVM\_GETINDENT**](tvm-getindent.md) message to retrieve the minimum indent value.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd719-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dd719-120">Requirements</span></span>



| <span data-ttu-id="dd719-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dd719-121">Requirement</span></span> | <span data-ttu-id="dd719-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="dd719-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dd719-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dd719-123">Minimum supported client</span></span><br/> | <span data-ttu-id="dd719-124">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dd719-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="dd719-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dd719-125">Minimum supported server</span></span><br/> | <span data-ttu-id="dd719-126">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dd719-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="dd719-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="dd719-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="dd719-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd719-128"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd719-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dd719-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd719-130">**\_SetIndent TreeView**</span><span class="sxs-lookup"><span data-stu-id="dd719-130">**TreeView\_SetIndent**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setindent)
</dt> </dl>

 

 





