---
description: 'Méthode CMediaPosition. GetTypeInfo : la méthode GetTypeInfo récupère les informations de type de l’objet, qui peuvent ensuite être utilisées pour obtenir les informations de type d’une interface.'
ms.assetid: 0a04c43d-8b4b-4780-b02f-04053c405c77
title: Méthode CMediaPosition. GetTypeInfo (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaPosition.GetTypeInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f7827a3599f05061b5760084bed46cd2554b45f9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099137"
---
# <a name="cmediapositiongettypeinfo-method"></a><span data-ttu-id="115a5-103">Méthode CMediaPosition. GetTypeInfo</span><span class="sxs-lookup"><span data-stu-id="115a5-103">CMediaPosition.GetTypeInfo method</span></span>

<span data-ttu-id="115a5-104">La `GetTypeInfo` méthode récupère les informations de type de l’objet, qui peuvent ensuite être utilisées pour obtenir les informations de type d’une interface.</span><span class="sxs-lookup"><span data-stu-id="115a5-104">The `GetTypeInfo` method retrieves the type information for the object, which can then be used to get the type information for an interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="115a5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="115a5-105">Syntax</span></span>


```C++
HRESULT GetTypeInfo(
   UINT      itinfo,
   LCID      lcid,
   ITypeInfo **pptinfo
);
```



## <a name="parameters"></a><span data-ttu-id="115a5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="115a5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="115a5-107">*itinfo*</span><span class="sxs-lookup"><span data-stu-id="115a5-107">*itinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="115a5-108">Informations de type à retourner.</span><span class="sxs-lookup"><span data-stu-id="115a5-108">Type information to return.</span></span> <span data-ttu-id="115a5-109">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="115a5-109">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="115a5-110">*lcid*</span><span class="sxs-lookup"><span data-stu-id="115a5-110">*lcid*</span></span> 
</dt> <dd>

<span data-ttu-id="115a5-111">Identificateur de paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="115a5-111">Locale identifier.</span></span>

</dd> <dt>

<span data-ttu-id="115a5-112">*ppTInfo*</span><span class="sxs-lookup"><span data-stu-id="115a5-112">*pptinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="115a5-113">Adresse d’une variable qui reçoit un pointeur **ITypeInfo** .</span><span class="sxs-lookup"><span data-stu-id="115a5-113">Address of a variable that receives an **ITypeInfo** pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="115a5-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="115a5-114">Return value</span></span>

<span data-ttu-id="115a5-115">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="115a5-115">Returns an **HRESULT** value.</span></span> <span data-ttu-id="115a5-116">Les valeurs possibles sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="115a5-116">Possible values include the following.</span></span>



| <span data-ttu-id="115a5-117">Code de retour</span><span class="sxs-lookup"><span data-stu-id="115a5-117">Return code</span></span>                                                                                             | <span data-ttu-id="115a5-118">Description</span><span class="sxs-lookup"><span data-stu-id="115a5-118">Description</span></span>                                    |
|---------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="115a5-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="115a5-119"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="115a5-120">Réussite.</span><span class="sxs-lookup"><span data-stu-id="115a5-120">Success.</span></span><br/>                            |
| <dl> <span data-ttu-id="115a5-121"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="115a5-121"><dt>**E\_POINTER**</dt></span></span> </dl>               | <span data-ttu-id="115a5-122">Argument de pointeur **null** .</span><span class="sxs-lookup"><span data-stu-id="115a5-122">**NULL** pointer argument.</span></span><br/>          |
| <dl> <span data-ttu-id="115a5-123"><dt>**TAPEZ \_ E \_ ELEMENTNOTFOUND**</dt></span><span class="sxs-lookup"><span data-stu-id="115a5-123"><dt>**TYPE\_E\_ELEMENTNOTFOUND**</dt></span></span> </dl> | <span data-ttu-id="115a5-124">Le paramètre *iTInfo* n’est pas égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="115a5-124">The *itinfo* parameter is not zero.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="115a5-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="115a5-125">Requirements</span></span>



| <span data-ttu-id="115a5-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="115a5-126">Requirement</span></span> | <span data-ttu-id="115a5-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="115a5-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="115a5-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="115a5-128">Header</span></span><br/>  | <dl> <span data-ttu-id="115a5-129"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="115a5-129"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="115a5-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="115a5-130">Library</span></span><br/> | <dl> <span data-ttu-id="115a5-131"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="115a5-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="115a5-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="115a5-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="115a5-133">**CMediaPosition, classe**</span><span class="sxs-lookup"><span data-stu-id="115a5-133">**CMediaPosition Class**</span></span>](cmediaposition.md)
</dt> </dl>

 

 




