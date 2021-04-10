---
title: Message TBM_GETLINESIZE (commctrl. h)
description: Récupère le nombre de positions logiques placées dans le curseur de la barre de défilement en réponse à l’entrée au clavier à partir des touches de direction, telles que les touches ou. Les positions logiques sont les incréments de l’entier dans la plage de la plage de la barre de défilement minimale à la position maximale du curseur.
ms.assetid: b596060a-5bac-4b31-82f3-ee4744a9779c
keywords:
- TBM_GETLINESIZE les contrôles de message Windows
topic_type:
- apiref
api_name:
- TBM_GETLINESIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86eb103f34461e545f5a9f56148c48364d880dbe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942904"
---
# <a name="tbm_getlinesize-message"></a><span data-ttu-id="d7ef4-105">\_Message TBM GETLINESIZE</span><span class="sxs-lookup"><span data-stu-id="d7ef4-105">TBM\_GETLINESIZE message</span></span>

<span data-ttu-id="d7ef4-106">Récupère le nombre de positions logiques placées dans le curseur de la barre de défilement en réponse à l’entrée au clavier à partir des touches de direction, telles que les touches ou.</span><span class="sxs-lookup"><span data-stu-id="d7ef4-106">Retrieves the number of logical positions the trackbar's slider moves in response to keyboard input from the arrow keys, such as the or keys.</span></span> <span data-ttu-id="d7ef4-107">Les positions logiques sont les incréments de l’entier dans la plage de la plage de la barre de défilement minimale à la position maximale du curseur.</span><span class="sxs-lookup"><span data-stu-id="d7ef4-107">The logical positions are the integer increments in the trackbar's range of minimum to maximum slider positions.</span></span>

## <a name="parameters"></a><span data-ttu-id="d7ef4-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d7ef4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7ef4-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d7ef4-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="d7ef4-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="d7ef4-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="d7ef4-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d7ef4-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="d7ef4-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="d7ef4-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7ef4-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d7ef4-113">Return value</span></span>

<span data-ttu-id="d7ef4-114">Retourne une valeur 32 bits qui spécifie la taille de ligne du TrackBar.</span><span class="sxs-lookup"><span data-stu-id="d7ef4-114">Returns a 32-bit value that specifies the line size for the trackbar.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7ef4-115">Notes</span><span class="sxs-lookup"><span data-stu-id="d7ef4-115">Remarks</span></span>

<span data-ttu-id="d7ef4-116">La valeur par défaut de la taille de ligne est 1.</span><span class="sxs-lookup"><span data-stu-id="d7ef4-116">The default setting for the line size is 1.</span></span>

<span data-ttu-id="d7ef4-117">Le TrackBar envoie également un message [**WM \_ HSCROLL**](wm-hscroll.md) ou [**WM \_ VSCROLL**](wm-vscroll.md) avec les \_ codes de notification de la programmation to et de to \_ LINEDOWN à sa fenêtre parente quand l’utilisateur appuie sur les touches de direction.</span><span class="sxs-lookup"><span data-stu-id="d7ef4-117">The trackbar also sends a [**WM\_HSCROLL**](wm-hscroll.md) or [**WM\_VSCROLL**](wm-vscroll.md) message with the TB\_LINEUP and TB\_LINEDOWN notification codes to its parent window when the user presses the arrow keys.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7ef4-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d7ef4-118">Requirements</span></span>



| <span data-ttu-id="d7ef4-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d7ef4-119">Requirement</span></span> | <span data-ttu-id="d7ef4-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="d7ef4-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d7ef4-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d7ef4-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d7ef4-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d7ef4-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d7ef4-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d7ef4-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d7ef4-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d7ef4-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d7ef4-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="d7ef4-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7ef4-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7ef4-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





