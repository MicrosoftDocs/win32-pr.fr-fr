---
title: Message HDM_SETFOCUSEDITEM (commctrl. h)
description: Définit le focus sur un élément spécifié dans un contrôle header. Envoyez ce message de manière explicite ou à l’aide de la macro SetFocusedItem d’en-tête \_ .
ms.assetid: 20a321ce-4420-4239-b34d-9e7f24a89fc3
keywords:
- HDM_SETFOCUSEDITEM les contrôles de message Windows
topic_type:
- apiref
api_name:
- HDM_SETFOCUSEDITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fd416744478248760f4e2c9f94a362db5a8d327
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105292"
---
# <a name="hdm_setfocuseditem-message"></a><span data-ttu-id="85622-105">\_Message HDM SETFOCUSEDITEM</span><span class="sxs-lookup"><span data-stu-id="85622-105">HDM\_SETFOCUSEDITEM message</span></span>

<span data-ttu-id="85622-106">Définit le focus sur un élément spécifié dans un contrôle header.</span><span class="sxs-lookup"><span data-stu-id="85622-106">Sets the focus to a specified item in a header control.</span></span> <span data-ttu-id="85622-107">Envoyez ce message de manière explicite ou à l’aide de la macro [**\_ SetFocusedItem d’en-tête**](/windows/desktop/api/Commctrl/nf-commctrl-header_setfocuseditem) .</span><span class="sxs-lookup"><span data-stu-id="85622-107">Send this message explicitly or by using the [**Header\_SetFocusedItem**](/windows/desktop/api/Commctrl/nf-commctrl-header_setfocuseditem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="85622-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="85622-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85622-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="85622-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="85622-110">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="85622-110">Not used.</span></span> <span data-ttu-id="85622-111">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="85622-111">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="85622-112">*lParam* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="85622-112">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85622-113">Index de l’élément.</span><span class="sxs-lookup"><span data-stu-id="85622-113">The index of item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85622-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="85622-114">Return value</span></span>

<span data-ttu-id="85622-115">Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="85622-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="85622-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="85622-116">Requirements</span></span>



| <span data-ttu-id="85622-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="85622-117">Requirement</span></span> | <span data-ttu-id="85622-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="85622-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="85622-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="85622-119">Minimum supported client</span></span><br/> | <span data-ttu-id="85622-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="85622-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="85622-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="85622-121">Minimum supported server</span></span><br/> | <span data-ttu-id="85622-122">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="85622-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="85622-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="85622-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="85622-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="85622-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85622-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="85622-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85622-126">À propos des contrôles Header</span><span class="sxs-lookup"><span data-stu-id="85622-126">About Header Controls</span></span>](header-controls.md)
</dt> </dl>

 

 





