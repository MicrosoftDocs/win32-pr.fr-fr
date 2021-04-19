---
description: Méthode de constructeur.
ms.assetid: 6213ce92-d98a-4fb6-b66c-e7cdea6dff0d
title: Constructeur CTransformOutputPin. CTransformOutputPin (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.CTransformOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 730149ae67abb2924174954bb8b620a02cfae2b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539296"
---
# <a name="ctransformoutputpinctransformoutputpin-constructor"></a><span data-ttu-id="f1b9b-103">Constructeur CTransformOutputPin. CTransformOutputPin</span><span class="sxs-lookup"><span data-stu-id="f1b9b-103">CTransformOutputPin.CTransformOutputPin constructor</span></span>

<span data-ttu-id="f1b9b-104">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="f1b9b-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1b9b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f1b9b-105">Syntax</span></span>


```C++
CTransformOutputPin(
   TCHAR            *pObjectName,
   CTransformFilter *pTransformFilter,
   HRESULT          *phr,
   LPCWSTR          pName
);
```



## <a name="parameters"></a><span data-ttu-id="f1b9b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f1b9b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1b9b-107">*pObjectName*</span><span class="sxs-lookup"><span data-stu-id="f1b9b-107">*pObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="f1b9b-108">Chaîne contenant le nom de débogage de l’objet.</span><span class="sxs-lookup"><span data-stu-id="f1b9b-108">String containing the debug name of the object.</span></span> <span data-ttu-id="f1b9b-109">Pour plus d’informations, consultez [**CBaseObject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="f1b9b-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1b9b-110">*pTransformFilter*</span><span class="sxs-lookup"><span data-stu-id="f1b9b-110">*pTransformFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="f1b9b-111">Pointeur vers le filtre qui a créé ce code confidentiel, qui doit être un objet [**CTransformFilter**](ctransformfilter.md) .</span><span class="sxs-lookup"><span data-stu-id="f1b9b-111">Pointer to the filter that created this pin, which must be a [**CTransformFilter**](ctransformfilter.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="f1b9b-112">*phr*</span><span class="sxs-lookup"><span data-stu-id="f1b9b-112">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="f1b9b-113">Pointeur vers une variable qui reçoit une valeur **HRESULT** indiquant la réussite ou l’échec de la méthode.</span><span class="sxs-lookup"><span data-stu-id="f1b9b-113">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span> <span data-ttu-id="f1b9b-114">Initialisez la valeur sur \_ OK avant de créer l’objet.</span><span class="sxs-lookup"><span data-stu-id="f1b9b-114">Initialize the value to S\_OK before creating the object.</span></span> <span data-ttu-id="f1b9b-115">La valeur est modifiée uniquement si une erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="f1b9b-115">The value is changed only if an error occurs.</span></span>

</dd> <dt>

<span data-ttu-id="f1b9b-116">*pName*</span><span class="sxs-lookup"><span data-stu-id="f1b9b-116">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="f1b9b-117">Chaîne de caractères larges contenant le nom du code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="f1b9b-117">Wide-character string containing the pin name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f1b9b-118">Notes</span><span class="sxs-lookup"><span data-stu-id="f1b9b-118">Remarks</span></span>

<span data-ttu-id="f1b9b-119">Le paramètre *pname* spécifie le nom du code confidentiel, qui est retourné par la méthode [**IPIN :: QueryPinInfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) .</span><span class="sxs-lookup"><span data-stu-id="f1b9b-119">The *pName* parameter specifies the pin name, which is returned by the [**IPin::QueryPinInfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) method.</span></span> <span data-ttu-id="f1b9b-120">Toutefois, la chaîne n’est pas utilisée pour l’identificateur de code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="f1b9b-120">However, the string is not used for the pin identifier.</span></span> <span data-ttu-id="f1b9b-121">L’identificateur de code confidentiel pour cette classe est toujours « out ».</span><span class="sxs-lookup"><span data-stu-id="f1b9b-121">The pin identifier for this class is always "Out".</span></span> <span data-ttu-id="f1b9b-122">Pour plus d’informations, consultez [**QueryId**](ctransformoutputpin-queryid.md).</span><span class="sxs-lookup"><span data-stu-id="f1b9b-122">For more information, see [**QueryId**](ctransformoutputpin-queryid.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f1b9b-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f1b9b-123">Requirements</span></span>



| <span data-ttu-id="f1b9b-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f1b9b-124">Requirement</span></span> | <span data-ttu-id="f1b9b-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1b9b-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1b9b-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="f1b9b-126">Header</span></span><br/>  | <dl> <span data-ttu-id="f1b9b-127"><dt>Transfrm. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f1b9b-127"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="f1b9b-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f1b9b-128">Library</span></span><br/> | <dl> <span data-ttu-id="f1b9b-129"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="f1b9b-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




