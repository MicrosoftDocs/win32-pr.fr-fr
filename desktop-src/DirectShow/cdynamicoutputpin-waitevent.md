---
description: La méthode WaitEvent attend que l’événement spécifié soit signalé.
ms.assetid: 64880f46-7b8f-4823-9d50-052e30ecf04b
title: Méthode CDynamicOutputPin. WaitEvent (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.WaitEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b27f3c387c82eaeebc119f967deaca8e7314ccd7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545570"
---
# <a name="cdynamicoutputpinwaitevent-method"></a><span data-ttu-id="b54cc-103">Méthode CDynamicOutputPin. WaitEvent</span><span class="sxs-lookup"><span data-stu-id="b54cc-103">CDynamicOutputPin.WaitEvent method</span></span>

<span data-ttu-id="b54cc-104">La `WaitEvent` méthode attend que l’événement spécifié soit signalé.</span><span class="sxs-lookup"><span data-stu-id="b54cc-104">The `WaitEvent` method waits until the specified event is signaled.</span></span>

## <a name="syntax"></a><span data-ttu-id="b54cc-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b54cc-105">Syntax</span></span>


```C++
static HRESULT WaitEvent(
   HANDLE hEvent
);
```



## <a name="parameters"></a><span data-ttu-id="b54cc-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b54cc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b54cc-107">*hEvent*</span><span class="sxs-lookup"><span data-stu-id="b54cc-107">*hEvent*</span></span> 
</dt> <dd>

<span data-ttu-id="b54cc-108">Handle vers un événement.</span><span class="sxs-lookup"><span data-stu-id="b54cc-108">Handle to an event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b54cc-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b54cc-109">Return value</span></span>

<span data-ttu-id="b54cc-110">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b54cc-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="b54cc-111">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="b54cc-111">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="b54cc-112">Code de retour</span><span class="sxs-lookup"><span data-stu-id="b54cc-112">Return code</span></span>                                                                                  | <span data-ttu-id="b54cc-113">Description</span><span class="sxs-lookup"><span data-stu-id="b54cc-113">Description</span></span>                  |
|----------------------------------------------------------------------------------------------|------------------------------|
| <dl> <span data-ttu-id="b54cc-114"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b54cc-114"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="b54cc-115">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="b54cc-115">Success.</span></span><br/>          |
| <dl> <span data-ttu-id="b54cc-116"><dt>**E \_ inattendu**</dt></span><span class="sxs-lookup"><span data-stu-id="b54cc-116"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="b54cc-117">Erreur inattendue.</span><span class="sxs-lookup"><span data-stu-id="b54cc-117">Unexpected error.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="b54cc-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b54cc-118">Requirements</span></span>



| <span data-ttu-id="b54cc-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b54cc-119">Requirement</span></span> | <span data-ttu-id="b54cc-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="b54cc-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b54cc-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="b54cc-121">Header</span></span><br/>  | <dl> <span data-ttu-id="b54cc-122"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b54cc-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="b54cc-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b54cc-123">Library</span></span><br/> | <dl> <span data-ttu-id="b54cc-124"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="b54cc-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b54cc-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b54cc-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b54cc-126">**CDynamicOutputPin, classe**</span><span class="sxs-lookup"><span data-stu-id="b54cc-126">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




