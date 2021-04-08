---
title: Message TVM_SHOWINFOTIP (commctrl. h)
description: Affiche l’info-bulle d’un élément spécifié dans un contrôle Tree-View. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ShowInfoTip TreeView.
ms.assetid: ed5a1bda-5754-4bb3-aa22-8faaf1af1268
keywords:
- TVM_SHOWINFOTIP les contrôles de message Windows
topic_type:
- apiref
api_name:
- TVM_SHOWINFOTIP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76f147253800469a800677a242ff0ab0ccdbdfa4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844362"
---
# <a name="tvm_showinfotip-message"></a><span data-ttu-id="9c692-105">TVM \_ SHOWINFOTIP message</span><span class="sxs-lookup"><span data-stu-id="9c692-105">TVM\_SHOWINFOTIP message</span></span>

<span data-ttu-id="9c692-106">Affiche l’info-bulle d’un élément spécifié dans un contrôle Tree-View.</span><span class="sxs-lookup"><span data-stu-id="9c692-106">Shows the infotip for a specified item in a tree-view control.</span></span> <span data-ttu-id="9c692-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**\_ ShowInfoTip TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_showinfotip) .</span><span class="sxs-lookup"><span data-stu-id="9c692-107">You can send this message explicitly or by using the [**TreeView\_ShowInfoTip**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_showinfotip) macro..</span></span>

## <a name="parameters"></a><span data-ttu-id="9c692-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9c692-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c692-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9c692-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="9c692-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="9c692-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="9c692-111">*lParam* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9c692-111">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c692-112">Handle de l’élément.</span><span class="sxs-lookup"><span data-stu-id="9c692-112">Handle to the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c692-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9c692-113">Return value</span></span>

<span data-ttu-id="9c692-114">Retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="9c692-114">Returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="9c692-115">Notes</span><span class="sxs-lookup"><span data-stu-id="9c692-115">Remarks</span></span>

<span data-ttu-id="9c692-116">La plupart des applications n’utilisent pas ce message.</span><span class="sxs-lookup"><span data-stu-id="9c692-116">Most applications do not use this message.</span></span> <span data-ttu-id="9c692-117">Les info-bulles sont affichés automatiquement.</span><span class="sxs-lookup"><span data-stu-id="9c692-117">Infotips are shown automatically.</span></span> <span data-ttu-id="9c692-118">Pour plus d’informations, consultez Utilisation de l’arborescence info-bulles dans la vue d’ensemble des [contrôles à propos de Tree-View](tree-view-controls.md) .</span><span class="sxs-lookup"><span data-stu-id="9c692-118">For more information, see Using Tree-view Infotips in the [About Tree-View Controls](tree-view-controls.md) overview.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c692-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9c692-119">Requirements</span></span>



| <span data-ttu-id="9c692-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9c692-120">Requirement</span></span> | <span data-ttu-id="9c692-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="9c692-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9c692-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9c692-122">Minimum supported client</span></span><br/> | <span data-ttu-id="9c692-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9c692-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9c692-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9c692-124">Minimum supported server</span></span><br/> | <span data-ttu-id="9c692-125">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9c692-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9c692-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="9c692-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="9c692-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9c692-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





