---
description: La méthode OnError est appelée si une erreur se produit pendant la diffusion en continu. La classe dérivée doit implémenter cette méthode.
ms.assetid: 0f135cab-611c-4464-9605-360a30de7eb3
title: CPullPin. OnError, méthode (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.OnError
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2dc8bf7f307ab56609b5f90f6955a1f666854270
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541429"
---
# <a name="cpullpinonerror-method"></a><span data-ttu-id="a64c9-104">CPullPin. OnError, méthode</span><span class="sxs-lookup"><span data-stu-id="a64c9-104">CPullPin.OnError method</span></span>

<span data-ttu-id="a64c9-105">La `OnError` méthode est appelée si une erreur se produit pendant la diffusion en continu.</span><span class="sxs-lookup"><span data-stu-id="a64c9-105">The `OnError` method is called if an error occurs during streaming.</span></span> <span data-ttu-id="a64c9-106">La classe dérivée doit implémenter cette méthode.</span><span class="sxs-lookup"><span data-stu-id="a64c9-106">The derived class must implement this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a64c9-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a64c9-107">Syntax</span></span>


```C++
virtual void OnError(
   HRESULT hr
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="a64c9-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a64c9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a64c9-109">*heure(s)*</span><span class="sxs-lookup"><span data-stu-id="a64c9-109">*hr*</span></span> 
</dt> <dd>

<span data-ttu-id="a64c9-110">Spécifie la valeur **HRESULT** retournée par la méthode qui a échoué.</span><span class="sxs-lookup"><span data-stu-id="a64c9-110">Specifies the **HRESULT** value returned by the method that failed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a64c9-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a64c9-111">Return value</span></span>

<span data-ttu-id="a64c9-112">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="a64c9-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a64c9-113">Notes</span><span class="sxs-lookup"><span data-stu-id="a64c9-113">Remarks</span></span>

<span data-ttu-id="a64c9-114">L’objet appelle cette méthode chaque fois qu’une erreur se produit et arrête le thread d’extraction de données.</span><span class="sxs-lookup"><span data-stu-id="a64c9-114">The object calls this method whenever an error occurs that halts the data-pulling thread.</span></span> <span data-ttu-id="a64c9-115">Le filtre peut utiliser cette méthode pour récupérer les erreurs de diffusion en continu de manière appropriée.</span><span class="sxs-lookup"><span data-stu-id="a64c9-115">The filter can use this method to recover from streaming errors gracefully.</span></span> <span data-ttu-id="a64c9-116">Dans la plupart des cas, l’erreur est retournée à partir du filtre en amont. le filtre en amont est donc chargé de les signaler au gestionnaire de graphes de filtre.</span><span class="sxs-lookup"><span data-stu-id="a64c9-116">In most cases, the error is returned from the upstream filter, so the upstream filter is responsible for reporting it to the Filter Graph Manager.</span></span> <span data-ttu-id="a64c9-117">Si l’erreur se produit à l’intérieur de la méthode [**CPullPin :: Receive**](cpullpin-receive.md) , votre filtre doit envoyer un événement [**EC \_ ERRORABORT**](ec-errorabort.md) .</span><span class="sxs-lookup"><span data-stu-id="a64c9-117">If the error occurs inside the [**CPullPin::Receive**](cpullpin-receive.md) method, your filter should send an [**EC\_ERRORABORT**](ec-errorabort.md) event.</span></span> <span data-ttu-id="a64c9-118">(Voir [**IMediaEventSink :: Notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify).)</span><span class="sxs-lookup"><span data-stu-id="a64c9-118">(See [**IMediaEventSink::Notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify).)</span></span>

## <a name="requirements"></a><span data-ttu-id="a64c9-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a64c9-119">Requirements</span></span>



| <span data-ttu-id="a64c9-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a64c9-120">Requirement</span></span> | <span data-ttu-id="a64c9-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="a64c9-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a64c9-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="a64c9-122">Header</span></span><br/>  | <dl> <span data-ttu-id="a64c9-123"><dt>Pullpin. h</dt></span><span class="sxs-lookup"><span data-stu-id="a64c9-123"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="a64c9-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a64c9-124">Library</span></span><br/> | <dl> <span data-ttu-id="a64c9-125"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="a64c9-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a64c9-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a64c9-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a64c9-127">**CPullPin, classe**</span><span class="sxs-lookup"><span data-stu-id="a64c9-127">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 




