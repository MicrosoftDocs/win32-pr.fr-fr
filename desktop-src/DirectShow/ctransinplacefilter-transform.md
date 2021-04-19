---
description: La méthode Transform transforme un exemple en place.
ms.assetid: 2268041b-70d4-48a9-9bb8-4ab921cce649
title: CTransInPlaceFilter. Transform, méthode (Transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.Transform
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d5b84f326807f730745268a217b6066dacb9aaa7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533268"
---
# <a name="ctransinplacefiltertransform-method"></a><span data-ttu-id="b79eb-103">CTransInPlaceFilter. Transform, méthode</span><span class="sxs-lookup"><span data-stu-id="b79eb-103">CTransInPlaceFilter.Transform method</span></span>

<span data-ttu-id="b79eb-104">La `Transform` méthode transforme un exemple en place.</span><span class="sxs-lookup"><span data-stu-id="b79eb-104">The `Transform` method transforms a sample in place.</span></span>

## <a name="syntax"></a><span data-ttu-id="b79eb-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b79eb-105">Syntax</span></span>


```C++
virtual HRESULT Transform(
   IMediaSample *pSample
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="b79eb-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b79eb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b79eb-107">*pSample*</span><span class="sxs-lookup"><span data-stu-id="b79eb-107">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="b79eb-108">Pointeur vers l’interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) de l’exemple.</span><span class="sxs-lookup"><span data-stu-id="b79eb-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b79eb-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b79eb-109">Return value</span></span>

<span data-ttu-id="b79eb-110">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b79eb-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="b79eb-111">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="b79eb-111">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="b79eb-112">Code de retour</span><span class="sxs-lookup"><span data-stu-id="b79eb-112">Return code</span></span>                                                                             | <span data-ttu-id="b79eb-113">Description</span><span class="sxs-lookup"><span data-stu-id="b79eb-113">Description</span></span>                            |
|-----------------------------------------------------------------------------------------|----------------------------------------|
| <dl> <span data-ttu-id="b79eb-114"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="b79eb-114"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="b79eb-115">Ne fournissez pas cet exemple.</span><span class="sxs-lookup"><span data-stu-id="b79eb-115">Do not deliver this sample.</span></span><br/> |
| <dl> <span data-ttu-id="b79eb-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b79eb-116"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="b79eb-117">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="b79eb-117">Success.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="b79eb-118">Notes</span><span class="sxs-lookup"><span data-stu-id="b79eb-118">Remarks</span></span>

<span data-ttu-id="b79eb-119">La classe dérivée doit implémenter cette méthode.</span><span class="sxs-lookup"><span data-stu-id="b79eb-119">The derived class must implement this method.</span></span> <span data-ttu-id="b79eb-120">Transformez les exemples de données sur place.</span><span class="sxs-lookup"><span data-stu-id="b79eb-120">Transform the sample data in place.</span></span> <span data-ttu-id="b79eb-121">Si le filtre utilise deux allocations, il copie les données de l’exemple d’entrée vers un nouvel exemple et passe la copie à cette méthode.</span><span class="sxs-lookup"><span data-stu-id="b79eb-121">If the filter is using two allocators, it copies the data from the input sample to a new sample, and passes the copy to this method.</span></span>

<span data-ttu-id="b79eb-122">Si le filtre ne doit pas livrer cet exemple (par exemple, pour prendre en charge le contrôle de qualité), la méthode doit retourner S \_ false.</span><span class="sxs-lookup"><span data-stu-id="b79eb-122">If the filter should not deliver this sample (for example, to support quality control), the method should return S\_FALSE.</span></span>

## <a name="requirements"></a><span data-ttu-id="b79eb-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b79eb-123">Requirements</span></span>



| <span data-ttu-id="b79eb-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b79eb-124">Requirement</span></span> | <span data-ttu-id="b79eb-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="b79eb-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b79eb-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="b79eb-126">Header</span></span><br/>  | <dl> <span data-ttu-id="b79eb-127"><dt>Transip. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b79eb-127"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b79eb-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b79eb-128">Library</span></span><br/> | <dl> <span data-ttu-id="b79eb-129"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="b79eb-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b79eb-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b79eb-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b79eb-131">**CTransInPlaceFilter, classe**</span><span class="sxs-lookup"><span data-stu-id="b79eb-131">**CTransInPlaceFilter Class**</span></span>](ctransinplacefilter.md)
</dt> </dl>

 

 




