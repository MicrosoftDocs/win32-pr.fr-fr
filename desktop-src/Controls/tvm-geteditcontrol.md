---
title: Message TVM_GETEDITCONTROL (commctrl. h)
description: Récupère le handle du contrôle d’édition utilisé pour modifier le texte d’un élément d’affichage d’arborescence. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro GetEditControl TreeView.
ms.assetid: c89e57e8-e113-47a1-85e6-bb68990f9c1a
keywords:
- TVM_GETEDITCONTROL les contrôles de message Windows
topic_type:
- apiref
api_name:
- TVM_GETEDITCONTROL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79b4ce0beb125218e65c2c342caf59b57473088e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105961"
---
# <a name="tvm_geteditcontrol-message"></a><span data-ttu-id="79671-105">TVM \_ GETEDITCONTROL message</span><span class="sxs-lookup"><span data-stu-id="79671-105">TVM\_GETEDITCONTROL message</span></span>

<span data-ttu-id="79671-106">Récupère le handle du contrôle d’édition utilisé pour modifier le texte d’un élément d’affichage d’arborescence.</span><span class="sxs-lookup"><span data-stu-id="79671-106">Retrieves the handle to the edit control being used to edit a tree-view item's text.</span></span> <span data-ttu-id="79671-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**\_ GetEditControl TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_geteditcontrol) .</span><span class="sxs-lookup"><span data-stu-id="79671-107">You can send this message explicitly or by using the [**TreeView\_GetEditControl**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_geteditcontrol) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="79671-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="79671-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79671-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="79671-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="79671-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="79671-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="79671-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="79671-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="79671-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="79671-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79671-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="79671-113">Return value</span></span>

<span data-ttu-id="79671-114">Retourne le handle du contrôle d’édition en cas de réussite, ou **null** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="79671-114">Returns the handle to the edit control if successful, or **NULL** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="79671-115">Notes</span><span class="sxs-lookup"><span data-stu-id="79671-115">Remarks</span></span>

<span data-ttu-id="79671-116">Lorsque la modification d’étiquette commence, un contrôle d’édition est créé, mais n’est pas positionné ni affiché.</span><span class="sxs-lookup"><span data-stu-id="79671-116">When label editing begins, an edit control is created, but not positioned or displayed.</span></span> <span data-ttu-id="79671-117">Avant qu’il ne soit affiché, le contrôle Tree-View envoie sa fenêtre parente à un code de notification [TVN \_ BEGINLABELEDIT](tvn-beginlabeledit.md) .</span><span class="sxs-lookup"><span data-stu-id="79671-117">Before it is displayed, the tree-view control sends its parent window an [TVN\_BEGINLABELEDIT](tvn-beginlabeledit.md) notification code.</span></span>

<span data-ttu-id="79671-118">Pour personnaliser la modification des étiquettes, implémentez un gestionnaire pour [TVN \_ BEGINLABELEDIT](tvn-beginlabeledit.md) et envoyez un message **TVM \_ GETEDITCONTROL** au contrôle Tree-View.</span><span class="sxs-lookup"><span data-stu-id="79671-118">To customize label editing, implement a handler for [TVN\_BEGINLABELEDIT](tvn-beginlabeledit.md) and have it send a **TVM\_GETEDITCONTROL** message to the tree-view control.</span></span> <span data-ttu-id="79671-119">Si une étiquette est en cours de modification, la valeur de retour est un handle pour le contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="79671-119">If a label is being edited, the return value will be a handle to the edit control.</span></span> <span data-ttu-id="79671-120">Utilisez ce handle pour personnaliser le contrôle d’édition en envoyant les messages **em \_ xxx** habituels.</span><span class="sxs-lookup"><span data-stu-id="79671-120">Use this handle to customize the edit control by sending the usual **EM\_XXX** messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="79671-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="79671-121">Requirements</span></span>



| <span data-ttu-id="79671-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="79671-122">Requirement</span></span> | <span data-ttu-id="79671-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="79671-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="79671-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="79671-124">Minimum supported client</span></span><br/> | <span data-ttu-id="79671-125">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="79671-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="79671-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="79671-126">Minimum supported server</span></span><br/> | <span data-ttu-id="79671-127">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="79671-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="79671-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="79671-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="79671-129"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="79671-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





