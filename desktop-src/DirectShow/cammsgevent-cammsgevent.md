---
description: Méthode de constructeur.
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
ms.openlocfilehash: 0d207afae53a715728d8307656b0c2427ce9574c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528996"
---
# <a name="cammsgeventcammsgevent-constructor"></a><span data-ttu-id="32a54-103">Constructeur CAMMsgEvent. CAMMsgEvent</span><span class="sxs-lookup"><span data-stu-id="32a54-103">CAMMsgEvent.CAMMsgEvent constructor</span></span>

<span data-ttu-id="32a54-104">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="32a54-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="32a54-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="32a54-105">Syntax</span></span>


```C++
CAMMsgEvent(
   HRESULT *phr
);
```



## <a name="parameters"></a><span data-ttu-id="32a54-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="32a54-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32a54-107">*phr*</span><span class="sxs-lookup"><span data-stu-id="32a54-107">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="32a54-108">Pointeur vers une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="32a54-108">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="32a54-109">Si le constructeur échoue, ce paramètre reçoit un code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="32a54-109">If the constructor fails, this parameter receives an error code.</span></span> <span data-ttu-id="32a54-110">Si cela se produit, l’état de l’objet n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="32a54-110">If this occurs, the object is not in a valid state.</span></span>

<span data-ttu-id="32a54-111">Pour la compatibilité descendante avec les versions antérieures de strmbase. lib, la valeur par défaut de ce paramètre est **null**.</span><span class="sxs-lookup"><span data-stu-id="32a54-111">For backward compatibility with earlier versions of strmbase.lib, this parameter defaults to **NULL**.</span></span> <span data-ttu-id="32a54-112">Toutefois, le passage d’une valeur non **null** est préférable, afin que l’appelant puisse vérifier l’état de l’objet.</span><span class="sxs-lookup"><span data-stu-id="32a54-112">However, passing a non-**NULL** value is preferred, so that the caller can check the status of the object.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="32a54-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="32a54-113">Requirements</span></span>



| <span data-ttu-id="32a54-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="32a54-114">Requirement</span></span> | <span data-ttu-id="32a54-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="32a54-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32a54-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="32a54-116">Header</span></span><br/>  | <dl> <span data-ttu-id="32a54-117"><dt>Wxutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="32a54-117"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="32a54-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="32a54-118">Library</span></span><br/> | <dl> <span data-ttu-id="32a54-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="32a54-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32a54-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="32a54-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32a54-121">**CAMMsgEvent, classe**</span><span class="sxs-lookup"><span data-stu-id="32a54-121">**CAMMsgEvent Class**</span></span>](cammsgevent.md)
</dt> </dl>

 

 




