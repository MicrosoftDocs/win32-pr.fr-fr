---
title: Message CB_DELETESTRING (winuser. h)
description: Supprime une chaîne dans la zone de liste d’une zone de liste déroulante.
ms.assetid: 8d526796-04ef-4c01-94d6-fb50e6fef27b
keywords:
- CB_DELETESTRING les contrôles de message Windows
topic_type:
- apiref
api_name:
- CB_DELETESTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb0d3900c86874db1113c219fd9f7967c5f6bb6e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106003"
---
# <a name="cb_deletestring-message"></a><span data-ttu-id="ade6b-104">\_Message DELETESTRING CB</span><span class="sxs-lookup"><span data-stu-id="ade6b-104">CB\_DELETESTRING message</span></span>

<span data-ttu-id="ade6b-105">Supprime une chaîne dans la zone de liste d’une zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="ade6b-105">Deletes a string in the list box of a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="ade6b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ade6b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ade6b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ade6b-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ade6b-108">Index de base zéro de la chaîne à supprimer.</span><span class="sxs-lookup"><span data-stu-id="ade6b-108">The zero-based index of the string to delete.</span></span>

</dd> <dt>

<span data-ttu-id="ade6b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ade6b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ade6b-110">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="ade6b-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ade6b-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ade6b-111">Return value</span></span>

<span data-ttu-id="ade6b-112">La valeur de retour est le nombre de chaînes restantes dans la liste.</span><span class="sxs-lookup"><span data-stu-id="ade6b-112">The return value is a count of the strings remaining in the list.</span></span> <span data-ttu-id="ade6b-113">Si le paramètre *wParam* spécifie un index supérieur au nombre d’éléments dans la liste, la valeur de retour est CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="ade6b-113">If the *wParam* parameter specifies an index greater than the number of items in the list, the return value is CB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="ade6b-114">Notes</span><span class="sxs-lookup"><span data-stu-id="ade6b-114">Remarks</span></span>

<span data-ttu-id="ade6b-115">Si vous créez la zone de liste déroulante avec un style owner-drawn mais sans le style [**CBS \_ HASSTRINGS**](combo-box-styles.md) , le système envoie un message [**WM \_ DELETEITEM**](wm-deleteitem.md) au propriétaire de la zone de liste déroulante afin que l’application puisse libérer toutes les données supplémentaires associées à l’élément.</span><span class="sxs-lookup"><span data-stu-id="ade6b-115">If you create the combo box with an owner-drawn style but without the [**CBS\_HASSTRINGS**](combo-box-styles.md) style, the system sends a [**WM\_DELETEITEM**](wm-deleteitem.md) message to the owner of the combo box so the application can free any additional data associated with the item.</span></span>

## <a name="requirements"></a><span data-ttu-id="ade6b-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ade6b-116">Requirements</span></span>



| <span data-ttu-id="ade6b-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ade6b-117">Requirement</span></span> | <span data-ttu-id="ade6b-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="ade6b-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ade6b-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ade6b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ade6b-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ade6b-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ade6b-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ade6b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ade6b-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ade6b-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ade6b-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="ade6b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ade6b-124"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ade6b-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ade6b-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ade6b-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="ade6b-126">**Référence**</span><span class="sxs-lookup"><span data-stu-id="ade6b-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ade6b-127">**\_RESETCONTENT CB**</span><span class="sxs-lookup"><span data-stu-id="ade6b-127">**CB\_RESETCONTENT**</span></span>](cb-resetcontent.md)
</dt> <dt>

[<span data-ttu-id="ade6b-128">**WM \_ DELETEITEM**</span><span class="sxs-lookup"><span data-stu-id="ade6b-128">**WM\_DELETEITEM**</span></span>](wm-deleteitem.md)
</dt> </dl>

 

 





