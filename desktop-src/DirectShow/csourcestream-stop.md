---
description: La méthode Stop signale l’arrêt du thread de streaming.
ms.assetid: 79bc528a-cf53-43f3-aa17-c459063c99ab
title: Méthode CSourceStream. Stop (source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.Stop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 44c9f845c092280ef5fafa808036654bd868a796
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532608"
---
# <a name="csourcestreamstop-method"></a><span data-ttu-id="1e66b-103">CSourceStream. Stop, méthode</span><span class="sxs-lookup"><span data-stu-id="1e66b-103">CSourceStream.Stop method</span></span>

<span data-ttu-id="1e66b-104">La `Stop` méthode signale l’arrêt du thread de streaming.</span><span class="sxs-lookup"><span data-stu-id="1e66b-104">The `Stop` method signals the streaming thread to stop.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e66b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1e66b-105">Syntax</span></span>


```C++
HRESULT Stop();
```



## <a name="parameters"></a><span data-ttu-id="1e66b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1e66b-106">Parameters</span></span>

<span data-ttu-id="1e66b-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="1e66b-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1e66b-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1e66b-108">Return value</span></span>

<span data-ttu-id="1e66b-109">Retourne S \_ OK ou E \_ inattendu.</span><span class="sxs-lookup"><span data-stu-id="1e66b-109">Returns S\_OK or E\_UNEXPECTED.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e66b-110">Notes</span><span class="sxs-lookup"><span data-stu-id="1e66b-110">Remarks</span></span>

<span data-ttu-id="1e66b-111">La méthode [**CSourceStream :: inactive**](csourcestream-inactive.md) appelle cette méthode.</span><span class="sxs-lookup"><span data-stu-id="1e66b-111">The [**CSourceStream::Inactive**](csourcestream-inactive.md) method calls this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e66b-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1e66b-112">Requirements</span></span>



| <span data-ttu-id="1e66b-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1e66b-113">Requirement</span></span> | <span data-ttu-id="1e66b-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="1e66b-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e66b-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="1e66b-115">Header</span></span><br/>  | <dl> <span data-ttu-id="1e66b-116"><dt>Source. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1e66b-116"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="1e66b-117">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1e66b-117">Library</span></span><br/> | <dl> <span data-ttu-id="1e66b-118"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="1e66b-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e66b-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1e66b-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e66b-120">**CSourceStream, classe**</span><span class="sxs-lookup"><span data-stu-id="1e66b-120">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




