---
description: Méthode de constructeur.
ms.assetid: f696e433-b051-4de0-80e5-f9cd31fd0f23
title: Constructeur CEnumPins. CEnumPins (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumPins.CEnumPins
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 536782de6992acfc1613d5866f13af658fba6e71
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540546"
---
# <a name="cenumpinscenumpins-constructor"></a><span data-ttu-id="5275c-103">Constructeur CEnumPins. CEnumPins</span><span class="sxs-lookup"><span data-stu-id="5275c-103">CEnumPins.CEnumPins constructor</span></span>

<span data-ttu-id="5275c-104">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="5275c-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="5275c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5275c-105">Syntax</span></span>


```C++
CEnumPins(
   CBaseFilter *pFilter,
   CEnumPins   *pEnumPins
);
```



## <a name="parameters"></a><span data-ttu-id="5275c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5275c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5275c-107">*pFilter*</span><span class="sxs-lookup"><span data-stu-id="5275c-107">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="5275c-108">Pointeur vers le filtre sur lequel énumérer les broches.</span><span class="sxs-lookup"><span data-stu-id="5275c-108">Pointer to the filter on which to enumerate the pins.</span></span>

</dd> <dt>

<span data-ttu-id="5275c-109">*pEnumPins*</span><span class="sxs-lookup"><span data-stu-id="5275c-109">*pEnumPins*</span></span> 
</dt> <dd>

<span data-ttu-id="5275c-110">Pointeur vers l’interface [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) d’un énumérateur à cloner, ou **null**.</span><span class="sxs-lookup"><span data-stu-id="5275c-110">Pointer to the [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) interface of an enumerator to clone, or **NULL**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5275c-111">Notes</span><span class="sxs-lookup"><span data-stu-id="5275c-111">Remarks</span></span>

<span data-ttu-id="5275c-112">Si *pEnumPins* a la **valeur null**, cette méthode initialise l’énumérateur au début de la séquence d’énumération.</span><span class="sxs-lookup"><span data-stu-id="5275c-112">If *pEnumPins* is **NULL**, this method initializes the enumerator to the beginning of the enumeration sequence.</span></span> <span data-ttu-id="5275c-113">Sinon, elle duplique l’état interne de l’énumérateur spécifié par *pEnumPins*.</span><span class="sxs-lookup"><span data-stu-id="5275c-113">Otherwise, it duplicates the internal state of the enumerator specified by *pEnumPins*.</span></span>

## <a name="requirements"></a><span data-ttu-id="5275c-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5275c-114">Requirements</span></span>



| <span data-ttu-id="5275c-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5275c-115">Requirement</span></span> | <span data-ttu-id="5275c-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="5275c-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5275c-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="5275c-117">Header</span></span><br/>  | <dl> <span data-ttu-id="5275c-118"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5275c-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="5275c-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5275c-119">Library</span></span><br/> | <dl> <span data-ttu-id="5275c-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="5275c-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5275c-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5275c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5275c-122">**CEnumPins, classe**</span><span class="sxs-lookup"><span data-stu-id="5275c-122">**CEnumPins Class**</span></span>](cenumpins.md)
</dt> </dl>

 

 




