---
title: Message LVM_GETCOUNTPERPAGE (commctrl. h)
description: Calcule le nombre d’éléments qui peuvent s’ajuster verticalement dans la zone visible d’un contrôle List View en mode liste ou rapport. Seuls les éléments entièrement visibles sont comptés. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView GetCountPerPage.
ms.assetid: 2ffd2bb1-cddf-4a4a-a4a8-087c9dc3fec0
keywords:
- LVM_GETCOUNTPERPAGE les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_GETCOUNTPERPAGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 734d460754f9ae8a11c3a42d8eacebf31d0b6fc0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032358"
---
# <a name="lvm_getcountperpage-message"></a><span data-ttu-id="17940-106">\_Message GETCOUNTPERPAGE LVM</span><span class="sxs-lookup"><span data-stu-id="17940-106">LVM\_GETCOUNTPERPAGE message</span></span>

<span data-ttu-id="17940-107">Calcule le nombre d’éléments qui peuvent s’ajuster verticalement dans la zone visible d’un contrôle List View en mode liste ou rapport.</span><span class="sxs-lookup"><span data-stu-id="17940-107">Calculates the number of items that can fit vertically in the visible area of a list-view control when in list or report view.</span></span> <span data-ttu-id="17940-108">Seuls les éléments entièrement visibles sont comptés.</span><span class="sxs-lookup"><span data-stu-id="17940-108">Only fully visible items are counted.</span></span> <span data-ttu-id="17940-109">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ListView \_ GetCountPerPage**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcountperpage) .</span><span class="sxs-lookup"><span data-stu-id="17940-109">You can send this message explicitly or by using the [**ListView\_GetCountPerPage**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcountperpage) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="17940-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="17940-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17940-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="17940-111">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="17940-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="17940-112">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="17940-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="17940-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="17940-114">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="17940-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17940-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="17940-115">Return value</span></span>

<span data-ttu-id="17940-116">Retourne le nombre d’éléments entièrement visibles en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="17940-116">Returns the number of fully visible items if successful.</span></span> <span data-ttu-id="17940-117">Si la vue actuelle est vue icône ou petite icône, la valeur de retour est le nombre total d’éléments dans le contrôle List-View.</span><span class="sxs-lookup"><span data-stu-id="17940-117">If the current view is icon or small icon view, the return value is the total number of items in the list-view control.</span></span>

## <a name="requirements"></a><span data-ttu-id="17940-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="17940-118">Requirements</span></span>



| <span data-ttu-id="17940-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="17940-119">Requirement</span></span> | <span data-ttu-id="17940-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="17940-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="17940-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="17940-121">Minimum supported client</span></span><br/> | <span data-ttu-id="17940-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="17940-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="17940-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="17940-123">Minimum supported server</span></span><br/> | <span data-ttu-id="17940-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="17940-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="17940-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="17940-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="17940-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="17940-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





