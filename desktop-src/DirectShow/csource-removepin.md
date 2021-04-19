---
description: La méthode RemovePin supprime un pin spécifié du filtre. La méthode ne supprime pas le code confidentiel.
ms.assetid: 104eccfa-3fff-4f47-ba1b-3206eab9eef8
title: Méthode CSource. RemovePin (source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource.RemovePin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b71ced14a6f92a3056ac4f42e55bc3858c578ff6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537116"
---
# <a name="csourceremovepin-method"></a><span data-ttu-id="60f83-104">Méthode CSource. RemovePin</span><span class="sxs-lookup"><span data-stu-id="60f83-104">CSource.RemovePin method</span></span>

<span data-ttu-id="60f83-105">La `RemovePin` méthode supprime un pin spécifié du filtre.</span><span class="sxs-lookup"><span data-stu-id="60f83-105">The `RemovePin` method removes a specified pin from the filter.</span></span> <span data-ttu-id="60f83-106">La méthode ne supprime pas le code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="60f83-106">The method does not delete the pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="60f83-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="60f83-107">Syntax</span></span>


```C++
HRESULT RemovePin(
   CSourceStream *pStream
);
```



## <a name="parameters"></a><span data-ttu-id="60f83-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="60f83-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60f83-109">*pStream*</span><span class="sxs-lookup"><span data-stu-id="60f83-109">*pStream*</span></span> 
</dt> <dd>

<span data-ttu-id="60f83-110">Pointeur vers l’objet [**CSourceStream**](csourcestream.md) qui implémente le code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="60f83-110">Pointer to the [**CSourceStream**](csourcestream.md) object that implements the pin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60f83-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="60f83-111">Return value</span></span>

<span data-ttu-id="60f83-112">Retourne l’une des valeurs **HRESULT** indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="60f83-112">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="60f83-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="60f83-113">Return code</span></span>                                                                             | <span data-ttu-id="60f83-114">Description</span><span class="sxs-lookup"><span data-stu-id="60f83-114">Description</span></span>                                      |
|-----------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="60f83-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="60f83-115"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="60f83-116">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="60f83-116">Success.</span></span><br/>                              |
| <dl> <span data-ttu-id="60f83-117"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="60f83-117"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="60f83-118">Le filtre ne contient pas ce code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="60f83-118">The filter does not contain this pin.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="60f83-119">Notes</span><span class="sxs-lookup"><span data-stu-id="60f83-119">Remarks</span></span>

<span data-ttu-id="60f83-120">La méthode de destructeur appelle cette méthode pour supprimer la broche de sortie du filtre.</span><span class="sxs-lookup"><span data-stu-id="60f83-120">The destructor method calls this method, to remove the output pin from the filter.</span></span>

## <a name="requirements"></a><span data-ttu-id="60f83-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="60f83-121">Requirements</span></span>



| <span data-ttu-id="60f83-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="60f83-122">Requirement</span></span> | <span data-ttu-id="60f83-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="60f83-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60f83-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="60f83-124">Header</span></span><br/>  | <dl> <span data-ttu-id="60f83-125"><dt>Source. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="60f83-125"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="60f83-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="60f83-126">Library</span></span><br/> | <dl> <span data-ttu-id="60f83-127"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="60f83-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60f83-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="60f83-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60f83-129">**CSource, classe**</span><span class="sxs-lookup"><span data-stu-id="60f83-129">**CSource Class**</span></span>](csource.md)
</dt> </dl>

 

 




