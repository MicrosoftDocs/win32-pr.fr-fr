---
description: La méthode SetVariableSize spécifie que les exemples n’ont pas de taille fixe.
ms.assetid: 2a207cdb-f8e6-44aa-8bf6-868267aeb42d
title: Méthode CMediaType. SetVariableSize (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetVariableSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4621a639b3bc18382bc41ae9425c4de50db920ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106529008"
---
# <a name="cmediatypesetvariablesize-method"></a><span data-ttu-id="c0699-103">Méthode CMediaType. SetVariableSize</span><span class="sxs-lookup"><span data-stu-id="c0699-103">CMediaType.SetVariableSize method</span></span>

<span data-ttu-id="c0699-104">La `SetVariableSize` méthode spécifie que les exemples n’ont pas de taille fixe.</span><span class="sxs-lookup"><span data-stu-id="c0699-104">The `SetVariableSize` method specifies that samples do not have a fixed size.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0699-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c0699-105">Syntax</span></span>


```C++
void SetVariableSize();
```



## <a name="parameters"></a><span data-ttu-id="c0699-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c0699-106">Parameters</span></span>

<span data-ttu-id="c0699-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="c0699-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c0699-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c0699-108">Return value</span></span>

<span data-ttu-id="c0699-109">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="c0699-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c0699-110">Notes</span><span class="sxs-lookup"><span data-stu-id="c0699-110">Remarks</span></span>

<span data-ttu-id="c0699-111">Cette méthode affecte la **valeur false** au membre **bFixedSizeSamples** .</span><span class="sxs-lookup"><span data-stu-id="c0699-111">This method sets the **bFixedSizeSamples** member to **FALSE**.</span></span> <span data-ttu-id="c0699-112">Les appels suivants à la méthode [**CMediaType :: GetSampleSize**](cmediatype-getsamplesize.md) retournent zéro.</span><span class="sxs-lookup"><span data-stu-id="c0699-112">Subsequent calls to the [**CMediaType::GetSampleSize**](cmediatype-getsamplesize.md) method return zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0699-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c0699-113">Requirements</span></span>



| <span data-ttu-id="c0699-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c0699-114">Requirement</span></span> | <span data-ttu-id="c0699-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="c0699-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0699-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="c0699-116">Header</span></span><br/>  | <dl> <span data-ttu-id="c0699-117"><dt>Mtype. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c0699-117"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="c0699-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c0699-118">Library</span></span><br/> | <dl> <span data-ttu-id="c0699-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="c0699-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0699-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c0699-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0699-121">**CMediaType, classe**</span><span class="sxs-lookup"><span data-stu-id="c0699-121">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




