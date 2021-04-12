---
title: Message SB_GETPARTS (commctrl. h)
description: Récupère le nombre de parties dans une fenêtre d’État. Le message récupère également la coordonnée du bord droit du nombre spécifié de parties.
ms.assetid: 2535f490-4d6b-468a-b13c-096941e61bf4
keywords:
- SB_GETPARTS les contrôles de message Windows
topic_type:
- apiref
api_name:
- SB_GETPARTS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cee0f33331c579490cf66a38b9ce6655215ae673
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509021"
---
# <a name="sb_getparts-message"></a><span data-ttu-id="ea07a-105">\_Message SB GETPARTS</span><span class="sxs-lookup"><span data-stu-id="ea07a-105">SB\_GETPARTS message</span></span>

<span data-ttu-id="ea07a-106">Récupère le nombre de parties dans une fenêtre d’État.</span><span class="sxs-lookup"><span data-stu-id="ea07a-106">Retrieves a count of the parts in a status window.</span></span> <span data-ttu-id="ea07a-107">Le message récupère également la coordonnée du bord droit du nombre spécifié de parties.</span><span class="sxs-lookup"><span data-stu-id="ea07a-107">The message also retrieves the coordinate of the right edge of the specified number of parts.</span></span>

## <a name="parameters"></a><span data-ttu-id="ea07a-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ea07a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea07a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ea07a-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ea07a-110">Nombre de parties pour lesquelles récupérer les coordonnées.</span><span class="sxs-lookup"><span data-stu-id="ea07a-110">Number of parts for which to retrieve coordinates.</span></span> <span data-ttu-id="ea07a-111">Si ce paramètre est supérieur au nombre de parties dans la fenêtre, le message récupère les coordonnées des parties existantes uniquement.</span><span class="sxs-lookup"><span data-stu-id="ea07a-111">If this parameter is greater than the number of parts in the window, the message retrieves coordinates for existing parts only.</span></span>

</dd> <dt>

<span data-ttu-id="ea07a-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ea07a-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ea07a-113">Pointeur vers un tableau d’entiers qui a le même nombre d’éléments que les éléments spécifiés par *wParam*.</span><span class="sxs-lookup"><span data-stu-id="ea07a-113">Pointer to an integer array that has the same number of elements as parts specified by *wParam*.</span></span> <span data-ttu-id="ea07a-114">Chaque élément du tableau reçoit la coordonnée cliente du bord droit du composant correspondant.</span><span class="sxs-lookup"><span data-stu-id="ea07a-114">Each element in the array receives the client coordinate of the right edge of the corresponding part.</span></span> <span data-ttu-id="ea07a-115">Si un élément a la valeur-1, la position du bord droit de cette partie s’étend jusqu’au bord droit de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="ea07a-115">If an element is set to -1, the position of the right edge for that part extends to the right edge of the window.</span></span> <span data-ttu-id="ea07a-116">Pour récupérer le nombre actuel de parties, définissez ce paramètre sur zéro.</span><span class="sxs-lookup"><span data-stu-id="ea07a-116">To retrieve the current number of parts, set this parameter to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea07a-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ea07a-117">Return value</span></span>

<span data-ttu-id="ea07a-118">Retourne le nombre de parties dans la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="ea07a-118">Returns the number of parts in the window.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea07a-119">Notes</span><span class="sxs-lookup"><span data-stu-id="ea07a-119">Remarks</span></span>

<span data-ttu-id="ea07a-120">Ce message retourne toujours le nombre de parties dans la barre d’État.</span><span class="sxs-lookup"><span data-stu-id="ea07a-120">This message always returns the number of parts in the status bar.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea07a-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ea07a-121">Requirements</span></span>



| <span data-ttu-id="ea07a-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ea07a-122">Requirement</span></span> | <span data-ttu-id="ea07a-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="ea07a-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ea07a-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ea07a-124">Minimum supported client</span></span><br/> | <span data-ttu-id="ea07a-125">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ea07a-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ea07a-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ea07a-126">Minimum supported server</span></span><br/> | <span data-ttu-id="ea07a-127">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ea07a-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ea07a-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="ea07a-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="ea07a-129"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea07a-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





