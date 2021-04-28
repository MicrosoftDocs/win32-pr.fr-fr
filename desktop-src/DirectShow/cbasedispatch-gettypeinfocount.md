---
description: 'Méthode CBaseDispatch. GetTypeInfoCount : la méthode GetTypeInfoCount récupère le nombre d’interfaces d’informations de type fourni par l’objet.'
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
ms.openlocfilehash: 81e68c94420b3d7715845f8d6bd14e26b770b44f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099887"
---
# <a name="cbasedispatchgettypeinfocount-method"></a><span data-ttu-id="ac12c-103">Méthode CBaseDispatch. GetTypeInfoCount</span><span class="sxs-lookup"><span data-stu-id="ac12c-103">CBaseDispatch.GetTypeInfoCount method</span></span>

<span data-ttu-id="ac12c-104">La `GetTypeInfoCount` méthode récupère le nombre d’interfaces d’informations de type fourni par l’objet.</span><span class="sxs-lookup"><span data-stu-id="ac12c-104">The `GetTypeInfoCount` method retrieves the number of type information interfaces the object provides.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac12c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ac12c-105">Syntax</span></span>


```C++
HRESULT GetTypeInfoCount(
   UINT *pctinfo
);
```



## <a name="parameters"></a><span data-ttu-id="ac12c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ac12c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac12c-107">*pctinfo*</span><span class="sxs-lookup"><span data-stu-id="ac12c-107">*pctinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="ac12c-108">Pointeur vers une variable qui reçoit le nombre d’interfaces d’informations de type fournies par l’objet.</span><span class="sxs-lookup"><span data-stu-id="ac12c-108">Pointer to a variable that receives the number of type-information interfaces provided by the object.</span></span> <span data-ttu-id="ac12c-109">Lorsque la méthode retourne, la valeur est 1.</span><span class="sxs-lookup"><span data-stu-id="ac12c-109">When the method returns, the value is 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac12c-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ac12c-110">Return value</span></span>

<span data-ttu-id="ac12c-111">Retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="ac12c-111">Returns one of the following values.</span></span>



| <span data-ttu-id="ac12c-112">Code de retour</span><span class="sxs-lookup"><span data-stu-id="ac12c-112">Return code</span></span>                                                                               | <span data-ttu-id="ac12c-113">Description</span><span class="sxs-lookup"><span data-stu-id="ac12c-113">Description</span></span>                           |
|-------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="ac12c-114"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ac12c-114"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="ac12c-115">Réussite.</span><span class="sxs-lookup"><span data-stu-id="ac12c-115">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="ac12c-116"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="ac12c-116"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="ac12c-117">Argument de pointeur **null** .</span><span class="sxs-lookup"><span data-stu-id="ac12c-117">**NULL** pointer argument.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="ac12c-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ac12c-118">Requirements</span></span>



| <span data-ttu-id="ac12c-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ac12c-119">Requirement</span></span> | <span data-ttu-id="ac12c-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="ac12c-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac12c-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="ac12c-121">Header</span></span><br/>  | <dl> <span data-ttu-id="ac12c-122"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ac12c-122"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ac12c-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ac12c-123">Library</span></span><br/> | <dl> <span data-ttu-id="ac12c-124"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="ac12c-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac12c-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ac12c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac12c-126">**CBaseDispatch, classe**</span><span class="sxs-lookup"><span data-stu-id="ac12c-126">**CBaseDispatch Class**</span></span>](cbasedispatch.md)
</dt> </dl>

 

 




