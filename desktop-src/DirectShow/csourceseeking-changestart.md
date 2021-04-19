---
description: La méthode modifiez l’est appelée lorsque la position de début change.
ms.assetid: d0a5497e-43e9-4d1f-9106-1f4cd8fcb372
title: Méthode CSourceSeeking. modifiez l' (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.ChangeStart
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d0a2751cf0ad1ecc6fddeeffd97b97c32b4a31b1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541526"
---
# <a name="csourceseekingchangestart-method"></a><span data-ttu-id="18780-103">Méthode CSourceSeeking. modifiez l'</span><span class="sxs-lookup"><span data-stu-id="18780-103">CSourceSeeking.ChangeStart method</span></span>

<span data-ttu-id="18780-104">La `ChangeStart` méthode est appelée lorsque la position de début change.</span><span class="sxs-lookup"><span data-stu-id="18780-104">The `ChangeStart` method is called when the start position changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="18780-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="18780-105">Syntax</span></span>


```C++
virtual HRESULT ChangeStart() = 0;
```



## <a name="parameters"></a><span data-ttu-id="18780-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="18780-106">Parameters</span></span>

<span data-ttu-id="18780-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="18780-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="18780-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="18780-108">Return value</span></span>

<span data-ttu-id="18780-109">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="18780-109">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="18780-110">Notes</span><span class="sxs-lookup"><span data-stu-id="18780-110">Remarks</span></span>

<span data-ttu-id="18780-111">La méthode [**CSourceSeeking :: SetPositions**](csourceseeking-setpositions.md) appelle cette méthode si la position de début change.</span><span class="sxs-lookup"><span data-stu-id="18780-111">The [**CSourceSeeking::SetPositions**](csourceseeking-setpositions.md) method calls this method if the start position changes.</span></span> <span data-ttu-id="18780-112">Cette méthode est virtuelle pure ; la classe dérivée doit l’implémenter.</span><span class="sxs-lookup"><span data-stu-id="18780-112">This method is pure virtual; the derived class must implement it.</span></span> <span data-ttu-id="18780-113">Après une opération de recherche, les horodatages doivent redémarrer à partir de zéro.</span><span class="sxs-lookup"><span data-stu-id="18780-113">After a seek operation, time stamps should restart from zero.</span></span> <span data-ttu-id="18780-114">Les temps de support doivent refléter la nouvelle heure de début.</span><span class="sxs-lookup"><span data-stu-id="18780-114">Media times should reflect the new start time.</span></span> <span data-ttu-id="18780-115">L’exemple suivant illustre une implémentation possible :</span><span class="sxs-lookup"><span data-stu-id="18780-115">The following example shows a possible implementation:</span></span>


```C++
HRESULT CMyStream::ChangeStart( )
{
    m_rtSampleTime = 0;          // Reset the time stamps.
    m_rtMediaTime = m_rtStart;   // Reset the media times.
    UpdateFromSeek();
    return S_OK;
}
```



## <a name="requirements"></a><span data-ttu-id="18780-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="18780-116">Requirements</span></span>



| <span data-ttu-id="18780-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="18780-117">Requirement</span></span> | <span data-ttu-id="18780-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="18780-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18780-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="18780-119">Header</span></span><br/>  | <dl> <span data-ttu-id="18780-120"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="18780-120"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="18780-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="18780-121">Library</span></span><br/> | <dl> <span data-ttu-id="18780-122"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="18780-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18780-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="18780-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18780-124">**CSourceSeeking, classe**</span><span class="sxs-lookup"><span data-stu-id="18780-124">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




