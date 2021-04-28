---
description: Méthode constructeur CTransInPlaceOutputPin. CTransInPlaceOutputPin.
ms.assetid: fe7b2d62-0e6a-4253-b469-6cede5dc9bb1
title: Constructeur CTransInPlaceOutputPin. CTransInPlaceOutputPin (Transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceOutputPin.CTransInPlaceOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d6b63ee3aa52bc0363bcab90275be4148659b3bb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094707"
---
# <a name="ctransinplaceoutputpinctransinplaceoutputpin-constructor"></a><span data-ttu-id="6569d-103">Constructeur CTransInPlaceOutputPin. CTransInPlaceOutputPin</span><span class="sxs-lookup"><span data-stu-id="6569d-103">CTransInPlaceOutputPin.CTransInPlaceOutputPin constructor</span></span>

<span data-ttu-id="6569d-104">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="6569d-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6569d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6569d-105">Syntax</span></span>


```C++
CTransInPlaceOutputPin(
   TCHAR               *pObjectName,
   CTransInPlaceFilter *pFilter,
   HRESULT             *phr,
   LPCWSTR             pName
);
```



## <a name="parameters"></a><span data-ttu-id="6569d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6569d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6569d-107">*pObjectName*</span><span class="sxs-lookup"><span data-stu-id="6569d-107">*pObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="6569d-108">Chaîne contenant le nom de débogage de l’objet.</span><span class="sxs-lookup"><span data-stu-id="6569d-108">String containing the debug name of the object.</span></span> <span data-ttu-id="6569d-109">Pour plus d’informations, consultez [**CBaseObject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="6569d-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="6569d-110">*pFilter*</span><span class="sxs-lookup"><span data-stu-id="6569d-110">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="6569d-111">Pointeur vers le filtre qui a créé ce code confidentiel, qui doit être un objet [**CTransInPlaceFilter**](ctransinplacefilter.md) .</span><span class="sxs-lookup"><span data-stu-id="6569d-111">Pointer to the filter that created this pin, which must be a [**CTransInPlaceFilter**](ctransinplacefilter.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="6569d-112">*phr*</span><span class="sxs-lookup"><span data-stu-id="6569d-112">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="6569d-113">Pointeur vers une variable qui reçoit une valeur **HRESULT** indiquant la réussite ou l’échec de la méthode.</span><span class="sxs-lookup"><span data-stu-id="6569d-113">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span> <span data-ttu-id="6569d-114">Initialisez la valeur sur \_ OK avant de créer l’objet.</span><span class="sxs-lookup"><span data-stu-id="6569d-114">Initialize the value to S\_OK before creating the object.</span></span> <span data-ttu-id="6569d-115">La valeur est modifiée uniquement si une erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="6569d-115">The value is changed only if an error occurs.</span></span>

</dd> <dt>

<span data-ttu-id="6569d-116">*pName*</span><span class="sxs-lookup"><span data-stu-id="6569d-116">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="6569d-117">Chaîne de caractères larges contenant le nom du code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="6569d-117">Wide-character string containing the pin name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6569d-118">Notes </span><span class="sxs-lookup"><span data-stu-id="6569d-118">Remarks</span></span>

<span data-ttu-id="6569d-119">Le paramètre *pname* spécifie le nom du code confidentiel, qui est retourné par la méthode [**IPIN :: QueryPinInfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) .</span><span class="sxs-lookup"><span data-stu-id="6569d-119">The *pName* parameter specifies the pin name, which is returned by the [**IPin::QueryPinInfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) method.</span></span> <span data-ttu-id="6569d-120">Toutefois, la chaîne n’est pas utilisée pour l’identificateur de code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="6569d-120">However, the string is not used for the pin identifier.</span></span> <span data-ttu-id="6569d-121">L’identificateur de code confidentiel pour cette classe est toujours « out ».</span><span class="sxs-lookup"><span data-stu-id="6569d-121">The pin identifier for this class is always "Out".</span></span> <span data-ttu-id="6569d-122">Pour plus d’informations, consultez [**QueryId**](ctransforminputpin-queryid.md).</span><span class="sxs-lookup"><span data-stu-id="6569d-122">For more information, see [**QueryId**](ctransforminputpin-queryid.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6569d-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6569d-123">Requirements</span></span>



| <span data-ttu-id="6569d-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6569d-124">Requirement</span></span> | <span data-ttu-id="6569d-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="6569d-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6569d-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="6569d-126">Header</span></span><br/>  | <dl> <span data-ttu-id="6569d-127"><dt>Transip. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6569d-127"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="6569d-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6569d-128">Library</span></span><br/> | <dl> <span data-ttu-id="6569d-129"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="6569d-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6569d-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6569d-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6569d-131">**CTransInPlaceOutputPin, classe**</span><span class="sxs-lookup"><span data-stu-id="6569d-131">**CTransInPlaceOutputPin Class**</span></span>](ctransinplaceoutputpin.md)
</dt> </dl>

 

 




