---
title: Message TVM_HITTEST (commctrl. h)
description: Détermine l’emplacement du point spécifié par rapport à la zone cliente d’un contrôle Tree-View. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro TreeView HitTest.
ms.assetid: 18ea3737-f429-4c10-9133-3b5729aa36fa
keywords:
- TVM_HITTEST les contrôles de message Windows
topic_type:
- apiref
api_name:
- TVM_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50b91a11892a2bb904d2cd7d82b5b08cea18331b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032600"
---
# <a name="tvm_hittest-message"></a><span data-ttu-id="f03d3-105">\_Message TVM HITTEST</span><span class="sxs-lookup"><span data-stu-id="f03d3-105">TVM\_HITTEST message</span></span>

<span data-ttu-id="f03d3-106">Détermine l’emplacement du point spécifié par rapport à la zone cliente d’un contrôle Tree-View.</span><span class="sxs-lookup"><span data-stu-id="f03d3-106">Determines the location of the specified point relative to the client area of a tree-view control.</span></span> <span data-ttu-id="f03d3-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**TreeView \_ HitTest**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_hittest) .</span><span class="sxs-lookup"><span data-stu-id="f03d3-107">You can send this message explicitly or by using the [**TreeView\_HitTest**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_hittest) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="f03d3-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f03d3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f03d3-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f03d3-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="f03d3-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="f03d3-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="f03d3-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f03d3-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f03d3-112">Pointeur vers une structure [**TVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-tvhittestinfo) .</span><span class="sxs-lookup"><span data-stu-id="f03d3-112">Pointer to a [**TVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-tvhittestinfo) structure.</span></span> <span data-ttu-id="f03d3-113">Lorsque le message est envoyé, le membre **PT** spécifie les coordonnées du point à tester.</span><span class="sxs-lookup"><span data-stu-id="f03d3-113">When the message is sent, the **pt** member specifies the coordinates of the point to test.</span></span> <span data-ttu-id="f03d3-114">Lorsque le message est retourné, le membre **hitem** est le handle de l’élément au point spécifié ou **null** si aucun élément n’occupe le point.</span><span class="sxs-lookup"><span data-stu-id="f03d3-114">When the message returns, the **hItem** member is the handle to the item at the specified point or **NULL** if no item occupies the point.</span></span> <span data-ttu-id="f03d3-115">En outre, lorsque le message retourne, le membre **indicateurs** est une valeur de test de positionnement qui indique l’emplacement du point spécifié.</span><span class="sxs-lookup"><span data-stu-id="f03d3-115">Also, when the message returns, the **flags** member is a hit test value that indicates the location of the specified point.</span></span> <span data-ttu-id="f03d3-116">Pour obtenir la liste des valeurs de test de positionnement, consultez la description de la structure **TVHITTESTINFO** .</span><span class="sxs-lookup"><span data-stu-id="f03d3-116">For a list of hit test values, see the description of the **TVHITTESTINFO** structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f03d3-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f03d3-117">Return value</span></span>

<span data-ttu-id="f03d3-118">Retourne le handle de l’élément d’arborescence qui occupe le point spécifié, ou **null** si aucun élément n’occupe le point.</span><span class="sxs-lookup"><span data-stu-id="f03d3-118">Returns the handle to the tree-view item that occupies the specified point, or **NULL** if no item occupies the point.</span></span>

## <a name="requirements"></a><span data-ttu-id="f03d3-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f03d3-119">Requirements</span></span>



| <span data-ttu-id="f03d3-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f03d3-120">Requirement</span></span> | <span data-ttu-id="f03d3-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="f03d3-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f03d3-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f03d3-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f03d3-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f03d3-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f03d3-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f03d3-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f03d3-125">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f03d3-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f03d3-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="f03d3-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="f03d3-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f03d3-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





