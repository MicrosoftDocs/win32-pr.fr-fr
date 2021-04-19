---
description: La méthode CreateInstance crée une instance de l’objet. Cette méthode prend en charge la création de l’objet par le biais d’une fabrique de classe. Pour plus d’informations, consultez CFactoryTemplate.
ms.assetid: 88dfa933-6fa1-4b57-8b0d-579233fa960c
title: Méthode CSeekingPassThru. CreateInstance (Seekpt. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSeekingPassThru.CreateInstance
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3640cbd6a0a3e582899e7f5cd349ca48498f3532
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542353"
---
# <a name="cseekingpassthrucreateinstance-method"></a><span data-ttu-id="b391c-105">CSeekingPassThru. CreateInstance, méthode</span><span class="sxs-lookup"><span data-stu-id="b391c-105">CSeekingPassThru.CreateInstance method</span></span>

<span data-ttu-id="b391c-106">La `CreateInstance` méthode crée une instance de l’objet.</span><span class="sxs-lookup"><span data-stu-id="b391c-106">The `CreateInstance` method creates an instance of the object.</span></span> <span data-ttu-id="b391c-107">Cette méthode prend en charge la création de l’objet par le biais d’une fabrique de classe.</span><span class="sxs-lookup"><span data-stu-id="b391c-107">This method supports creation of the object through a class factory.</span></span> <span data-ttu-id="b391c-108">Pour plus d’informations, consultez [**CFactoryTemplate**](cfactorytemplate.md).</span><span class="sxs-lookup"><span data-stu-id="b391c-108">For more information, see [**CFactoryTemplate**](cfactorytemplate.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b391c-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b391c-109">Syntax</span></span>


```C++
static CUnknown* CreateInstance(
   LPUNKNOWN pUnk,
   HRESULT   *phr
);
```



## <a name="parameters"></a><span data-ttu-id="b391c-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b391c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b391c-111">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="b391c-111">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="b391c-112">Pointeur vers le propriétaire de cet objet.</span><span class="sxs-lookup"><span data-stu-id="b391c-112">Pointer to the owner of this object.</span></span> <span data-ttu-id="b391c-113">Si l’objet est agrégé, passer un pointeur vers l’interface **IUnknown** de l’objet d’agrégation.</span><span class="sxs-lookup"><span data-stu-id="b391c-113">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="b391c-114">Sinon, affectez la valeur **null** à ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="b391c-114">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b391c-115">*phr*</span><span class="sxs-lookup"><span data-stu-id="b391c-115">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="b391c-116">Pointeur vers une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b391c-116">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="b391c-117">Ignoré.</span><span class="sxs-lookup"><span data-stu-id="b391c-117">Ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b391c-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b391c-118">Return value</span></span>

<span data-ttu-id="b391c-119">Retourne un pointeur vers un nouvel objet **CSeekingPassThru** .</span><span class="sxs-lookup"><span data-stu-id="b391c-119">Returns a pointer to a new **CSeekingPassThru** object.</span></span>

## <a name="requirements"></a><span data-ttu-id="b391c-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b391c-120">Requirements</span></span>



| <span data-ttu-id="b391c-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b391c-121">Requirement</span></span> | <span data-ttu-id="b391c-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="b391c-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b391c-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="b391c-123">Header</span></span><br/>  | <dl> <span data-ttu-id="b391c-124"><dt>Seekpt. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b391c-124"><dt>Seekpt.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="b391c-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b391c-125">Library</span></span><br/> | <dl> <span data-ttu-id="b391c-126"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="b391c-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b391c-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b391c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b391c-128">**CSeekingPassThru, classe**</span><span class="sxs-lookup"><span data-stu-id="b391c-128">**CSeekingPassThru Class**</span></span>](cseekingpassthru.md)
</dt> </dl>

 

 




