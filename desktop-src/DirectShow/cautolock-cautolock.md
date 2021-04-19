---
description: Méthode de constructeur. Le constructeur verrouille l’objet de section critique spécifié.
ms.assetid: 5a0d74f9-bb99-4922-9a92-2e7c1863421f
title: Constructeur CAutoLock. CAutoLock (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAutoLock.CAutoLock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fed29011d4fe581ed146f64800351a3f1053d957
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528514"
---
# <a name="cautolockcautolock-constructor"></a><span data-ttu-id="08c3f-104">Constructeur CAutoLock. CAutoLock</span><span class="sxs-lookup"><span data-stu-id="08c3f-104">CAutoLock.CAutoLock constructor</span></span>

<span data-ttu-id="08c3f-105">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="08c3f-105">Constructor method.</span></span> <span data-ttu-id="08c3f-106">Le constructeur verrouille l’objet de section critique spécifié.</span><span class="sxs-lookup"><span data-stu-id="08c3f-106">The constructor locks the specified critical section object.</span></span>

## <a name="syntax"></a><span data-ttu-id="08c3f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="08c3f-107">Syntax</span></span>


```C++
CAutoLock(
   CCritSec *plock
);
```



## <a name="parameters"></a><span data-ttu-id="08c3f-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="08c3f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08c3f-109">*plock*</span><span class="sxs-lookup"><span data-stu-id="08c3f-109">*plock*</span></span> 
</dt> <dd>

<span data-ttu-id="08c3f-110">Pointeur vers un objet [**CCritSec**](ccritsec.md) , qui contient un objet de section critique.</span><span class="sxs-lookup"><span data-stu-id="08c3f-110">Pointer to a [**CCritSec**](ccritsec.md) object, which contains a critical section object.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="08c3f-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="08c3f-111">Requirements</span></span>



| <span data-ttu-id="08c3f-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="08c3f-112">Requirement</span></span> | <span data-ttu-id="08c3f-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="08c3f-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08c3f-114">En-tête</span><span class="sxs-lookup"><span data-stu-id="08c3f-114">Header</span></span><br/>  | <dl> <span data-ttu-id="08c3f-115"><dt>Wxutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="08c3f-115"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="08c3f-116">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="08c3f-116">Library</span></span><br/> | <dl> <span data-ttu-id="08c3f-117"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="08c3f-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08c3f-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="08c3f-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08c3f-119">**CAutoLock, classe**</span><span class="sxs-lookup"><span data-stu-id="08c3f-119">**CAutoLock Class**</span></span>](cautolock.md)
</dt> </dl>

 

 




