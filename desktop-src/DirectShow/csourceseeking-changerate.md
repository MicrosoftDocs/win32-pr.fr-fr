---
description: La méthode ChangeRate est appelée lorsque la vitesse de lecture change.
ms.assetid: c4f1f9d0-6c09-4cab-8a37-dd1ff3f5619f
title: Méthode CSourceSeeking. ChangeRate (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.ChangeRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 02fab05d65929233b97f7d53e497bae6593c472a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528670"
---
# <a name="csourceseekingchangerate-method"></a><span data-ttu-id="c4286-103">Méthode CSourceSeeking. ChangeRate</span><span class="sxs-lookup"><span data-stu-id="c4286-103">CSourceSeeking.ChangeRate method</span></span>

<span data-ttu-id="c4286-104">La `ChangeRate` méthode est appelée lorsque la vitesse de lecture change.</span><span class="sxs-lookup"><span data-stu-id="c4286-104">The `ChangeRate` method is called when the playback rate changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4286-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c4286-105">Syntax</span></span>


```C++
virtual HRESULT ChangeRate() = 0;
```



## <a name="parameters"></a><span data-ttu-id="c4286-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c4286-106">Parameters</span></span>

<span data-ttu-id="c4286-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="c4286-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c4286-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c4286-108">Return value</span></span>

<span data-ttu-id="c4286-109">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c4286-109">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c4286-110">Notes</span><span class="sxs-lookup"><span data-stu-id="c4286-110">Remarks</span></span>

<span data-ttu-id="c4286-111">La méthode [**CSourceSeeking ::**](csourceseeking-setrate.md) se, appelle cette méthode, que la classe dérivée doit implémenter.</span><span class="sxs-lookup"><span data-stu-id="c4286-111">The [**CSourceSeeking::SetRate**](csourceseeking-setrate.md) method calls this method, which the derived class must implement.</span></span> <span data-ttu-id="c4286-112">La méthode sesente met à **jour la variable** membre [**CSourceSeeking :: m \_ dRateSeeking**](csourceseeking-m-drateseeking.md) , mais ne valide pas la nouvelle valeur.</span><span class="sxs-lookup"><span data-stu-id="c4286-112">The **SetRate** method updates the [**CSourceSeeking::m\_dRateSeeking**](csourceseeking-m-drateseeking.md) member variable, but does not validate the new value.</span></span> <span data-ttu-id="c4286-113">Un taux de zéro doit toujours être rejeté.</span><span class="sxs-lookup"><span data-stu-id="c4286-113">A rate of zero should always be rejected.</span></span> <span data-ttu-id="c4286-114">Les taux inférieurs à zéro indiquent une lecture négative.</span><span class="sxs-lookup"><span data-stu-id="c4286-114">Rates less than zero indicate negative playback.</span></span> <span data-ttu-id="c4286-115">La plupart des filtres ne prennent pas en charge les taux négatifs.</span><span class="sxs-lookup"><span data-stu-id="c4286-115">Most filters do not support negative rates.</span></span>

<span data-ttu-id="c4286-116">L’exemple suivant illustre une implémentation possible :</span><span class="sxs-lookup"><span data-stu-id="c4286-116">The following example shows a possible implementation:</span></span>


```C++
HRESULT CMyStream::ChangeRate( )
{
    {   // Scope for critical section lock.
        CAutoLock cAutoLockSeeking(CSourceSeeking::m_pLock);
        if( m_dRateSeeking <= 0 ) {
            m_dRateSeeking = 1.0;  // Reset to a reasonable value.
            return E_FAIL;
        }
    }
    UpdateFromSeek();
    return S_OK;
}
```



## <a name="requirements"></a><span data-ttu-id="c4286-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c4286-117">Requirements</span></span>



| <span data-ttu-id="c4286-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c4286-118">Requirement</span></span> | <span data-ttu-id="c4286-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="c4286-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4286-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="c4286-120">Header</span></span><br/>  | <dl> <span data-ttu-id="c4286-121"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c4286-121"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c4286-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c4286-122">Library</span></span><br/> | <dl> <span data-ttu-id="c4286-123"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="c4286-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4286-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c4286-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4286-125">**CSourceSeeking, classe**</span><span class="sxs-lookup"><span data-stu-id="c4286-125">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




