---
title: Message TBM_SETPOS (commctrl. h)
description: Définit la position logique actuelle du curseur dans un TrackBar.
ms.assetid: df6c4e5d-2847-419d-82b5-334d53bb6ba1
keywords:
- TBM_SETPOS les contrôles de message Windows
topic_type:
- apiref
api_name:
- TBM_SETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8e8da6e8e231a26b216ca8f9314d59474384857
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942875"
---
# <a name="tbm_setpos-message"></a><span data-ttu-id="f880c-104">\_Message TBM SetPos</span><span class="sxs-lookup"><span data-stu-id="f880c-104">TBM\_SETPOS message</span></span>

<span data-ttu-id="f880c-105">Définit la position logique actuelle du curseur dans un TrackBar.</span><span class="sxs-lookup"><span data-stu-id="f880c-105">Sets the current logical position of the slider in a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="f880c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f880c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f880c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f880c-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f880c-108">Indicateur de redessin.</span><span class="sxs-lookup"><span data-stu-id="f880c-108">Redraw flag.</span></span> <span data-ttu-id="f880c-109">Si ce paramètre a la **valeur true**, le message redessine le contrôle à l’aide du curseur à la position donnée par *lParam*.</span><span class="sxs-lookup"><span data-stu-id="f880c-109">If this parameter is **TRUE**, the message redraws the control with the slider at the position given by *lParam*.</span></span> <span data-ttu-id="f880c-110">Si ce paramètre a la **valeur false**, le message ne redessine pas le curseur à la nouvelle position.</span><span class="sxs-lookup"><span data-stu-id="f880c-110">If this parameter is **FALSE**, the message does not redraw the slider at the new position.</span></span> <span data-ttu-id="f880c-111">Notez que le message définit la valeur de la position du curseur (telle qu’elle est retournée par le message [**\_ GETPOS TBM**](tbm-getpos.md) ) quel que soit le paramètre *wParam* .</span><span class="sxs-lookup"><span data-stu-id="f880c-111">Note that the message sets the value of the slider position (as returned by the [**TBM\_GETPOS**](tbm-getpos.md) message) regardless of the *wParam* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="f880c-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f880c-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f880c-113">Nouvelle position logique du curseur.</span><span class="sxs-lookup"><span data-stu-id="f880c-113">New logical position of the slider.</span></span> <span data-ttu-id="f880c-114">Les positions logiques valides sont les valeurs entières de la plage de la plage de la barre de défilement minimale à la position maximale du curseur.</span><span class="sxs-lookup"><span data-stu-id="f880c-114">Valid logical positions are the integer values in the trackbar's range of minimum to maximum slider positions.</span></span> <span data-ttu-id="f880c-115">Si cette valeur est en dehors de la plage maximale et minimale du contrôle, la position est définie sur la valeur maximale ou minimale.</span><span class="sxs-lookup"><span data-stu-id="f880c-115">If this value is outside the control's maximum and minimum range, the position is set to the maximum or minimum value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f880c-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f880c-116">Return value</span></span>

<span data-ttu-id="f880c-117">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="f880c-117">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="f880c-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f880c-118">Requirements</span></span>



| <span data-ttu-id="f880c-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f880c-119">Requirement</span></span> | <span data-ttu-id="f880c-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="f880c-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f880c-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f880c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f880c-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f880c-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f880c-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f880c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f880c-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f880c-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f880c-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="f880c-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="f880c-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f880c-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





