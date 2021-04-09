---
title: Message TBM_GETRANGEMIN (commctrl. h)
description: Récupère la position minimale du curseur dans un TrackBar.
ms.assetid: 64334aed-0403-4785-829e-693292734d10
keywords:
- TBM_GETRANGEMIN les contrôles de message Windows
topic_type:
- apiref
api_name:
- TBM_GETRANGEMIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fddef597f7b129f8334f75136f56404a8ef117fa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942160"
---
# <a name="tbm_getrangemin-message"></a><span data-ttu-id="c3462-104">\_Message TBM GETRANGEMIN</span><span class="sxs-lookup"><span data-stu-id="c3462-104">TBM\_GETRANGEMIN message</span></span>

<span data-ttu-id="c3462-105">Récupère la position minimale du curseur dans un TrackBar.</span><span class="sxs-lookup"><span data-stu-id="c3462-105">Retrieves the minimum position for the slider in a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="c3462-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c3462-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3462-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c3462-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="c3462-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="c3462-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="c3462-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c3462-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="c3462-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="c3462-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3462-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c3462-111">Return value</span></span>

<span data-ttu-id="c3462-112">Retourne une valeur de 32 bits qui spécifie la position minimale dans la plage des positions minimale et maximale des curseurs dans la plage du TrackBar.</span><span class="sxs-lookup"><span data-stu-id="c3462-112">Returns a 32-bit value that specifies the minimum position in the trackbar's range of minimum to maximum slider positions.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3462-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c3462-113">Requirements</span></span>



| <span data-ttu-id="c3462-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c3462-114">Requirement</span></span> | <span data-ttu-id="c3462-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="c3462-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c3462-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c3462-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c3462-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c3462-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c3462-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c3462-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c3462-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c3462-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c3462-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="c3462-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="c3462-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c3462-121"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3462-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c3462-122">See also</span></span>

<dl> <dt>

<span data-ttu-id="c3462-123">**Référence**</span><span class="sxs-lookup"><span data-stu-id="c3462-123">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c3462-124">**TBM \_ GETRANGEMAX**</span><span class="sxs-lookup"><span data-stu-id="c3462-124">**TBM\_GETRANGEMAX**</span></span>](tbm-getrangemax.md)
</dt> <dt>

[<span data-ttu-id="c3462-125">**TBM \_ SEtrange**</span><span class="sxs-lookup"><span data-stu-id="c3462-125">**TBM\_SETRANGE**</span></span>](tbm-setrange.md)
</dt> <dt>

[<span data-ttu-id="c3462-126">**TBM \_ SETRANGEMAX**</span><span class="sxs-lookup"><span data-stu-id="c3462-126">**TBM\_SETRANGEMAX**</span></span>](tbm-setrangemax.md)
</dt> </dl>

 

 





