---
title: Message TVM_SETAUTOSCROLLINFO (commctrl. h)
description: Définit les informations utilisées pour déterminer les caractéristiques de défilement automatique. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro SetAutoScrollInfo TreeView.
ms.assetid: de55933f-1caa-4193-84de-0486c41e8f1f
keywords:
- TVM_SETAUTOSCROLLINFO les contrôles de message Windows
topic_type:
- apiref
api_name:
- TVM_SETAUTOSCROLLINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: faa1f7920d2ec8c443b2ec5f1ff9189c22c5f21e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511139"
---
# <a name="tvm_setautoscrollinfo-message"></a><span data-ttu-id="a1a89-105">TVM \_ SETAUTOSCROLLINFO message</span><span class="sxs-lookup"><span data-stu-id="a1a89-105">TVM\_SETAUTOSCROLLINFO message</span></span>

<span data-ttu-id="a1a89-106">Définit les informations utilisées pour déterminer les caractéristiques de défilement automatique.</span><span class="sxs-lookup"><span data-stu-id="a1a89-106">Sets information used to determine auto-scroll characteristics.</span></span> <span data-ttu-id="a1a89-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**\_ SetAutoScrollInfo TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setautoscrollinfo) .</span><span class="sxs-lookup"><span data-stu-id="a1a89-107">You can send this message explicitly or by using the [**TreeView\_SetAutoScrollInfo**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setautoscrollinfo) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="a1a89-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a1a89-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1a89-109">*wParam* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a1a89-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1a89-110">Spécifie les pixels par seconde.</span><span class="sxs-lookup"><span data-stu-id="a1a89-110">Specifies pixels per second.</span></span> <span data-ttu-id="a1a89-111">Le décalage à faire défiler est divisé par le *wParam* pour déterminer la durée totale du défilement automatique.</span><span class="sxs-lookup"><span data-stu-id="a1a89-111">The offset to scroll is divided by the *wParam* to determine the total duration of the auto-scroll.</span></span>

</dd> <dt>

<span data-ttu-id="a1a89-112">*lParam* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a1a89-112">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1a89-113">Spécifie l’intervalle de redessination.</span><span class="sxs-lookup"><span data-stu-id="a1a89-113">Specifies the redraw time interval.</span></span> <span data-ttu-id="a1a89-114">Redessinez à chaque intervalle de elasped jusqu’à ce que l’élément fasse l’objet d’un défilement.</span><span class="sxs-lookup"><span data-stu-id="a1a89-114">Redraw at every elasped interval, until the item is scrolled into view.</span></span> <span data-ttu-id="a1a89-115">Avec *wParam* donné, l’emplacement de l’élément est calculé et un redessin se produit.</span><span class="sxs-lookup"><span data-stu-id="a1a89-115">Given *wParam*, the location of the item is calculated and a repaint occurs.</span></span> <span data-ttu-id="a1a89-116">Définissez cette valeur pour créer un défilement fluide.</span><span class="sxs-lookup"><span data-stu-id="a1a89-116">Set this value to create smooth scrolling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1a89-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a1a89-117">Return value</span></span>

<span data-ttu-id="a1a89-118">Retourne la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="a1a89-118">Returns **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1a89-119">Notes</span><span class="sxs-lookup"><span data-stu-id="a1a89-119">Remarks</span></span>

<span data-ttu-id="a1a89-120">Les informations de défilement automatique sont utilisées pour faire défiler un élément non visible dans l’affichage.</span><span class="sxs-lookup"><span data-stu-id="a1a89-120">Autoscroll information is used to scroll a nonvisible item into view.</span></span> <span data-ttu-id="a1a89-121">Le contrôle doit avoir le style étendu [**TV \_ ex \_ AUTOHSCROLL**](tree-view-control-window-extended-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="a1a89-121">The control must have the [**TVS\_EX\_AUTOHSCROLL**](tree-view-control-window-extended-styles.md) extended style.</span></span> <span data-ttu-id="a1a89-122">Pour plus d’informations sur les styles étendus, consultez Tree-View les styles étendus de contrôle.</span><span class="sxs-lookup"><span data-stu-id="a1a89-122">For information on extended styles, see Tree-View Control Extended Styles.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1a89-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a1a89-123">Requirements</span></span>



| <span data-ttu-id="a1a89-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a1a89-124">Requirement</span></span> | <span data-ttu-id="a1a89-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="a1a89-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a1a89-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a1a89-126">Minimum supported client</span></span><br/> | <span data-ttu-id="a1a89-127">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a1a89-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a1a89-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a1a89-128">Minimum supported server</span></span><br/> | <span data-ttu-id="a1a89-129">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a1a89-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a1a89-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="a1a89-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="a1a89-131"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a1a89-131"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





