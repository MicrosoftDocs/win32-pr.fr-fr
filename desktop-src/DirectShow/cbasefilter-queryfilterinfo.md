---
description: 'La méthode QueryFilterInfo récupère des informations sur le filtre. Cette méthode implémente la méthode IBaseFilter :: QueryFilterInfo.'
ms.assetid: 0c25aa9e-933c-4c45-a1cc-ffc9253dd561
title: Méthode CBaseFilter. QueryFilterInfo (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.QueryFilterInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4a706663c1fb39e0e2e84b4097ec620f9e608843
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543968"
---
# <a name="cbasefilterqueryfilterinfo-method"></a><span data-ttu-id="35aa5-104">Méthode CBaseFilter. QueryFilterInfo</span><span class="sxs-lookup"><span data-stu-id="35aa5-104">CBaseFilter.QueryFilterInfo method</span></span>

<span data-ttu-id="35aa5-105">La `QueryFilterInfo` méthode récupère des informations sur le filtre.</span><span class="sxs-lookup"><span data-stu-id="35aa5-105">The `QueryFilterInfo` method retrieves information about the filter.</span></span> <span data-ttu-id="35aa5-106">Cette méthode implémente la méthode [**IBaseFilter :: QueryFilterInfo**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-queryfilterinfo) .</span><span class="sxs-lookup"><span data-stu-id="35aa5-106">This method implements the [**IBaseFilter::QueryFilterInfo**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-queryfilterinfo) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="35aa5-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="35aa5-107">Syntax</span></span>


```C++
HRESULT QueryFilterInfo(
   FILTER_INFO *pInfo
);
```



## <a name="parameters"></a><span data-ttu-id="35aa5-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="35aa5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35aa5-109">*pInfo*</span><span class="sxs-lookup"><span data-stu-id="35aa5-109">*pInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="35aa5-110">Pointeur vers une structure d' [**\_ informations de filtre**](/windows/win32/api/strmif/ns-strmif-filter_info) .</span><span class="sxs-lookup"><span data-stu-id="35aa5-110">Pointer to a [**FILTER\_INFO**](/windows/win32/api/strmif/ns-strmif-filter_info) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35aa5-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="35aa5-111">Return value</span></span>

<span data-ttu-id="35aa5-112">Retourne le \_ pointeur S ou OK \_ .</span><span class="sxs-lookup"><span data-stu-id="35aa5-112">Returns S\_OK or E\_POINTER.</span></span>

## <a name="remarks"></a><span data-ttu-id="35aa5-113">Notes</span><span class="sxs-lookup"><span data-stu-id="35aa5-113">Remarks</span></span>

<span data-ttu-id="35aa5-114">Cette méthode copie le nom du filtre à partir de la variable de membre [**CBaseFilter :: m \_ pname**](cbasefilter-m-pname.md) dans le membre **achName** de la structure d’informations de filtre \_ .</span><span class="sxs-lookup"><span data-stu-id="35aa5-114">This method copies the filter's name from the [**CBaseFilter::m\_pName**](cbasefilter-m-pname.md) member variable into the **achName** member of the FILTER\_INFO structure.</span></span> <span data-ttu-id="35aa5-115">Si **m \_ pname** a la **valeur null**, la méthode définit **achName** sur L' \\ 0 '.</span><span class="sxs-lookup"><span data-stu-id="35aa5-115">If **m\_pName** is **NULL**, the method sets **achName** to L'\\0'.</span></span>

<span data-ttu-id="35aa5-116">La méthode définit le membre **pGraph** de la structure d’informations de filtre \_ égal à la variable membre [**CBaseFilter :: m \_ pGraph**](cbasefilter-m-pgraph.md) et incrémente le décompte de références.</span><span class="sxs-lookup"><span data-stu-id="35aa5-116">The method sets the **pGraph** member of the FILTER\_INFO structure equal to the [**CBaseFilter::m\_pGraph**](cbasefilter-m-pgraph.md) member variable, and increments the reference count.</span></span> <span data-ttu-id="35aa5-117">L’appelant doit libérer l’interface.</span><span class="sxs-lookup"><span data-stu-id="35aa5-117">The caller must release the interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="35aa5-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="35aa5-118">Requirements</span></span>



| <span data-ttu-id="35aa5-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="35aa5-119">Requirement</span></span> | <span data-ttu-id="35aa5-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="35aa5-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35aa5-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="35aa5-121">Header</span></span><br/>  | <dl> <span data-ttu-id="35aa5-122"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="35aa5-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="35aa5-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="35aa5-123">Library</span></span><br/> | <dl> <span data-ttu-id="35aa5-124"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="35aa5-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35aa5-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="35aa5-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35aa5-126">**CBaseFilter, classe**</span><span class="sxs-lookup"><span data-stu-id="35aa5-126">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




