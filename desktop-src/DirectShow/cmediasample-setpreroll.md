---
description: 'La méthode SetPreroll spécifie si cet exemple est un exemple de préroll. Un exemple de préroll ne doit pas être affiché. Cette méthode implémente la méthode IMediaSample :: SetPreroll.'
ms.assetid: 2887e627-5999-407a-88d3-811c803c9a43
title: Méthode CMediaSample. SetPreroll (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetPreroll
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 594f26ebb738a986c85a14b88f8896b122b58f47
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525156"
---
# <a name="cmediasamplesetpreroll-method"></a><span data-ttu-id="ff0f1-105">Méthode CMediaSample. SetPreroll</span><span class="sxs-lookup"><span data-stu-id="ff0f1-105">CMediaSample.SetPreroll method</span></span>

<span data-ttu-id="ff0f1-106">La `SetPreroll` méthode spécifie si cet exemple est un exemple de préroll.</span><span class="sxs-lookup"><span data-stu-id="ff0f1-106">The `SetPreroll` method specifies whether this sample is a preroll sample.</span></span> <span data-ttu-id="ff0f1-107">Un exemple de préroll ne doit pas être affiché.</span><span class="sxs-lookup"><span data-stu-id="ff0f1-107">A preroll sample should not be displayed.</span></span> <span data-ttu-id="ff0f1-108">Cette méthode implémente la méthode [**IMediaSample :: SetPreroll**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setpreroll) .</span><span class="sxs-lookup"><span data-stu-id="ff0f1-108">This method implements the [**IMediaSample::SetPreroll**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setpreroll) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff0f1-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ff0f1-109">Syntax</span></span>


```C++
HRESULT SetPreroll(
   BOOL bIsPreroll
);
```



## <a name="parameters"></a><span data-ttu-id="ff0f1-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ff0f1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff0f1-111">*bIsPreroll*</span><span class="sxs-lookup"><span data-stu-id="ff0f1-111">*bIsPreroll*</span></span> 
</dt> <dd>

<span data-ttu-id="ff0f1-112">Valeur booléenne qui spécifie s’il s’agit d’un exemple de préroll.</span><span class="sxs-lookup"><span data-stu-id="ff0f1-112">Boolean value that specifies whether this is a preroll sample.</span></span> <span data-ttu-id="ff0f1-113">Si la **valeur est true**, il s’agit d’un exemple de préroll.</span><span class="sxs-lookup"><span data-stu-id="ff0f1-113">If **TRUE**, this is a preroll sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff0f1-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ff0f1-114">Return value</span></span>

<span data-ttu-id="ff0f1-115">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ff0f1-115">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="ff0f1-116">Notes</span><span class="sxs-lookup"><span data-stu-id="ff0f1-116">Remarks</span></span>

<span data-ttu-id="ff0f1-117">Cette méthode met à jour la variable de membre [**CMediaSample :: m \_ dwFlags**](cmediasample-m-dwflags.md) , qui spécifie la propriété preroll.</span><span class="sxs-lookup"><span data-stu-id="ff0f1-117">This method updates the [**CMediaSample::m\_dwFlags**](cmediasample-m-dwflags.md) member variable, which specifies the preroll property.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff0f1-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ff0f1-118">Requirements</span></span>



| <span data-ttu-id="ff0f1-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ff0f1-119">Requirement</span></span> | <span data-ttu-id="ff0f1-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="ff0f1-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff0f1-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="ff0f1-121">Header</span></span><br/>  | <dl> <span data-ttu-id="ff0f1-122"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ff0f1-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="ff0f1-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ff0f1-123">Library</span></span><br/> | <dl> <span data-ttu-id="ff0f1-124"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="ff0f1-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff0f1-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ff0f1-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff0f1-126">**CMediaSample, classe**</span><span class="sxs-lookup"><span data-stu-id="ff0f1-126">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




