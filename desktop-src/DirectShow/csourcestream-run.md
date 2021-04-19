---
description: La méthode Run indique au thread de streaming de s’exécuter.
ms.assetid: 9aef7801-dcfb-4597-bccb-5ba19327b2d5
title: Méthode CSourceStream. Run (source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.Run
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 39093654677ab4828f8a1d5a01a8cf7deaf42507
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535367"
---
# <a name="csourcestreamrun-method"></a><span data-ttu-id="ea4f6-103">CSourceStream. Run, méthode</span><span class="sxs-lookup"><span data-stu-id="ea4f6-103">CSourceStream.Run method</span></span>

<span data-ttu-id="ea4f6-104">La `Run` méthode signale l’exécution du thread de streaming.</span><span class="sxs-lookup"><span data-stu-id="ea4f6-104">The `Run` method signals the streaming thread to run.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea4f6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ea4f6-105">Syntax</span></span>


```C++
HRESULT Run();
```



## <a name="parameters"></a><span data-ttu-id="ea4f6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ea4f6-106">Parameters</span></span>

<span data-ttu-id="ea4f6-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="ea4f6-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ea4f6-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ea4f6-108">Return value</span></span>

<span data-ttu-id="ea4f6-109">Retourne S \_ OK ou E \_ inattendu.</span><span class="sxs-lookup"><span data-stu-id="ea4f6-109">Returns S\_OK or E\_UNEXPECTED.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea4f6-110">Notes</span><span class="sxs-lookup"><span data-stu-id="ea4f6-110">Remarks</span></span>

<span data-ttu-id="ea4f6-111">Dans la classe de base, cette méthode a le même effet que la demande [**CSourceStream ::P ause**](csourcestream-pause.md) et n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="ea4f6-111">In the base class, this method has the same effect as the [**CSourceStream::Pause**](csourcestream-pause.md) request, and is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea4f6-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ea4f6-112">Requirements</span></span>



| <span data-ttu-id="ea4f6-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ea4f6-113">Requirement</span></span> | <span data-ttu-id="ea4f6-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="ea4f6-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea4f6-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="ea4f6-115">Header</span></span><br/>  | <dl> <span data-ttu-id="ea4f6-116"><dt>Source. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ea4f6-116"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="ea4f6-117">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ea4f6-117">Library</span></span><br/> | <dl> <span data-ttu-id="ea4f6-118"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="ea4f6-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea4f6-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ea4f6-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea4f6-120">**CSourceStream, classe**</span><span class="sxs-lookup"><span data-stu-id="ea4f6-120">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




