---
title: Message ACM_STOP (commctrl. h)
description: Arrête la diffusion d’un clip AVI dans un contrôle d’animation. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro arrêter l’animation.
ms.assetid: ba39a579-665e-4d45-8f1f-f190acd76db7
keywords:
- ACM_STOP les contrôles de message Windows
topic_type:
- apiref
api_name:
- ACM_STOP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e81cfc92ac2778ae559fcd9fb8db2b0cd7bb866
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103137"
---
# <a name="acm_stop-message"></a><span data-ttu-id="c1eb7-105">\_Message d’arrêt ACM</span><span class="sxs-lookup"><span data-stu-id="c1eb7-105">ACM\_STOP message</span></span>

<span data-ttu-id="c1eb7-106">Arrête la diffusion d’un clip AVI dans un contrôle d’animation.</span><span class="sxs-lookup"><span data-stu-id="c1eb7-106">Stops playing an AVI clip in an animation control.</span></span> <span data-ttu-id="c1eb7-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**\_ arrêter l’animation**](/windows/desktop/api/Commctrl/nf-commctrl-animate_stop) .</span><span class="sxs-lookup"><span data-stu-id="c1eb7-107">You can send this message explicitly or by using the [**Animate\_Stop**](/windows/desktop/api/Commctrl/nf-commctrl-animate_stop) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="c1eb7-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c1eb7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1eb7-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c1eb7-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="c1eb7-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="c1eb7-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="c1eb7-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c1eb7-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="c1eb7-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="c1eb7-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1eb7-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c1eb7-113">Return value</span></span>

<span data-ttu-id="c1eb7-114">Retourne une valeur différente de zéro en cas de réussite, ou zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="c1eb7-114">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1eb7-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c1eb7-115">Requirements</span></span>



| <span data-ttu-id="c1eb7-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c1eb7-116">Requirement</span></span> | <span data-ttu-id="c1eb7-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="c1eb7-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c1eb7-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c1eb7-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c1eb7-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c1eb7-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c1eb7-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c1eb7-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c1eb7-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c1eb7-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c1eb7-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="c1eb7-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1eb7-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c1eb7-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





