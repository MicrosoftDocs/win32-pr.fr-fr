---
title: Message LB_GETITEMDATA (winuser. h)
description: Obtient la valeur définie par l’application associée à l’élément de zone de liste spécifié.
ms.assetid: 3a3f7fa5-ce04-4e95-86e1-5c7de796d1b6
keywords:
- LB_GETITEMDATA les contrôles de message Windows
topic_type:
- apiref
api_name:
- LB_GETITEMDATA
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80da838828cad7354aaa244f2218e8f9a8346755
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105991"
---
# <a name="lb_getitemdata-message"></a><span data-ttu-id="07cf7-104">\_Message GETITEMDATA lb</span><span class="sxs-lookup"><span data-stu-id="07cf7-104">LB\_GETITEMDATA message</span></span>

<span data-ttu-id="07cf7-105">Obtient la valeur définie par l’application associée à l’élément de zone de liste spécifié.</span><span class="sxs-lookup"><span data-stu-id="07cf7-105">Gets the application-defined value associated with the specified list box item.</span></span>

## <a name="parameters"></a><span data-ttu-id="07cf7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="07cf7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07cf7-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="07cf7-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="07cf7-108">Index de l'élément.</span><span class="sxs-lookup"><span data-stu-id="07cf7-108">The index of the item.</span></span>

<span data-ttu-id="07cf7-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : le paramètre *wParam* est limité aux valeurs 16 bits.</span><span class="sxs-lookup"><span data-stu-id="07cf7-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="07cf7-110">Cela signifie que les zones de liste ne peuvent pas contenir plus de 32 767 éléments.</span><span class="sxs-lookup"><span data-stu-id="07cf7-110">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="07cf7-111">Bien que le nombre d’éléments soit limité, la taille totale, en octets, des éléments d’une zone de liste n’est limitée que par la mémoire disponible.</span><span class="sxs-lookup"><span data-stu-id="07cf7-111">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="07cf7-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="07cf7-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="07cf7-113">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="07cf7-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07cf7-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="07cf7-114">Return value</span></span>

<span data-ttu-id="07cf7-115">La valeur de retour est la valeur associée à l’élément, ou LB \_ Err si une erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="07cf7-115">The return value is the value associated with the item, or LB\_ERR if an error occurs.</span></span> <span data-ttu-id="07cf7-116">Si l’élément se trouve dans une zone de liste owner-drawn et qu’il a été créé sans le style [**\_ HASSTRINGS**](list-box-styles.md) , cette valeur était dans le paramètre *lParam* du message [**lb \_ ADDSTRING**](lb-addstring.md) ou [**lb \_ INSERTSTRING**](lb-insertstring.md) qui a ajouté l’élément à la zone de liste.</span><span class="sxs-lookup"><span data-stu-id="07cf7-116">If the item is in an owner-drawn list box and was created without the [**LBS\_HASSTRINGS**](list-box-styles.md) style, this value was in the *lParam* parameter of the [**LB\_ADDSTRING**](lb-addstring.md) or [**LB\_INSERTSTRING**](lb-insertstring.md) message that added the item to the list box.</span></span> <span data-ttu-id="07cf7-117">Dans le cas contraire, il s’agit de la valeur dans le *lParam* du message [**lb \_ SETITEMDATA**](lb-setitemdata.md) .</span><span class="sxs-lookup"><span data-stu-id="07cf7-117">Otherwise, it is the value in the *lParam* of the [**LB\_SETITEMDATA**](lb-setitemdata.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="07cf7-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="07cf7-118">Requirements</span></span>



| <span data-ttu-id="07cf7-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="07cf7-119">Requirement</span></span> | <span data-ttu-id="07cf7-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="07cf7-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07cf7-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="07cf7-121">Minimum supported client</span></span><br/> | <span data-ttu-id="07cf7-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="07cf7-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="07cf7-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="07cf7-123">Minimum supported server</span></span><br/> | <span data-ttu-id="07cf7-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="07cf7-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="07cf7-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="07cf7-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="07cf7-126"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="07cf7-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07cf7-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="07cf7-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="07cf7-128">**Référence**</span><span class="sxs-lookup"><span data-stu-id="07cf7-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="07cf7-129">**LB \_ ADDSTRING**</span><span class="sxs-lookup"><span data-stu-id="07cf7-129">**LB\_ADDSTRING**</span></span>](lb-addstring.md)
</dt> <dt>

[<span data-ttu-id="07cf7-130">**\_INSERTSTRING lb**</span><span class="sxs-lookup"><span data-stu-id="07cf7-130">**LB\_INSERTSTRING**</span></span>](lb-insertstring.md)
</dt> <dt>

[<span data-ttu-id="07cf7-131">**\_SETITEMDATA lb**</span><span class="sxs-lookup"><span data-stu-id="07cf7-131">**LB\_SETITEMDATA**</span></span>](lb-setitemdata.md)
</dt> </dl>

 

 





