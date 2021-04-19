---
description: La méthode Copy copie un exemple de support.
ms.assetid: 3fbc6925-6e9c-4419-ab0d-0bbdbdf9bb8e
title: CTransInPlaceFilter. Copy, méthode (Transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.Copy
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3063427611cd3a5aae74fecf6be273c07fdb917c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530014"
---
# <a name="ctransinplacefiltercopy-method"></a><span data-ttu-id="b1b81-103">CTransInPlaceFilter. Copy, méthode</span><span class="sxs-lookup"><span data-stu-id="b1b81-103">CTransInPlaceFilter.Copy method</span></span>

<span data-ttu-id="b1b81-104">La `Copy` méthode copie un échantillon de média.</span><span class="sxs-lookup"><span data-stu-id="b1b81-104">The `Copy` method copies a media sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1b81-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b1b81-105">Syntax</span></span>


```C++
IMediaSample* Copy(
   IMediaSample *pSource
);
```



## <a name="parameters"></a><span data-ttu-id="b1b81-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b1b81-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1b81-107">*pSource*</span><span class="sxs-lookup"><span data-stu-id="b1b81-107">*pSource*</span></span> 
</dt> <dd>

<span data-ttu-id="b1b81-108">Pointeur vers l’interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) de l’exemple.</span><span class="sxs-lookup"><span data-stu-id="b1b81-108">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface of the sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1b81-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b1b81-109">Return value</span></span>

<span data-ttu-id="b1b81-110">Retourne un pointeur vers l’interface **IMediaSample** sur le nouvel exemple.</span><span class="sxs-lookup"><span data-stu-id="b1b81-110">Returns a pointer to the **IMediaSample** interface on the new sample.</span></span>

## <a name="remarks"></a><span data-ttu-id="b1b81-111">Notes</span><span class="sxs-lookup"><span data-stu-id="b1b81-111">Remarks</span></span>

<span data-ttu-id="b1b81-112">Cette méthode récupère une mémoire tampon vide à partir de l’allocateur en aval.</span><span class="sxs-lookup"><span data-stu-id="b1b81-112">This method retrieves an empty buffer from the downstream allocator.</span></span> <span data-ttu-id="b1b81-113">Elle copie tous les exemples de propriétés de *pSource* dans le nouvel exemple, ainsi que les données réelles dans l’exemple.</span><span class="sxs-lookup"><span data-stu-id="b1b81-113">It copies all of the sample properties from *pSource* into the new sample, along with the actual data in the sample.</span></span> <span data-ttu-id="b1b81-114">Si le filtre utilise deux allocations, il appelle cette méthode pour copier des données dans les mémoires tampons.</span><span class="sxs-lookup"><span data-stu-id="b1b81-114">If the filter is using two allocators, it calls this method to copy data across buffers.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1b81-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b1b81-115">Requirements</span></span>



| <span data-ttu-id="b1b81-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b1b81-116">Requirement</span></span> | <span data-ttu-id="b1b81-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="b1b81-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1b81-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="b1b81-118">Header</span></span><br/>  | <dl> <span data-ttu-id="b1b81-119"><dt>Transip. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b1b81-119"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b1b81-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b1b81-120">Library</span></span><br/> | <dl> <span data-ttu-id="b1b81-121"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="b1b81-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1b81-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b1b81-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1b81-123">**CTransInPlaceFilter, classe**</span><span class="sxs-lookup"><span data-stu-id="b1b81-123">**CTransInPlaceFilter Class**</span></span>](ctransinplacefilter.md)
</dt> </dl>

 

 




