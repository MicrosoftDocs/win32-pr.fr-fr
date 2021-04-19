---
description: La méthode CheckMediaType détermine si le filtre accepte un type de média spécifique.
ms.assetid: 90d26cf6-443c-4a06-98c6-ffa14e27ee41
title: Méthode CBaseRenderer. CheckMediaType (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dc0d4fc70e9ed64f9481d827cb678eb3ff9721d4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526540"
---
# <a name="cbaserenderercheckmediatype-method"></a><span data-ttu-id="f70fd-103">Méthode CBaseRenderer. CheckMediaType</span><span class="sxs-lookup"><span data-stu-id="f70fd-103">CBaseRenderer.CheckMediaType method</span></span>

<span data-ttu-id="f70fd-104">La `CheckMediaType` méthode détermine si le filtre accepte un type de média spécifique.</span><span class="sxs-lookup"><span data-stu-id="f70fd-104">The `CheckMediaType` method determines if the filter accepts a specific media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="f70fd-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f70fd-105">Syntax</span></span>


```C++
virtual HRESULT CheckMediaType(
   const CMediaType *pmt
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="f70fd-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f70fd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f70fd-107">*crédit*</span><span class="sxs-lookup"><span data-stu-id="f70fd-107">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="f70fd-108">Pointeur vers un objet [**CMediaType**](cmediatype.md) qui contient le type de média proposé.</span><span class="sxs-lookup"><span data-stu-id="f70fd-108">Pointer to a [**CMediaType**](cmediatype.md) object that contains the proposed media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f70fd-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f70fd-109">Return value</span></span>

<span data-ttu-id="f70fd-110">Retourne S \_ OK si le type de média proposé est acceptable.</span><span class="sxs-lookup"><span data-stu-id="f70fd-110">Returns S\_OK if the proposed media type is acceptable.</span></span> <span data-ttu-id="f70fd-111">Sinon, retourne S \_ false ou un code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="f70fd-111">Otherwise, returns S\_FALSE or an error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f70fd-112">Notes</span><span class="sxs-lookup"><span data-stu-id="f70fd-112">Remarks</span></span>

<span data-ttu-id="f70fd-113">La broche d’entrée appelle cette méthode à partir de sa propre méthode [**CBasePin :: CheckMediaType**](cbasepin-checkmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="f70fd-113">The input pin calls this method from its own [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md) method.</span></span> <span data-ttu-id="f70fd-114">La classe dérivée doit implémenter cette méthode.</span><span class="sxs-lookup"><span data-stu-id="f70fd-114">The derived class must implement this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="f70fd-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f70fd-115">Requirements</span></span>



| <span data-ttu-id="f70fd-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f70fd-116">Requirement</span></span> | <span data-ttu-id="f70fd-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="f70fd-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f70fd-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="f70fd-118">Header</span></span><br/>  | <dl> <span data-ttu-id="f70fd-119"><dt>Renbase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f70fd-119"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f70fd-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f70fd-120">Library</span></span><br/> | <dl> <span data-ttu-id="f70fd-121"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="f70fd-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f70fd-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f70fd-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f70fd-123">**CBaseRenderer, classe**</span><span class="sxs-lookup"><span data-stu-id="f70fd-123">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




