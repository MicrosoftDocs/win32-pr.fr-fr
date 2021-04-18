---
description: La méthode de transformation transforme un exemple d’entrée pour produire un échantillon de sortie.
ms.assetid: 30ef8c0c-e834-481a-93ff-d06e6fa1ddeb
title: CTransformFilter. Transform, méthode (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.Transform
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8498a9a6ce266e0646dbbdcb4f322c093d6e0cc3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532822"
---
# <a name="ctransformfiltertransform-method"></a><span data-ttu-id="17fa6-103">CTransformFilter. Transform, méthode</span><span class="sxs-lookup"><span data-stu-id="17fa6-103">CTransformFilter.Transform method</span></span>

<span data-ttu-id="17fa6-104">La `Transform` méthode transforme un exemple d’entrée pour produire un échantillon de sortie.</span><span class="sxs-lookup"><span data-stu-id="17fa6-104">The `Transform` method transforms an input sample to produce an output sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="17fa6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="17fa6-105">Syntax</span></span>


```C++
virtual HRESULT Transform(
   IMediaSample *pIn,
   IMediaSample *pOut
);
```



## <a name="parameters"></a><span data-ttu-id="17fa6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="17fa6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17fa6-107">*Définis*</span><span class="sxs-lookup"><span data-stu-id="17fa6-107">*pIn*</span></span> 
</dt> <dd>

<span data-ttu-id="17fa6-108">Pointeur vers l’interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) de l’exemple d’entrée.</span><span class="sxs-lookup"><span data-stu-id="17fa6-108">Pointer to the input sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> <dt>

<span data-ttu-id="17fa6-109">*Moue*</span><span class="sxs-lookup"><span data-stu-id="17fa6-109">*pOut*</span></span> 
</dt> <dd>

<span data-ttu-id="17fa6-110">Pointeur vers l’interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) de l’exemple de sortie.</span><span class="sxs-lookup"><span data-stu-id="17fa6-110">Pointer to the output sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17fa6-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="17fa6-111">Return value</span></span>

<span data-ttu-id="17fa6-112">La classe de base retourne E \_ inattendue.</span><span class="sxs-lookup"><span data-stu-id="17fa6-112">The base class returns E\_UNEXPECTED.</span></span>

<span data-ttu-id="17fa6-113">La classe dérivée doit retourner une valeur **HRESULT** indiquant la réussite ou l’échec.</span><span class="sxs-lookup"><span data-stu-id="17fa6-113">The derived class should return an **HRESULT** value, indicating success or failure.</span></span> <span data-ttu-id="17fa6-114">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="17fa6-114">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="17fa6-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="17fa6-115">Return code</span></span>                                                                             | <span data-ttu-id="17fa6-116">Description</span><span class="sxs-lookup"><span data-stu-id="17fa6-116">Description</span></span>                            |
|-----------------------------------------------------------------------------------------|----------------------------------------|
| <dl> <span data-ttu-id="17fa6-117"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="17fa6-117"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="17fa6-118">Ne fournissez pas cet exemple.</span><span class="sxs-lookup"><span data-stu-id="17fa6-118">Do not deliver this sample.</span></span><br/> |
| <dl> <span data-ttu-id="17fa6-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="17fa6-119"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="17fa6-120">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="17fa6-120">Success.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="17fa6-121">Notes</span><span class="sxs-lookup"><span data-stu-id="17fa6-121">Remarks</span></span>

<span data-ttu-id="17fa6-122">Substituez cette méthode pour produire des données de sortie.</span><span class="sxs-lookup"><span data-stu-id="17fa6-122">Override this method to produce output data.</span></span> <span data-ttu-id="17fa6-123">Lit les données d’entrée de l’exemple spécifié par le paramètre *pin* et écrit les nouvelles données dans l’exemple spécifié par le paramètre *moue* .</span><span class="sxs-lookup"><span data-stu-id="17fa6-123">Read the input data from the sample specified by the *pIn* parameter, and write the new data into the sample specified by the *pOut* parameter.</span></span>

<span data-ttu-id="17fa6-124">Avant que le filtre appelle cette méthode, il copie les propriétés de l’exemple d’entrée dans l’exemple de sortie.</span><span class="sxs-lookup"><span data-stu-id="17fa6-124">Before the filter calls this method, it copies the properties from the input sample to the output sample.</span></span> <span data-ttu-id="17fa6-125">La `Transform` méthode doit définir toutes les propriétés qui diffèrent entre les deux exemples, à l’aide des méthodes **IMediaSample** ou de l’interface [**IMediaSample2**](/windows/desktop/api/Strmif/nn-strmif-imediasample2) (si disponible).</span><span class="sxs-lookup"><span data-stu-id="17fa6-125">The `Transform` method should set any properties that differ between the two samples, using **IMediaSample** methods or the [**IMediaSample2**](/windows/desktop/api/Strmif/nn-strmif-imediasample2) interface (if available).</span></span>

<span data-ttu-id="17fa6-126">Si le filtre ne doit pas livrer cet exemple (par exemple, pour prendre en charge le contrôle de qualité), la méthode doit retourner S \_ false.</span><span class="sxs-lookup"><span data-stu-id="17fa6-126">If the filter should not deliver this sample (for example, to support quality control), the method should return S\_FALSE.</span></span>

## <a name="requirements"></a><span data-ttu-id="17fa6-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="17fa6-127">Requirements</span></span>



| <span data-ttu-id="17fa6-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="17fa6-128">Requirement</span></span> | <span data-ttu-id="17fa6-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="17fa6-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17fa6-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="17fa6-130">Header</span></span><br/>  | <dl> <span data-ttu-id="17fa6-131"><dt>Transfrm. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="17fa6-131"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="17fa6-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="17fa6-132">Library</span></span><br/> | <dl> <span data-ttu-id="17fa6-133"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="17fa6-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17fa6-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="17fa6-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17fa6-135">**CTransformFilter, classe**</span><span class="sxs-lookup"><span data-stu-id="17fa6-135">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




