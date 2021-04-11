---
title: Message LVM_SETWORKAREAS (commctrl. h)
description: Définit les zones de travail dans un contrôle List-View. Vous pouvez envoyer ce message explicitement ou utiliser la \_ macro ListView SetWorkAreas.
ms.assetid: 87ac192d-f481-43ac-b8a5-c754cf33e487
keywords:
- LVM_SETWORKAREAS les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_SETWORKAREAS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4166238c97b5766a5f2bbb19e0de853526d83385
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942639"
---
# <a name="lvm_setworkareas-message"></a><span data-ttu-id="d7786-105">\_Message SETWORKAREAS LVM</span><span class="sxs-lookup"><span data-stu-id="d7786-105">LVM\_SETWORKAREAS message</span></span>

<span data-ttu-id="d7786-106">Définit les zones de travail dans un contrôle List-View.</span><span class="sxs-lookup"><span data-stu-id="d7786-106">Sets the working areas within a list-view control.</span></span> <span data-ttu-id="d7786-107">Vous pouvez envoyer ce message explicitement ou utiliser la macro [**ListView \_ SetWorkAreas**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setworkareas) .</span><span class="sxs-lookup"><span data-stu-id="d7786-107">You can send this message explicitly or use the [**ListView\_SetWorkAreas**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setworkareas) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="d7786-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d7786-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7786-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d7786-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d7786-110">Nombre de structures dans le tableau à *LPRC*.</span><span class="sxs-lookup"><span data-stu-id="d7786-110">The number of structures in the array at *lprc*.</span></span> <span data-ttu-id="d7786-111">Le nombre maximal de zones de travail autorisées est défini par la \_ valeur LV Max \_ WORKAREAS.</span><span class="sxs-lookup"><span data-stu-id="d7786-111">The maximum number of working areas allowed is defined by the LV\_MAX\_WORKAREAS value.</span></span>

</dd> <dt>

<span data-ttu-id="d7786-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d7786-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d7786-113">Pointeur vers un tableau de structures [**Rect**](/previous-versions//dd162897(v=vs.85)) qui contiennent les nouvelles zones de travail du contrôle List-View.</span><span class="sxs-lookup"><span data-stu-id="d7786-113">Pointer to an array of [**RECT**](/previous-versions//dd162897(v=vs.85)) structures that contain the new working areas of the list-view control.</span></span> <span data-ttu-id="d7786-114">Les valeurs de ces structures sont exprimées en coordonnées clientes.</span><span class="sxs-lookup"><span data-stu-id="d7786-114">Values in these structures are in client coordinates.</span></span> <span data-ttu-id="d7786-115">Si ce paramètre a la **valeur null**, la zone de travail est définie sur la zone cliente du contrôle.</span><span class="sxs-lookup"><span data-stu-id="d7786-115">If this parameter is **NULL**, the working area will be set to the client area of the control.</span></span> <span data-ttu-id="d7786-116">*wParam* spécifie le nombre de structures dans ce tableau.</span><span class="sxs-lookup"><span data-stu-id="d7786-116">*wParam* specifies the number of structures in this array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7786-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d7786-117">Return value</span></span>

<span data-ttu-id="d7786-118">La valeur de retour de ce message n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="d7786-118">The return value for this message is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7786-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d7786-119">Requirements</span></span>



| <span data-ttu-id="d7786-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d7786-120">Requirement</span></span> | <span data-ttu-id="d7786-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="d7786-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d7786-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d7786-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d7786-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d7786-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d7786-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d7786-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d7786-125">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d7786-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d7786-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="d7786-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7786-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7786-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7786-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d7786-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7786-129">Utilisation de contrôles List-View</span><span class="sxs-lookup"><span data-stu-id="d7786-129">Using List-View Controls</span></span>](using-list-view-controls.md)
</dt> </dl>

 

