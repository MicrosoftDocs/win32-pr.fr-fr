---
title: Message TBM_SETPOS (commctrl. h)
description: 'TBM_SETPOS message : définit la position logique actuelle du curseur dans un TrackBar.'
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
ms.openlocfilehash: 3f10e05a677119f18489d0eb9eebc4528d3ad115
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085867"
---
# <a name="tbm_setpos-message"></a><span data-ttu-id="ef81e-104">\_Message TBM SetPos</span><span class="sxs-lookup"><span data-stu-id="ef81e-104">TBM\_SETPOS message</span></span>

<span data-ttu-id="ef81e-105">Définit la position logique actuelle du curseur dans un TrackBar.</span><span class="sxs-lookup"><span data-stu-id="ef81e-105">Sets the current logical position of the slider in a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="ef81e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ef81e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef81e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ef81e-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ef81e-108">Indicateur de redessin.</span><span class="sxs-lookup"><span data-stu-id="ef81e-108">Redraw flag.</span></span> <span data-ttu-id="ef81e-109">Si ce paramètre a la **valeur true**, le message redessine le contrôle à l’aide du curseur à la position donnée par *lParam*.</span><span class="sxs-lookup"><span data-stu-id="ef81e-109">If this parameter is **TRUE**, the message redraws the control with the slider at the position given by *lParam*.</span></span> <span data-ttu-id="ef81e-110">Si ce paramètre a la **valeur false**, le message ne redessine pas le curseur à la nouvelle position.</span><span class="sxs-lookup"><span data-stu-id="ef81e-110">If this parameter is **FALSE**, the message does not redraw the slider at the new position.</span></span> <span data-ttu-id="ef81e-111">Notez que le message définit la valeur de la position du curseur (telle qu’elle est retournée par le message [**\_ GETPOS TBM**](tbm-getpos.md) ) quel que soit le paramètre *wParam* .</span><span class="sxs-lookup"><span data-stu-id="ef81e-111">Note that the message sets the value of the slider position (as returned by the [**TBM\_GETPOS**](tbm-getpos.md) message) regardless of the *wParam* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="ef81e-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ef81e-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ef81e-113">Nouvelle position logique du curseur.</span><span class="sxs-lookup"><span data-stu-id="ef81e-113">New logical position of the slider.</span></span> <span data-ttu-id="ef81e-114">Les positions logiques valides sont les valeurs entières de la plage de la plage de la barre de défilement minimale à la position maximale du curseur.</span><span class="sxs-lookup"><span data-stu-id="ef81e-114">Valid logical positions are the integer values in the trackbar's range of minimum to maximum slider positions.</span></span> <span data-ttu-id="ef81e-115">Si cette valeur est en dehors de la plage maximale et minimale du contrôle, la position est définie sur la valeur maximale ou minimale.</span><span class="sxs-lookup"><span data-stu-id="ef81e-115">If this value is outside the control's maximum and minimum range, the position is set to the maximum or minimum value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef81e-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ef81e-116">Return value</span></span>

<span data-ttu-id="ef81e-117">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="ef81e-117">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef81e-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ef81e-118">Requirements</span></span>



| <span data-ttu-id="ef81e-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ef81e-119">Requirement</span></span> | <span data-ttu-id="ef81e-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="ef81e-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ef81e-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ef81e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ef81e-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ef81e-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ef81e-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ef81e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ef81e-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ef81e-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ef81e-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="ef81e-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef81e-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef81e-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





