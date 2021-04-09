---
title: Message PGM_SETPOS (commctrl. h)
description: Définit la position de défilement actuelle pour le contrôle de pagineur. Vous pouvez envoyer ce message de manière explicite ou utiliser la macro de radiomessagerie \_ SetPos.
ms.assetid: b882ea2d-9dab-4d36-9201-29522141f779
keywords:
- PGM_SETPOS les contrôles de message Windows
topic_type:
- apiref
api_name:
- PGM_SETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5af4497e97a8263fa9ec8e454d367bb57e830c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741221"
---
# <a name="pgm_setpos-message"></a><span data-ttu-id="1dc77-105">\_Message SetPos PGM</span><span class="sxs-lookup"><span data-stu-id="1dc77-105">PGM\_SETPOS message</span></span>

<span data-ttu-id="1dc77-106">Définit la position de défilement actuelle pour le contrôle de pagineur.</span><span class="sxs-lookup"><span data-stu-id="1dc77-106">Sets the current scroll position for the pager control.</span></span> <span data-ttu-id="1dc77-107">Vous pouvez envoyer ce message de manière explicite ou utiliser la macro de [**radiomessagerie \_ SetPos**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setpos) .</span><span class="sxs-lookup"><span data-stu-id="1dc77-107">You can send this message explicitly or use the [**Pager\_SetPos**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setpos) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="1dc77-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1dc77-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1dc77-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1dc77-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="1dc77-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="1dc77-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="1dc77-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1dc77-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1dc77-112">Valeur de type **int** qui contient la nouvelle position de défilement, en pixels.</span><span class="sxs-lookup"><span data-stu-id="1dc77-112">Value of type **int** that contains the new scroll position, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1dc77-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1dc77-113">Return value</span></span>

<span data-ttu-id="1dc77-114">La valeur de retour n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="1dc77-114">The return value is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="1dc77-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1dc77-115">Requirements</span></span>



| <span data-ttu-id="1dc77-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1dc77-116">Requirement</span></span> | <span data-ttu-id="1dc77-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="1dc77-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1dc77-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1dc77-118">Minimum supported client</span></span><br/> | <span data-ttu-id="1dc77-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1dc77-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1dc77-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1dc77-120">Minimum supported server</span></span><br/> | <span data-ttu-id="1dc77-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1dc77-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1dc77-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="1dc77-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="1dc77-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1dc77-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





