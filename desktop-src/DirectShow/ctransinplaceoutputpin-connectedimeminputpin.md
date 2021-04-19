---
description: 'La méthode ConnectedIMemInputPin récupère un pointeur vers la broche d’entrée en aval. Cette méthode retourne la variable de membre CBaseOutputPin :: m \_ pInputPin.'
ms.assetid: 39a12603-7768-43c3-9558-7caaa8f55108
title: Méthode CTransInPlaceOutputPin. ConnectedIMemInputPin (Transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceOutputPin.ConnectedIMemInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 83f92472e67e1d37a51cd2526b8be65ea9bdbc6d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540224"
---
# <a name="ctransinplaceoutputpinconnectedimeminputpin-method"></a><span data-ttu-id="7fb6a-104">Méthode CTransInPlaceOutputPin. ConnectedIMemInputPin</span><span class="sxs-lookup"><span data-stu-id="7fb6a-104">CTransInPlaceOutputPin.ConnectedIMemInputPin method</span></span>

<span data-ttu-id="7fb6a-105">La `ConnectedIMemInputPin` méthode récupère un pointeur vers la broche d’entrée en aval.</span><span class="sxs-lookup"><span data-stu-id="7fb6a-105">The `ConnectedIMemInputPin` method retrieves a pointer to the downstream input pin.</span></span> <span data-ttu-id="7fb6a-106">Cette méthode retourne la variable de membre [**CBaseOutputPin :: m \_ pInputPin**](cbaseoutputpin-m-pinputpin.md) .</span><span class="sxs-lookup"><span data-stu-id="7fb6a-106">This method returns the [**CBaseOutputPin::m\_pInputPin**](cbaseoutputpin-m-pinputpin.md) member variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="7fb6a-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7fb6a-107">Syntax</span></span>


```C++
IMemInputPin* ConnectedIMemInputPin();
```



## <a name="parameters"></a><span data-ttu-id="7fb6a-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7fb6a-108">Parameters</span></span>

<span data-ttu-id="7fb6a-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="7fb6a-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7fb6a-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7fb6a-110">Return value</span></span>

<span data-ttu-id="7fb6a-111">Retourne un pointeur vers l’interface [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) sur la broche d’entrée en aval.</span><span class="sxs-lookup"><span data-stu-id="7fb6a-111">Returns a pointer to the [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface on the downstream input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="7fb6a-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7fb6a-112">Requirements</span></span>



| <span data-ttu-id="7fb6a-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7fb6a-113">Requirement</span></span> | <span data-ttu-id="7fb6a-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="7fb6a-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7fb6a-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="7fb6a-115">Header</span></span><br/>  | <dl> <span data-ttu-id="7fb6a-116"><dt>Transip. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7fb6a-116"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7fb6a-117">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7fb6a-117">Library</span></span><br/> | <dl> <span data-ttu-id="7fb6a-118"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="7fb6a-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7fb6a-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7fb6a-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fb6a-120">**CTransInPlaceOutputPin, classe**</span><span class="sxs-lookup"><span data-stu-id="7fb6a-120">**CTransInPlaceOutputPin Class**</span></span>](ctransinplaceoutputpin.md)
</dt> </dl>

 

 




