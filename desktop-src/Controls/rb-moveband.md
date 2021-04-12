---
title: Message RB_MOVEBAND (commctrl. h)
description: Déplace une bande d’un index vers un autre.
ms.assetid: bb5b45de-957e-46fb-b59a-18b55b69c395
keywords:
- RB_MOVEBAND les contrôles de message Windows
topic_type:
- apiref
api_name:
- RB_MOVEBAND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 146103c4c3d70fc0514729a00eac152c4847b85c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464391"
---
# <a name="rb_moveband-message"></a><span data-ttu-id="1091e-104">\_Message MOVEBAND RB</span><span class="sxs-lookup"><span data-stu-id="1091e-104">RB\_MOVEBAND message</span></span>

<span data-ttu-id="1091e-105">Déplace une bande d’un index vers un autre.</span><span class="sxs-lookup"><span data-stu-id="1091e-105">Moves a band from one index to another.</span></span>

## <a name="parameters"></a><span data-ttu-id="1091e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1091e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1091e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1091e-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1091e-108">Index de base zéro de la bande à déplacer.</span><span class="sxs-lookup"><span data-stu-id="1091e-108">Zero-based index of the band to be moved.</span></span>

</dd> <dt>

<span data-ttu-id="1091e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1091e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1091e-110">Index de base zéro de la nouvelle position de la bande.</span><span class="sxs-lookup"><span data-stu-id="1091e-110">Zero-based index of the new band position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1091e-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1091e-111">Return value</span></span>

<span data-ttu-id="1091e-112">Retourne une valeur différente de zéro en cas de réussite, ou zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="1091e-112">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="1091e-113">Notes</span><span class="sxs-lookup"><span data-stu-id="1091e-113">Remarks</span></span>

<span data-ttu-id="1091e-114">Ce message modifiera probablement l’index d’autres bandes dans le contrôle rebar.</span><span class="sxs-lookup"><span data-stu-id="1091e-114">This message will most likely change the index of other bands in the rebar control.</span></span> <span data-ttu-id="1091e-115">Si une bande est déplacée de l’index 6 à l’index 0, toutes les bandes comprises entre auront l’index incrémenté d’une unité.</span><span class="sxs-lookup"><span data-stu-id="1091e-115">If a band is moved from index 6 to index 0, all of the bands in between will have their index incremented by one.</span></span>

<span data-ttu-id="1091e-116">*lParam* ne doit jamais être supérieur au nombre de bandes moins un.</span><span class="sxs-lookup"><span data-stu-id="1091e-116">*lParam* must never be greater than the number of bands minus one.</span></span> <span data-ttu-id="1091e-117">Le nombre de bandes peut être obtenu avec le message [**RB \_ GETBANDCOUNT**](rb-getbandcount.md) .</span><span class="sxs-lookup"><span data-stu-id="1091e-117">The number of bands can be obtained with the [**RB\_GETBANDCOUNT**](rb-getbandcount.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="1091e-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1091e-118">Requirements</span></span>



| <span data-ttu-id="1091e-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1091e-119">Requirement</span></span> | <span data-ttu-id="1091e-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="1091e-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1091e-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1091e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="1091e-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1091e-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1091e-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1091e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="1091e-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1091e-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1091e-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="1091e-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="1091e-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1091e-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





