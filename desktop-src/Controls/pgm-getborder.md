---
title: Message PGM_GETBORDER (commctrl. h)
description: Récupère la taille de bordure actuelle pour le contrôle de pagineur. Vous pouvez envoyer ce message de manière explicite ou utiliser la macro de radiomessagerie \_ GetBorder.
ms.assetid: 5d2f49ad-d940-4a0b-b5a0-05d742151b1c
keywords:
- PGM_GETBORDER les contrôles de message Windows
topic_type:
- apiref
api_name:
- PGM_GETBORDER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be510af44c9cf53000420531843a79e9856c40dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106513618"
---
# <a name="pgm_getborder-message"></a><span data-ttu-id="9d5d7-105">\_Message GETBORDER PGM</span><span class="sxs-lookup"><span data-stu-id="9d5d7-105">PGM\_GETBORDER message</span></span>

<span data-ttu-id="9d5d7-106">Récupère la taille de bordure actuelle pour le contrôle de pagineur.</span><span class="sxs-lookup"><span data-stu-id="9d5d7-106">Retrieves the current border size for the pager control.</span></span> <span data-ttu-id="9d5d7-107">Vous pouvez envoyer ce message de manière explicite ou utiliser la macro de [**radiomessagerie \_ GetBorder**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getborder) .</span><span class="sxs-lookup"><span data-stu-id="9d5d7-107">You can send this message explicitly or use the [**Pager\_GetBorder**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getborder) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="9d5d7-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9d5d7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d5d7-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9d5d7-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="9d5d7-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="9d5d7-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="9d5d7-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9d5d7-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="9d5d7-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="9d5d7-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d5d7-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9d5d7-113">Return value</span></span>

<span data-ttu-id="9d5d7-114">Retourne une valeur INT qui contient la taille actuelle de la bordure, en pixels.</span><span class="sxs-lookup"><span data-stu-id="9d5d7-114">Returns an INT value that contains the current border size, in pixels.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d5d7-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9d5d7-115">Requirements</span></span>



| <span data-ttu-id="9d5d7-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9d5d7-116">Requirement</span></span> | <span data-ttu-id="9d5d7-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="9d5d7-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9d5d7-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9d5d7-118">Minimum supported client</span></span><br/> | <span data-ttu-id="9d5d7-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9d5d7-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9d5d7-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9d5d7-120">Minimum supported server</span></span><br/> | <span data-ttu-id="9d5d7-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9d5d7-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9d5d7-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="9d5d7-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="9d5d7-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9d5d7-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d5d7-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9d5d7-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d5d7-125">**\_SETBORDER PGM**</span><span class="sxs-lookup"><span data-stu-id="9d5d7-125">**PGM\_SETBORDER**</span></span>](pgm-setborder.md)
</dt> </dl>

 

 





