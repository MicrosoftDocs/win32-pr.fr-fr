---
description: 'Méthode CMediaPosition. GetTypeInfoCount : la méthode GetTypeInfoCount récupère le nombre d’interfaces d’informations de type fourni par l’objet.'
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
ms.openlocfilehash: 8cfc54f414a6722f7f69a0330fad2d1a0cfab425
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095477"
---
# <a name="cmediapositiongettypeinfocount-method"></a><span data-ttu-id="5326d-103">Méthode CMediaPosition. GetTypeInfoCount</span><span class="sxs-lookup"><span data-stu-id="5326d-103">CMediaPosition.GetTypeInfoCount method</span></span>

<span data-ttu-id="5326d-104">La `GetTypeInfoCount` méthode récupère le nombre d’interfaces d’informations de type fourni par l’objet.</span><span class="sxs-lookup"><span data-stu-id="5326d-104">The `GetTypeInfoCount` method retrieves the number of type information interfaces the object provides.</span></span>

## <a name="syntax"></a><span data-ttu-id="5326d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5326d-105">Syntax</span></span>


```C++
HRESULT GetTypeInfoCount(
   UINT *pctinfo
);
```



## <a name="parameters"></a><span data-ttu-id="5326d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5326d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5326d-107">*pctinfo*</span><span class="sxs-lookup"><span data-stu-id="5326d-107">*pctinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="5326d-108">Pointeur vers une variable qui reçoit le nombre d’interfaces d’informations de type fournies par l’objet.</span><span class="sxs-lookup"><span data-stu-id="5326d-108">Pointer to a variable that receives the number of type-information interfaces provided by the object.</span></span> <span data-ttu-id="5326d-109">Lorsque la méthode retourne, la valeur est 1.</span><span class="sxs-lookup"><span data-stu-id="5326d-109">When the method returns, the value is 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5326d-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="5326d-110">Return value</span></span>

<span data-ttu-id="5326d-111">Retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="5326d-111">Returns one of the following values.</span></span>



| <span data-ttu-id="5326d-112">Code de retour</span><span class="sxs-lookup"><span data-stu-id="5326d-112">Return code</span></span>                                                                               | <span data-ttu-id="5326d-113">Description</span><span class="sxs-lookup"><span data-stu-id="5326d-113">Description</span></span>                           |
|-------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="5326d-114"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="5326d-114"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="5326d-115">Réussite.</span><span class="sxs-lookup"><span data-stu-id="5326d-115">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="5326d-116"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="5326d-116"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="5326d-117">Argument de pointeur **null** .</span><span class="sxs-lookup"><span data-stu-id="5326d-117">**NULL** pointer argument.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="5326d-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5326d-118">Requirements</span></span>



| <span data-ttu-id="5326d-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5326d-119">Requirement</span></span> | <span data-ttu-id="5326d-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="5326d-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5326d-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="5326d-121">Header</span></span><br/>  | <dl> <span data-ttu-id="5326d-122"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5326d-122"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5326d-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5326d-123">Library</span></span><br/> | <dl> <span data-ttu-id="5326d-124"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="5326d-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5326d-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5326d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5326d-126">**CMediaPosition, classe**</span><span class="sxs-lookup"><span data-stu-id="5326d-126">**CMediaPosition Class**</span></span>](cmediaposition.md)
</dt> </dl>

 

 




