---
description: 'La méthode Clone effectue une copie de l’énumérateur avec le même état d’énumération. Cette méthode implémente la méthode IEnumMediaTypes :: Clone.'
ms.assetid: 3b4eb29e-48fc-4f00-a5f3-597b9aa94ce1
title: Méthode CEnumMediaTypes. Clone (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumMediaTypes.Clone
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 43f051bf90afa231d3b677045468f26d06d55150
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106521613"
---
# <a name="cenummediatypesclone-method"></a><span data-ttu-id="60011-104">CEnumMediaTypes. Clone, méthode</span><span class="sxs-lookup"><span data-stu-id="60011-104">CEnumMediaTypes.Clone method</span></span>

<span data-ttu-id="60011-105">La `Clone` méthode effectue une copie de l’énumérateur avec le même état d’énumération.</span><span class="sxs-lookup"><span data-stu-id="60011-105">The `Clone` method makes a copy of the enumerator with the same enumeration state.</span></span> <span data-ttu-id="60011-106">Cette méthode implémente la méthode [**IEnumMediaTypes :: Clone**](/windows/desktop/api/Strmif/nf-strmif-ienummediatypes-clone) .</span><span class="sxs-lookup"><span data-stu-id="60011-106">This method implements the [**IEnumMediaTypes::Clone**](/windows/desktop/api/Strmif/nf-strmif-ienummediatypes-clone) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="60011-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="60011-107">Syntax</span></span>


```C++
HRESULT Clone(
   IEnumMediaTypes **ppEnum
);
```



## <a name="parameters"></a><span data-ttu-id="60011-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="60011-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60011-109">*ppEnum*</span><span class="sxs-lookup"><span data-stu-id="60011-109">*ppEnum*</span></span> 
</dt> <dd>

<span data-ttu-id="60011-110">Adresse d’une variable qui reçoit un pointeur vers l’interface [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) du nouvel énumérateur.</span><span class="sxs-lookup"><span data-stu-id="60011-110">Address of a variable that receives a pointer to the [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) interface of the new enumerator.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60011-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="60011-111">Return value</span></span>

<span data-ttu-id="60011-112">Retourne l’une des valeurs **HRESULT** indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="60011-112">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="60011-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="60011-113">Return code</span></span>                                                                                                | <span data-ttu-id="60011-114">Description</span><span class="sxs-lookup"><span data-stu-id="60011-114">Description</span></span>                                                                         |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="60011-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="60011-115"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="60011-116">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="60011-116">Success.</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="60011-117"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="60011-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>              | <span data-ttu-id="60011-118">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="60011-118">Insufficient memory.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="60011-119"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="60011-119"><dt>**E\_POINTER**</dt></span></span> </dl>                  | <span data-ttu-id="60011-120">Argument de pointeur **null** .</span><span class="sxs-lookup"><span data-stu-id="60011-120">**NULL** pointer argument.</span></span><br/>                                               |
| <dl> <span data-ttu-id="60011-121"><dt>**VFW \_ E \_ enum \_ non \_ \_ synchronisé**</dt></span><span class="sxs-lookup"><span data-stu-id="60011-121"><dt>**VFW\_E\_ENUM\_OUT\_OF\_SYNC**</dt></span></span> </dl> | <span data-ttu-id="60011-122">L’état du pin a changé et est désormais incohérent avec l’énumérateur.</span><span class="sxs-lookup"><span data-stu-id="60011-122">The pin's state has changed and is now inconsistent with the enumerator.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="60011-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="60011-123">Requirements</span></span>



| <span data-ttu-id="60011-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="60011-124">Requirement</span></span> | <span data-ttu-id="60011-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="60011-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60011-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="60011-126">Header</span></span><br/>  | <dl> <span data-ttu-id="60011-127"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="60011-127"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="60011-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="60011-128">Library</span></span><br/> | <dl> <span data-ttu-id="60011-129"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="60011-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60011-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="60011-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60011-131">**CEnumMediaTypes, classe**</span><span class="sxs-lookup"><span data-stu-id="60011-131">**CEnumMediaTypes Class**</span></span>](cenummediatypes.md)
</dt> </dl>

 

 




