---
description: Méthode de constructeur.
ms.assetid: facc2c9d-034a-4fed-b6fe-77a40e36c305
title: Constructeur CSystemClock. CSystemClock (Sysclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSystemClock.CSystemClock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fea99d95aa4c1b1cadefbb95384fb871374362f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537779"
---
# <a name="csystemclockcsystemclock-constructor"></a><span data-ttu-id="f9ad2-103">Constructeur CSystemClock. CSystemClock</span><span class="sxs-lookup"><span data-stu-id="f9ad2-103">CSystemClock.CSystemClock constructor</span></span>

<span data-ttu-id="f9ad2-104">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="f9ad2-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9ad2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f9ad2-105">Syntax</span></span>


```C++
CSystemClock(
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   HRESULT   *phr
);
```



## <a name="parameters"></a><span data-ttu-id="f9ad2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f9ad2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9ad2-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="f9ad2-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="f9ad2-108">Chaîne contenant le nom de débogage de l’objet.</span><span class="sxs-lookup"><span data-stu-id="f9ad2-108">String containing the debug name of the object.</span></span> <span data-ttu-id="f9ad2-109">Pour plus d’informations, consultez [**CBaseObject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="f9ad2-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="f9ad2-110">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="f9ad2-110">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="f9ad2-111">Pointeur vers le propriétaire de cet objet.</span><span class="sxs-lookup"><span data-stu-id="f9ad2-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="f9ad2-112">Si l’objet est agrégé, passer un pointeur vers l’interface **IUnknown** de l’objet d’agrégation.</span><span class="sxs-lookup"><span data-stu-id="f9ad2-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="f9ad2-113">Sinon, affectez la valeur **null** à ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="f9ad2-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="f9ad2-114">*phr*</span><span class="sxs-lookup"><span data-stu-id="f9ad2-114">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="f9ad2-115">Pointeur vers la valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f9ad2-115">Pointer to the **HRESULT** value.</span></span> <span data-ttu-id="f9ad2-116">Si une erreur se produit, la méthode retourne un code d’erreur dans ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="f9ad2-116">If an error occurs, the method returns an error code in this parameter.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f9ad2-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f9ad2-117">Requirements</span></span>



| <span data-ttu-id="f9ad2-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f9ad2-118">Requirement</span></span> | <span data-ttu-id="f9ad2-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="f9ad2-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9ad2-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="f9ad2-120">Header</span></span><br/>  | <dl> <span data-ttu-id="f9ad2-121"><dt>Sysclock. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f9ad2-121"><dt>Sysclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="f9ad2-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f9ad2-122">Library</span></span><br/> | <dl> <span data-ttu-id="f9ad2-123"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="f9ad2-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




