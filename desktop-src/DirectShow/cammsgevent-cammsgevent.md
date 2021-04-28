---
description: Méthode constructeur CAMMsgEvent. CAMMsgEvent.
ms.assetid: 7871a624-70c0-4f21-b62a-2c4c2eaa762b
title: Constructeur CAMMsgEvent. CAMMsgEvent (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMMsgEvent.CAMMsgEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dac72ecb97a1ea1fd2594af9c11b8a03078cf2cb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096533"
---
# <a name="cammsgeventcammsgevent-constructor"></a><span data-ttu-id="c6c20-103">Constructeur CAMMsgEvent. CAMMsgEvent</span><span class="sxs-lookup"><span data-stu-id="c6c20-103">CAMMsgEvent.CAMMsgEvent constructor</span></span>

<span data-ttu-id="c6c20-104">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="c6c20-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6c20-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c6c20-105">Syntax</span></span>


```C++
CAMMsgEvent(
   HRESULT *phr
);
```



## <a name="parameters"></a><span data-ttu-id="c6c20-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c6c20-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6c20-107">*phr*</span><span class="sxs-lookup"><span data-stu-id="c6c20-107">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="c6c20-108">Pointeur vers une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c6c20-108">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="c6c20-109">Si le constructeur échoue, ce paramètre reçoit un code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="c6c20-109">If the constructor fails, this parameter receives an error code.</span></span> <span data-ttu-id="c6c20-110">Si cela se produit, l’état de l’objet n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="c6c20-110">If this occurs, the object is not in a valid state.</span></span>

<span data-ttu-id="c6c20-111">Pour la compatibilité descendante avec les versions antérieures de strmbase. lib, la valeur par défaut de ce paramètre est **null**.</span><span class="sxs-lookup"><span data-stu-id="c6c20-111">For backward compatibility with earlier versions of strmbase.lib, this parameter defaults to **NULL**.</span></span> <span data-ttu-id="c6c20-112">Toutefois, le passage d’une valeur non **null** est préférable, afin que l’appelant puisse vérifier l’état de l’objet.</span><span class="sxs-lookup"><span data-stu-id="c6c20-112">However, passing a non-**NULL** value is preferred, so that the caller can check the status of the object.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c6c20-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c6c20-113">Requirements</span></span>



| <span data-ttu-id="c6c20-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c6c20-114">Requirement</span></span> | <span data-ttu-id="c6c20-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="c6c20-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6c20-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="c6c20-116">Header</span></span><br/>  | <dl> <span data-ttu-id="c6c20-117"><dt>Wxutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c6c20-117"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="c6c20-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c6c20-118">Library</span></span><br/> | <dl> <span data-ttu-id="c6c20-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="c6c20-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6c20-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c6c20-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6c20-121">**CAMMsgEvent, classe**</span><span class="sxs-lookup"><span data-stu-id="c6c20-121">**CAMMsgEvent Class**</span></span>](cammsgevent.md)
</dt> </dl>

 

 




