---
title: Message WM_COMPAREITEM (winuser. h)
description: Envoyé pour déterminer la position relative d’un nouvel élément dans la liste triée d’une zone de liste déroulante ou d’une zone de liste owner-drawn.
ms.assetid: 22882730-9fd6-4b45-a563-d7b00ed26564
keywords:
- WM_COMPAREITEM les contrôles de message Windows
topic_type:
- apiref
api_name:
- WM_COMPAREITEM
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f269b90f00e69cce2fb84e6b4efa76e554ad96f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464239"
---
# <a name="wm_compareitem-message"></a><span data-ttu-id="076a4-104">\_Message WM COMPAREITEM</span><span class="sxs-lookup"><span data-stu-id="076a4-104">WM\_COMPAREITEM message</span></span>

<span data-ttu-id="076a4-105">Envoyé pour déterminer la position relative d’un nouvel élément dans la liste triée d’une zone de liste déroulante ou d’une zone de liste owner-drawn.</span><span class="sxs-lookup"><span data-stu-id="076a4-105">Sent to determine the relative position of a new item in the sorted list of an owner-drawn combo box or list box.</span></span> <span data-ttu-id="076a4-106">Chaque fois que l’application ajoute un nouvel élément, le système envoie ce message au propriétaire d’une zone de liste déroulante ou d’une zone de liste créée avec le style de [**\_ Tri**](list-box-styles.md) [**CBS \_**](combo-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="076a4-106">Whenever the application adds a new item, the system sends this message to the owner of a combo box or list box created with the [**CBS\_SORT**](combo-box-styles.md) or [**LBS\_SORT**](list-box-styles.md) style.</span></span>


```C++
WM_COMPAREITEM

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="076a4-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="076a4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="076a4-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="076a4-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="076a4-109">Spécifie l’identificateur du contrôle qui a envoyé le message **WM \_ COMPAREITEM** .</span><span class="sxs-lookup"><span data-stu-id="076a4-109">Specifies the identifier of the control that sent the **WM\_COMPAREITEM** message.</span></span>

</dd> <dt>

<span data-ttu-id="076a4-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="076a4-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="076a4-111">Pointeur vers une structure [**compareitemstruct,**](/windows/win32/api/winuser/ns-winuser-compareitemstruct) qui contient les identificateurs et les données fournies par l’application pour deux éléments dans la zone de liste ou de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="076a4-111">Pointer to a [**COMPAREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-compareitemstruct) structure that contains the identifiers and application-supplied data for two items in the combo or list box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="076a4-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="076a4-112">Return value</span></span>

<span data-ttu-id="076a4-113">La valeur de retour indique la position relative des deux éléments.</span><span class="sxs-lookup"><span data-stu-id="076a4-113">The return value indicates the relative position of the two items.</span></span> <span data-ttu-id="076a4-114">Il peut s’agir de l’une des valeurs répertoriées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="076a4-114">It may be any of the values shown in the following table.</span></span>



| <span data-ttu-id="076a4-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="076a4-115">Return code</span></span>                                                                          | <span data-ttu-id="076a4-116">Description</span><span class="sxs-lookup"><span data-stu-id="076a4-116">Description</span></span>                                                  |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <dl> <span data-ttu-id="076a4-117"><dt>**Valeur**</dt></span><span class="sxs-lookup"><span data-stu-id="076a4-117"><dt>**Value**</dt></span></span> </dl> | <span data-ttu-id="076a4-118">Signification</span><span class="sxs-lookup"><span data-stu-id="076a4-118">Meaning</span></span><br/>                                           |
| <dl> <span data-ttu-id="076a4-119"><dt>**-1**</dt></span><span class="sxs-lookup"><span data-stu-id="076a4-119"><dt>**-1**</dt></span></span> </dl>    | <span data-ttu-id="076a4-120">L’élément 1 précède l’élément 2 dans l’ordre de tri.</span><span class="sxs-lookup"><span data-stu-id="076a4-120">Item 1 precedes item 2 in the sorted order.</span></span><br/>       |
| <dl> <span data-ttu-id="076a4-121"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="076a4-121"><dt>**0**</dt></span></span> </dl>     | <span data-ttu-id="076a4-122">Les éléments 1 et 2 sont équivalents dans l’ordre de tri.</span><span class="sxs-lookup"><span data-stu-id="076a4-122">Items 1 and 2 are equivalent in the sorted order.</span></span><br/> |
| <dl> <span data-ttu-id="076a4-123"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="076a4-123"><dt>**1**</dt></span></span> </dl>     | <span data-ttu-id="076a4-124">L’élément 1 suit l’élément 2 dans l’ordre de tri.</span><span class="sxs-lookup"><span data-stu-id="076a4-124">Item 1 follows item 2 in the sorted order.</span></span><br/>        |



 

## <a name="remarks"></a><span data-ttu-id="076a4-125">Notes</span><span class="sxs-lookup"><span data-stu-id="076a4-125">Remarks</span></span>

<span data-ttu-id="076a4-126">Lorsque le propriétaire d’une zone de liste déroulante ou d’une zone de liste owner-drawn reçoit ce message, le propriétaire retourne une valeur indiquant les éléments spécifiés par la structure [**compareitemstruct,**](/windows/win32/api/winuser/ns-winuser-compareitemstruct) qui apparaîtront avant l’autre.</span><span class="sxs-lookup"><span data-stu-id="076a4-126">When the owner of an owner-drawn combo box or list box receives this message, the owner returns a value indicating which of the items specified by the [**COMPAREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-compareitemstruct) structure will appear before the other.</span></span> <span data-ttu-id="076a4-127">En règle générale, le système envoie ce message plusieurs fois jusqu’à ce qu’il détermine la position exacte du nouvel élément.</span><span class="sxs-lookup"><span data-stu-id="076a4-127">Typically, the system sends this message several times until it determines the exact position for the new item.</span></span>

<span data-ttu-id="076a4-128">Si une procédure de boîte de dialogue gère ce message, elle doit effectuer un cast de la valeur de retour souhaitée en valeur **booléenne** et retourner la valeur directement.</span><span class="sxs-lookup"><span data-stu-id="076a4-128">If a dialog box procedure handles this message, it should cast the desired return value to a **BOOL** and return the value directly.</span></span> <span data-ttu-id="076a4-129">La \_ valeur DWL MSGRESULT définie par la fonction [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) est ignorée.</span><span class="sxs-lookup"><span data-stu-id="076a4-129">The DWL\_MSGRESULT value set by the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="076a4-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="076a4-130">Requirements</span></span>



| <span data-ttu-id="076a4-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="076a4-131">Requirement</span></span> | <span data-ttu-id="076a4-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="076a4-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="076a4-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="076a4-133">Minimum supported client</span></span><br/> | <span data-ttu-id="076a4-134">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="076a4-134">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="076a4-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="076a4-135">Minimum supported server</span></span><br/> | <span data-ttu-id="076a4-136">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="076a4-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="076a4-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="076a4-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="076a4-138"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="076a4-138"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="076a4-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="076a4-139">See also</span></span>

<dl> <dt>

<span data-ttu-id="076a4-140">**Référence**</span><span class="sxs-lookup"><span data-stu-id="076a4-140">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="076a4-141">**COMPAREITEMSTRUCT,**</span><span class="sxs-lookup"><span data-stu-id="076a4-141">**COMPAREITEMSTRUCT**</span></span>](/windows/win32/api/winuser/ns-winuser-compareitemstruct)
</dt> <dt>

<span data-ttu-id="076a4-142">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="076a4-142">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="076a4-143">**SetWindowLong**</span><span class="sxs-lookup"><span data-stu-id="076a4-143">**SetWindowLong**</span></span>](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)
</dt> </dl>

 

