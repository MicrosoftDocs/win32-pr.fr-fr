---
title: Message PGM_GETBUTTONSIZE (commctrl. h)
description: Récupère la taille de bouton actuelle pour le contrôle de pagineur. Vous pouvez envoyer ce message de manière explicite ou utiliser la macro de radiomessagerie \_ GetButtonSize.
ms.assetid: fa8b4814-4587-4149-83a7-84faad2a4641
keywords:
- PGM_GETBUTTONSIZE les contrôles de message Windows
topic_type:
- apiref
api_name:
- PGM_GETBUTTONSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae5cb36d203aaeae748db9adb1b13cacf2e40f5e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033049"
---
# <a name="pgm_getbuttonsize-message"></a><span data-ttu-id="f6bf6-105">\_Message GETBUTTONSIZE PGM</span><span class="sxs-lookup"><span data-stu-id="f6bf6-105">PGM\_GETBUTTONSIZE message</span></span>

<span data-ttu-id="f6bf6-106">Récupère la taille de bouton actuelle pour le contrôle de pagineur.</span><span class="sxs-lookup"><span data-stu-id="f6bf6-106">Retrieves the current button size for the pager control.</span></span> <span data-ttu-id="f6bf6-107">Vous pouvez envoyer ce message de manière explicite ou utiliser la macro de [**radiomessagerie \_ GetButtonSize**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbuttonsize) .</span><span class="sxs-lookup"><span data-stu-id="f6bf6-107">You can send this message explicitly or use the [**Pager\_GetButtonSize**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbuttonsize) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="f6bf6-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f6bf6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6bf6-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f6bf6-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="f6bf6-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="f6bf6-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="f6bf6-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f6bf6-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="f6bf6-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="f6bf6-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6bf6-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f6bf6-113">Return value</span></span>

<span data-ttu-id="f6bf6-114">Retourne une valeur INT qui contient la taille actuelle du bouton, en pixels.</span><span class="sxs-lookup"><span data-stu-id="f6bf6-114">Returns an INT value that contains the current button size, in pixels.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6bf6-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f6bf6-115">Requirements</span></span>



| <span data-ttu-id="f6bf6-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f6bf6-116">Requirement</span></span> | <span data-ttu-id="f6bf6-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="f6bf6-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f6bf6-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f6bf6-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f6bf6-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f6bf6-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f6bf6-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f6bf6-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f6bf6-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f6bf6-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f6bf6-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="f6bf6-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="f6bf6-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f6bf6-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6bf6-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f6bf6-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6bf6-125">**\_SETBUTTONSIZE PGM**</span><span class="sxs-lookup"><span data-stu-id="f6bf6-125">**PGM\_SETBUTTONSIZE**</span></span>](pgm-setbuttonsize.md)
</dt> </dl>

 

 





