---
title: Message LVM_GETITEMPOSITION (commctrl. h)
description: Récupère la position d’un élément de vue de liste. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView GetItemPosition.
ms.assetid: e5841089-c34e-498e-b94c-45c845bfc747
keywords:
- LVM_GETITEMPOSITION les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_GETITEMPOSITION
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f40b5899634e2f357068caa6ef96339be82f600b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844101"
---
# <a name="lvm_getitemposition-message"></a><span data-ttu-id="a220b-105">\_Message GETITEMPOSITION LVM</span><span class="sxs-lookup"><span data-stu-id="a220b-105">LVM\_GETITEMPOSITION message</span></span>

<span data-ttu-id="a220b-106">Récupère la position d’un élément de vue de liste.</span><span class="sxs-lookup"><span data-stu-id="a220b-106">Retrieves the position of a list-view item.</span></span> <span data-ttu-id="a220b-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ListView \_ GetItemPosition**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemposition) .</span><span class="sxs-lookup"><span data-stu-id="a220b-107">You can send this message explicitly or by using the [**ListView\_GetItemPosition**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemposition) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="a220b-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a220b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a220b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a220b-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a220b-110">Index de l’élément de vue de liste.</span><span class="sxs-lookup"><span data-stu-id="a220b-110">Index of the list-view item.</span></span>

</dd> <dt>

<span data-ttu-id="a220b-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a220b-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a220b-112">Pointeur vers une structure de [**points**](/previous-versions//dd162805(v=vs.85)) qui reçoit la position de l’angle supérieur gauche de l’élément, dans les coordonnées de la vue.</span><span class="sxs-lookup"><span data-stu-id="a220b-112">Pointer to a [**POINT**](/previous-versions//dd162805(v=vs.85)) structure that receives the position of the item's upper-left corner, in view coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a220b-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a220b-113">Return value</span></span>

<span data-ttu-id="a220b-114">Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="a220b-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="a220b-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a220b-115">Requirements</span></span>



| <span data-ttu-id="a220b-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a220b-116">Requirement</span></span> | <span data-ttu-id="a220b-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="a220b-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a220b-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a220b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a220b-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a220b-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a220b-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a220b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a220b-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a220b-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a220b-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="a220b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="a220b-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a220b-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

