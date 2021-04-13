---
title: IReferenceClock méthode GetTime
description: La méthode GetTime récupère le temps de référence actuel.
ms.assetid: 9bf5050a-ae09-4a72-a3f2-3df8339d99b9
keywords:
- Méthode GetTime format Windows Media
- Méthode GetTime Windows Media format, interface IReferenceClock
- Interface IReferenceClock Windows Media format, GetTime, méthode
topic_type:
- apiref
api_name:
- IReferenceClock.GetTime
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c679ce0adbbc6cc7ddc014c12f1b0ace4be6b4b0
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104380977"
---
# <a name="ireferenceclockgettime-method"></a><span data-ttu-id="495af-106">IReferenceClock :: GetTime, méthode</span><span class="sxs-lookup"><span data-stu-id="495af-106">IReferenceClock::GetTime method</span></span>

<span data-ttu-id="495af-107">La méthode **getTime** récupère le temps de référence actuel.</span><span class="sxs-lookup"><span data-stu-id="495af-107">The **GetTime** method retrieves the current reference time.</span></span>

## <a name="syntax"></a><span data-ttu-id="495af-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="495af-108">Syntax</span></span>


```C++
HRESULT GetTime(
  [out] REFERENCE_TIME *pTime
);
```



## <a name="parameters"></a><span data-ttu-id="495af-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="495af-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="495af-110">*pTime* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="495af-110">*pTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="495af-111">Pointeur vers une variable qui reçoit l’heure actuelle, en unités de 100 nanosecondes.</span><span class="sxs-lookup"><span data-stu-id="495af-111">Pointer to a variable that receives the current time, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="495af-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="495af-112">Return value</span></span>

<span data-ttu-id="495af-113">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="495af-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="495af-114">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="495af-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="495af-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="495af-115">Return code</span></span>                                                                               | <span data-ttu-id="495af-116">Description</span><span class="sxs-lookup"><span data-stu-id="495af-116">Description</span></span>                                   |
|-------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="495af-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="495af-117"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="495af-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="495af-118">The method succeeded.</span></span><br/>              |
| <dl> <span data-ttu-id="495af-119"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="495af-119"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="495af-120">Le paramètre *pTime* a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="495af-120">The *pTime* parameter is **NULL**.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="495af-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="495af-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="495af-122">**Interface IReferenceClock**</span><span class="sxs-lookup"><span data-stu-id="495af-122">**IReferenceClock Interface**</span></span>](ireferenceclock.md)
</dt> </dl>

 

 





