---
description: La méthode AddPin ajoute une nouvelle broche de sortie au filtre.
ms.assetid: 48850a1f-ecb7-460c-9bfc-ce1d1103a00b
title: Méthode CSource. AddPin (source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource.AddPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 224550756f5935ce26c106ba01c9ef64f0767140
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525949"
---
# <a name="csourceaddpin-method"></a><span data-ttu-id="94f64-103">Méthode CSource. AddPin</span><span class="sxs-lookup"><span data-stu-id="94f64-103">CSource.AddPin method</span></span>

<span data-ttu-id="94f64-104">La `AddPin` méthode ajoute une nouvelle broche de sortie au filtre.</span><span class="sxs-lookup"><span data-stu-id="94f64-104">The `AddPin` method adds a new output pin to the filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="94f64-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="94f64-105">Syntax</span></span>


```C++
HRESULT AddPin(
   CSourceStream *pStream
);
```



## <a name="parameters"></a><span data-ttu-id="94f64-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="94f64-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94f64-107">*pStream*</span><span class="sxs-lookup"><span data-stu-id="94f64-107">*pStream*</span></span> 
</dt> <dd>

<span data-ttu-id="94f64-108">Pointeur vers l’objet [**CSourceStream**](csourcestream.md) qui implémente le code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="94f64-108">Pointer to the [**CSourceStream**](csourcestream.md) object that implements the pin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94f64-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="94f64-109">Return value</span></span>

<span data-ttu-id="94f64-110">Retourne l’une des valeurs **HRESULT** indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="94f64-110">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="94f64-111">Code de retour</span><span class="sxs-lookup"><span data-stu-id="94f64-111">Return code</span></span>                                                                                   | <span data-ttu-id="94f64-112">Description</span><span class="sxs-lookup"><span data-stu-id="94f64-112">Description</span></span>                    |
|-----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <span data-ttu-id="94f64-113"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="94f64-113"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="94f64-114">Succès</span><span class="sxs-lookup"><span data-stu-id="94f64-114">Success</span></span><br/>             |
| <dl> <span data-ttu-id="94f64-115"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="94f64-115"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="94f64-116">Mémoire insuffisante</span><span class="sxs-lookup"><span data-stu-id="94f64-116">Insufficient memory</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="94f64-117">Notes</span><span class="sxs-lookup"><span data-stu-id="94f64-117">Remarks</span></span>

<span data-ttu-id="94f64-118">Lorsque vous créez un nouveau code confidentiel dérivé de **CSourceStream**, le constructeur **CSourceStream** appelle automatiquement cette méthode pour ajouter la broche de sortie au filtre.</span><span class="sxs-lookup"><span data-stu-id="94f64-118">When you create a new pin derived from **CSourceStream**, the **CSourceStream** constructor automatically calls this method, to add the output pin to the filter.</span></span>

## <a name="requirements"></a><span data-ttu-id="94f64-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="94f64-119">Requirements</span></span>



| <span data-ttu-id="94f64-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="94f64-120">Requirement</span></span> | <span data-ttu-id="94f64-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="94f64-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94f64-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="94f64-122">Header</span></span><br/>  | <dl> <span data-ttu-id="94f64-123"><dt>Source. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="94f64-123"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="94f64-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="94f64-124">Library</span></span><br/> | <dl> <span data-ttu-id="94f64-125"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="94f64-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94f64-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="94f64-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94f64-127">**CSource, classe**</span><span class="sxs-lookup"><span data-stu-id="94f64-127">**CSource Class**</span></span>](csource.md)
</dt> </dl>

 

 




