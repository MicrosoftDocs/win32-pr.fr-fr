---
title: Message TBM_GETRANGEMAX (commctrl. h)
description: Récupère la position maximale du curseur dans un TrackBar.
ms.assetid: c0ae5f96-f4ce-46cd-84d0-9e7c473441a0
keywords:
- TBM_GETRANGEMAX les contrôles de message Windows
topic_type:
- apiref
api_name:
- TBM_GETRANGEMAX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bdd9687b617759ab8b8fdea59ed06d7fcd78b6d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032888"
---
# <a name="tbm_getrangemax-message"></a><span data-ttu-id="5db99-104">\_Message TBM GETRANGEMAX</span><span class="sxs-lookup"><span data-stu-id="5db99-104">TBM\_GETRANGEMAX message</span></span>

<span data-ttu-id="5db99-105">Récupère la position maximale du curseur dans un TrackBar.</span><span class="sxs-lookup"><span data-stu-id="5db99-105">Retrieves the maximum position for the slider in a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="5db99-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5db99-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5db99-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5db99-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="5db99-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="5db99-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="5db99-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5db99-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="5db99-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="5db99-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5db99-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5db99-111">Return value</span></span>

<span data-ttu-id="5db99-112">Retourne une valeur de 32 bits qui spécifie la position maximale dans la plage de la plage de la barre de défilement minimale à la position maximale du curseur.</span><span class="sxs-lookup"><span data-stu-id="5db99-112">Returns a 32-bit value that specifies the maximum position in the trackbar's range of minimum to maximum slider positions.</span></span>

## <a name="requirements"></a><span data-ttu-id="5db99-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5db99-113">Requirements</span></span>



| <span data-ttu-id="5db99-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5db99-114">Requirement</span></span> | <span data-ttu-id="5db99-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="5db99-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5db99-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5db99-116">Minimum supported client</span></span><br/> | <span data-ttu-id="5db99-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5db99-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5db99-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5db99-118">Minimum supported server</span></span><br/> | <span data-ttu-id="5db99-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5db99-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5db99-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="5db99-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="5db99-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5db99-121"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5db99-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5db99-122">See also</span></span>

<dl> <dt>

<span data-ttu-id="5db99-123">**Référence**</span><span class="sxs-lookup"><span data-stu-id="5db99-123">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5db99-124">**TBM \_ GETRANGEMIN**</span><span class="sxs-lookup"><span data-stu-id="5db99-124">**TBM\_GETRANGEMIN**</span></span>](tbm-getrangemin.md)
</dt> <dt>

[<span data-ttu-id="5db99-125">**TBM \_ SEtrange**</span><span class="sxs-lookup"><span data-stu-id="5db99-125">**TBM\_SETRANGE**</span></span>](tbm-setrange.md)
</dt> <dt>

[<span data-ttu-id="5db99-126">**TBM \_ SETRANGEMAX**</span><span class="sxs-lookup"><span data-stu-id="5db99-126">**TBM\_SETRANGEMAX**</span></span>](tbm-setrangemax.md)
</dt> </dl>

 

 





