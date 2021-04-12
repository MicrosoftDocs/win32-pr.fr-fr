---
title: Message TBM_GETPOS (commctrl. h)
description: Récupère la position logique actuelle du curseur dans un TrackBar. Les positions logiques sont les valeurs entières de la plage de la plage de la barre de défilement minimale à la position maximale du curseur.
ms.assetid: 6f082ab2-2f9a-4bc0-bfca-56f7b1a2d921
keywords:
- TBM_GETPOS les contrôles de message Windows
topic_type:
- apiref
api_name:
- TBM_GETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 072ff9b8a107fe19afb1fee6107a2f05bad36025
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465367"
---
# <a name="tbm_getpos-message"></a><span data-ttu-id="315f6-105">\_Message TBM GETPOS</span><span class="sxs-lookup"><span data-stu-id="315f6-105">TBM\_GETPOS message</span></span>

<span data-ttu-id="315f6-106">Récupère la position logique actuelle du curseur dans un TrackBar.</span><span class="sxs-lookup"><span data-stu-id="315f6-106">Retrieves the current logical position of the slider in a trackbar.</span></span> <span data-ttu-id="315f6-107">Les positions logiques sont les valeurs entières de la plage de la plage de la barre de défilement minimale à la position maximale du curseur.</span><span class="sxs-lookup"><span data-stu-id="315f6-107">The logical positions are the integer values in the trackbar's range of minimum to maximum slider positions.</span></span>

## <a name="parameters"></a><span data-ttu-id="315f6-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="315f6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="315f6-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="315f6-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="315f6-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="315f6-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="315f6-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="315f6-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="315f6-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="315f6-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="315f6-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="315f6-113">Return value</span></span>

<span data-ttu-id="315f6-114">Retourne une valeur 32 bits qui spécifie la position logique actuelle du curseur de la barre de défilement.</span><span class="sxs-lookup"><span data-stu-id="315f6-114">Returns a 32-bit value that specifies the current logical position of the trackbar's slider.</span></span>

## <a name="requirements"></a><span data-ttu-id="315f6-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="315f6-115">Requirements</span></span>



| <span data-ttu-id="315f6-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="315f6-116">Requirement</span></span> | <span data-ttu-id="315f6-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="315f6-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="315f6-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="315f6-118">Minimum supported client</span></span><br/> | <span data-ttu-id="315f6-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="315f6-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="315f6-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="315f6-120">Minimum supported server</span></span><br/> | <span data-ttu-id="315f6-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="315f6-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="315f6-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="315f6-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="315f6-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="315f6-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="315f6-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="315f6-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="315f6-125">**TBM \_ SetPos**</span><span class="sxs-lookup"><span data-stu-id="315f6-125">**TBM\_SETPOS**</span></span>](tbm-setpos.md)
</dt> </dl>

 

 





