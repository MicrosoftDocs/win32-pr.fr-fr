---
description: Méthode de constructeur.
ms.assetid: db0a3f78-ddb9-43b5-aab5-da2faaebb527
title: Constructeur CTransInPlaceInputPin. CTransInPlaceInputPin (Transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin.CTransInPlaceInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a801b2c4286f903ef450cac2fd76252f451f9add
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542284"
---
# <a name="ctransinplaceinputpinctransinplaceinputpin-constructor"></a><span data-ttu-id="ba66d-103">Constructeur CTransInPlaceInputPin. CTransInPlaceInputPin</span><span class="sxs-lookup"><span data-stu-id="ba66d-103">CTransInPlaceInputPin.CTransInPlaceInputPin constructor</span></span>

<span data-ttu-id="ba66d-104">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="ba66d-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba66d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ba66d-105">Syntax</span></span>


```C++
CTransInPlaceInputPin(
   TCHAR               *pObjectName,
   CTransInPlaceFilter *pFilter,
   HRESULT             *phr,
   LPCWSTR             pName
);
```



## <a name="parameters"></a><span data-ttu-id="ba66d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ba66d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba66d-107">*pObjectName*</span><span class="sxs-lookup"><span data-stu-id="ba66d-107">*pObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="ba66d-108">Chaîne contenant le nom de débogage de l’objet.</span><span class="sxs-lookup"><span data-stu-id="ba66d-108">String containing the debug name of the object.</span></span> <span data-ttu-id="ba66d-109">Pour plus d’informations, consultez [**CBaseObject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="ba66d-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="ba66d-110">*pFilter*</span><span class="sxs-lookup"><span data-stu-id="ba66d-110">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="ba66d-111">Pointeur vers le filtre qui a créé ce code confidentiel, qui doit être un objet [**CTransInPlaceFilter**](ctransinplacefilter.md) .</span><span class="sxs-lookup"><span data-stu-id="ba66d-111">Pointer to the filter that created this pin, which must be a [**CTransInPlaceFilter**](ctransinplacefilter.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="ba66d-112">*phr*</span><span class="sxs-lookup"><span data-stu-id="ba66d-112">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="ba66d-113">Pointeur vers une variable qui reçoit une valeur **HRESULT** indiquant la réussite ou l’échec de la méthode.</span><span class="sxs-lookup"><span data-stu-id="ba66d-113">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span> <span data-ttu-id="ba66d-114">Initialisez la valeur sur \_ OK avant de créer l’objet.</span><span class="sxs-lookup"><span data-stu-id="ba66d-114">Initialize the value to S\_OK before creating the object.</span></span> <span data-ttu-id="ba66d-115">La valeur est modifiée uniquement si une erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="ba66d-115">The value is changed only if an error occurs.</span></span>

</dd> <dt>

<span data-ttu-id="ba66d-116">*pName*</span><span class="sxs-lookup"><span data-stu-id="ba66d-116">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="ba66d-117">Chaîne de caractères larges contenant le nom du code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="ba66d-117">Wide-character string containing the pin name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ba66d-118">Notes</span><span class="sxs-lookup"><span data-stu-id="ba66d-118">Remarks</span></span>

<span data-ttu-id="ba66d-119">Le paramètre *pname* spécifie le nom du code confidentiel, qui est retourné par la méthode [**IPIN :: QueryPinInfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) .</span><span class="sxs-lookup"><span data-stu-id="ba66d-119">The *pName* parameter specifies the pin name, which is returned by the [**IPin::QueryPinInfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) method.</span></span> <span data-ttu-id="ba66d-120">Toutefois, cette chaîne n’est pas utilisée pour l’identificateur de code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="ba66d-120">However, this string is not used for the pin identifier.</span></span> <span data-ttu-id="ba66d-121">L’identificateur de code confidentiel pour cette classe est toujours dans.</span><span class="sxs-lookup"><span data-stu-id="ba66d-121">The pin identifier for this class is always In.</span></span> <span data-ttu-id="ba66d-122">Pour plus d’informations, consultez [**CTransformInputPin :: QueryId**](ctransforminputpin-queryid.md).</span><span class="sxs-lookup"><span data-stu-id="ba66d-122">For more information, see [**CTransformInputPin::QueryId**](ctransforminputpin-queryid.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ba66d-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ba66d-123">Requirements</span></span>



| <span data-ttu-id="ba66d-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ba66d-124">Requirement</span></span> | <span data-ttu-id="ba66d-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="ba66d-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba66d-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="ba66d-126">Header</span></span><br/>  | <dl> <span data-ttu-id="ba66d-127"><dt>Transip. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ba66d-127"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ba66d-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ba66d-128">Library</span></span><br/> | <dl> <span data-ttu-id="ba66d-129"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="ba66d-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba66d-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ba66d-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba66d-131">**CTransInPlaceInputPin, classe**</span><span class="sxs-lookup"><span data-stu-id="ba66d-131">**CTransInPlaceInputPin Class**</span></span>](ctransinplaceinputpin.md)
</dt> </dl>

 

 




