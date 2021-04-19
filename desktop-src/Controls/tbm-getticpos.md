---
title: Message TBM_GETTICPOS (commctrl. h)
description: Récupère la position physique actuelle d’une graduation dans un TrackBar.
ms.assetid: a4b0ec32-ef4e-4607-ade1-5e2be02bebe4
keywords:
- TBM_GETTICPOS les contrôles de message Windows
topic_type:
- apiref
api_name:
- TBM_GETTICPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bb1346f63e9bb10b919c678373e0e8df0724861
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511151"
---
# <a name="tbm_getticpos-message"></a><span data-ttu-id="68577-104">\_Message TBM GETTICPOS</span><span class="sxs-lookup"><span data-stu-id="68577-104">TBM\_GETTICPOS message</span></span>

<span data-ttu-id="68577-105">Récupère la position physique actuelle d’une graduation dans un TrackBar.</span><span class="sxs-lookup"><span data-stu-id="68577-105">Retrieves the current physical position of a tick mark in a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="68577-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="68577-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68577-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="68577-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="68577-108">Index de base zéro identifiant une graduation.</span><span class="sxs-lookup"><span data-stu-id="68577-108">Zero-based index identifying a tick mark.</span></span> <span data-ttu-id="68577-109">Les positions des première et dernière graduations ne sont pas directement disponibles par le biais de ce message.</span><span class="sxs-lookup"><span data-stu-id="68577-109">The positions of the first and last tick marks are not directly available via this message.</span></span>

</dd> <dt>

<span data-ttu-id="68577-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="68577-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="68577-111">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="68577-111">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68577-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="68577-112">Return value</span></span>

<span data-ttu-id="68577-113">Retourne la distance, en coordonnées clientes, à partir de la gauche ou du haut de la zone cliente du TrackBar jusqu’à la graduation spécifiée.</span><span class="sxs-lookup"><span data-stu-id="68577-113">Returns the distance, in client coordinates, from the left or top of the trackbar's client area to the specified tick mark.</span></span> <span data-ttu-id="68577-114">La valeur de retour est la coordonnée x de la graduation pour un TrackBar horizontal ou la coordonnée y pour un TrackBar vertical.</span><span class="sxs-lookup"><span data-stu-id="68577-114">The return value is the x-coordinate of the tick mark for a horizontal trackbar or the y-coordinate for a vertical trackbar.</span></span> <span data-ttu-id="68577-115">Si *wParam* n’est pas un index valide, la valeur de retour est-1.</span><span class="sxs-lookup"><span data-stu-id="68577-115">If *wParam* is not a valid index, the return value is -1.</span></span>

## <a name="remarks"></a><span data-ttu-id="68577-116">Notes</span><span class="sxs-lookup"><span data-stu-id="68577-116">Remarks</span></span>

<span data-ttu-id="68577-117">Étant donné que les première et dernière graduations ne sont pas disponibles par le biais de ce message, les index valides sont décalés par rapport à leur position de graduation sur le TrackBar.</span><span class="sxs-lookup"><span data-stu-id="68577-117">Because the first and last tick marks are not available through this message, valid indexes are offset from their tick position on the trackbar.</span></span> <span data-ttu-id="68577-118">Si la différence entre [**TBM \_ GETRANGEMIN**](tbm-getrangemin.md) et [**TBM \_ GETRANGEMAX**](tbm-getrangemax.md) est inférieure à deux, alors il n’y a pas d’index valide et ce message échoue.</span><span class="sxs-lookup"><span data-stu-id="68577-118">If the difference between [**TBM\_GETRANGEMIN**](tbm-getrangemin.md) and [**TBM\_GETRANGEMAX**](tbm-getrangemax.md) is less than two, then there is no valid index and this message will fail.</span></span>

<span data-ttu-id="68577-119">L’exemple suivant illustre la relation entre les graduations sur un TrackBar, les graduations disponibles dans ce message et leurs index de base zéro.</span><span class="sxs-lookup"><span data-stu-id="68577-119">The following illustrates the relation between the ticks on a trackbar, the ticks available through this message, and their zero-based indexes.</span></span>

``` syntax
0 1 2 3 4 5 6 7 8 9    // Tick positions seen on the trackbar.
  1 2 3 4 5 6 7 8      // Tick positions whose position can be identified.
  0 1 2 3 4 5 6 7      // Index numbers for the identifiable positions.
```

## <a name="requirements"></a><span data-ttu-id="68577-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="68577-120">Requirements</span></span>



| <span data-ttu-id="68577-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="68577-121">Requirement</span></span> | <span data-ttu-id="68577-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="68577-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="68577-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="68577-123">Minimum supported client</span></span><br/> | <span data-ttu-id="68577-124">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="68577-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="68577-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="68577-125">Minimum supported server</span></span><br/> | <span data-ttu-id="68577-126">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="68577-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="68577-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="68577-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="68577-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="68577-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





