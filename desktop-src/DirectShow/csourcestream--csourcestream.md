---
description: CSourceStream. ~ CSourceStream, destructeur, méthode de destructeur.
ms.assetid: 678085c2-5999-4e62-8749-99b783787cc6
title: CSourceStream. ~ CSourceStream, destructeur (source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.~CSourceStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bbf53184dadc42145758ab387d15e8b0a1bfe09d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085207"
---
# <a name="csourcestreamcsourcestream-destructor"></a><span data-ttu-id="b014d-103">CSourceStream. ~ CSourceStream, destructeur</span><span class="sxs-lookup"><span data-stu-id="b014d-103">CSourceStream.~CSourceStream destructor</span></span>

<span data-ttu-id="b014d-104">Méthode de destructeur.</span><span class="sxs-lookup"><span data-stu-id="b014d-104">Destructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b014d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b014d-105">Syntax</span></span>


```C++
~CSourceStream();
```



## <a name="remarks"></a><span data-ttu-id="b014d-106">Notes </span><span class="sxs-lookup"><span data-stu-id="b014d-106">Remarks</span></span>

<span data-ttu-id="b014d-107">Le destructeur supprime automatiquement le code confidentiel du filtre propriétaire en appelant [**CSource :: RemovePin**](csource-removepin.md).</span><span class="sxs-lookup"><span data-stu-id="b014d-107">The destructor automatically removes the pin from the owning filter, by calling [**CSource::RemovePin**](csource-removepin.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b014d-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b014d-108">Requirements</span></span>



| <span data-ttu-id="b014d-109">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b014d-109">Requirement</span></span> | <span data-ttu-id="b014d-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="b014d-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b014d-111">En-tête</span><span class="sxs-lookup"><span data-stu-id="b014d-111">Header</span></span><br/>  | <dl> <span data-ttu-id="b014d-112"><dt>Source. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b014d-112"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="b014d-113">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b014d-113">Library</span></span><br/> | <dl> <span data-ttu-id="b014d-114"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="b014d-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b014d-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b014d-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b014d-116">**CSourceStream, classe**</span><span class="sxs-lookup"><span data-stu-id="b014d-116">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




