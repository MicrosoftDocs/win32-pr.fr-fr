---
description: La méthode Exit signale que le thread de streaming est en cours de fermeture.
ms.assetid: 1bb59848-e405-40f9-87ec-33de8754e2dd
title: CSourceStream. Exit, méthode (source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.Exit
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1ede6cf2318fa9226b8e220ff526f411def9b0f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543809"
---
# <a name="csourcestreamexit-method"></a><span data-ttu-id="4b981-103">CSourceStream. Exit, méthode</span><span class="sxs-lookup"><span data-stu-id="4b981-103">CSourceStream.Exit method</span></span>

<span data-ttu-id="4b981-104">La `Exit` méthode signale au thread de streaming de se fermer.</span><span class="sxs-lookup"><span data-stu-id="4b981-104">The `Exit` method signals the streaming thread to exit.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b981-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4b981-105">Syntax</span></span>


```C++
HRESULT Exit();
```



## <a name="parameters"></a><span data-ttu-id="4b981-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4b981-106">Parameters</span></span>

<span data-ttu-id="4b981-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="4b981-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4b981-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4b981-108">Return value</span></span>

<span data-ttu-id="4b981-109">Retourne S \_ OK ou E \_ inattendu.</span><span class="sxs-lookup"><span data-stu-id="4b981-109">Returns S\_OK or E\_UNEXPECTED.</span></span>

## <a name="remarks"></a><span data-ttu-id="4b981-110">Notes</span><span class="sxs-lookup"><span data-stu-id="4b981-110">Remarks</span></span>

<span data-ttu-id="4b981-111">La méthode [**CSourceStream :: inactive**](csourcestream-inactive.md) appelle cette méthode.</span><span class="sxs-lookup"><span data-stu-id="4b981-111">The [**CSourceStream::Inactive**](csourcestream-inactive.md) method calls this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b981-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4b981-112">Requirements</span></span>



| <span data-ttu-id="4b981-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4b981-113">Requirement</span></span> | <span data-ttu-id="4b981-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="4b981-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b981-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="4b981-115">Header</span></span><br/>  | <dl> <span data-ttu-id="4b981-116"><dt>Source. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4b981-116"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="4b981-117">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4b981-117">Library</span></span><br/> | <dl> <span data-ttu-id="4b981-118"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="4b981-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b981-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4b981-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b981-120">**CSourceStream, classe**</span><span class="sxs-lookup"><span data-stu-id="4b981-120">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




