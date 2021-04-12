---
description: Récupère une valeur qui indique si le ConfirmationType passé à cette méthode a été défini sur ce IContextNode.
ms.assetid: 4a96bc46-b627-4784-ad1d-1079f49592e5
title: 'IContextNode :: IsConfirmed, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.IsConfirmed
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 300e0126b4a1ff55d372ff31deebde0eab686645
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526518"
---
# <a name="icontextnodeisconfirmed-method"></a><span data-ttu-id="30ce4-103">IContextNode :: IsConfirmed, méthode</span><span class="sxs-lookup"><span data-stu-id="30ce4-103">IContextNode::IsConfirmed method</span></span>

<span data-ttu-id="30ce4-104">Récupère une valeur qui indique si le ConfirmationType passé à cette méthode a été défini sur ce IContextNode.</span><span class="sxs-lookup"><span data-stu-id="30ce4-104">Retrieves a value that indicates whether the ConfirmationType passed in to this method has been set on this IContextNode.</span></span>

## <a name="syntax"></a><span data-ttu-id="30ce4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="30ce4-105">Syntax</span></span>


```C++
HRESULT IsConfirmed(
  [in]  ConfirmationType confirmedType,
  [out] VARIANT_BOOL     *pfTypeConfirmed
);
```



## <a name="parameters"></a><span data-ttu-id="30ce4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="30ce4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30ce4-107">*confirmedType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="30ce4-107">*confirmedType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30ce4-108">Type de confirmation pour lequel le test est effectué.</span><span class="sxs-lookup"><span data-stu-id="30ce4-108">The confirmation type being tested for.</span></span>

</dd> <dt>

<span data-ttu-id="30ce4-109">*pfTypeConfirmed* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="30ce4-109">*pfTypeConfirmed* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="30ce4-110">**Variante \_ TRUE** si le type passé dans confirmedType a été défini sur cet objet [**IContextNode**](icontextnode.md) ; Sinon, **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="30ce4-110">**VARIANT\_TRUE** if the type passed in confirmedType has been set on this [**IContextNode**](icontextnode.md) object; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30ce4-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="30ce4-111">Return value</span></span>

<span data-ttu-id="30ce4-112">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="30ce4-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="30ce4-113">Notes</span><span class="sxs-lookup"><span data-stu-id="30ce4-113">Remarks</span></span>

<span data-ttu-id="30ce4-114">Cette valeur est définie par la méthode [**IContextNode :: Confirm**](icontextnode-confirm.md) .</span><span class="sxs-lookup"><span data-stu-id="30ce4-114">This value is set by the [**IContextNode::Confirm**](icontextnode-confirm.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="30ce4-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="30ce4-115">Requirements</span></span>



| <span data-ttu-id="30ce4-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="30ce4-116">Requirement</span></span> | <span data-ttu-id="30ce4-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="30ce4-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30ce4-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="30ce4-118">Minimum supported client</span></span><br/> | <span data-ttu-id="30ce4-119">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="30ce4-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="30ce4-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="30ce4-120">Minimum supported server</span></span><br/> | <span data-ttu-id="30ce4-121">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="30ce4-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="30ce4-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="30ce4-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="30ce4-123"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="30ce4-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="30ce4-124">DLL</span><span class="sxs-lookup"><span data-stu-id="30ce4-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="30ce4-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="30ce4-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="30ce4-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="30ce4-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30ce4-127">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="30ce4-127">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="30ce4-128">**IContextNode :: Confirm**</span><span class="sxs-lookup"><span data-stu-id="30ce4-128">**IContextNode::Confirm**</span></span>](icontextnode-confirm.md)
</dt> <dt>

[<span data-ttu-id="30ce4-129">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="30ce4-129">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




