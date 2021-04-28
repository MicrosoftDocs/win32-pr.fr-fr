---
description: 'Méthode CTransformFilter. CheckConnect : la méthode CheckConnect détermine si une connexion de code confidentiel est appropriée.'
ms.assetid: 4bec4b19-3f7c-43d8-9a45-2eb2cc15a0d4
title: Méthode CTransformFilter. CheckConnect (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.CheckConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5927aac2fa58322c93a23489a22dc96a1e2a67f0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085097"
---
# <a name="ctransformfiltercheckconnect-method"></a><span data-ttu-id="a87a3-103">Méthode CTransformFilter. CheckConnect</span><span class="sxs-lookup"><span data-stu-id="a87a3-103">CTransformFilter.CheckConnect method</span></span>

<span data-ttu-id="a87a3-104">La `CheckConnect` méthode détermine si une connexion de code confidentiel est appropriée.</span><span class="sxs-lookup"><span data-stu-id="a87a3-104">The `CheckConnect` method determines whether a pin connection is suitable.</span></span>

## <a name="syntax"></a><span data-ttu-id="a87a3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a87a3-105">Syntax</span></span>


```C++
virtual HRESULT CheckConnect(
   PIN_DIRECTION dir,
   IPin          *pPin
);
```



## <a name="parameters"></a><span data-ttu-id="a87a3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a87a3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a87a3-107">*dir*</span><span class="sxs-lookup"><span data-stu-id="a87a3-107">*dir*</span></span> 
</dt> <dd>

<span data-ttu-id="a87a3-108">Membre du type énuméré dans la [**\_ direction du code confidentiel**](/windows/win32/api/strmif/ne-strmif-pin_direction) , en spécifiant quelle broche du filtre effectue la connexion.</span><span class="sxs-lookup"><span data-stu-id="a87a3-108">Member of the [**PIN\_DIRECTION**](/windows/win32/api/strmif/ne-strmif-pin_direction) enumerated type, specifying which pin on the filter is making the connection.</span></span>

</dd> <dt>

<span data-ttu-id="a87a3-109">*pPin*</span><span class="sxs-lookup"><span data-stu-id="a87a3-109">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="a87a3-110">Pointeur vers l’interface [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin) de l’autre code confidentiel dans cette tentative de connexion.</span><span class="sxs-lookup"><span data-stu-id="a87a3-110">Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface of the other pin in this connection attempt.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a87a3-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="a87a3-111">Return value</span></span>

<span data-ttu-id="a87a3-112">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a87a3-112">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="a87a3-113">Notes </span><span class="sxs-lookup"><span data-stu-id="a87a3-113">Remarks</span></span>

<span data-ttu-id="a87a3-114">Les méthodes [**CTransformInputPin :: CheckConnect**](ctransforminputpin-checkconnect.md) et [**CTransformOutputPin :: CheckConnect**](ctransformoutputpin-checkconnect.md) appellent cette méthode pendant le processus de connexion du code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="a87a3-114">The [**CTransformInputPin::CheckConnect**](ctransforminputpin-checkconnect.md) and [**CTransformOutputPin::CheckConnect**](ctransformoutputpin-checkconnect.md) methods call this method during the pin connection process.</span></span> <span data-ttu-id="a87a3-115">Cette méthode n’a aucun effet dans la classe de base.</span><span class="sxs-lookup"><span data-stu-id="a87a3-115">This method does nothing in the base class.</span></span> <span data-ttu-id="a87a3-116">La classe dérivée peut la substituer.</span><span class="sxs-lookup"><span data-stu-id="a87a3-116">The derived class can override it.</span></span> <span data-ttu-id="a87a3-117">Par exemple, la classe dérivée peut interroger l’autre code confidentiel pour une interface particulière.</span><span class="sxs-lookup"><span data-stu-id="a87a3-117">For example, the derived class might query the other pin for a particular interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="a87a3-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a87a3-118">Requirements</span></span>



| <span data-ttu-id="a87a3-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a87a3-119">Requirement</span></span> | <span data-ttu-id="a87a3-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="a87a3-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a87a3-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="a87a3-121">Header</span></span><br/>  | <dl> <span data-ttu-id="a87a3-122"><dt>Transfrm. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a87a3-122"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="a87a3-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a87a3-123">Library</span></span><br/> | <dl> <span data-ttu-id="a87a3-124"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="a87a3-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a87a3-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a87a3-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a87a3-126">**CTransformFilter, classe**</span><span class="sxs-lookup"><span data-stu-id="a87a3-126">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




