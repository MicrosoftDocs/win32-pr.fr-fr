---
description: Méthode de constructeur.
ms.assetid: f0d30125-5d16-470c-a5fb-a7df96814dad
title: Constructeur CTransInPlaceFilter. CTransInPlaceFilter (Transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.CTransInPlaceFilter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 091ea6e6a52d4cc9221ddb29db34b4823111a395
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526458"
---
# <a name="ctransinplacefilterctransinplacefilter-constructor"></a><span data-ttu-id="69f22-103">Constructeur CTransInPlaceFilter. CTransInPlaceFilter</span><span class="sxs-lookup"><span data-stu-id="69f22-103">CTransInPlaceFilter.CTransInPlaceFilter constructor</span></span>

<span data-ttu-id="69f22-104">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="69f22-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="69f22-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="69f22-105">Syntax</span></span>


```C++
CTransInPlaceFilter(
   TCHAR     *pObjectName,
   LPUNKNOWN lpUnk,
   REFCLSID  clsid,
   HRESULT   *phr,
   bool      bModifiesData = TRUE
);
```



## <a name="parameters"></a><span data-ttu-id="69f22-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="69f22-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69f22-107">*pObjectName*</span><span class="sxs-lookup"><span data-stu-id="69f22-107">*pObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="69f22-108">Chaîne contenant le nom de débogage du filtre.</span><span class="sxs-lookup"><span data-stu-id="69f22-108">String containing the debug name of the filter.</span></span> <span data-ttu-id="69f22-109">Pour plus d’informations, consultez [**CBaseObject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="69f22-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="69f22-110">*lpUnk*</span><span class="sxs-lookup"><span data-stu-id="69f22-110">*lpUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="69f22-111">Pointeur vers le propriétaire de cet objet.</span><span class="sxs-lookup"><span data-stu-id="69f22-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="69f22-112">Si l’objet est agrégé, passer un pointeur vers l’interface **IUnknown** de l’objet d’agrégation.</span><span class="sxs-lookup"><span data-stu-id="69f22-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="69f22-113">Sinon, affectez la valeur **null** à ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="69f22-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="69f22-114">*identificateur*</span><span class="sxs-lookup"><span data-stu-id="69f22-114">*clsid*</span></span> 
</dt> <dd>

<span data-ttu-id="69f22-115">Identificateur de classe du filtre.</span><span class="sxs-lookup"><span data-stu-id="69f22-115">Class identifier of the filter.</span></span>

</dd> <dt>

<span data-ttu-id="69f22-116">*phr*</span><span class="sxs-lookup"><span data-stu-id="69f22-116">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="69f22-117">Ignoré.</span><span class="sxs-lookup"><span data-stu-id="69f22-117">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="69f22-118">*bModifiesData*</span><span class="sxs-lookup"><span data-stu-id="69f22-118">*bModifiesData*</span></span> 
</dt> <dd>

<span data-ttu-id="69f22-119">Valeur booléenne qui spécifie si le filtre modifie les données d’entrée.</span><span class="sxs-lookup"><span data-stu-id="69f22-119">Boolean value that specifies whether the filter modifies the input data.</span></span> <span data-ttu-id="69f22-120">Si la **valeur est true**, le filtre modifie les données.</span><span class="sxs-lookup"><span data-stu-id="69f22-120">If **TRUE**, the filter modifies the data.</span></span> <span data-ttu-id="69f22-121">Dans le cas contraire, le filtre passe les données en aval inchangées.</span><span class="sxs-lookup"><span data-stu-id="69f22-121">Otherwise, the filter passes the data downstream unchanged.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="69f22-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="69f22-122">Requirements</span></span>



| <span data-ttu-id="69f22-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="69f22-123">Requirement</span></span> | <span data-ttu-id="69f22-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="69f22-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69f22-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="69f22-125">Header</span></span><br/>  | <dl> <span data-ttu-id="69f22-126"><dt>Transip. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="69f22-126"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="69f22-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="69f22-127">Library</span></span><br/> | <dl> <span data-ttu-id="69f22-128"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="69f22-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69f22-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="69f22-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69f22-130">**CTransInPlaceFilter, classe**</span><span class="sxs-lookup"><span data-stu-id="69f22-130">**CTransInPlaceFilter Class**</span></span>](ctransinplacefilter.md)
</dt> </dl>

 

 




