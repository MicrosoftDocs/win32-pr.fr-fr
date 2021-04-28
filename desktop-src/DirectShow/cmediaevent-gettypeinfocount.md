---
description: 'Méthode CMediaEvent. GetTypeInfoCount : récupère le nombre d’interfaces d’informations de type fournies par un objet.'
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
ms.openlocfilehash: c9402ad973a08afed4d338cfdc7b5df7fb14b9f0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099117"
---
# <a name="cmediaeventgettypeinfocount-method"></a><span data-ttu-id="0de10-103">Méthode CMediaEvent. GetTypeInfoCount</span><span class="sxs-lookup"><span data-stu-id="0de10-103">CMediaEvent.GetTypeInfoCount method</span></span>

<span data-ttu-id="0de10-104">Récupère le nombre d’interfaces d’informations de type fournies par un objet.</span><span class="sxs-lookup"><span data-stu-id="0de10-104">Retrieves the number of type-information interfaces provided by an object.</span></span>

## <a name="syntax"></a><span data-ttu-id="0de10-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0de10-105">Syntax</span></span>


```C++
HRESULT GetTypeInfoCount(
   UINT *pctinfo
);
```



## <a name="parameters"></a><span data-ttu-id="0de10-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0de10-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0de10-107">*pctinfo*</span><span class="sxs-lookup"><span data-stu-id="0de10-107">*pctinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="0de10-108">Pointeur vers le nombre d’interfaces d’informations de type fournies par l’objet.</span><span class="sxs-lookup"><span data-stu-id="0de10-108">Pointer to number of type-information interfaces that the object provides.</span></span> <span data-ttu-id="0de10-109">Si l’objet fournit des informations de type, ce nombre est 1 ; dans le cas contraire, le nombre est 0.</span><span class="sxs-lookup"><span data-stu-id="0de10-109">If the object provides type information, this number is 1; otherwise, the number is 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0de10-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="0de10-110">Return value</span></span>

<span data-ttu-id="0de10-111">Retourne le \_ pointeur E si *pcTInfo* n’est pas valide ; sinon, retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0de10-111">Returns E\_POINTER if *pctinfo* is invalid; otherwise, returns S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="0de10-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0de10-112">Requirements</span></span>



| <span data-ttu-id="0de10-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0de10-113">Requirement</span></span> | <span data-ttu-id="0de10-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="0de10-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0de10-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="0de10-115">Header</span></span><br/>  | <dl> <span data-ttu-id="0de10-116"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0de10-116"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0de10-117">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0de10-117">Library</span></span><br/> | <dl> <span data-ttu-id="0de10-118"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="0de10-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0de10-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0de10-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0de10-120">**CMediaEvent, classe**</span><span class="sxs-lookup"><span data-stu-id="0de10-120">**CMediaEvent Class**</span></span>](cmediaevent.md)
</dt> </dl>

 

 




