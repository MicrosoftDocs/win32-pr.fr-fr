---
description: La méthode SetSyncSource définit l’horloge utilisée pour le minutage.
ms.assetid: 646d4d24-f9b7-438a-b842-58e90eb6a945
title: Méthode CCmdQueue. SetSyncSource (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.SetSyncSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 995df3afa5185d8f50278899ac6a5d67dc6d230e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528602"
---
# <a name="ccmdqueuesetsyncsource-method"></a><span data-ttu-id="efb04-103">Méthode CCmdQueue. SetSyncSource</span><span class="sxs-lookup"><span data-stu-id="efb04-103">CCmdQueue.SetSyncSource method</span></span>

<span data-ttu-id="efb04-104">La `SetSyncSource` méthode définit l’horloge utilisée pour le minutage.</span><span class="sxs-lookup"><span data-stu-id="efb04-104">The `SetSyncSource` method sets the clock used for timing.</span></span>

## <a name="syntax"></a><span data-ttu-id="efb04-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="efb04-105">Syntax</span></span>


```C++
virtual HRESULT SetSyncSource(
   IReferenceClock *pIrc
);
```



## <a name="parameters"></a><span data-ttu-id="efb04-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="efb04-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="efb04-107">*pIrc*</span><span class="sxs-lookup"><span data-stu-id="efb04-107">*pIrc*</span></span> 
</dt> <dd>

<span data-ttu-id="efb04-108">Pointeur vers l’interface [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) .</span><span class="sxs-lookup"><span data-stu-id="efb04-108">Pointer to the [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="efb04-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="efb04-109">Return value</span></span>

<span data-ttu-id="efb04-110">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="efb04-110">Returns S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="efb04-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="efb04-111">Requirements</span></span>



| <span data-ttu-id="efb04-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="efb04-112">Requirement</span></span> | <span data-ttu-id="efb04-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="efb04-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="efb04-114">En-tête</span><span class="sxs-lookup"><span data-stu-id="efb04-114">Header</span></span><br/>  | <dl> <span data-ttu-id="efb04-115"><dt>Winutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="efb04-115"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="efb04-116">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="efb04-116">Library</span></span><br/> | <dl> <span data-ttu-id="efb04-117"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="efb04-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="efb04-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="efb04-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efb04-119">**CCmdQueue, classe**</span><span class="sxs-lookup"><span data-stu-id="efb04-119">**CCmdQueue Class**</span></span>](ccmdqueue.md)
</dt> </dl>

 

 




