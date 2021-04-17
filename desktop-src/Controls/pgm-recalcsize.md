---
title: Message PGM_RECALCSIZE (commctrl. h)
description: Force le contrôle de pagineur à recalculer la taille de la fenêtre contenue. L’envoi de ce message entraîne l’envoi d’une \_ notification PGN CALCSIZE. Vous pouvez envoyer ce message de manière explicite ou utiliser la macro de radiomessagerie \_ RecalcSize.
ms.assetid: 51b75ce8-2b41-4f1a-830e-b25e7d77dccb
keywords:
- PGM_RECALCSIZE les contrôles de message Windows
topic_type:
- apiref
api_name:
- PGM_RECALCSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b407221543a42b4dbff4490508a02b570622d69c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465038"
---
# <a name="pgm_recalcsize-message"></a><span data-ttu-id="bc7f3-106">\_Message RECALCSIZE PGM</span><span class="sxs-lookup"><span data-stu-id="bc7f3-106">PGM\_RECALCSIZE message</span></span>

<span data-ttu-id="bc7f3-107">Force le contrôle de pagineur à recalculer la taille de la fenêtre contenue.</span><span class="sxs-lookup"><span data-stu-id="bc7f3-107">Forces the pager control to recalculate the size of the contained window.</span></span> <span data-ttu-id="bc7f3-108">L’envoi de ce message entraîne l’envoi d’une notification [PGN \_ CALCSIZE](pgn-calcsize.md) .</span><span class="sxs-lookup"><span data-stu-id="bc7f3-108">Sending this message will result in a [PGN\_CALCSIZE](pgn-calcsize.md) notification being sent.</span></span> <span data-ttu-id="bc7f3-109">Vous pouvez envoyer ce message de manière explicite ou utiliser la macro de [**radiomessagerie \_ RecalcSize**](/windows/desktop/api/Commctrl/nf-commctrl-pager_recalcsize) .</span><span class="sxs-lookup"><span data-stu-id="bc7f3-109">You can send this message explicitly or use the [**Pager\_RecalcSize**](/windows/desktop/api/Commctrl/nf-commctrl-pager_recalcsize) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="bc7f3-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bc7f3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc7f3-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bc7f3-111">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="bc7f3-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="bc7f3-112">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="bc7f3-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bc7f3-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="bc7f3-114">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="bc7f3-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc7f3-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bc7f3-115">Return value</span></span>

<span data-ttu-id="bc7f3-116">La valeur de retour n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="bc7f3-116">The return value is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc7f3-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bc7f3-117">Requirements</span></span>



| <span data-ttu-id="bc7f3-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bc7f3-118">Requirement</span></span> | <span data-ttu-id="bc7f3-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="bc7f3-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bc7f3-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bc7f3-120">Minimum supported client</span></span><br/> | <span data-ttu-id="bc7f3-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bc7f3-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bc7f3-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bc7f3-122">Minimum supported server</span></span><br/> | <span data-ttu-id="bc7f3-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bc7f3-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bc7f3-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="bc7f3-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="bc7f3-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="bc7f3-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





