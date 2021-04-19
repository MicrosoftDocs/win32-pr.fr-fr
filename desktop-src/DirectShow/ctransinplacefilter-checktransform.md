---
description: 'La méthode CheckTransform vérifie si un type de média d’entrée est compatible avec un type de média de sortie. Cette méthode remplace la méthode CTransformFilter :: CheckTransform.'
ms.assetid: d0953014-4a49-4738-a449-c247396a6794
title: Méthode CTransInPlaceFilter. CheckTransform (Transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.CheckTransform
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6a80132723be0b70f2c4afe93306d7f581b7734c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528561"
---
# <a name="ctransinplacefilterchecktransform-method"></a><span data-ttu-id="a18e7-104">Méthode CTransInPlaceFilter. CheckTransform</span><span class="sxs-lookup"><span data-stu-id="a18e7-104">CTransInPlaceFilter.CheckTransform method</span></span>

<span data-ttu-id="a18e7-105">La `CheckTransform` méthode vérifie si un type de média d’entrée est compatible avec un type de média de sortie.</span><span class="sxs-lookup"><span data-stu-id="a18e7-105">The `CheckTransform` method checks whether an input media type is compatible with an output media type.</span></span> <span data-ttu-id="a18e7-106">Cette méthode remplace la méthode [**CTransformFilter :: CheckTransform**](ctransformfilter-checktransform.md) .</span><span class="sxs-lookup"><span data-stu-id="a18e7-106">This method overrides the [**CTransformFilter::CheckTransform**](ctransformfilter-checktransform.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a18e7-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a18e7-107">Syntax</span></span>


```C++
HRESULT CheckTransform(
   const CMediaType *mtIn,
   const CMediaType *mtOut
);
```



## <a name="parameters"></a><span data-ttu-id="a18e7-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a18e7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a18e7-109">*mtIn*</span><span class="sxs-lookup"><span data-stu-id="a18e7-109">*mtIn*</span></span> 
</dt> <dd>

<span data-ttu-id="a18e7-110">Pointeur vers un objet [**CMediaType**](cmediatype.md) qui spécifie le type d’entrée.</span><span class="sxs-lookup"><span data-stu-id="a18e7-110">Pointer to a [**CMediaType**](cmediatype.md) object that specifies the input type.</span></span>

</dd> <dt>

<span data-ttu-id="a18e7-111">*mtOut*</span><span class="sxs-lookup"><span data-stu-id="a18e7-111">*mtOut*</span></span> 
</dt> <dd>

<span data-ttu-id="a18e7-112">Pointeur vers un objet **CMediaType** qui spécifie le type de sortie.</span><span class="sxs-lookup"><span data-stu-id="a18e7-112">Pointer to a **CMediaType** object that specifies the output type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a18e7-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a18e7-113">Return value</span></span>

<span data-ttu-id="a18e7-114">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a18e7-114">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="a18e7-115">Notes</span><span class="sxs-lookup"><span data-stu-id="a18e7-115">Remarks</span></span>

<span data-ttu-id="a18e7-116">Le filtre **CTransInPlace** n’appelle jamais `CheckTransform` .</span><span class="sxs-lookup"><span data-stu-id="a18e7-116">The **CTransInPlace** filter never calls `CheckTransform`.</span></span> <span data-ttu-id="a18e7-117">Au lieu de cela, toute connexion de code confidentiel utilise [**CTransformFilter :: CheckInputType**](ctransformfilter-checkinputtype.md) pour vérifier le type de média, en partant du principe que les types d’entrée et de sortie correspondent toujours.</span><span class="sxs-lookup"><span data-stu-id="a18e7-117">Instead, all pin connection use [**CTransformFilter::CheckInputType**](ctransformfilter-checkinputtype.md) to check the media type, with the assumption that the input and output types always match.</span></span>

## <a name="requirements"></a><span data-ttu-id="a18e7-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a18e7-118">Requirements</span></span>



| <span data-ttu-id="a18e7-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a18e7-119">Requirement</span></span> | <span data-ttu-id="a18e7-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="a18e7-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a18e7-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="a18e7-121">Header</span></span><br/>  | <dl> <span data-ttu-id="a18e7-122"><dt>Transip. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a18e7-122"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a18e7-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a18e7-123">Library</span></span><br/> | <dl> <span data-ttu-id="a18e7-124"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="a18e7-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a18e7-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a18e7-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a18e7-126">**CTransInPlaceFilter, classe**</span><span class="sxs-lookup"><span data-stu-id="a18e7-126">**CTransInPlaceFilter Class**</span></span>](ctransinplacefilter.md)
</dt> </dl>

 

 




