---
description: La méthode InitMediaType Initialise le type de média.
ms.assetid: 141ced68-11ed-4567-b2e1-82c040d3b4a4
title: CMediaType.Iniméthode tMediaType (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.InitMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c3bbe170c6d896f3b28d9b85cf49f18269341d50
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543578"
---
# <a name="cmediatypeinitmediatype-method"></a><span data-ttu-id="be9ec-103">CMediaType.Iniméthode tMediaType</span><span class="sxs-lookup"><span data-stu-id="be9ec-103">CMediaType.InitMediaType method</span></span>

<span data-ttu-id="be9ec-104">La `InitMediaType` méthode initialise le type de média.</span><span class="sxs-lookup"><span data-stu-id="be9ec-104">The `InitMediaType` method initializes the media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="be9ec-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="be9ec-105">Syntax</span></span>


```C++
void InitMediaType();
```



## <a name="parameters"></a><span data-ttu-id="be9ec-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="be9ec-106">Parameters</span></span>

<span data-ttu-id="be9ec-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="be9ec-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="be9ec-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="be9ec-108">Return value</span></span>

<span data-ttu-id="be9ec-109">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="be9ec-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="be9ec-110">Notes</span><span class="sxs-lookup"><span data-stu-id="be9ec-110">Remarks</span></span>

<span data-ttu-id="be9ec-111">Cette méthode met à zéro la mémoire de l’objet, affecte la **valeur true** à la propriété Fixed-Sample-size et définit la taille de l’échantillon sur 1.</span><span class="sxs-lookup"><span data-stu-id="be9ec-111">This method zeroes the object's memory, sets the fixed-sample-size property to **TRUE**, and sets the sample size to 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="be9ec-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="be9ec-112">Requirements</span></span>



| <span data-ttu-id="be9ec-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="be9ec-113">Requirement</span></span> | <span data-ttu-id="be9ec-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="be9ec-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be9ec-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="be9ec-115">Header</span></span><br/>  | <dl> <span data-ttu-id="be9ec-116"><dt>Mtype. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="be9ec-116"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="be9ec-117">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="be9ec-117">Library</span></span><br/> | <dl> <span data-ttu-id="be9ec-118"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="be9ec-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be9ec-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="be9ec-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be9ec-120">**CMediaType, classe**</span><span class="sxs-lookup"><span data-stu-id="be9ec-120">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




