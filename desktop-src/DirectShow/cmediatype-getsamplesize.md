---
description: La méthode GetSampleSize récupère la taille de l’échantillon.
ms.assetid: 5cc98556-cca6-46ca-ad33-cd40011ff6f4
title: Méthode CMediaType. GetSampleSize (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.GetSampleSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cc5b80e20ad2a16af9c25c68499348ffa744c0fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106520367"
---
# <a name="cmediatypegetsamplesize-method"></a><span data-ttu-id="6d7d9-103">Méthode CMediaType. GetSampleSize</span><span class="sxs-lookup"><span data-stu-id="6d7d9-103">CMediaType.GetSampleSize method</span></span>

<span data-ttu-id="6d7d9-104">La `GetSampleSize` méthode récupère la taille de l’échantillon.</span><span class="sxs-lookup"><span data-stu-id="6d7d9-104">The `GetSampleSize` method retrieves the sample size.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d7d9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6d7d9-105">Syntax</span></span>


```C++
ULONG GetSampleSize() const;
```



## <a name="parameters"></a><span data-ttu-id="6d7d9-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6d7d9-106">Parameters</span></span>

<span data-ttu-id="6d7d9-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="6d7d9-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6d7d9-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6d7d9-108">Return value</span></span>

<span data-ttu-id="6d7d9-109">Si la taille de l’échantillon est fixe, retourne la taille de l’échantillon en octets.</span><span class="sxs-lookup"><span data-stu-id="6d7d9-109">If the sample size is fixed, returns the sample size in bytes.</span></span> <span data-ttu-id="6d7d9-110">Sinon, retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="6d7d9-110">Otherwise, returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d7d9-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6d7d9-111">Requirements</span></span>



| <span data-ttu-id="6d7d9-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6d7d9-112">Requirement</span></span> | <span data-ttu-id="6d7d9-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="6d7d9-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d7d9-114">En-tête</span><span class="sxs-lookup"><span data-stu-id="6d7d9-114">Header</span></span><br/>  | <dl> <span data-ttu-id="6d7d9-115"><dt>Mtype. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6d7d9-115"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="6d7d9-116">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6d7d9-116">Library</span></span><br/> | <dl> <span data-ttu-id="6d7d9-117"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="6d7d9-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d7d9-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6d7d9-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d7d9-119">**CMediaType, classe**</span><span class="sxs-lookup"><span data-stu-id="6d7d9-119">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




