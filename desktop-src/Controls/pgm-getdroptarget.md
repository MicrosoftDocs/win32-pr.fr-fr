---
title: Message PGM_GETDROPTARGET (commctrl. h)
description: Récupère le pointeur d’interface IDropTarget d’un contrôle de pagineur. Vous pouvez envoyer ce message de manière explicite ou utiliser la macro de radiomessagerie \_ GetDropTarget.
ms.assetid: 6b548c30-2d32-4372-90e4-346a27dda218
keywords:
- PGM_GETDROPTARGET les contrôles de message Windows
topic_type:
- apiref
api_name:
- PGM_GETDROPTARGET
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b90f7f9667dd30a79b9345eec211a6ebfcd7a12
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466095"
---
# <a name="pgm_getdroptarget-message"></a><span data-ttu-id="0a40b-105">\_Message GETDROPTARGET PGM</span><span class="sxs-lookup"><span data-stu-id="0a40b-105">PGM\_GETDROPTARGET message</span></span>

<span data-ttu-id="0a40b-106">Récupère le pointeur d’interface [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) d’un contrôle de pagineur.</span><span class="sxs-lookup"><span data-stu-id="0a40b-106">Retrieves a pager control's [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) interface pointer.</span></span> <span data-ttu-id="0a40b-107">Vous pouvez envoyer ce message de manière explicite ou utiliser la macro de [**radiomessagerie \_ GetDropTarget**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getdroptarget) .</span><span class="sxs-lookup"><span data-stu-id="0a40b-107">You can send this message explicitly or use the [**Pager\_GetDropTarget**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getdroptarget) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="0a40b-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0a40b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a40b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0a40b-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="0a40b-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="0a40b-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="0a40b-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0a40b-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0a40b-112">Pointeur vers un pointeur [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) qui reçoit le pointeur d’interface.</span><span class="sxs-lookup"><span data-stu-id="0a40b-112">Pointer to an [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) pointer that receives the interface pointer.</span></span> <span data-ttu-id="0a40b-113">Il incombe à l’appelant d’appeler [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) sur ce pointeur lorsqu’il n’est plus nécessaire.</span><span class="sxs-lookup"><span data-stu-id="0a40b-113">It is the caller's responsibility to call [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on this pointer when it is no longer needed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a40b-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0a40b-114">Return value</span></span>

<span data-ttu-id="0a40b-115">La valeur de retour de ce message n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="0a40b-115">The return value for this message is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a40b-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0a40b-116">Requirements</span></span>



| <span data-ttu-id="0a40b-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0a40b-117">Requirement</span></span> | <span data-ttu-id="0a40b-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="0a40b-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0a40b-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0a40b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="0a40b-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0a40b-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0a40b-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0a40b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="0a40b-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0a40b-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0a40b-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="0a40b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="0a40b-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0a40b-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

