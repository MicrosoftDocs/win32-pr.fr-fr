---
description: 'Méthode CBasePin. CompleteConnect : la méthode CompleteConnect effectue une connexion à une autre broche.'
ms.assetid: 10cbf29c-2e1a-419c-b0c0-c99f9a285810
title: Méthode CBasePin. CompleteConnect (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fee207d7a17f12cc81036fbd4f82ec49a99f4a31
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096037"
---
# <a name="cbasepincompleteconnect-method"></a><span data-ttu-id="73654-103">Méthode CBasePin. CompleteConnect</span><span class="sxs-lookup"><span data-stu-id="73654-103">CBasePin.CompleteConnect method</span></span>

<span data-ttu-id="73654-104">La `CompleteConnect` méthode termine une connexion à une autre broche.</span><span class="sxs-lookup"><span data-stu-id="73654-104">The `CompleteConnect` method completes a connection to another pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="73654-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="73654-105">Syntax</span></span>


```C++
virtual HRESULT CompleteConnect(
   IPin *pReceivePin
);
```



## <a name="parameters"></a><span data-ttu-id="73654-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="73654-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73654-107">*pReceivePin*</span><span class="sxs-lookup"><span data-stu-id="73654-107">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="73654-108">Pointeur vers l’interface [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin) de l’autre pin.</span><span class="sxs-lookup"><span data-stu-id="73654-108">Pointer to the other pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73654-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="73654-109">Return value</span></span>

<span data-ttu-id="73654-110">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="73654-110">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="73654-111">Notes </span><span class="sxs-lookup"><span data-stu-id="73654-111">Remarks</span></span>

<span data-ttu-id="73654-112">Cette méthode est appelée sur les deux codes confidentiels à la fin du processus de connexion.</span><span class="sxs-lookup"><span data-stu-id="73654-112">This method is called on both pins at the end of the connection process.</span></span> <span data-ttu-id="73654-113">Le code PIN de connexion l’appelle à partir de la méthode [**CBasePin :: Connect**](cbasepin-connect.md) , et l’épingle de réception l’appelle à partir de la méthode [**CBasePin :: ReceiveConnection**](cbasepin-receiveconnection.md) .</span><span class="sxs-lookup"><span data-stu-id="73654-113">The connecting pin calls it from within the [**CBasePin::Connect**](cbasepin-connect.md) method, and the receiving pin calls it from within the [**CBasePin::ReceiveConnection**](cbasepin-receiveconnection.md) method.</span></span>

<span data-ttu-id="73654-114">Dans la classe de base, cette méthode retourne simplement S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="73654-114">In the base class, this method simply returns S\_OK.</span></span> <span data-ttu-id="73654-115">Si une classe dérivée a des exigences pour effectuer une connexion, elle doit substituer cette méthode.</span><span class="sxs-lookup"><span data-stu-id="73654-115">If a derived class has any requirements for completing a connection, it should override this method.</span></span> <span data-ttu-id="73654-116">Par exemple, la classe [**CBaseOutputPin**](cbaseoutputpin.md) utilise cette méthode pour décider de l’allocation de mémoire.</span><span class="sxs-lookup"><span data-stu-id="73654-116">For example, the [**CBaseOutputPin**](cbaseoutputpin.md) class uses this method to decide the memory allocator.</span></span>

<span data-ttu-id="73654-117">Si cette méthode échoue, l’ensemble de la tentative de connexion échoue également et le code confidentiel se déconnecte du code confidentiel de réception.</span><span class="sxs-lookup"><span data-stu-id="73654-117">If this method fails, the overall connection attempt also fails, and the pin disconnects from the receiving pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="73654-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="73654-118">Requirements</span></span>



| <span data-ttu-id="73654-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="73654-119">Requirement</span></span> | <span data-ttu-id="73654-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="73654-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73654-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="73654-121">Header</span></span><br/>  | <dl> <span data-ttu-id="73654-122"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="73654-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="73654-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="73654-123">Library</span></span><br/> | <dl> <span data-ttu-id="73654-124"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="73654-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73654-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="73654-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73654-126">**CBasePin, classe**</span><span class="sxs-lookup"><span data-stu-id="73654-126">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




