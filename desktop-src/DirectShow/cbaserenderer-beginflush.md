---
description: La méthode BeginFlush commence une opération de vidage.
ms.assetid: dc652394-c24e-4cea-ac28-30a1e6de205f
title: Méthode CBaseRenderer. BeginFlush (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.BeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e218e3b2d9c0cef8ce0fe052ad1b3c4b6f786858
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535273"
---
# <a name="cbaserendererbeginflush-method"></a><span data-ttu-id="10bd9-103">Méthode CBaseRenderer. BeginFlush</span><span class="sxs-lookup"><span data-stu-id="10bd9-103">CBaseRenderer.BeginFlush method</span></span>

<span data-ttu-id="10bd9-104">La `BeginFlush` méthode commence une opération de vidage.</span><span class="sxs-lookup"><span data-stu-id="10bd9-104">The `BeginFlush` method begins a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="10bd9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="10bd9-105">Syntax</span></span>


```C++
virtual HRESULT BeginFlush();
```



## <a name="parameters"></a><span data-ttu-id="10bd9-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="10bd9-106">Parameters</span></span>

<span data-ttu-id="10bd9-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="10bd9-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="10bd9-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="10bd9-108">Return value</span></span>

<span data-ttu-id="10bd9-109">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="10bd9-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="10bd9-110">Notes</span><span class="sxs-lookup"><span data-stu-id="10bd9-110">Remarks</span></span>

<span data-ttu-id="10bd9-111">La broche d’entrée du filtre appelle cette méthode lorsqu’elle reçoit un appel à la méthode [**IPIN :: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) .</span><span class="sxs-lookup"><span data-stu-id="10bd9-111">The filter's input pin calls this method when it receives a call to the [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) method.</span></span> <span data-ttu-id="10bd9-112">Le filtre libère le thread de diffusion en continu et libère les exemples qu’il détient pour le rendu.</span><span class="sxs-lookup"><span data-stu-id="10bd9-112">The filter releases the streaming thread, and releases any sample that it was holding for rendering.</span></span>

## <a name="requirements"></a><span data-ttu-id="10bd9-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="10bd9-113">Requirements</span></span>



| <span data-ttu-id="10bd9-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="10bd9-114">Requirement</span></span> | <span data-ttu-id="10bd9-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="10bd9-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10bd9-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="10bd9-116">Header</span></span><br/>  | <dl> <span data-ttu-id="10bd9-117"><dt>Renbase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="10bd9-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="10bd9-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="10bd9-118">Library</span></span><br/> | <dl> <span data-ttu-id="10bd9-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="10bd9-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10bd9-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="10bd9-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10bd9-121">**CBaseRenderer, classe**</span><span class="sxs-lookup"><span data-stu-id="10bd9-121">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




