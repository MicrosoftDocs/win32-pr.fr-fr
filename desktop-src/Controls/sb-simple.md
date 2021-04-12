---
title: Message SB_SIMPLE (commctrl. h)
description: Spécifie si une fenêtre d’état affiche du texte simple ou affiche toutes les parties de fenêtre définies par un \_ message SB SETPARTS précédent.
ms.assetid: 457209cb-67d4-4a9f-8d18-75aa5eb9ca1d
keywords:
- SB_SIMPLE les contrôles de message Windows
topic_type:
- apiref
api_name:
- SB_SIMPLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f7a462a917c86531cd70f5f5c8ea60bf448ff6f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105064"
---
# <a name="sb_simple-message"></a><span data-ttu-id="dd40e-104">\_Message simple SB</span><span class="sxs-lookup"><span data-stu-id="dd40e-104">SB\_SIMPLE message</span></span>

<span data-ttu-id="dd40e-105">Spécifie si une fenêtre d’état affiche du texte simple ou affiche toutes les parties de fenêtre définies par un message [**SB \_ SETPARTS**](sb-setparts.md) précédent.</span><span class="sxs-lookup"><span data-stu-id="dd40e-105">Specifies whether a status window displays simple text or displays all window parts set by a previous [**SB\_SETPARTS**](sb-setparts.md) message.</span></span>

## <a name="parameters"></a><span data-ttu-id="dd40e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dd40e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd40e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="dd40e-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dd40e-108">Indicateur de type d’affichage.</span><span class="sxs-lookup"><span data-stu-id="dd40e-108">Display type flag.</span></span> <span data-ttu-id="dd40e-109">Si ce paramètre a la **valeur true**, la fenêtre affiche un texte simple.</span><span class="sxs-lookup"><span data-stu-id="dd40e-109">If this parameter is **TRUE**, the window displays simple text.</span></span> <span data-ttu-id="dd40e-110">Si la **valeur est false**, elle affiche plusieurs parties.</span><span class="sxs-lookup"><span data-stu-id="dd40e-110">If it is **FALSE**, it displays multiple parts.</span></span>

</dd> <dt>

<span data-ttu-id="dd40e-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="dd40e-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="dd40e-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="dd40e-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd40e-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dd40e-113">Return value</span></span>

<span data-ttu-id="dd40e-114">La valeur de retour n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="dd40e-114">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="dd40e-115">Notes</span><span class="sxs-lookup"><span data-stu-id="dd40e-115">Remarks</span></span>

<span data-ttu-id="dd40e-116">Si la fenêtre d’état passe de non simple à simple, ou vice versa, la fenêtre est immédiatement redessinée.</span><span class="sxs-lookup"><span data-stu-id="dd40e-116">If the status window is being changed from nonsimple to simple, or vice versa, the window is immediately redrawn.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd40e-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dd40e-117">Requirements</span></span>



| <span data-ttu-id="dd40e-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dd40e-118">Requirement</span></span> | <span data-ttu-id="dd40e-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="dd40e-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dd40e-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dd40e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="dd40e-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dd40e-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="dd40e-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dd40e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="dd40e-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dd40e-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="dd40e-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="dd40e-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="dd40e-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd40e-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





