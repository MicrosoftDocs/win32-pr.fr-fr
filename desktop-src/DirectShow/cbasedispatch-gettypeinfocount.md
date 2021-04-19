---
description: La méthode GetTypeInfoCount récupère le nombre d’interfaces d’informations de type fourni par l’objet.
ms.assetid: e09e6f6c-6ac8-4ce1-8ce1-ee5374d54183
title: Méthode CBaseDispatch. GetTypeInfoCount (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseDispatch.GetTypeInfoCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 39c5b78181f5f26fb5f57831345bb6345a26da85
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525471"
---
# <a name="cbasedispatchgettypeinfocount-method"></a><span data-ttu-id="51840-103">Méthode CBaseDispatch. GetTypeInfoCount</span><span class="sxs-lookup"><span data-stu-id="51840-103">CBaseDispatch.GetTypeInfoCount method</span></span>

<span data-ttu-id="51840-104">La `GetTypeInfoCount` méthode récupère le nombre d’interfaces d’informations de type fourni par l’objet.</span><span class="sxs-lookup"><span data-stu-id="51840-104">The `GetTypeInfoCount` method retrieves the number of type information interfaces the object provides.</span></span>

## <a name="syntax"></a><span data-ttu-id="51840-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="51840-105">Syntax</span></span>


```C++
HRESULT GetTypeInfoCount(
   UINT *pctinfo
);
```



## <a name="parameters"></a><span data-ttu-id="51840-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="51840-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51840-107">*pctinfo*</span><span class="sxs-lookup"><span data-stu-id="51840-107">*pctinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="51840-108">Pointeur vers une variable qui reçoit le nombre d’interfaces d’informations de type fournies par l’objet.</span><span class="sxs-lookup"><span data-stu-id="51840-108">Pointer to a variable that receives the number of type-information interfaces provided by the object.</span></span> <span data-ttu-id="51840-109">Lorsque la méthode retourne, la valeur est 1.</span><span class="sxs-lookup"><span data-stu-id="51840-109">When the method returns, the value is 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51840-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="51840-110">Return value</span></span>

<span data-ttu-id="51840-111">Retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="51840-111">Returns one of the following values.</span></span>



| <span data-ttu-id="51840-112">Code de retour</span><span class="sxs-lookup"><span data-stu-id="51840-112">Return code</span></span>                                                                               | <span data-ttu-id="51840-113">Description</span><span class="sxs-lookup"><span data-stu-id="51840-113">Description</span></span>                           |
|-------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="51840-114"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="51840-114"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="51840-115">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="51840-115">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="51840-116"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="51840-116"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="51840-117">Argument de pointeur **null** .</span><span class="sxs-lookup"><span data-stu-id="51840-117">**NULL** pointer argument.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="51840-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="51840-118">Requirements</span></span>



| <span data-ttu-id="51840-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="51840-119">Requirement</span></span> | <span data-ttu-id="51840-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="51840-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51840-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="51840-121">Header</span></span><br/>  | <dl> <span data-ttu-id="51840-122"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="51840-122"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="51840-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="51840-123">Library</span></span><br/> | <dl> <span data-ttu-id="51840-124"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="51840-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51840-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="51840-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51840-126">**CBaseDispatch, classe**</span><span class="sxs-lookup"><span data-stu-id="51840-126">**CBaseDispatch Class**</span></span>](cbasedispatch.md)
</dt> </dl>

 

 




