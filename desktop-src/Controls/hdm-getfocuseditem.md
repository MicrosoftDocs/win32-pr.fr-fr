---
title: Message HDM_GETFOCUSEDITEM (commctrl. h)
description: Obtient l’élément dans un contrôle d’en-tête qui a le focus. Envoyez ce message de manière explicite ou à l’aide de la macro GetFocusedItem d’en-tête \_ .
ms.assetid: 9ad8e497-6f81-4226-b138-d1101f2fd8b3
keywords:
- HDM_GETFOCUSEDITEM les contrôles de message Windows
topic_type:
- apiref
api_name:
- HDM_GETFOCUSEDITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c21fcb29f5f431e32ca3f07265b7e96620d5a67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465887"
---
# <a name="hdm_getfocuseditem-message"></a><span data-ttu-id="bff65-105">\_Message HDM GETFOCUSEDITEM</span><span class="sxs-lookup"><span data-stu-id="bff65-105">HDM\_GETFOCUSEDITEM message</span></span>

<span data-ttu-id="bff65-106">Obtient l’élément dans un contrôle d’en-tête qui a le focus.</span><span class="sxs-lookup"><span data-stu-id="bff65-106">Gets the item in a header control that has the focus.</span></span> <span data-ttu-id="bff65-107">Envoyez ce message de manière explicite ou à l’aide de la macro [**\_ GetFocusedItem d’en-tête**](/windows/desktop/api/Commctrl/nf-commctrl-header_getfocuseditem) .</span><span class="sxs-lookup"><span data-stu-id="bff65-107">Send this message explicitly or by using the [**Header\_GetFocusedItem**](/windows/desktop/api/Commctrl/nf-commctrl-header_getfocuseditem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="bff65-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bff65-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bff65-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bff65-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="bff65-110">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="bff65-110">Not used.</span></span> <span data-ttu-id="bff65-111">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="bff65-111">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="bff65-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bff65-112">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="bff65-113">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="bff65-113">Not used.</span></span> <span data-ttu-id="bff65-114">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="bff65-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bff65-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bff65-115">Return value</span></span>

<span data-ttu-id="bff65-116">Retourne l’index de l’élément dans le focus.</span><span class="sxs-lookup"><span data-stu-id="bff65-116">Returns the index of the item in focus.</span></span>

## <a name="requirements"></a><span data-ttu-id="bff65-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bff65-117">Requirements</span></span>



| <span data-ttu-id="bff65-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bff65-118">Requirement</span></span> | <span data-ttu-id="bff65-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="bff65-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bff65-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bff65-120">Minimum supported client</span></span><br/> | <span data-ttu-id="bff65-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bff65-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bff65-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bff65-122">Minimum supported server</span></span><br/> | <span data-ttu-id="bff65-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bff65-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bff65-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="bff65-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="bff65-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="bff65-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bff65-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bff65-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bff65-127">À propos des contrôles Header</span><span class="sxs-lookup"><span data-stu-id="bff65-127">About Header Controls</span></span>](header-controls.md)
</dt> </dl>

 

 





