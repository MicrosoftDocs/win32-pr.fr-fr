---
title: Message PGM_SETBORDER (commctrl. h)
description: Définit la taille de bordure actuelle pour le contrôle de pagineur. Vous pouvez envoyer ce message de manière explicite ou utiliser la macro de radiomessagerie \_ setBorder.
ms.assetid: 073a1f9e-f05b-4203-9035-8106e87e55cd
keywords:
- PGM_SETBORDER les contrôles de message Windows
topic_type:
- apiref
api_name:
- PGM_SETBORDER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a987246a56da213098ba8632044af97ae51462df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032756"
---
# <a name="pgm_setborder-message"></a><span data-ttu-id="680e3-105">\_Message SETBORDER PGM</span><span class="sxs-lookup"><span data-stu-id="680e3-105">PGM\_SETBORDER message</span></span>

<span data-ttu-id="680e3-106">Définit la taille de bordure actuelle pour le contrôle de pagineur.</span><span class="sxs-lookup"><span data-stu-id="680e3-106">Sets the current border size for the pager control.</span></span> <span data-ttu-id="680e3-107">Vous pouvez envoyer ce message de manière explicite ou utiliser la macro de [**radiomessagerie \_ setBorder**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setborder) .</span><span class="sxs-lookup"><span data-stu-id="680e3-107">You can send this message explicitly or use the [**Pager\_SetBorder**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setborder) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="680e3-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="680e3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="680e3-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="680e3-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="680e3-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="680e3-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="680e3-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="680e3-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="680e3-112">Nouvelle taille de la bordure, en pixels.</span><span class="sxs-lookup"><span data-stu-id="680e3-112">New size of the border, in pixels.</span></span> <span data-ttu-id="680e3-113">Cette valeur ne doit pas être supérieure au bouton du pagineur ou inférieure à zéro.</span><span class="sxs-lookup"><span data-stu-id="680e3-113">This value should not be larger than the pager button or less than zero.</span></span> <span data-ttu-id="680e3-114">Si *lParam* est trop grand, la bordure est dessinée avec la même taille que le bouton.</span><span class="sxs-lookup"><span data-stu-id="680e3-114">If *lParam* is too large, the border will be drawn the same size as the button.</span></span> <span data-ttu-id="680e3-115">Si *lParam* est négatif, la taille de la bordure sera définie sur zéro.</span><span class="sxs-lookup"><span data-stu-id="680e3-115">If *lParam* is negative, the border size will be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="680e3-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="680e3-116">Return value</span></span>

<span data-ttu-id="680e3-117">Retourne une valeur INT qui contient la taille de bordure précédente, en pixels.</span><span class="sxs-lookup"><span data-stu-id="680e3-117">Returns an INT value that contains the previous border size, in pixels.</span></span>

## <a name="requirements"></a><span data-ttu-id="680e3-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="680e3-118">Requirements</span></span>



| <span data-ttu-id="680e3-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="680e3-119">Requirement</span></span> | <span data-ttu-id="680e3-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="680e3-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="680e3-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="680e3-121">Minimum supported client</span></span><br/> | <span data-ttu-id="680e3-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="680e3-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="680e3-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="680e3-123">Minimum supported server</span></span><br/> | <span data-ttu-id="680e3-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="680e3-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="680e3-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="680e3-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="680e3-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="680e3-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





