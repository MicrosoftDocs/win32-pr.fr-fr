---
title: Message LVM_GETWORKAREAS (commctrl. h)
description: Récupère les zones de travail à partir d’un contrôle List-View. Vous pouvez envoyer ce message explicitement ou utiliser la \_ macro ListView GetWorkAreas.
ms.assetid: 956368d9-bbb4-414a-ba17-0e8e4f0f1a45
keywords:
- LVM_GETWORKAREAS les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_GETWORKAREAS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a64546a17489eaf88a4d15430c6be26017a8d33
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466499"
---
# <a name="lvm_getworkareas-message"></a><span data-ttu-id="10dda-105">\_Message GETWORKAREAS LVM</span><span class="sxs-lookup"><span data-stu-id="10dda-105">LVM\_GETWORKAREAS message</span></span>

<span data-ttu-id="10dda-106">Récupère les zones de travail à partir d’un contrôle List-View.</span><span class="sxs-lookup"><span data-stu-id="10dda-106">Retrieves the working areas from a list-view control.</span></span> <span data-ttu-id="10dda-107">Vous pouvez envoyer ce message explicitement ou utiliser la macro [**ListView \_ GetWorkAreas**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getworkareas) .</span><span class="sxs-lookup"><span data-stu-id="10dda-107">You can send this message explicitly or use the [**ListView\_GetWorkAreas**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getworkareas) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="10dda-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="10dda-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10dda-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="10dda-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="10dda-110">Nombre de structures [**Rect**](/previous-versions//dd162897(v=vs.85)) dans le tableau au niveau de *lParam*.</span><span class="sxs-lookup"><span data-stu-id="10dda-110">The number of [**RECT**](/previous-versions//dd162897(v=vs.85)) structures in the array at *lParam*.</span></span>

</dd> <dt>

<span data-ttu-id="10dda-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="10dda-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="10dda-112">Pointeur vers un tableau de structures [**Rect**](/previous-versions//dd162897(v=vs.85)) qui reçoivent les zones de travail actuelles du contrôle List-View.</span><span class="sxs-lookup"><span data-stu-id="10dda-112">Pointer to an array of [**RECT**](/previous-versions//dd162897(v=vs.85)) structures that receive the current working areas of the list-view control.</span></span> <span data-ttu-id="10dda-113">Les valeurs de ces structures sont exprimées en coordonnées clientes.</span><span class="sxs-lookup"><span data-stu-id="10dda-113">Values in these structures are in client coordinates.</span></span> <span data-ttu-id="10dda-114">*wParam* spécifie le nombre de structures dans ce tableau.</span><span class="sxs-lookup"><span data-stu-id="10dda-114">*wParam* specifies the number of structures in this array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10dda-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="10dda-115">Return value</span></span>

<span data-ttu-id="10dda-116">La valeur de retour de ce message n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="10dda-116">The return value for this message is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="10dda-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="10dda-117">Requirements</span></span>



| <span data-ttu-id="10dda-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="10dda-118">Requirement</span></span> | <span data-ttu-id="10dda-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="10dda-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="10dda-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="10dda-120">Minimum supported client</span></span><br/> | <span data-ttu-id="10dda-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="10dda-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="10dda-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="10dda-122">Minimum supported server</span></span><br/> | <span data-ttu-id="10dda-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="10dda-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="10dda-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="10dda-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="10dda-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="10dda-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10dda-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="10dda-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10dda-127">Utilisation de contrôles List-View</span><span class="sxs-lookup"><span data-stu-id="10dda-127">Using List-View Controls</span></span>](using-list-view-controls.md)
</dt> </dl>

 

