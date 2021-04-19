---
title: Message UDM_GETPOS (commctrl. h)
description: Récupère la position actuelle d’un contrôle up-up avec une précision de 16 bits.
ms.assetid: 5f395de0-11b3-44f8-9bf4-42e27ce88a0c
keywords:
- UDM_GETPOS les contrôles de message Windows
topic_type:
- apiref
api_name:
- UDM_GETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8e78ad19289d85b93ebcb39a244a896ddb4f33f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510739"
---
# <a name="udm_getpos-message"></a><span data-ttu-id="db429-104">\_Message GETPOS UDM</span><span class="sxs-lookup"><span data-stu-id="db429-104">UDM\_GETPOS message</span></span>

<span data-ttu-id="db429-105">Récupère la position actuelle d’un contrôle up-up avec une précision de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="db429-105">Retrieves the current position of an up-down control with 16-bit precision.</span></span>

## <a name="parameters"></a><span data-ttu-id="db429-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="db429-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db429-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="db429-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="db429-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="db429-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="db429-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="db429-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="db429-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="db429-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db429-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="db429-111">Return value</span></span>

<span data-ttu-id="db429-112">En cas de réussite, [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) a la valeur zéro et [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) est défini à la position actuelle du contrôle.</span><span class="sxs-lookup"><span data-stu-id="db429-112">If successful, the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) is set to zero and the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is set to the control's current position.</span></span> <span data-ttu-id="db429-113">Si une erreur se produit, **HIWORD** est défini sur une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="db429-113">If an error occurs, the **HIWORD** is set to a nonzero value.</span></span>

## <a name="remarks"></a><span data-ttu-id="db429-114">Notes</span><span class="sxs-lookup"><span data-stu-id="db429-114">Remarks</span></span>

<span data-ttu-id="db429-115">Lors du traitement de ce message, le contrôle up-up met à jour sa position actuelle en fonction de la légende de la fenêtre associée.</span><span class="sxs-lookup"><span data-stu-id="db429-115">When processing this message, the up-down control updates its current position based on the caption of the buddy window.</span></span> <span data-ttu-id="db429-116">Le contrôle up-up retourne une erreur s’il n’existe aucune fenêtre associée ou si la légende spécifie une valeur non valide ou hors limites.</span><span class="sxs-lookup"><span data-stu-id="db429-116">The up-down control returns an error if there is no buddy window or if the caption specifies an invalid or out-of-range value.</span></span> <span data-ttu-id="db429-117">En outre, un indicateur d’erreur est défini dans le HIWORD du retour si le contrôle est créé sans le style [**uds \_ SETBUDDYINT**](up-down-control-styles.md) , même s’il retourne une valeur position valide dans le LOWORD du retour.</span><span class="sxs-lookup"><span data-stu-id="db429-117">Also, an error flag is set in the HIWORD of the return if the control is created without the [**UDS\_SETBUDDYINT**](up-down-control-styles.md) style, even though it returns a valid position value in the LOWORD of the return.</span></span>

<span data-ttu-id="db429-118">Si les valeurs 32 bits ont été activées pour un contrôle up-UpDown avec [**UDM \_ SETRANGE32**](udm-setrange32.md), ce message retourne uniquement les 16 bits inférieurs de la position.</span><span class="sxs-lookup"><span data-stu-id="db429-118">If 32-bit values have been enabled for an up-down control with [**UDM\_SETRANGE32**](udm-setrange32.md), this message returns only the lower 16 bits of the position.</span></span> <span data-ttu-id="db429-119">Pour récupérer la position 32 bits complète, utilisez [**UDM \_ GETPOS32**](udm-getpos32.md).</span><span class="sxs-lookup"><span data-stu-id="db429-119">To retrieve the full 32-bit position, use [**UDM\_GETPOS32**](udm-getpos32.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="db429-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="db429-120">Requirements</span></span>



| <span data-ttu-id="db429-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="db429-121">Requirement</span></span> | <span data-ttu-id="db429-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="db429-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="db429-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="db429-123">Minimum supported client</span></span><br/> | <span data-ttu-id="db429-124">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="db429-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="db429-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="db429-125">Minimum supported server</span></span><br/> | <span data-ttu-id="db429-126">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="db429-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="db429-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="db429-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="db429-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="db429-128"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db429-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="db429-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="db429-130">**Référence**</span><span class="sxs-lookup"><span data-stu-id="db429-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="db429-131">**\_GETRANGE UDM**</span><span class="sxs-lookup"><span data-stu-id="db429-131">**UDM\_GETRANGE**</span></span>](udm-getrange.md)
</dt> <dt>

[<span data-ttu-id="db429-132">**\_GETRANGE32 UDM**</span><span class="sxs-lookup"><span data-stu-id="db429-132">**UDM\_GETRANGE32**</span></span>](udm-getrange32.md)
</dt> <dt>

[<span data-ttu-id="db429-133">**\_SetPos UDM**</span><span class="sxs-lookup"><span data-stu-id="db429-133">**UDM\_SETPOS**</span></span>](udm-setpos.md)
</dt> <dt>

[<span data-ttu-id="db429-134">**\_SETRANGE32 UDM**</span><span class="sxs-lookup"><span data-stu-id="db429-134">**UDM\_SETRANGE32**</span></span>](udm-setrange32.md)
</dt> </dl>

 

