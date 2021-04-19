---
description: 'La méthode Clone effectue une copie de l’énumérateur avec le même état d’énumération. Cette méthode implémente la méthode IEnumPins :: Clone.'
ms.assetid: 6e44c970-b90a-4bdb-8c60-dd8f31516249
title: Méthode CEnumPins. Clone (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumPins.Clone
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2aa3e4604b260779a5d203e75e8e0790a7378b11
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541585"
---
# <a name="cenumpinsclone-method"></a><span data-ttu-id="e2f45-104">CEnumPins. Clone, méthode</span><span class="sxs-lookup"><span data-stu-id="e2f45-104">CEnumPins.Clone method</span></span>

<span data-ttu-id="e2f45-105">La `Clone` méthode effectue une copie de l’énumérateur avec le même état d’énumération.</span><span class="sxs-lookup"><span data-stu-id="e2f45-105">The `Clone` method makes a copy of the enumerator with the same enumeration state.</span></span> <span data-ttu-id="e2f45-106">Cette méthode implémente la méthode [**IEnumPins :: Clone**](/windows/desktop/api/Strmif/nf-strmif-ienumpins-clone) .</span><span class="sxs-lookup"><span data-stu-id="e2f45-106">This method implements the [**IEnumPins::Clone**](/windows/desktop/api/Strmif/nf-strmif-ienumpins-clone) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2f45-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e2f45-107">Syntax</span></span>


```C++
HRESULT Clone(
   IEnumPins **ppEnum
);
```



## <a name="parameters"></a><span data-ttu-id="e2f45-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e2f45-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2f45-109">*ppEnum*</span><span class="sxs-lookup"><span data-stu-id="e2f45-109">*ppEnum*</span></span> 
</dt> <dd>

<span data-ttu-id="e2f45-110">Adresse d’une variable qui reçoit un pointeur vers l’interface [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) du nouvel énumérateur.</span><span class="sxs-lookup"><span data-stu-id="e2f45-110">Address of a variable that receives a pointer to the [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) interface of the new enumerator.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2f45-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e2f45-111">Return value</span></span>

<span data-ttu-id="e2f45-112">Retourne l’une des valeurs **HRESULT** indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="e2f45-112">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="e2f45-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="e2f45-113">Return code</span></span>                                                                                                | <span data-ttu-id="e2f45-114">Description</span><span class="sxs-lookup"><span data-stu-id="e2f45-114">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e2f45-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e2f45-115"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="e2f45-116">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="e2f45-116">Success.</span></span><br/>                                                                    |
| <dl> <span data-ttu-id="e2f45-117"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="e2f45-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>              | <span data-ttu-id="e2f45-118">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="e2f45-118">Insufficient memory.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="e2f45-119"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="e2f45-119"><dt>**E\_POINTER**</dt></span></span> </dl>                  | <span data-ttu-id="e2f45-120">Argument de pointeur **null** .</span><span class="sxs-lookup"><span data-stu-id="e2f45-120">**NULL** pointer argument.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="e2f45-121"><dt>**VFW \_ E \_ enum \_ non \_ \_ synchronisé**</dt></span><span class="sxs-lookup"><span data-stu-id="e2f45-121"><dt>**VFW\_E\_ENUM\_OUT\_OF\_SYNC**</dt></span></span> </dl> | <span data-ttu-id="e2f45-122">L’état du filtre a changé et est désormais incohérent avec l’énumérateur.</span><span class="sxs-lookup"><span data-stu-id="e2f45-122">The filter's state has changed and is now inconsistent with the enumerator.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="e2f45-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e2f45-123">Requirements</span></span>



| <span data-ttu-id="e2f45-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e2f45-124">Requirement</span></span> | <span data-ttu-id="e2f45-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="e2f45-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2f45-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="e2f45-126">Header</span></span><br/>  | <dl> <span data-ttu-id="e2f45-127"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e2f45-127"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="e2f45-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e2f45-128">Library</span></span><br/> | <dl> <span data-ttu-id="e2f45-129"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="e2f45-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2f45-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e2f45-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2f45-131">**CEnumPins, classe**</span><span class="sxs-lookup"><span data-stu-id="e2f45-131">**CEnumPins Class**</span></span>](cenumpins.md)
</dt> </dl>

 

 




