---
description: La méthode ForceRefresh est obsolète.
ms.assetid: 9895f72b-abf8-46a8-aa75-2a30901a4c41
title: Méthode CPosPassThru. ForceRefresh (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.ForceRefresh
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1955afe069dc419b710978eecf662758916e4cb1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526330"
---
# <a name="cpospassthruforcerefresh-method"></a><span data-ttu-id="0759b-103">Méthode CPosPassThru. ForceRefresh</span><span class="sxs-lookup"><span data-stu-id="0759b-103">CPosPassThru.ForceRefresh method</span></span>

<span data-ttu-id="0759b-104">La `ForceRefresh` méthode est obsolète.</span><span class="sxs-lookup"><span data-stu-id="0759b-104">The `ForceRefresh` method is obsolete.</span></span>

## <a name="syntax"></a><span data-ttu-id="0759b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0759b-105">Syntax</span></span>


```C++
HRESULT ForceRefresh();
```



## <a name="parameters"></a><span data-ttu-id="0759b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0759b-106">Parameters</span></span>

<span data-ttu-id="0759b-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="0759b-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0759b-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0759b-108">Return value</span></span>

<span data-ttu-id="0759b-109">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0759b-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="0759b-110">Notes</span><span class="sxs-lookup"><span data-stu-id="0759b-110">Remarks</span></span>

<span data-ttu-id="0759b-111">Initialement, cette classe a été conçue pour mettre en cache les pointeurs vers les interfaces [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) et [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) du pin connecté.</span><span class="sxs-lookup"><span data-stu-id="0759b-111">Originally this class was designed to cache pointers to the connected pin's [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) and [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interfaces.</span></span> <span data-ttu-id="0759b-112">La `ForceRefresh` méthode a publié ces interfaces.</span><span class="sxs-lookup"><span data-stu-id="0759b-112">The `ForceRefresh` method released those interfaces.</span></span>

<span data-ttu-id="0759b-113">Comme c’est actuellement le cas, cette classe ne met pas en cache ces interfaces.</span><span class="sxs-lookup"><span data-stu-id="0759b-113">As currently implemented, this class does not cache those interfaces.</span></span> <span data-ttu-id="0759b-114">Pour des éléments de compatibilité, la `ForceRefresh` méthode est toujours incluse, mais retourne la valeur \_ OK sans rien faire.</span><span class="sxs-lookup"><span data-stu-id="0759b-114">For compatibility, the `ForceRefresh` method is still included, but it returns S\_OK without doing anything.</span></span>

## <a name="requirements"></a><span data-ttu-id="0759b-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0759b-115">Requirements</span></span>



| <span data-ttu-id="0759b-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0759b-116">Requirement</span></span> | <span data-ttu-id="0759b-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="0759b-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0759b-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="0759b-118">Header</span></span><br/>  | <dl> <span data-ttu-id="0759b-119"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0759b-119"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0759b-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0759b-120">Library</span></span><br/> | <dl> <span data-ttu-id="0759b-121"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="0759b-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0759b-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0759b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0759b-123">**CPosPassThru, classe**</span><span class="sxs-lookup"><span data-stu-id="0759b-123">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




