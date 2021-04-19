---
description: La méthode BreakConnect libère un code confidentiel d’une connexion.
ms.assetid: cc384786-9cba-4f68-9c60-740205b35661
title: Méthode CTransformFilter. BreakConnect (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.BreakConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: aec60322a4782d84e84dc2030b69f6c385783e98
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539585"
---
# <a name="ctransformfilterbreakconnect-method"></a><span data-ttu-id="02cac-103">Méthode CTransformFilter. BreakConnect</span><span class="sxs-lookup"><span data-stu-id="02cac-103">CTransformFilter.BreakConnect method</span></span>

<span data-ttu-id="02cac-104">La `BreakConnect` méthode libère un code confidentiel d’une connexion.</span><span class="sxs-lookup"><span data-stu-id="02cac-104">The `BreakConnect` method releases a pin from a connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="02cac-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="02cac-105">Syntax</span></span>


```C++
virtual HRESULT BreakConnect(
   PIN_DIRECTION dir
);
```



## <a name="parameters"></a><span data-ttu-id="02cac-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="02cac-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02cac-107">*dir*</span><span class="sxs-lookup"><span data-stu-id="02cac-107">*dir*</span></span> 
</dt> <dd>

<span data-ttu-id="02cac-108">Membre du type énuméré de [**\_ direction du code confidentiel**](/windows/win32/api/strmif/ne-strmif-pin_direction) , spécifiant la connexion de code confidentiel qui a été rompue (entrée ou sortie).</span><span class="sxs-lookup"><span data-stu-id="02cac-108">Member of the [**PIN\_DIRECTION**](/windows/win32/api/strmif/ne-strmif-pin_direction) enumerated type, specifying which pin connection was broken (input or output).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02cac-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="02cac-109">Return value</span></span>

<span data-ttu-id="02cac-110">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="02cac-110">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="02cac-111">Notes</span><span class="sxs-lookup"><span data-stu-id="02cac-111">Remarks</span></span>

<span data-ttu-id="02cac-112">Les méthodes [**CTransformInputPin :: BreakConnect**](ctransforminputpin-breakconnect.md) et [**CTransformOutputPin :: BreakConnect**](ctransformoutputpin-breakconnect.md) appellent cette méthode lorsqu’une connexion de code confidentiel est interrompue.</span><span class="sxs-lookup"><span data-stu-id="02cac-112">The [**CTransformInputPin::BreakConnect**](ctransforminputpin-breakconnect.md) and [**CTransformOutputPin::BreakConnect**](ctransformoutputpin-breakconnect.md) methods call this method when a pin connection is broken.</span></span> <span data-ttu-id="02cac-113">Cette méthode n’a aucun effet dans la classe de base.</span><span class="sxs-lookup"><span data-stu-id="02cac-113">This method does nothing in the base class.</span></span> <span data-ttu-id="02cac-114">Si vous substituez la méthode [**CheckConnect**](ctransformfilter-checkconnect.md) , substituez cette méthode pour libérer toutes les ressources obtenues dans la méthode **CheckConnect** , y compris les pointeurs d’interface.</span><span class="sxs-lookup"><span data-stu-id="02cac-114">If you override the [**CheckConnect**](ctransformfilter-checkconnect.md) method, override this method to release any resources obtained in the **CheckConnect** method, including interface pointers.</span></span>

## <a name="requirements"></a><span data-ttu-id="02cac-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="02cac-115">Requirements</span></span>



| <span data-ttu-id="02cac-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="02cac-116">Requirement</span></span> | <span data-ttu-id="02cac-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="02cac-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02cac-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="02cac-118">Header</span></span><br/>  | <dl> <span data-ttu-id="02cac-119"><dt>Transfrm. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="02cac-119"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="02cac-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="02cac-120">Library</span></span><br/> | <dl> <span data-ttu-id="02cac-121"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="02cac-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02cac-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="02cac-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02cac-123">**CTransformFilter, classe**</span><span class="sxs-lookup"><span data-stu-id="02cac-123">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




