---
title: Message CB_GETDROPPEDWIDTH (winuser. h)
description: Obtient la largeur minimale autorisée, en pixels, de la zone de liste d’une zone de liste déroulante avec la \_ liste déroulante CBS ou le \_ style DropDownList SCC.
ms.assetid: d7f37a6c-a623-4b15-8ef7-4b64d85c15fa
keywords:
- CB_GETDROPPEDWIDTH les contrôles de message Windows
topic_type:
- apiref
api_name:
- CB_GETDROPPEDWIDTH
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 299b360348a6bf7378fdfc9bc9f0959b01366642
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032858"
---
# <a name="cb_getdroppedwidth-message"></a><span data-ttu-id="603be-104">\_Message GETDROPPEDWIDTH CB</span><span class="sxs-lookup"><span data-stu-id="603be-104">CB\_GETDROPPEDWIDTH message</span></span>

<span data-ttu-id="603be-105">Obtient la largeur minimale autorisée, en pixels, de la zone de liste d’une zone de liste déroulante avec la [**\_ liste déroulante CBS**](combo-box-styles.md) ou le style [**\_ DropDownList SCC**](combo-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="603be-105">Gets the minimum allowable width, in pixels, of the list box of a combo box with the [**CBS\_DROPDOWN**](combo-box-styles.md) or [**CBS\_DROPDOWNLIST**](combo-box-styles.md) style.</span></span>

## <a name="parameters"></a><span data-ttu-id="603be-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="603be-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="603be-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="603be-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="603be-108">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="603be-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="603be-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="603be-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="603be-110">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="603be-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="603be-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="603be-111">Return value</span></span>

<span data-ttu-id="603be-112">Si le message est correctement exécuté, la valeur de retour est la largeur, en pixels.</span><span class="sxs-lookup"><span data-stu-id="603be-112">If the message succeeds, the return value is the width, in pixels.</span></span>

<span data-ttu-id="603be-113">Si le message échoue, la valeur de retour est CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="603be-113">If the message fails, the return value is CB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="603be-114">Notes</span><span class="sxs-lookup"><span data-stu-id="603be-114">Remarks</span></span>

<span data-ttu-id="603be-115">Par défaut, la largeur minimale autorisée de la zone de liste déroulante est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="603be-115">By default, the minimum allowable width of the drop-down list box is zero.</span></span> <span data-ttu-id="603be-116">La largeur de la zone de liste est la largeur minimale autorisée ou la largeur de zone de liste déroulante, selon la valeur la plus grande.</span><span class="sxs-lookup"><span data-stu-id="603be-116">The width of the list box is either the minimum allowable width or the combo box width, whichever is larger.</span></span>

## <a name="requirements"></a><span data-ttu-id="603be-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="603be-117">Requirements</span></span>



| <span data-ttu-id="603be-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="603be-118">Requirement</span></span> | <span data-ttu-id="603be-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="603be-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="603be-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="603be-120">Minimum supported client</span></span><br/> | <span data-ttu-id="603be-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="603be-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="603be-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="603be-122">Minimum supported server</span></span><br/> | <span data-ttu-id="603be-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="603be-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="603be-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="603be-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="603be-125"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="603be-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="603be-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="603be-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="603be-127">**\_SETDROPPEDWIDTH CB**</span><span class="sxs-lookup"><span data-stu-id="603be-127">**CB\_SETDROPPEDWIDTH**</span></span>](cb-setdroppedwidth.md)
</dt> </dl>

 

 





