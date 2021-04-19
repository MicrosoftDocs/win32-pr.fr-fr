---
description: 'La méthode QueryVendorInfo récupère une chaîne contenant des informations sur le fournisseur. Cette méthode implémente la méthode IBaseFilter :: QueryVendorInfo.'
ms.assetid: 083c0556-d516-4daf-8621-e158ea78b5a3
title: Méthode CBaseFilter. QueryVendorInfo (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.QueryVendorInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1786477c042bb1d9ecc6340056a771141d0a3c74
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530034"
---
# <a name="cbasefilterqueryvendorinfo-method"></a><span data-ttu-id="a5f92-104">Méthode CBaseFilter. QueryVendorInfo</span><span class="sxs-lookup"><span data-stu-id="a5f92-104">CBaseFilter.QueryVendorInfo method</span></span>

<span data-ttu-id="a5f92-105">La `QueryVendorInfo` méthode récupère une chaîne contenant des informations sur le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="a5f92-105">The `QueryVendorInfo` method retrieves a string containing vendor information.</span></span> <span data-ttu-id="a5f92-106">Cette méthode implémente la méthode [**IBaseFilter :: QueryVendorInfo**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-queryvendorinfo) .</span><span class="sxs-lookup"><span data-stu-id="a5f92-106">This method implements the [**IBaseFilter::QueryVendorInfo**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-queryvendorinfo) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5f92-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a5f92-107">Syntax</span></span>


```C++
HRESULT QueryVendorInfo(
   LPWSTR *pVendorInfo
);
```



## <a name="parameters"></a><span data-ttu-id="a5f92-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a5f92-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5f92-109">*pVendorInfo*</span><span class="sxs-lookup"><span data-stu-id="a5f92-109">*pVendorInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="a5f92-110">Adresse d’une variable qui reçoit un pointeur vers une chaîne de caractères larges contenant les informations sur le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="a5f92-110">Address of a variable that receives a pointer to a wide-character string containing the vendor information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5f92-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a5f92-111">Return value</span></span>

<span data-ttu-id="a5f92-112">Retourne E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="a5f92-112">Returns E\_NOTIMPL.</span></span>

## <a name="remarks"></a><span data-ttu-id="a5f92-113">Notes</span><span class="sxs-lookup"><span data-stu-id="a5f92-113">Remarks</span></span>

<span data-ttu-id="a5f92-114">Pour fournir des informations sur le fournisseur d’un filtre, substituez cette méthode.</span><span class="sxs-lookup"><span data-stu-id="a5f92-114">To provide vendor information for a filter, override this method.</span></span> <span data-ttu-id="a5f92-115">Si vous implémentez cette méthode, utilisez la fonction **CoTaskMemAlloc** pour allouer de la mémoire à la chaîne.</span><span class="sxs-lookup"><span data-stu-id="a5f92-115">If you implement this method, use the **CoTaskMemAlloc** function to allocate memory for the string.</span></span> <span data-ttu-id="a5f92-116">L’appelant est chargé d’appeler la fonction **CoTaskMemFree** .</span><span class="sxs-lookup"><span data-stu-id="a5f92-116">The caller is responsible for calling the **CoTaskMemFree** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5f92-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a5f92-117">Requirements</span></span>



| <span data-ttu-id="a5f92-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a5f92-118">Requirement</span></span> | <span data-ttu-id="a5f92-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="a5f92-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5f92-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="a5f92-120">Header</span></span><br/>  | <dl> <span data-ttu-id="a5f92-121"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a5f92-121"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="a5f92-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a5f92-122">Library</span></span><br/> | <dl> <span data-ttu-id="a5f92-123"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="a5f92-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5f92-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a5f92-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5f92-125">**CBaseFilter, classe**</span><span class="sxs-lookup"><span data-stu-id="a5f92-125">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




