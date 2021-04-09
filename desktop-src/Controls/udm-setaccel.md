---
title: Message UDM_SETACCEL (commctrl. h)
description: Définit l’accélération pour un contrôle up-up.
ms.assetid: af1d0a34-13ba-4bda-82f5-d7afab6bb1ed
keywords:
- UDM_SETACCEL les contrôles de message Windows
topic_type:
- apiref
api_name:
- UDM_SETACCEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b43ed290ce1668ffcaa9fb086a99ad52e5129ad6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033257"
---
# <a name="udm_setaccel-message"></a><span data-ttu-id="1ee0f-104">\_Message SETACCEL UDM</span><span class="sxs-lookup"><span data-stu-id="1ee0f-104">UDM\_SETACCEL message</span></span>

<span data-ttu-id="1ee0f-105">Définit l’accélération pour un contrôle up-up.</span><span class="sxs-lookup"><span data-stu-id="1ee0f-105">Sets the acceleration for an up-down control.</span></span>

## <a name="parameters"></a><span data-ttu-id="1ee0f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1ee0f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ee0f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1ee0f-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1ee0f-108">Nombre de structures [**UDACCEL**](/windows/desktop/api/Commctrl/ns-commctrl-udaccel) spécifiées par *aAccels*.</span><span class="sxs-lookup"><span data-stu-id="1ee0f-108">Number of [**UDACCEL**](/windows/desktop/api/Commctrl/ns-commctrl-udaccel) structures specified by *aAccels*.</span></span>

</dd> <dt>

<span data-ttu-id="1ee0f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1ee0f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1ee0f-110">Pointeur vers un tableau de structures [**UDACCEL**](/windows/desktop/api/Commctrl/ns-commctrl-udaccel) qui contiennent des informations d’accélération.</span><span class="sxs-lookup"><span data-stu-id="1ee0f-110">Pointer to an array of [**UDACCEL**](/windows/desktop/api/Commctrl/ns-commctrl-udaccel) structures that contain acceleration information.</span></span> <span data-ttu-id="1ee0f-111">Les éléments doivent être triés dans l’ordre croissant en fonction du membre **nSec** .</span><span class="sxs-lookup"><span data-stu-id="1ee0f-111">Elements should be sorted in ascending order based on the **nSec** member.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ee0f-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1ee0f-112">Return value</span></span>

<span data-ttu-id="1ee0f-113">Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="1ee0f-113">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ee0f-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1ee0f-114">Requirements</span></span>



| <span data-ttu-id="1ee0f-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1ee0f-115">Requirement</span></span> | <span data-ttu-id="1ee0f-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="1ee0f-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1ee0f-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1ee0f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="1ee0f-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1ee0f-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1ee0f-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1ee0f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="1ee0f-120">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1ee0f-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1ee0f-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="1ee0f-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ee0f-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ee0f-122"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ee0f-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1ee0f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ee0f-124">**\_GETACCEL UDM**</span><span class="sxs-lookup"><span data-stu-id="1ee0f-124">**UDM\_GETACCEL**</span></span>](udm-getaccel.md)
</dt> </dl>

 

 





