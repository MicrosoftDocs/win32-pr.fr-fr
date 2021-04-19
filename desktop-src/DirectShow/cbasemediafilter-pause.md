---
description: Suspend l’objet. Implémente la méthode IMediaFilter ::P ause.
ms.assetid: 4f4cbe7e-3004-4731-864f-737c2f51afff
title: CBaseMediaFilter. pause, méthode (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.Pause
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a75cbcf1d629b997584cff35ebd4095094fe8607
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528011"
---
# <a name="cbasemediafilterpause-method"></a><span data-ttu-id="b7f54-104">CBaseMediaFilter. pause, méthode</span><span class="sxs-lookup"><span data-stu-id="b7f54-104">CBaseMediaFilter.Pause method</span></span>

<span data-ttu-id="b7f54-105">Suspend l’objet.</span><span class="sxs-lookup"><span data-stu-id="b7f54-105">Pauses the object.</span></span> <span data-ttu-id="b7f54-106">Implémente la méthode [**IMediaFilter ::P ause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause) .</span><span class="sxs-lookup"><span data-stu-id="b7f54-106">Implements the [**IMediaFilter::Pause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7f54-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b7f54-107">Syntax</span></span>


```C++
HRESULT Pause();
```



## <a name="parameters"></a><span data-ttu-id="b7f54-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b7f54-108">Parameters</span></span>

<span data-ttu-id="b7f54-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="b7f54-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b7f54-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b7f54-110">Return value</span></span>

<span data-ttu-id="b7f54-111">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b7f54-111">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7f54-112">Notes</span><span class="sxs-lookup"><span data-stu-id="b7f54-112">Remarks</span></span>

<span data-ttu-id="b7f54-113">Dans la classe de base, cette méthode définit la variable de membre d' [**\_ État CBaseMediaFilter :: m**](cbasemediafilter-m-state.md) sur State \_ suspendue, mais n’effectue aucune autre opération.</span><span class="sxs-lookup"><span data-stu-id="b7f54-113">In the base class, this method sets the [**CBaseMediaFilter::m\_State**](cbasemediafilter-m-state.md) member variable to State\_Paused but does nothing else.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7f54-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b7f54-114">Requirements</span></span>



| <span data-ttu-id="b7f54-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b7f54-115">Requirement</span></span> | <span data-ttu-id="b7f54-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="b7f54-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7f54-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="b7f54-117">Header</span></span><br/>  | <dl> <span data-ttu-id="b7f54-118"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b7f54-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="b7f54-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b7f54-119">Library</span></span><br/> | <dl> <span data-ttu-id="b7f54-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="b7f54-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7f54-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b7f54-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7f54-122">**CBaseMediaFilter, classe**</span><span class="sxs-lookup"><span data-stu-id="b7f54-122">**CBaseMediaFilter Class**</span></span>](cbasemediafilter.md)
</dt> </dl>

 

 




