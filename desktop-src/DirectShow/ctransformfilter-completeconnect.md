---
description: La méthode CompleteConnect termine une connexion de code confidentiel.
ms.assetid: b687d2ee-4aee-4fae-bc2f-23ee037d0e6d
title: Méthode CTransformFilter. CompleteConnect (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 630950cf9b05c08412394bf9270f2369b3f3b94b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525296"
---
# <a name="ctransformfiltercompleteconnect-method"></a><span data-ttu-id="a953e-103">Méthode CTransformFilter. CompleteConnect</span><span class="sxs-lookup"><span data-stu-id="a953e-103">CTransformFilter.CompleteConnect method</span></span>

<span data-ttu-id="a953e-104">La `CompleteConnect` méthode termine une connexion de code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="a953e-104">The `CompleteConnect` method completes a pin connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="a953e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a953e-105">Syntax</span></span>


```C++
virtual HRESULT CompleteConnect(
   PIN_DIRECTION direction,
   IPin          *pReceivePin
);
```



## <a name="parameters"></a><span data-ttu-id="a953e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a953e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a953e-107">*direction*</span><span class="sxs-lookup"><span data-stu-id="a953e-107">*direction*</span></span> 
</dt> <dd>

<span data-ttu-id="a953e-108">Membre du type énuméré dans la [**\_ direction du code confidentiel**](/windows/win32/api/strmif/ne-strmif-pin_direction) , en spécifiant quelle broche du filtre effectue la connexion.</span><span class="sxs-lookup"><span data-stu-id="a953e-108">Member of the [**PIN\_DIRECTION**](/windows/win32/api/strmif/ne-strmif-pin_direction) enumerated type, specifying which pin on the filter is making the connection.</span></span>

</dd> <dt>

<span data-ttu-id="a953e-109">*pReceivePin*</span><span class="sxs-lookup"><span data-stu-id="a953e-109">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="a953e-110">Pointeur vers l’interface [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin) de l’autre code confidentiel dans cette tentative de connexion.</span><span class="sxs-lookup"><span data-stu-id="a953e-110">Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface of the other pin in this connection attempt.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a953e-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a953e-111">Return value</span></span>

<span data-ttu-id="a953e-112">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a953e-112">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="a953e-113">Notes</span><span class="sxs-lookup"><span data-stu-id="a953e-113">Remarks</span></span>

<span data-ttu-id="a953e-114">Les méthodes [**CTransformInputPin :: CompleteConnect**](ctransforminputpin-completeconnect.md) et [**CTransformOutputPin :: CompleteConnect**](ctransformoutputpin-completeconnect.md) appellent cette méthode pendant le processus de connexion du code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="a953e-114">The [**CTransformInputPin::CompleteConnect**](ctransforminputpin-completeconnect.md) and [**CTransformOutputPin::CompleteConnect**](ctransformoutputpin-completeconnect.md) methods call this method during the pin connection process.</span></span> <span data-ttu-id="a953e-115">Cette méthode n’a aucun effet dans la classe de base, mais la classe dérivée peut la substituer.</span><span class="sxs-lookup"><span data-stu-id="a953e-115">This method does nothing in the base class, but the derived class can override it.</span></span>

## <a name="requirements"></a><span data-ttu-id="a953e-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a953e-116">Requirements</span></span>



| <span data-ttu-id="a953e-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a953e-117">Requirement</span></span> | <span data-ttu-id="a953e-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="a953e-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a953e-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="a953e-119">Header</span></span><br/>  | <dl> <span data-ttu-id="a953e-120"><dt>Transfrm. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a953e-120"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="a953e-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a953e-121">Library</span></span><br/> | <dl> <span data-ttu-id="a953e-122"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="a953e-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a953e-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a953e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a953e-124">**CTransformFilter, classe**</span><span class="sxs-lookup"><span data-stu-id="a953e-124">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




