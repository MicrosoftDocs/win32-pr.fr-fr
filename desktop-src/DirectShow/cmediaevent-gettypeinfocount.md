---
description: Récupère le nombre d’interfaces d’informations de type fournies par un objet.
ms.assetid: e16bc324-bb49-4df2-afeb-2c2cd1620693
title: Méthode CMediaEvent. GetTypeInfoCount (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaEvent.GetTypeInfoCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4de7a79251f2d25c1c55642050ad06513a1bfe6f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532998"
---
# <a name="cmediaeventgettypeinfocount-method"></a><span data-ttu-id="38a0b-103">Méthode CMediaEvent. GetTypeInfoCount</span><span class="sxs-lookup"><span data-stu-id="38a0b-103">CMediaEvent.GetTypeInfoCount method</span></span>

<span data-ttu-id="38a0b-104">Récupère le nombre d’interfaces d’informations de type fournies par un objet.</span><span class="sxs-lookup"><span data-stu-id="38a0b-104">Retrieves the number of type-information interfaces provided by an object.</span></span>

## <a name="syntax"></a><span data-ttu-id="38a0b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="38a0b-105">Syntax</span></span>


```C++
HRESULT GetTypeInfoCount(
   UINT *pctinfo
);
```



## <a name="parameters"></a><span data-ttu-id="38a0b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="38a0b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38a0b-107">*pctinfo*</span><span class="sxs-lookup"><span data-stu-id="38a0b-107">*pctinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="38a0b-108">Pointeur vers le nombre d’interfaces d’informations de type fournies par l’objet.</span><span class="sxs-lookup"><span data-stu-id="38a0b-108">Pointer to number of type-information interfaces that the object provides.</span></span> <span data-ttu-id="38a0b-109">Si l’objet fournit des informations de type, ce nombre est 1 ; dans le cas contraire, le nombre est 0.</span><span class="sxs-lookup"><span data-stu-id="38a0b-109">If the object provides type information, this number is 1; otherwise, the number is 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38a0b-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="38a0b-110">Return value</span></span>

<span data-ttu-id="38a0b-111">Retourne le \_ pointeur E si *pcTInfo* n’est pas valide ; sinon, retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="38a0b-111">Returns E\_POINTER if *pctinfo* is invalid; otherwise, returns S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="38a0b-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="38a0b-112">Requirements</span></span>



| <span data-ttu-id="38a0b-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="38a0b-113">Requirement</span></span> | <span data-ttu-id="38a0b-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="38a0b-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38a0b-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="38a0b-115">Header</span></span><br/>  | <dl> <span data-ttu-id="38a0b-116"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="38a0b-116"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="38a0b-117">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="38a0b-117">Library</span></span><br/> | <dl> <span data-ttu-id="38a0b-118"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="38a0b-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38a0b-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="38a0b-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38a0b-120">**CMediaEvent, classe**</span><span class="sxs-lookup"><span data-stu-id="38a0b-120">**CMediaEvent Class**</span></span>](cmediaevent.md)
</dt> </dl>

 

 




