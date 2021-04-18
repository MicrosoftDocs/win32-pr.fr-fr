---
description: La méthode Receive reçoit un exemple de support, le traite et le remet au filtre en aval.
ms.assetid: 87126353-b73a-45f5-a8e7-b719efdf9d76
title: CTransInPlaceFilter. Receive, méthode (Transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5e7a1f87617b59c31139cb3d857c83d4470fd709
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533405"
---
# <a name="ctransinplacefilterreceive-method"></a><span data-ttu-id="ab7c2-103">CTransInPlaceFilter. Receive, méthode</span><span class="sxs-lookup"><span data-stu-id="ab7c2-103">CTransInPlaceFilter.Receive method</span></span>

<span data-ttu-id="ab7c2-104">La `Receive` méthode reçoit un exemple de support, le traite et le remet au filtre en aval.</span><span class="sxs-lookup"><span data-stu-id="ab7c2-104">The `Receive` method receives a media sample, processes it, and delivers it to the downstream filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab7c2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ab7c2-105">Syntax</span></span>


```C++
HRESULT Receive(
   IMediaSample *pSample
);
```



## <a name="parameters"></a><span data-ttu-id="ab7c2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ab7c2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab7c2-107">*pSample*</span><span class="sxs-lookup"><span data-stu-id="ab7c2-107">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="ab7c2-108">Pointeur vers l’interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) sur l’exemple.</span><span class="sxs-lookup"><span data-stu-id="ab7c2-108">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface on the sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab7c2-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ab7c2-109">Return value</span></span>

<span data-ttu-id="ab7c2-110">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ab7c2-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="ab7c2-111">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="ab7c2-111">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="ab7c2-112">Code de retour</span><span class="sxs-lookup"><span data-stu-id="ab7c2-112">Return code</span></span>                                                                                  | <span data-ttu-id="ab7c2-113">Description</span><span class="sxs-lookup"><span data-stu-id="ab7c2-113">Description</span></span>                 |
|----------------------------------------------------------------------------------------------|-----------------------------|
| <dl> <span data-ttu-id="ab7c2-114"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ab7c2-114"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="ab7c2-115">Succès</span><span class="sxs-lookup"><span data-stu-id="ab7c2-115">Success</span></span><br/>          |
| <dl> <span data-ttu-id="ab7c2-116"><dt>**E \_ inattendu**</dt></span><span class="sxs-lookup"><span data-stu-id="ab7c2-116"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="ab7c2-117">Erreur inattendue</span><span class="sxs-lookup"><span data-stu-id="ab7c2-117">Unexpected error</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ab7c2-118">Notes</span><span class="sxs-lookup"><span data-stu-id="ab7c2-118">Remarks</span></span>

<span data-ttu-id="ab7c2-119">La broche d’entrée du filtre appelle cette méthode lorsqu’elle reçoit un exemple.</span><span class="sxs-lookup"><span data-stu-id="ab7c2-119">The filter's input pin calls this method when it receives a sample.</span></span> <span data-ttu-id="ab7c2-120">Le filtre appelle la méthode [**Transform**](ctransinplacefilter-transform.md) , que la classe dérivée doit implémenter.</span><span class="sxs-lookup"><span data-stu-id="ab7c2-120">The filter calls the [**Transform**](ctransinplacefilter-transform.md) method, which the derived class must implement.</span></span> <span data-ttu-id="ab7c2-121">La méthode **Transform** traite les données.</span><span class="sxs-lookup"><span data-stu-id="ab7c2-121">The **Transform** method processes the data.</span></span> <span data-ttu-id="ab7c2-122">Si le filtre n’utilise qu’un seul Allocator, il passe directement *pSample* à la méthode **Transform** .</span><span class="sxs-lookup"><span data-stu-id="ab7c2-122">If the filter is using only one allocator, it passes *pSample* directly to the **Transform** method.</span></span> <span data-ttu-id="ab7c2-123">Dans le cas contraire, il copie *pSample* et passe la copie.</span><span class="sxs-lookup"><span data-stu-id="ab7c2-123">Otherwise, it copies *pSample* and passes the copy.</span></span>

<span data-ttu-id="ab7c2-124">Si la méthode **Transform** retourne S \_ false, la `Receive` méthode supprime l’exemple.</span><span class="sxs-lookup"><span data-stu-id="ab7c2-124">If the **Transform** method returns S\_FALSE, the `Receive` method drops the sample.</span></span> <span data-ttu-id="ab7c2-125">Sur le premier exemple supprimé, le filtre envoie un événement de [**\_ \_ modification de la qualité ce**](ec-quality-change.md) au gestionnaire de graphes de filtre.</span><span class="sxs-lookup"><span data-stu-id="ab7c2-125">On the first dropped sample, the filter sends an [**EC\_QUALITY\_CHANGE**](ec-quality-change.md) event to the filter graph manager.</span></span> <span data-ttu-id="ab7c2-126">Dans le cas contraire, si la méthode **Transform** retourne \_ la valeur OK, le filtre remet l’exemple de sortie.</span><span class="sxs-lookup"><span data-stu-id="ab7c2-126">Otherwise, if the **Transform** method returns S\_OK, the filter delivers the output sample.</span></span> <span data-ttu-id="ab7c2-127">Pour ce faire, il appelle la méthode [**IMemInputPin :: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) sur la broche d’entrée en aval.</span><span class="sxs-lookup"><span data-stu-id="ab7c2-127">To do so, it calls the [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method on the downstream input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab7c2-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ab7c2-128">Requirements</span></span>



| <span data-ttu-id="ab7c2-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ab7c2-129">Requirement</span></span> | <span data-ttu-id="ab7c2-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="ab7c2-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab7c2-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="ab7c2-131">Header</span></span><br/>  | <dl> <span data-ttu-id="ab7c2-132"><dt>Transip. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ab7c2-132"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ab7c2-133">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ab7c2-133">Library</span></span><br/> | <dl> <span data-ttu-id="ab7c2-134"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="ab7c2-134"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab7c2-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ab7c2-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab7c2-136">**CTransInPlaceFilter, classe**</span><span class="sxs-lookup"><span data-stu-id="ab7c2-136">**CTransInPlaceFilter Class**</span></span>](ctransinplacefilter.md)
</dt> </dl>

 

 




