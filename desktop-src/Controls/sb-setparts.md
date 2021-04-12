---
title: Message SB_SETPARTS (commctrl. h)
description: Définit le nombre de parties dans une fenêtre d’État et la coordonnée du bord droit de chaque partie.
ms.assetid: e29e8b09-c018-4ea4-8b47-6f3713113427
keywords:
- SB_SETPARTS les contrôles de message Windows
topic_type:
- apiref
api_name:
- SB_SETPARTS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 062058fa3778cd0394cadd9d76b363a0353ffb2e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509014"
---
# <a name="sb_setparts-message"></a><span data-ttu-id="b1c82-104">\_Message SB SETPARTS</span><span class="sxs-lookup"><span data-stu-id="b1c82-104">SB\_SETPARTS message</span></span>

<span data-ttu-id="b1c82-105">Définit le nombre de parties dans une fenêtre d’État et la coordonnée du bord droit de chaque partie.</span><span class="sxs-lookup"><span data-stu-id="b1c82-105">Sets the number of parts in a status window and the coordinate of the right edge of each part.</span></span>

## <a name="parameters"></a><span data-ttu-id="b1c82-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b1c82-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1c82-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b1c82-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b1c82-108">Nombre de parties à définir (ne peut pas être supérieur à 256).</span><span class="sxs-lookup"><span data-stu-id="b1c82-108">Number of parts to set (cannot be greater than 256).</span></span>

</dd> <dt>

<span data-ttu-id="b1c82-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b1c82-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b1c82-110">Pointeur vers un tableau d’entiers.</span><span class="sxs-lookup"><span data-stu-id="b1c82-110">Pointer to an integer array.</span></span> <span data-ttu-id="b1c82-111">Le nombre d’éléments est spécifié dans *wParam*.</span><span class="sxs-lookup"><span data-stu-id="b1c82-111">The number of elements is specified in *wParam*.</span></span> <span data-ttu-id="b1c82-112">Chaque élément spécifie la position, dans les coordonnées clientes, du bord droit de la partie correspondante.</span><span class="sxs-lookup"><span data-stu-id="b1c82-112">Each element specifies the position, in client coordinates, of the right edge of the corresponding part.</span></span> <span data-ttu-id="b1c82-113">Si un élément est-1, le bord droit de la partie correspondante s’étend jusqu’à la bordure de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="b1c82-113">If an element is -1, the right edge of the corresponding part extends to the border of the window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1c82-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b1c82-114">Return value</span></span>

<span data-ttu-id="b1c82-115">Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="b1c82-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1c82-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b1c82-116">Requirements</span></span>



| <span data-ttu-id="b1c82-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b1c82-117">Requirement</span></span> | <span data-ttu-id="b1c82-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="b1c82-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b1c82-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b1c82-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b1c82-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b1c82-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b1c82-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b1c82-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b1c82-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b1c82-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b1c82-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="b1c82-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b1c82-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b1c82-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





