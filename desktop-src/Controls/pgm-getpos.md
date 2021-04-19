---
title: Message PGM_GETPOS (commctrl. h)
description: Récupère la position de défilement actuelle du contrôle de pagineur. Vous pouvez envoyer ce message de manière explicite ou utiliser la macro de radiomessagerie \_ GetPos.
ms.assetid: 1e0f967a-3290-43b7-b812-8cf56abf2d32
keywords:
- PGM_GETPOS les contrôles de message Windows
topic_type:
- apiref
api_name:
- PGM_GETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 611a27e9cb952c5be190fa041af3d238f0184b03
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106544174"
---
# <a name="pgm_getpos-message"></a><span data-ttu-id="e7709-105">\_Message GETPOS PGM</span><span class="sxs-lookup"><span data-stu-id="e7709-105">PGM\_GETPOS message</span></span>

<span data-ttu-id="e7709-106">Récupère la position de défilement actuelle du contrôle de pagineur.</span><span class="sxs-lookup"><span data-stu-id="e7709-106">Retrieves the current scroll position of the pager control.</span></span> <span data-ttu-id="e7709-107">Vous pouvez envoyer ce message de manière explicite ou utiliser la macro de [**radiomessagerie \_ GetPos**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getpos) .</span><span class="sxs-lookup"><span data-stu-id="e7709-107">You can send this message explicitly or use the [**Pager\_GetPos**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getpos) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="e7709-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e7709-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7709-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e7709-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="e7709-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="e7709-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="e7709-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e7709-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="e7709-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="e7709-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7709-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e7709-113">Return value</span></span>

<span data-ttu-id="e7709-114">Retourne une valeur INT qui contient la position de défilement actuelle, en pixels.</span><span class="sxs-lookup"><span data-stu-id="e7709-114">Returns an INT value that contains the current scroll position, in pixels.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7709-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e7709-115">Requirements</span></span>



| <span data-ttu-id="e7709-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e7709-116">Requirement</span></span> | <span data-ttu-id="e7709-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="e7709-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e7709-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e7709-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e7709-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e7709-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e7709-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e7709-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e7709-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e7709-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e7709-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="e7709-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7709-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7709-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





