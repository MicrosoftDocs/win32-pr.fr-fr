---
description: La méthode ChangeStop est appelée lorsque la position d’arrêt change.
ms.assetid: 3d4a73a4-68e6-449c-9637-62cad937c4b4
title: Méthode CSourceSeeking. ChangeStop (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.ChangeStop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: eefcc64b4692363c8caa8f39a3a0db9beb0d08b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532221"
---
# <a name="csourceseekingchangestop-method"></a><span data-ttu-id="632b8-103">Méthode CSourceSeeking. ChangeStop</span><span class="sxs-lookup"><span data-stu-id="632b8-103">CSourceSeeking.ChangeStop method</span></span>

<span data-ttu-id="632b8-104">La `ChangeStop` méthode est appelée lorsque la position d’arrêt change.</span><span class="sxs-lookup"><span data-stu-id="632b8-104">The `ChangeStop` method is called when the stop position changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="632b8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="632b8-105">Syntax</span></span>


```C++
virtual HRESULT ChangeStop() = 0;
```



## <a name="parameters"></a><span data-ttu-id="632b8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="632b8-106">Parameters</span></span>

<span data-ttu-id="632b8-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="632b8-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="632b8-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="632b8-108">Return value</span></span>

<span data-ttu-id="632b8-109">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="632b8-109">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="632b8-110">Notes</span><span class="sxs-lookup"><span data-stu-id="632b8-110">Remarks</span></span>

<span data-ttu-id="632b8-111">La méthode [**CSourceSeeking :: SetPositions**](csourceseeking-setpositions.md) appelle cette méthode si la position d’arrêt change.</span><span class="sxs-lookup"><span data-stu-id="632b8-111">The [**CSourceSeeking::SetPositions**](csourceseeking-setpositions.md) method calls this method if the stop position changes.</span></span> <span data-ttu-id="632b8-112">Cette méthode est virtuelle pure ; la classe dérivée doit l’implémenter.</span><span class="sxs-lookup"><span data-stu-id="632b8-112">This method is pure virtual; the derived class must implement it.</span></span> <span data-ttu-id="632b8-113">L’exemple suivant illustre une implémentation possible :</span><span class="sxs-lookup"><span data-stu-id="632b8-113">The following example shows a possible implementation:</span></span>


```C++
HRESULT CMyStream::ChangeStop( )
{
    UpdateFromSeek();
    return S_OK;
}
```



## <a name="requirements"></a><span data-ttu-id="632b8-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="632b8-114">Requirements</span></span>



| <span data-ttu-id="632b8-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="632b8-115">Requirement</span></span> | <span data-ttu-id="632b8-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="632b8-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="632b8-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="632b8-117">Header</span></span><br/>  | <dl> <span data-ttu-id="632b8-118"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="632b8-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="632b8-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="632b8-119">Library</span></span><br/> | <dl> <span data-ttu-id="632b8-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="632b8-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="632b8-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="632b8-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="632b8-122">**CSourceSeeking, classe**</span><span class="sxs-lookup"><span data-stu-id="632b8-122">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




