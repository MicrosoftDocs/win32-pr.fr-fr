---
description: Méthode de destructeur. Le destructeur déverrouille l’objet de section critique.
ms.assetid: 1148613e-03de-4c40-b7e5-cf5e9ca80f27
title: CAutoLock. ~ CAutoLock, destructeur (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAutoLock.~CAutoLock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4bace2c4a7c79755249e78fbecd0238e6f5961bd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106534844"
---
# <a name="cautolockcautolock-destructor"></a><span data-ttu-id="5308d-104">CAutoLock. ~ CAutoLock, destructeur</span><span class="sxs-lookup"><span data-stu-id="5308d-104">CAutoLock.~CAutoLock destructor</span></span>

<span data-ttu-id="5308d-105">Méthode de destructeur.</span><span class="sxs-lookup"><span data-stu-id="5308d-105">Destructor method.</span></span> <span data-ttu-id="5308d-106">Le destructeur déverrouille l’objet de section critique.</span><span class="sxs-lookup"><span data-stu-id="5308d-106">The destructor unlocks the critical section object.</span></span>

## <a name="syntax"></a><span data-ttu-id="5308d-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5308d-107">Syntax</span></span>


```C++
~CAutoLock();
```



## <a name="requirements"></a><span data-ttu-id="5308d-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5308d-108">Requirements</span></span>



| <span data-ttu-id="5308d-109">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5308d-109">Requirement</span></span> | <span data-ttu-id="5308d-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="5308d-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5308d-111">En-tête</span><span class="sxs-lookup"><span data-stu-id="5308d-111">Header</span></span><br/>  | <dl> <span data-ttu-id="5308d-112"><dt>Wxutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5308d-112"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="5308d-113">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5308d-113">Library</span></span><br/> | <dl> <span data-ttu-id="5308d-114"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="5308d-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5308d-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5308d-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5308d-116">**CAutoLock, classe**</span><span class="sxs-lookup"><span data-stu-id="5308d-116">**CAutoLock Class**</span></span>](cautolock.md)
</dt> </dl>

 

 




