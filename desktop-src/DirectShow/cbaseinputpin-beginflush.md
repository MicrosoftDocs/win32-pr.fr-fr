---
description: 'La méthode CBaseInputPin commence une opération de vidage. Cette méthode implémente la méthode IPin :: BeginFlush.'
ms.assetid: 3f149d4f-765b-44c1-87e5-6313f6a4d50d
title: Méthode CBaseInputPin. BeginFlush (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.BeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 93c0f687daf65e91443f4f59896d641b9b0cfd43
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539270"
---
# <a name="cbaseinputpinbeginflush-method"></a><span data-ttu-id="4e56e-104">Méthode CBaseInputPin. BeginFlush</span><span class="sxs-lookup"><span data-stu-id="4e56e-104">CBaseInputPin.BeginFlush method</span></span>

<span data-ttu-id="4e56e-105">La `CBaseInputPin` méthode commence une opération de vidage.</span><span class="sxs-lookup"><span data-stu-id="4e56e-105">The `CBaseInputPin` method begins a flush operation.</span></span> <span data-ttu-id="4e56e-106">Cette méthode implémente la méthode [**IPIN :: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) .</span><span class="sxs-lookup"><span data-stu-id="4e56e-106">This method implements the [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e56e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4e56e-107">Syntax</span></span>


```C++
HRESULT BeginFlush();
```



## <a name="parameters"></a><span data-ttu-id="4e56e-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4e56e-108">Parameters</span></span>

<span data-ttu-id="4e56e-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="4e56e-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4e56e-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4e56e-110">Return value</span></span>

<span data-ttu-id="4e56e-111">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="4e56e-111">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e56e-112">Notes</span><span class="sxs-lookup"><span data-stu-id="4e56e-112">Remarks</span></span>

<span data-ttu-id="4e56e-113">Cette méthode affecte à l’indicateur [**CBaseInputPin :: m \_ BFlushing**](cbaseinputpin-m-bflushing.md) la **valeur true**, ce qui amène la méthode [**CBaseInputPin :: Receive**](cbaseinputpin-receive.md) à rejeter tout autre échantillon.</span><span class="sxs-lookup"><span data-stu-id="4e56e-113">This method sets the [**CBaseInputPin::m\_bFlushing**](cbaseinputpin-m-bflushing.md) flag to **TRUE**, which causes the [**CBaseInputPin::Receive**](cbaseinputpin-receive.md) method to reject any more samples.</span></span>

<span data-ttu-id="4e56e-114">La classe dérivée doit substituer cette méthode et effectuer les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="4e56e-114">The derived class must override this method and perform the following steps:</span></span>

1.  <span data-ttu-id="4e56e-115">Appelez la méthode [**IPIN :: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) sur les broches d’entrée en aval.</span><span class="sxs-lookup"><span data-stu-id="4e56e-115">Call the [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) method on downstream input pins.</span></span> <span data-ttu-id="4e56e-116">Si le pin n’a pas encore remis d’exemples de supports en aval, vous pouvez ignorer cette étape.</span><span class="sxs-lookup"><span data-stu-id="4e56e-116">If the pin has not yet delivered any media samples downstream, you can skip this step.</span></span> <span data-ttu-id="4e56e-117">Si vos broches de sortie dérivent de la classe [**CBaseOutputPin**](cbaseoutputpin.md) , vous pouvez appeler la méthode [**CBaseOutputPin ::D eliverbeginflush**](cbaseoutputpin-deliverbeginflush.md) .</span><span class="sxs-lookup"><span data-stu-id="4e56e-117">If your output pins derive from the [**CBaseOutputPin**](cbaseoutputpin.md) class, you can call the [**CBaseOutputPin::DeliverBeginFlush**](cbaseoutputpin-deliverbeginflush.md) method.</span></span>
2.  <span data-ttu-id="4e56e-118">Appelez la méthode de la classe de base.</span><span class="sxs-lookup"><span data-stu-id="4e56e-118">Call the base class method.</span></span>
3.  <span data-ttu-id="4e56e-119">Début de la suppression des données en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="4e56e-119">Begin discarding queued data.</span></span>
4.  <span data-ttu-id="4e56e-120">Retour de tous les appels bloqués à la méthode **Receive** .</span><span class="sxs-lookup"><span data-stu-id="4e56e-120">Return from any blocked calls to the **Receive** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e56e-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4e56e-121">Requirements</span></span>



| <span data-ttu-id="4e56e-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4e56e-122">Requirement</span></span> | <span data-ttu-id="4e56e-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="4e56e-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e56e-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="4e56e-124">Header</span></span><br/>  | <dl> <span data-ttu-id="4e56e-125"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4e56e-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="4e56e-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4e56e-126">Library</span></span><br/> | <dl> <span data-ttu-id="4e56e-127"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="4e56e-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e56e-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4e56e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e56e-129">**CBaseInputPin, classe**</span><span class="sxs-lookup"><span data-stu-id="4e56e-129">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




