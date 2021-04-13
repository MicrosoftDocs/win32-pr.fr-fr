---
title: Message LVM_SCROLL (commctrl. h)
description: Fait défiler le contenu d’un contrôle List-View. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro de défilement ListView.
ms.assetid: 4bf6b74e-8fea-48ca-a151-8fd649fc50f8
keywords:
- LVM_SCROLL les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_SCROLL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c05c3ed991cfc933a4436baf332b49c67a907b11
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465870"
---
# <a name="lvm_scroll-message"></a><span data-ttu-id="dc222-105">\_Message de défilement LVM</span><span class="sxs-lookup"><span data-stu-id="dc222-105">LVM\_SCROLL message</span></span>

<span data-ttu-id="dc222-106">Fait défiler le contenu d’un contrôle List-View.</span><span class="sxs-lookup"><span data-stu-id="dc222-106">Scrolls the content of a list-view control.</span></span> <span data-ttu-id="dc222-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro de [**\_ défilement ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_scroll) .</span><span class="sxs-lookup"><span data-stu-id="dc222-107">You can send this message explicitly or by using the [**ListView\_Scroll**](/windows/desktop/api/Commctrl/nf-commctrl-listview_scroll) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="dc222-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dc222-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc222-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="dc222-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dc222-110">Valeur de type **int** qui spécifie la quantité de défilement horizontal, en pixels, par rapport à la position actuelle du contenu de la vue de liste.</span><span class="sxs-lookup"><span data-stu-id="dc222-110">Value of type **int** that specifies the amount of horizontal scrolling, in pixels, relative to the current position of the list view content.</span></span> <span data-ttu-id="dc222-111">Si le contrôle de liste est en mode liste, cette valeur est arrondie au nombre de pixels le plus proche qui forme une colonne entière.</span><span class="sxs-lookup"><span data-stu-id="dc222-111">If the list-view control is in list view, this value is rounded up to the nearest number of pixels that form a whole column.</span></span>

</dd> <dt>

<span data-ttu-id="dc222-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="dc222-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dc222-113">Valeur de type **int** qui spécifie la quantité de défilement vertical, en pixels, par rapport à la position actuelle du contenu de la vue de liste.</span><span class="sxs-lookup"><span data-stu-id="dc222-113">Value of type **int** that specifies the amount of vertical scrolling, in pixels, relative to the current position of the list view content.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc222-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dc222-114">Return value</span></span>

<span data-ttu-id="dc222-115">Retourne la **valeur true** en cas de réussite ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="dc222-115">Returns **TRUE** if successful; otherwise, **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="dc222-116">Notes</span><span class="sxs-lookup"><span data-stu-id="dc222-116">Remarks</span></span>

<span data-ttu-id="dc222-117">Lorsque le contrôle de liste est en mode rapport, le contrôle ne peut être défilé que verticalement dans l’intégralité des incréments de la ligne.</span><span class="sxs-lookup"><span data-stu-id="dc222-117">When the list-view control is in report view, the control can only be scrolled vertically in whole line increments.</span></span> <span data-ttu-id="dc222-118">Par conséquent, le paramètre *lParam* est arrondi au nombre de pixels le plus proche qui constitue un incrément de ligne entier.</span><span class="sxs-lookup"><span data-stu-id="dc222-118">Therefore, the *lParam* parameter will be rounded to the nearest number of pixels that form a whole line increment.</span></span> <span data-ttu-id="dc222-119">Par exemple, si la hauteur d’une ligne est de 16 pixels et que 8 est passé pour *lParam*, la liste défilera de 16 pixels (1 ligne).</span><span class="sxs-lookup"><span data-stu-id="dc222-119">For example, if the height of a line is 16 pixels and 8 is passed for *lParam*, the list will be scrolled by 16 pixels (1 line).</span></span> <span data-ttu-id="dc222-120">Si la valeur 7 est passée pour *lParam*, la liste est défilante de 0 pixel (0 ligne).</span><span class="sxs-lookup"><span data-stu-id="dc222-120">If 7 is passed for *lParam*, the list will be scrolled 0 pixels (0 lines).</span></span>

## <a name="requirements"></a><span data-ttu-id="dc222-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dc222-121">Requirements</span></span>



| <span data-ttu-id="dc222-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dc222-122">Requirement</span></span> | <span data-ttu-id="dc222-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="dc222-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dc222-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dc222-124">Minimum supported client</span></span><br/> | <span data-ttu-id="dc222-125">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dc222-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="dc222-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dc222-126">Minimum supported server</span></span><br/> | <span data-ttu-id="dc222-127">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dc222-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="dc222-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="dc222-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="dc222-129"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="dc222-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





