---
description: La méthode BeginFlush informe le filtre propriétaire de la vidange des filtres en aval. La classe dérivée doit implémenter cette méthode.
ms.assetid: 612f230c-7f23-42cf-b565-344fae0b6f9a
title: Méthode CPullPin. BeginFlush (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.BeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f2e4c26b99c78794449077e73040d98b5481fb91
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545488"
---
# <a name="cpullpinbeginflush-method"></a><span data-ttu-id="3cddd-104">Méthode CPullPin. BeginFlush</span><span class="sxs-lookup"><span data-stu-id="3cddd-104">CPullPin.BeginFlush method</span></span>

<span data-ttu-id="3cddd-105">La `BeginFlush` méthode informe le filtre propriétaire de la vidange des filtres en aval.</span><span class="sxs-lookup"><span data-stu-id="3cddd-105">The `BeginFlush` method informs the owning filter to flush the downstream filters.</span></span> <span data-ttu-id="3cddd-106">La classe dérivée doit implémenter cette méthode.</span><span class="sxs-lookup"><span data-stu-id="3cddd-106">The derived class must implement this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="3cddd-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3cddd-107">Syntax</span></span>


```C++
virtual HRESULT BeginFlush();
```



## <a name="parameters"></a><span data-ttu-id="3cddd-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3cddd-108">Parameters</span></span>

<span data-ttu-id="3cddd-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="3cddd-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3cddd-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3cddd-110">Return value</span></span>

<span data-ttu-id="3cddd-111">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3cddd-111">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3cddd-112">Notes</span><span class="sxs-lookup"><span data-stu-id="3cddd-112">Remarks</span></span>

<span data-ttu-id="3cddd-113">La méthode [**CPullPin :: Seek**](cpullpin-seek.md) appelle cette méthode.</span><span class="sxs-lookup"><span data-stu-id="3cddd-113">The [**CPullPin::Seek**](cpullpin-seek.md) method calls this method.</span></span> <span data-ttu-id="3cddd-114">Implémentez cette méthode pour appeler la méthode [**IPIN :: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) sur chaque broche d’entrée en aval qui reçoit les données de cet objet.</span><span class="sxs-lookup"><span data-stu-id="3cddd-114">Implement this method to call the [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) method on each downstream input pin that receives data from this object.</span></span> <span data-ttu-id="3cddd-115">Si la ou les broches de sortie de votre filtre dérivent de [**CBaseOutputPin**](cbaseoutputpin.md), appelez la méthode [**CBaseOutputPin ::D eliverbeginflush**](cbaseoutputpin-deliverbeginflush.md) .</span><span class="sxs-lookup"><span data-stu-id="3cddd-115">If your filter's output pin(s) derive from [**CBaseOutputPin**](cbaseoutputpin.md), call the [**CBaseOutputPin::DeliverBeginFlush**](cbaseoutputpin-deliverbeginflush.md) method.</span></span>

<span data-ttu-id="3cddd-116">Cette conception permet au filtre de Rechercher simplement le flux en appelant **Seek** sur l’objet **CPullPin** .</span><span class="sxs-lookup"><span data-stu-id="3cddd-116">This design enables the filter to seek the stream simply by calling **Seek** on the **CPullPin** object.</span></span>

## <a name="requirements"></a><span data-ttu-id="3cddd-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3cddd-117">Requirements</span></span>



| <span data-ttu-id="3cddd-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3cddd-118">Requirement</span></span> | <span data-ttu-id="3cddd-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="3cddd-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3cddd-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="3cddd-120">Header</span></span><br/>  | <dl> <span data-ttu-id="3cddd-121"><dt>Pullpin. h</dt></span><span class="sxs-lookup"><span data-stu-id="3cddd-121"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="3cddd-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3cddd-122">Library</span></span><br/> | <dl> <span data-ttu-id="3cddd-123"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="3cddd-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3cddd-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3cddd-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3cddd-125">**CPullPin, classe**</span><span class="sxs-lookup"><span data-stu-id="3cddd-125">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 




