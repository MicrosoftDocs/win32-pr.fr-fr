---
title: Message UDM_SETPOS32 (commctrl. h)
description: Définit la position d’un contrôle up-up avec une précision de 32 bits.
ms.assetid: a337f2a1-0e3d-4ff4-a224-57b7f25c4bd0
keywords:
- UDM_SETPOS32 les contrôles de message Windows
topic_type:
- apiref
api_name:
- UDM_SETPOS32
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0153305bb535a79dbed59e8d42a7c25157c30cd1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942451"
---
# <a name="udm_setpos32-message"></a><span data-ttu-id="0b859-104">\_Message SETPOS32 UDM</span><span class="sxs-lookup"><span data-stu-id="0b859-104">UDM\_SETPOS32 message</span></span>

<span data-ttu-id="0b859-105">Définit la position d’un contrôle up-up avec une précision de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="0b859-105">Sets the position of an up-down control with 32-bit precision.</span></span>

## <a name="parameters"></a><span data-ttu-id="0b859-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0b859-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b859-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0b859-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="0b859-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="0b859-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="0b859-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0b859-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0b859-110">Variable de type entier qui spécifie la nouvelle position pour le contrôle up-up.</span><span class="sxs-lookup"><span data-stu-id="0b859-110">Variable of type integer that specifies the new position for the up-down control.</span></span> <span data-ttu-id="0b859-111">Si le paramètre est en dehors de la plage spécifiée du contrôle, *lParam* prend la valeur valide la plus proche.</span><span class="sxs-lookup"><span data-stu-id="0b859-111">If the parameter is outside the control's specified range, *lParam* is set to the nearest valid value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b859-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0b859-112">Return value</span></span>

<span data-ttu-id="0b859-113">Retourne la position précédente.</span><span class="sxs-lookup"><span data-stu-id="0b859-113">Returns the previous position.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b859-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0b859-114">Requirements</span></span>



| <span data-ttu-id="0b859-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0b859-115">Requirement</span></span> | <span data-ttu-id="0b859-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="0b859-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0b859-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0b859-117">Minimum supported client</span></span><br/> | <span data-ttu-id="0b859-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0b859-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0b859-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0b859-119">Minimum supported server</span></span><br/> | <span data-ttu-id="0b859-120">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0b859-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0b859-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="0b859-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="0b859-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b859-122"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b859-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0b859-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="0b859-124">**Référence**</span><span class="sxs-lookup"><span data-stu-id="0b859-124">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="0b859-125">**\_GETPOS UDM**</span><span class="sxs-lookup"><span data-stu-id="0b859-125">**UDM\_GETPOS**</span></span>](udm-getpos.md)
</dt> <dt>

[<span data-ttu-id="0b859-126">**\_SetPos UDM**</span><span class="sxs-lookup"><span data-stu-id="0b859-126">**UDM\_SETPOS**</span></span>](udm-setpos.md)
</dt> <dt>

[<span data-ttu-id="0b859-127">**\_GETPOS32 UDM**</span><span class="sxs-lookup"><span data-stu-id="0b859-127">**UDM\_GETPOS32**</span></span>](udm-getpos32.md)
</dt> </dl>

 

 





