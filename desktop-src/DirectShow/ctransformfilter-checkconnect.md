---
description: La méthode CheckConnect détermine si une connexion de code confidentiel est appropriée.
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
ms.openlocfilehash: 0d41c50323bae7cb4eaca52a87d8c1b936237ccd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532548"
---
# <a name="ctransformfiltercheckconnect-method"></a><span data-ttu-id="69296-103">Méthode CTransformFilter. CheckConnect</span><span class="sxs-lookup"><span data-stu-id="69296-103">CTransformFilter.CheckConnect method</span></span>

<span data-ttu-id="69296-104">La `CheckConnect` méthode détermine si une connexion de code confidentiel est appropriée.</span><span class="sxs-lookup"><span data-stu-id="69296-104">The `CheckConnect` method determines whether a pin connection is suitable.</span></span>

## <a name="syntax"></a><span data-ttu-id="69296-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="69296-105">Syntax</span></span>


```C++
virtual HRESULT CheckConnect(
   PIN_DIRECTION dir,
   IPin          *pPin
);
```



## <a name="parameters"></a><span data-ttu-id="69296-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="69296-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69296-107">*dir*</span><span class="sxs-lookup"><span data-stu-id="69296-107">*dir*</span></span> 
</dt> <dd>

<span data-ttu-id="69296-108">Membre du type énuméré dans la [**\_ direction du code confidentiel**](/windows/win32/api/strmif/ne-strmif-pin_direction) , en spécifiant quelle broche du filtre effectue la connexion.</span><span class="sxs-lookup"><span data-stu-id="69296-108">Member of the [**PIN\_DIRECTION**](/windows/win32/api/strmif/ne-strmif-pin_direction) enumerated type, specifying which pin on the filter is making the connection.</span></span>

</dd> <dt>

<span data-ttu-id="69296-109">*pPin*</span><span class="sxs-lookup"><span data-stu-id="69296-109">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="69296-110">Pointeur vers l’interface [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin) de l’autre code confidentiel dans cette tentative de connexion.</span><span class="sxs-lookup"><span data-stu-id="69296-110">Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface of the other pin in this connection attempt.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69296-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="69296-111">Return value</span></span>

<span data-ttu-id="69296-112">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="69296-112">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="69296-113">Notes</span><span class="sxs-lookup"><span data-stu-id="69296-113">Remarks</span></span>

<span data-ttu-id="69296-114">Les méthodes [**CTransformInputPin :: CheckConnect**](ctransforminputpin-checkconnect.md) et [**CTransformOutputPin :: CheckConnect**](ctransformoutputpin-checkconnect.md) appellent cette méthode pendant le processus de connexion du code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="69296-114">The [**CTransformInputPin::CheckConnect**](ctransforminputpin-checkconnect.md) and [**CTransformOutputPin::CheckConnect**](ctransformoutputpin-checkconnect.md) methods call this method during the pin connection process.</span></span> <span data-ttu-id="69296-115">Cette méthode n’a aucun effet dans la classe de base.</span><span class="sxs-lookup"><span data-stu-id="69296-115">This method does nothing in the base class.</span></span> <span data-ttu-id="69296-116">La classe dérivée peut la substituer.</span><span class="sxs-lookup"><span data-stu-id="69296-116">The derived class can override it.</span></span> <span data-ttu-id="69296-117">Par exemple, la classe dérivée peut interroger l’autre code confidentiel pour une interface particulière.</span><span class="sxs-lookup"><span data-stu-id="69296-117">For example, the derived class might query the other pin for a particular interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="69296-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="69296-118">Requirements</span></span>



| <span data-ttu-id="69296-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="69296-119">Requirement</span></span> | <span data-ttu-id="69296-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="69296-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69296-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="69296-121">Header</span></span><br/>  | <dl> <span data-ttu-id="69296-122"><dt>Transfrm. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="69296-122"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="69296-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="69296-123">Library</span></span><br/> | <dl> <span data-ttu-id="69296-124"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="69296-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69296-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="69296-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69296-126">**CTransformFilter, classe**</span><span class="sxs-lookup"><span data-stu-id="69296-126">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




