---
description: La méthode GetTypeInfoCount récupère le nombre d’interfaces d’informations de type fourni par l’objet.
ms.assetid: c98368f2-ae0c-4301-be30-7332b19f53ee
title: Méthode CMediaPosition. GetTypeInfoCount (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaPosition.GetTypeInfoCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7cac543c49b7f2f6b9dc3357bbb1c691477d9b62
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540330"
---
# <a name="cmediapositiongettypeinfocount-method"></a><span data-ttu-id="dac41-103">Méthode CMediaPosition. GetTypeInfoCount</span><span class="sxs-lookup"><span data-stu-id="dac41-103">CMediaPosition.GetTypeInfoCount method</span></span>

<span data-ttu-id="dac41-104">La `GetTypeInfoCount` méthode récupère le nombre d’interfaces d’informations de type fourni par l’objet.</span><span class="sxs-lookup"><span data-stu-id="dac41-104">The `GetTypeInfoCount` method retrieves the number of type information interfaces the object provides.</span></span>

## <a name="syntax"></a><span data-ttu-id="dac41-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dac41-105">Syntax</span></span>


```C++
HRESULT GetTypeInfoCount(
   UINT *pctinfo
);
```



## <a name="parameters"></a><span data-ttu-id="dac41-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dac41-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dac41-107">*pctinfo*</span><span class="sxs-lookup"><span data-stu-id="dac41-107">*pctinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="dac41-108">Pointeur vers une variable qui reçoit le nombre d’interfaces d’informations de type fournies par l’objet.</span><span class="sxs-lookup"><span data-stu-id="dac41-108">Pointer to a variable that receives the number of type-information interfaces provided by the object.</span></span> <span data-ttu-id="dac41-109">Lorsque la méthode retourne, la valeur est 1.</span><span class="sxs-lookup"><span data-stu-id="dac41-109">When the method returns, the value is 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dac41-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dac41-110">Return value</span></span>

<span data-ttu-id="dac41-111">Retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="dac41-111">Returns one of the following values.</span></span>



| <span data-ttu-id="dac41-112">Code de retour</span><span class="sxs-lookup"><span data-stu-id="dac41-112">Return code</span></span>                                                                               | <span data-ttu-id="dac41-113">Description</span><span class="sxs-lookup"><span data-stu-id="dac41-113">Description</span></span>                           |
|-------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="dac41-114"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="dac41-114"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="dac41-115">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="dac41-115">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="dac41-116"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="dac41-116"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="dac41-117">Argument de pointeur **null** .</span><span class="sxs-lookup"><span data-stu-id="dac41-117">**NULL** pointer argument.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="dac41-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dac41-118">Requirements</span></span>



| <span data-ttu-id="dac41-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dac41-119">Requirement</span></span> | <span data-ttu-id="dac41-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="dac41-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dac41-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="dac41-121">Header</span></span><br/>  | <dl> <span data-ttu-id="dac41-122"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dac41-122"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="dac41-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="dac41-123">Library</span></span><br/> | <dl> <span data-ttu-id="dac41-124"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="dac41-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dac41-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dac41-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dac41-126">**CMediaPosition, classe**</span><span class="sxs-lookup"><span data-stu-id="dac41-126">**CMediaPosition Class**</span></span>](cmediaposition.md)
</dt> </dl>

 

 




