---
title: Message CB_GETCOUNT (winuser. h)
description: Obtient le nombre d’éléments dans la zone de liste d’une zone de liste déroulante.
ms.assetid: 69667724-5452-4fcc-afc3-0d98d3beedc8
keywords:
- CB_GETCOUNT les contrôles de message Windows
topic_type:
- apiref
api_name:
- CB_GETCOUNT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7900aadf3ba87cc7603a3fe15f4974911c9f9a37
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103744020"
---
# <a name="cb_getcount-message"></a><span data-ttu-id="f8121-104">\_Message CB GETCOUNT</span><span class="sxs-lookup"><span data-stu-id="f8121-104">CB\_GETCOUNT message</span></span>

<span data-ttu-id="f8121-105">Obtient le nombre d’éléments dans la zone de liste d’une zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="f8121-105">Gets the number of items in the list box of a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="f8121-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f8121-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8121-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f8121-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f8121-108">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="f8121-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="f8121-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f8121-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f8121-110">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="f8121-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8121-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f8121-111">Return value</span></span>

<span data-ttu-id="f8121-112">La valeur de retour est le nombre d’éléments dans la zone de liste.</span><span class="sxs-lookup"><span data-stu-id="f8121-112">The return value is the number of items in the list box.</span></span> <span data-ttu-id="f8121-113">Si une erreur se produit, il s’agit de CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="f8121-113">If an error occurs, it is CB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8121-114">Notes</span><span class="sxs-lookup"><span data-stu-id="f8121-114">Remarks</span></span>

<span data-ttu-id="f8121-115">L’index est de base zéro, le nombre retourné est donc supérieur à la valeur d’index du dernier élément.</span><span class="sxs-lookup"><span data-stu-id="f8121-115">The index is zero-based, so the returned count is one greater than the index value of the last item.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8121-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f8121-116">Requirements</span></span>



| <span data-ttu-id="f8121-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f8121-117">Requirement</span></span> | <span data-ttu-id="f8121-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="f8121-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8121-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f8121-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f8121-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f8121-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f8121-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f8121-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f8121-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f8121-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f8121-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="f8121-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8121-124"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f8121-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 

 





