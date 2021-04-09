---
title: Message UDM_SETPOS (commctrl. h)
description: Définit la position actuelle d’un contrôle up-up avec une précision de 16 bits.
ms.assetid: e7c8b55f-3a4f-47e7-8c7d-e47509f27f1d
keywords:
- UDM_SETPOS les contrôles de message Windows
topic_type:
- apiref
api_name:
- UDM_SETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b409f9e7468e3add89248b61b7b563ac592f0dcc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104761"
---
# <a name="udm_setpos-message"></a><span data-ttu-id="a1d59-104">\_Message SetPos UDM</span><span class="sxs-lookup"><span data-stu-id="a1d59-104">UDM\_SETPOS message</span></span>

<span data-ttu-id="a1d59-105">Définit la position actuelle d’un contrôle up-up avec une précision de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="a1d59-105">Sets the current position for an up-down control with 16-bit precision.</span></span>

## <a name="parameters"></a><span data-ttu-id="a1d59-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a1d59-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1d59-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a1d59-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="a1d59-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="a1d59-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="a1d59-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a1d59-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a1d59-110">Nouvelle position pour le contrôle up-up.</span><span class="sxs-lookup"><span data-stu-id="a1d59-110">New position for the up-down control.</span></span> <span data-ttu-id="a1d59-111">Si le paramètre est en dehors de la plage spécifiée du contrôle, *lParam* prend la valeur valide la plus proche.</span><span class="sxs-lookup"><span data-stu-id="a1d59-111">If the parameter is outside the control's specified range, *lParam* will be set to the nearest valid value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1d59-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a1d59-112">Return value</span></span>

<span data-ttu-id="a1d59-113">La valeur de retour est la position précédente.</span><span class="sxs-lookup"><span data-stu-id="a1d59-113">The return value is the previous position.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1d59-114">Notes</span><span class="sxs-lookup"><span data-stu-id="a1d59-114">Remarks</span></span>

<span data-ttu-id="a1d59-115">Ce message ne prend en charge que les positions 16 bits.</span><span class="sxs-lookup"><span data-stu-id="a1d59-115">This message only supports 16-bit positions.</span></span> <span data-ttu-id="a1d59-116">Si les valeurs 32 bits ont été activées pour un contrôle up-out avec [**UDM \_ SETRANGE32**](udm-setrange32.md), utilisez [**UDM \_ SETPOS32**](udm-setpos32.md).</span><span class="sxs-lookup"><span data-stu-id="a1d59-116">If 32-bit values have been enabled for an up-down control with [**UDM\_SETRANGE32**](udm-setrange32.md), use [**UDM\_SETPOS32**](udm-setpos32.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a1d59-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a1d59-117">Requirements</span></span>



| <span data-ttu-id="a1d59-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a1d59-118">Requirement</span></span> | <span data-ttu-id="a1d59-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="a1d59-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a1d59-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a1d59-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a1d59-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a1d59-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a1d59-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a1d59-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a1d59-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a1d59-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a1d59-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="a1d59-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="a1d59-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a1d59-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1d59-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a1d59-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="a1d59-127">**Référence**</span><span class="sxs-lookup"><span data-stu-id="a1d59-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a1d59-128">**\_GETRANGE UDM**</span><span class="sxs-lookup"><span data-stu-id="a1d59-128">**UDM\_GETRANGE**</span></span>](udm-getrange.md)
</dt> <dt>

[<span data-ttu-id="a1d59-129">**\_GETPOS UDM**</span><span class="sxs-lookup"><span data-stu-id="a1d59-129">**UDM\_GETPOS**</span></span>](udm-getpos.md)
</dt> </dl>

 

 





