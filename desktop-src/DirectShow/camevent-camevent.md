---
description: Méthode de constructeur.
ms.assetid: 35c9ac07-8756-42b1-beeb-5f0e79466742
title: Constructeur CAMEvent. CAMEvent (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMEvent.CAMEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a01d9d1f592675f58d19e81b800c966dddaca1c3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528609"
---
# <a name="cameventcamevent-constructor"></a><span data-ttu-id="61ee6-103">Constructeur CAMEvent. CAMEvent</span><span class="sxs-lookup"><span data-stu-id="61ee6-103">CAMEvent.CAMEvent constructor</span></span>

<span data-ttu-id="61ee6-104">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="61ee6-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="61ee6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="61ee6-105">Syntax</span></span>


```C++
CAMEvent(
   BOOL    fManualReset,
   HRESULT *phr
);
```



## <a name="parameters"></a><span data-ttu-id="61ee6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="61ee6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61ee6-107">*fManualReset*</span><span class="sxs-lookup"><span data-stu-id="61ee6-107">*fManualReset*</span></span> 
</dt> <dd>

<span data-ttu-id="61ee6-108">Valeur booléenne qui spécifie si l’objet est un événement de réinitialisation manuelle ou un événement de réinitialisation automatique.</span><span class="sxs-lookup"><span data-stu-id="61ee6-108">Boolean value that specifies whether the object is a manual-reset event or an auto-reset event.</span></span> <span data-ttu-id="61ee6-109">Si la **valeur est true**, l’objet est un événement de réinitialisation manuelle.</span><span class="sxs-lookup"><span data-stu-id="61ee6-109">If **TRUE**, the object is a manual-reset event.</span></span> <span data-ttu-id="61ee6-110">Dans le cas contraire, il s’agit d’un événement de réinitialisation automatique.</span><span class="sxs-lookup"><span data-stu-id="61ee6-110">Otherwise, it is an auto-reset event.</span></span>

</dd> <dt>

<span data-ttu-id="61ee6-111">*phr*</span><span class="sxs-lookup"><span data-stu-id="61ee6-111">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="61ee6-112">Pointeur vers une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="61ee6-112">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="61ee6-113">Si le constructeur échoue, ce paramètre reçoit un code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="61ee6-113">If the constructor fails, this parameter receives an error code.</span></span> <span data-ttu-id="61ee6-114">Si cela se produit, l’état de l’objet n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="61ee6-114">If this occurs, the object is not in a valid state.</span></span>

<span data-ttu-id="61ee6-115">Pour la compatibilité descendante avec les versions antérieures de strmbase. lib, la valeur par défaut de ce paramètre est **null**.</span><span class="sxs-lookup"><span data-stu-id="61ee6-115">For backward compatibility with earlier versions of strmbase.lib, this parameter defaults to **NULL**.</span></span> <span data-ttu-id="61ee6-116">Toutefois, le passage d’une valeur non **null** est préférable, afin que l’appelant puisse vérifier l’état de l’objet.</span><span class="sxs-lookup"><span data-stu-id="61ee6-116">However, passing a non-**NULL** value is preferred, so that the caller can check the status of the object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="61ee6-117">Notes</span><span class="sxs-lookup"><span data-stu-id="61ee6-117">Remarks</span></span>

<span data-ttu-id="61ee6-118">L’événement commence dans un État non signalé.</span><span class="sxs-lookup"><span data-stu-id="61ee6-118">The event begins in a nonsignaled state.</span></span>

<span data-ttu-id="61ee6-119">Avec un événement de réinitialisation automatique, la méthode [**CAMEvent :: wait**](camevent-wait.md) réinitialise l’événement à l’état non signalé lorsque la méthode est retournée.</span><span class="sxs-lookup"><span data-stu-id="61ee6-119">With an auto-reset event, the [**CAMEvent::Wait**](camevent-wait.md) method resets the event to nonsignaled when the method returns.</span></span> <span data-ttu-id="61ee6-120">Avec un événement de réinitialisation manuelle, l’événement reste signalé jusqu’à ce que vous appeliez la méthode [**CAMEvent :: Reset**](camevent-reset.md) .</span><span class="sxs-lookup"><span data-stu-id="61ee6-120">With a manual-reset event, the event remains signaled until you call the [**CAMEvent::Reset**](camevent-reset.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="61ee6-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="61ee6-121">Requirements</span></span>



| <span data-ttu-id="61ee6-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="61ee6-122">Requirement</span></span> | <span data-ttu-id="61ee6-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="61ee6-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61ee6-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="61ee6-124">Header</span></span><br/>  | <dl> <span data-ttu-id="61ee6-125"><dt>Wxutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="61ee6-125"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="61ee6-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="61ee6-126">Library</span></span><br/> | <dl> <span data-ttu-id="61ee6-127"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="61ee6-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61ee6-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="61ee6-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61ee6-129">**CAMEvent, classe**</span><span class="sxs-lookup"><span data-stu-id="61ee6-129">**CAMEvent Class**</span></span>](camevent.md)
</dt> </dl>

 

 




