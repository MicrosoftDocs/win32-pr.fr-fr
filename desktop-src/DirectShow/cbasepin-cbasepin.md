---
description: Méthode de constructeur.
ms.assetid: e8cb5f1d-171f-4bf8-8ab6-6e547c4678d2
title: Constructeur CBasePin. CBasePin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CBasePin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dd4883d3d8e906e1da2f377344b735037c5e5cd3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541737"
---
# <a name="cbasepincbasepin-constructor"></a><span data-ttu-id="22a97-103">Constructeur CBasePin. CBasePin</span><span class="sxs-lookup"><span data-stu-id="22a97-103">CBasePin.CBasePin constructor</span></span>

<span data-ttu-id="22a97-104">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="22a97-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="22a97-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="22a97-105">Syntax</span></span>


```C++
CBasePin(
   TCHAR         *pObjectName,
   CBaseFilter   *pFilter,
   CCritSec      *pLock,
   HRESULT       *phr,
   LPCWSTR       pName,
   PIN_DIRECTION dir
);
```



## <a name="parameters"></a><span data-ttu-id="22a97-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="22a97-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22a97-107">*pObjectName*</span><span class="sxs-lookup"><span data-stu-id="22a97-107">*pObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="22a97-108">Chaîne contenant le nom de débogage de l’objet.</span><span class="sxs-lookup"><span data-stu-id="22a97-108">String containing the debug name for the object.</span></span> <span data-ttu-id="22a97-109">Pour plus d’informations, consultez [**CBaseObject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="22a97-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="22a97-110">*pFilter*</span><span class="sxs-lookup"><span data-stu-id="22a97-110">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="22a97-111">Pointeur vers le filtre qui a créé ce code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="22a97-111">Pointer to the filter that created this pin.</span></span>

</dd> <dt>

<span data-ttu-id="22a97-112">*pLock*</span><span class="sxs-lookup"><span data-stu-id="22a97-112">*pLock*</span></span> 
</dt> <dd>

<span data-ttu-id="22a97-113">Pointeur vers un verrou [**CCritSec**](ccritsec.md) , utilisé pour sérialiser les modifications d’État.</span><span class="sxs-lookup"><span data-stu-id="22a97-113">Pointer to a [**CCritSec**](ccritsec.md) lock, used to serialize state changes.</span></span> <span data-ttu-id="22a97-114">Il peut s’agir de la même section critique que le verrou de filtre, [**CBaseFilter :: m \_ pLock**](cbasefilter-m-plock.md).</span><span class="sxs-lookup"><span data-stu-id="22a97-114">Can be the same critical section as the filter lock, [**CBaseFilter::m\_pLock**](cbasefilter-m-plock.md).</span></span>

</dd> <dt>

<span data-ttu-id="22a97-115">*phr*</span><span class="sxs-lookup"><span data-stu-id="22a97-115">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="22a97-116">Pointeur vers une variable qui reçoit une valeur **HRESULT** indiquant la réussite ou l’échec de la méthode.</span><span class="sxs-lookup"><span data-stu-id="22a97-116">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span> <span data-ttu-id="22a97-117">Initialisez la valeur sur \_ OK avant de créer l’objet.</span><span class="sxs-lookup"><span data-stu-id="22a97-117">Initialize the value to S\_OK before creating the object.</span></span> <span data-ttu-id="22a97-118">La valeur est modifiée uniquement si une erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="22a97-118">The value is changed only if an error occurs.</span></span>

</dd> <dt>

<span data-ttu-id="22a97-119">*pName*</span><span class="sxs-lookup"><span data-stu-id="22a97-119">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="22a97-120">Chaîne de caractères larges contenant le nom du code PIN.</span><span class="sxs-lookup"><span data-stu-id="22a97-120">Wide-character string containing the name of the pin.</span></span> <span data-ttu-id="22a97-121">Pour plus d’informations, consultez [**CBasePin :: QueryPinInfo**](cbasepin-querypininfo.md).</span><span class="sxs-lookup"><span data-stu-id="22a97-121">For more information, see [**CBasePin::QueryPinInfo**](cbasepin-querypininfo.md).</span></span>

</dd> <dt>

<span data-ttu-id="22a97-122">*dir*</span><span class="sxs-lookup"><span data-stu-id="22a97-122">*dir*</span></span> 
</dt> <dd>

<span data-ttu-id="22a97-123">Membre de l’énumération de [**\_ direction du code confidentiel**](/windows/win32/api/strmif/ne-strmif-pin_direction) spécifiant la direction du code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="22a97-123">Member of the [**PIN\_DIRECTION**](/windows/win32/api/strmif/ne-strmif-pin_direction) enumeration specifying the direction of the pin.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="22a97-124">Notes</span><span class="sxs-lookup"><span data-stu-id="22a97-124">Remarks</span></span>

<span data-ttu-id="22a97-125">La section critique spécifiée par *pLock* sérialise l’état du pin, y compris son état de connexion, le choix de l’allocateur, le type de média et l’état des opérations de vidage.</span><span class="sxs-lookup"><span data-stu-id="22a97-125">The critical section specified by *pLock* serializes the pin's state, including its connection status, choice of allocator, media type, and the status of flush operations.</span></span> <span data-ttu-id="22a97-126">N’utilisez pas cette section critique pour sérialiser les opérations de diffusion en continu.</span><span class="sxs-lookup"><span data-stu-id="22a97-126">Do not use this critical section to serialize streaming operations.</span></span> <span data-ttu-id="22a97-127">Pour plus d’informations, consultez [Data Flow dans le graphique de filtre](data-flow-in-the-filter-graph.md).</span><span class="sxs-lookup"><span data-stu-id="22a97-127">For more information, see [Data Flow in the Filter Graph](data-flow-in-the-filter-graph.md).</span></span>

<span data-ttu-id="22a97-128">Un filtre peut créer des codes confidentiels dans sa méthode de constructeur, donc à ce stade, le pointeur *pFilter* peut ne pas faire référence à un objet valide.</span><span class="sxs-lookup"><span data-stu-id="22a97-128">A filter might create pins in its constructor method, so at this point the *pFilter* pointer might not refer to a valid object.</span></span> <span data-ttu-id="22a97-129">Stockez le pointeur, mais ne le déréférencez pas dans le constructeur du pin.</span><span class="sxs-lookup"><span data-stu-id="22a97-129">Store the pointer, but do not dereference it while inside the pin's constructor.</span></span>

## <a name="requirements"></a><span data-ttu-id="22a97-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="22a97-130">Requirements</span></span>



| <span data-ttu-id="22a97-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="22a97-131">Requirement</span></span> | <span data-ttu-id="22a97-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="22a97-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22a97-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="22a97-133">Header</span></span><br/>  | <dl> <span data-ttu-id="22a97-134"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="22a97-134"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="22a97-135">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="22a97-135">Library</span></span><br/> | <dl> <span data-ttu-id="22a97-136"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="22a97-136"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22a97-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="22a97-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22a97-138">**CBasePin, classe**</span><span class="sxs-lookup"><span data-stu-id="22a97-138">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




