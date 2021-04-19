---
description: Nombre de threads de streaming utilisant ce code PIN.
ms.assetid: f8650a17-edab-4d69-91da-78107c3c60b9
title: 'Membre CDynamicOutputPin :: m_dwNumOutstandingOutputPinUsers (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_dwNumOutstandingOutputPinUsers
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2ba214a2c1c6d3d056147db54c936cb61b73dcfc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537696"
---
# <a name="cdynamicoutputpinm_dwnumoutstandingoutputpinusers-member"></a><span data-ttu-id="394f9-103">CDynamicOutputPin :: m \_ dwNumOutstandingOutputPinUsers, membre</span><span class="sxs-lookup"><span data-stu-id="394f9-103">CDynamicOutputPin::m\_dwNumOutstandingOutputPinUsers member</span></span>

<span data-ttu-id="394f9-104">Nombre de threads de streaming utilisant ce code PIN.</span><span class="sxs-lookup"><span data-stu-id="394f9-104">Number of streaming threads using this pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="394f9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="394f9-105">Syntax</span></span>


```C++
DWORD m_dwNumOutstandingOutputPinUsers;
```



## <a name="remarks"></a><span data-ttu-id="394f9-106">Notes</span><span class="sxs-lookup"><span data-stu-id="394f9-106">Remarks</span></span>

<span data-ttu-id="394f9-107">La méthode [**CDynamicOutputPin :: StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) incrémente cette variable, et la méthode [**CDynamicOutputPin :: StopUsingOutputPin**](cdynamicoutputpin-stopusingoutputpin.md) la décrémente.</span><span class="sxs-lookup"><span data-stu-id="394f9-107">The [**CDynamicOutputPin::StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) method increments this variable, and the [**CDynamicOutputPin::StopUsingOutputPin**](cdynamicoutputpin-stopusingoutputpin.md) method decrements it.</span></span> <span data-ttu-id="394f9-108">Lorsque la valeur est supérieure à zéro, un thread utilise ce code PIN pour diffuser des données en continu ou pour modifier le type de connexion.</span><span class="sxs-lookup"><span data-stu-id="394f9-108">When the value is greater than zero, some thread is using this pin to stream data or to change the connection type.</span></span> <span data-ttu-id="394f9-109">Le code PIN ne peut pas être bloqué tant que c’est le cas.</span><span class="sxs-lookup"><span data-stu-id="394f9-109">The pin cannot be blocked while this is the case.</span></span>

<span data-ttu-id="394f9-110">Avant d’accéder à cette variable, maintenez la section critique [**CDynamicOutputPin :: m \_ BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md) .</span><span class="sxs-lookup"><span data-stu-id="394f9-110">Before accessing this variable, hold the [**CDynamicOutputPin::m\_BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md) critical section.</span></span>

## <a name="requirements"></a><span data-ttu-id="394f9-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="394f9-111">Requirements</span></span>



| <span data-ttu-id="394f9-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="394f9-112">Requirement</span></span> | <span data-ttu-id="394f9-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="394f9-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="394f9-114">En-tête</span><span class="sxs-lookup"><span data-stu-id="394f9-114">Header</span></span><br/>  | <dl> <span data-ttu-id="394f9-115"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="394f9-115"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="394f9-116">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="394f9-116">Library</span></span><br/> | <dl> <span data-ttu-id="394f9-117"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="394f9-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="394f9-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="394f9-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="394f9-119">**CDynamicOutputPin, classe**</span><span class="sxs-lookup"><span data-stu-id="394f9-119">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> <dt>

[<span data-ttu-id="394f9-120">**CDynamicOutputPin::StreamingThreadUsingOutputPin**</span><span class="sxs-lookup"><span data-stu-id="394f9-120">**CDynamicOutputPin::StreamingThreadUsingOutputPin**</span></span>](cdynamicoutputpin-streamingthreadusingoutputpin.md)
</dt> </dl>

 

 




