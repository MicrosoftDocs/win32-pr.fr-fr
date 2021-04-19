---
description: La méthode BlockOutputPin bloque le code confidentiel.
ms.assetid: 49f6b8da-a8b2-482d-b70d-2c68a1b45a10
title: Méthode CDynamicOutputPin. BlockOutputPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.BlockOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3998774550363b7d22e05ca491f1d76ba7f2ff2b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541535"
---
# <a name="cdynamicoutputpinblockoutputpin-method"></a><span data-ttu-id="50f0b-103">Méthode CDynamicOutputPin. BlockOutputPin</span><span class="sxs-lookup"><span data-stu-id="50f0b-103">CDynamicOutputPin.BlockOutputPin method</span></span>

<span data-ttu-id="50f0b-104">La `BlockOutputPin` méthode bloque le code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="50f0b-104">The `BlockOutputPin` method blocks the pin.</span></span> <span data-ttu-id="50f0b-105">Pendant que le code confidentiel est bloqué, la méthode [**CDynamicOutputPin :: StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) attend que le code confidentiel soit débloqué.</span><span class="sxs-lookup"><span data-stu-id="50f0b-105">While the pin is blocked, the [**CDynamicOutputPin::StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) method waits for the pin to become unblocked.</span></span> <span data-ttu-id="50f0b-106">L’État bloqué empêche la broche de sortie de remettre des échantillons, de modifier son format de sortie ou de se reconnecter.</span><span class="sxs-lookup"><span data-stu-id="50f0b-106">The blocked state prevents the output pin from delivering samples, changing its output format, or reconnecting itself.</span></span>

## <a name="syntax"></a><span data-ttu-id="50f0b-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="50f0b-107">Syntax</span></span>


```C++
void BlockOutputPin();
```



## <a name="parameters"></a><span data-ttu-id="50f0b-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="50f0b-108">Parameters</span></span>

<span data-ttu-id="50f0b-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="50f0b-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="50f0b-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="50f0b-110">Return value</span></span>

<span data-ttu-id="50f0b-111">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="50f0b-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="50f0b-112">Notes</span><span class="sxs-lookup"><span data-stu-id="50f0b-112">Remarks</span></span>

<span data-ttu-id="50f0b-113">Avant d’appeler cette méthode, maintenez la section critique [**CDynamicOutputPin :: m \_ BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md) .</span><span class="sxs-lookup"><span data-stu-id="50f0b-113">Before calling this method, hold the [**CDynamicOutputPin::m\_BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md) critical section.</span></span> <span data-ttu-id="50f0b-114">N’appelez pas cette méthode si un thread de streaming utilise le code confidentiel, soit pour fournir des données, soit pour modifier la connexion.</span><span class="sxs-lookup"><span data-stu-id="50f0b-114">Do not call this method if a streaming thread is using the pin, either to deliver data or to change the connection.</span></span> <span data-ttu-id="50f0b-115">Pour vérifier si un thread de diffusion en continu utilise le code confidentiel, appelez la méthode [**CDynamicOutputPin :: StreamingThreadUsingOutputPin**](cdynamicoutputpin-streamingthreadusingoutputpin.md) .</span><span class="sxs-lookup"><span data-stu-id="50f0b-115">To check whether a streaming thread is using the pin, call the [**CDynamicOutputPin::StreamingThreadUsingOutputPin**](cdynamicoutputpin-streamingthreadusingoutputpin.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="50f0b-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="50f0b-116">Requirements</span></span>



| <span data-ttu-id="50f0b-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="50f0b-117">Requirement</span></span> | <span data-ttu-id="50f0b-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="50f0b-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50f0b-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="50f0b-119">Header</span></span><br/>  | <dl> <span data-ttu-id="50f0b-120"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="50f0b-120"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="50f0b-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="50f0b-121">Library</span></span><br/> | <dl> <span data-ttu-id="50f0b-122"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="50f0b-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50f0b-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="50f0b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50f0b-124">**CDynamicOutputPin, classe**</span><span class="sxs-lookup"><span data-stu-id="50f0b-124">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




