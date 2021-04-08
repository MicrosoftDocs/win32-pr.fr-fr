---
title: Message CB_RESETCONTENT (winuser. h)
description: Supprime tous les éléments de la zone de liste et le contrôle d’édition d’une zone de liste déroulante.
ms.assetid: 55203c34-87ca-46e9-a914-a480d43ccadd
keywords:
- CB_RESETCONTENT les contrôles de message Windows
topic_type:
- apiref
api_name:
- CB_RESETCONTENT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3567f31ef98fffe42e53c4811acc786d41ae9f78
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843565"
---
# <a name="cb_resetcontent-message"></a><span data-ttu-id="a170f-104">\_Message RESETCONTENT CB</span><span class="sxs-lookup"><span data-stu-id="a170f-104">CB\_RESETCONTENT message</span></span>

<span data-ttu-id="a170f-105">Supprime tous les éléments de la zone de liste et le contrôle d’édition d’une zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="a170f-105">Removes all items from the list box and edit control of a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="a170f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a170f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a170f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a170f-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a170f-108">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="a170f-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="a170f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a170f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a170f-110">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="a170f-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a170f-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a170f-111">Return value</span></span>

<span data-ttu-id="a170f-112">Ce message retourne toujours CB \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a170f-112">This message always returns CB\_OKAY.</span></span>

## <a name="remarks"></a><span data-ttu-id="a170f-113">Notes</span><span class="sxs-lookup"><span data-stu-id="a170f-113">Remarks</span></span>

<span data-ttu-id="a170f-114">Si vous créez la zone de liste déroulante avec un style owner-drawn mais sans le style [**CBS \_ HASSTRINGS**](combo-box-styles.md) , le propriétaire de la zone de liste déroulante reçoit un message [**WM \_ DELETEITEM**](wm-deleteitem.md) pour chaque élément de la zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="a170f-114">If you create the combo box with an owner-drawn style but without the [**CBS\_HASSTRINGS**](combo-box-styles.md) style, the owner of the combo box receives a [**WM\_DELETEITEM**](wm-deleteitem.md) message for each item in the combo box.</span></span>

## <a name="requirements"></a><span data-ttu-id="a170f-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a170f-115">Requirements</span></span>



| <span data-ttu-id="a170f-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a170f-116">Requirement</span></span> | <span data-ttu-id="a170f-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="a170f-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a170f-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a170f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a170f-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a170f-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a170f-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a170f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a170f-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a170f-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a170f-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="a170f-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="a170f-123"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a170f-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a170f-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a170f-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="a170f-125">**Référence**</span><span class="sxs-lookup"><span data-stu-id="a170f-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a170f-126">**\_DELETESTRING CB**</span><span class="sxs-lookup"><span data-stu-id="a170f-126">**CB\_DELETESTRING**</span></span>](cb-deletestring.md)
</dt> <dt>

[<span data-ttu-id="a170f-127">**WM \_ DELETEITEM**</span><span class="sxs-lookup"><span data-stu-id="a170f-127">**WM\_DELETEITEM**</span></span>](wm-deleteitem.md)
</dt> </dl>

 

 





