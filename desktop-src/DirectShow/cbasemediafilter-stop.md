---
description: 'La méthode Stop arrête l’objet. Cette méthode implémente la méthode IMediaFilter :: Stop.'
ms.assetid: 9282d90a-932c-4ba0-84f1-1de2c125bfbd
title: CBaseMediaFilter. Stop, méthode (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.Stop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 22bb45234c8be832f8ea30ed70b50c8f4919b7e9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535869"
---
# <a name="cbasemediafilterstop-method"></a><span data-ttu-id="7124e-104">CBaseMediaFilter. Stop, méthode</span><span class="sxs-lookup"><span data-stu-id="7124e-104">CBaseMediaFilter.Stop method</span></span>

<span data-ttu-id="7124e-105">La `Stop` méthode arrête l’objet.</span><span class="sxs-lookup"><span data-stu-id="7124e-105">The `Stop` method stops the object.</span></span> <span data-ttu-id="7124e-106">Cette méthode implémente la méthode [**IMediaFilter :: Stop**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop) .</span><span class="sxs-lookup"><span data-stu-id="7124e-106">This method implements the [**IMediaFilter::Stop**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="7124e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7124e-107">Syntax</span></span>


```C++
HRESULT Stop();
```



## <a name="parameters"></a><span data-ttu-id="7124e-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7124e-108">Parameters</span></span>

<span data-ttu-id="7124e-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="7124e-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7124e-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7124e-110">Return value</span></span>

<span data-ttu-id="7124e-111">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7124e-111">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="7124e-112">Notes</span><span class="sxs-lookup"><span data-stu-id="7124e-112">Remarks</span></span>

<span data-ttu-id="7124e-113">Dans la classe de base, cette méthode affecte à la variable d' [**\_ État CBaseMediaFilter :: m**](cbasemediafilter-m-state.md) la valeur State \_ Stopped, mais ne fait rien d’autre.</span><span class="sxs-lookup"><span data-stu-id="7124e-113">In the base class, this method sets the [**CBaseMediaFilter::m\_State**](cbasemediafilter-m-state.md) member variable to State\_Stopped but does nothing else.</span></span>

## <a name="requirements"></a><span data-ttu-id="7124e-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7124e-114">Requirements</span></span>



| <span data-ttu-id="7124e-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7124e-115">Requirement</span></span> | <span data-ttu-id="7124e-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="7124e-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7124e-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="7124e-117">Header</span></span><br/>  | <dl> <span data-ttu-id="7124e-118"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7124e-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="7124e-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7124e-119">Library</span></span><br/> | <dl> <span data-ttu-id="7124e-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="7124e-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7124e-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7124e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7124e-122">**CBaseMediaFilter, classe**</span><span class="sxs-lookup"><span data-stu-id="7124e-122">**CBaseMediaFilter Class**</span></span>](cbasemediafilter.md)
</dt> </dl>

 

 




