---
description: 'La méthode Desize récupère la taille de la mémoire tampon. Cette méthode implémente la méthode IMediaSample :: AD.'
ms.assetid: 14562ef4-f554-4d5a-83d3-1a29abae08a4
title: CMediaSample., méthode (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.GetSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ff4146b66ca62905fe54eeb88d1e38ccf56ceea9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106520804"
---
# <a name="cmediasamplegetsize-method"></a><span data-ttu-id="d9237-104">CMediaSample. adla méthode</span><span class="sxs-lookup"><span data-stu-id="d9237-104">CMediaSample.GetSize method</span></span>

<span data-ttu-id="d9237-105">La `GetSize` méthode récupère la taille de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="d9237-105">The `GetSize` method retrieves the size of the buffer.</span></span> <span data-ttu-id="d9237-106">Cette méthode implémente la méthode [**IMediaSample :: AD**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getsize) .</span><span class="sxs-lookup"><span data-stu-id="d9237-106">This method implements the [**IMediaSample::GetSize**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getsize) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9237-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d9237-107">Syntax</span></span>


```C++
LONG GetSize();
```



## <a name="parameters"></a><span data-ttu-id="d9237-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d9237-108">Parameters</span></span>

<span data-ttu-id="d9237-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="d9237-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d9237-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d9237-110">Return value</span></span>

<span data-ttu-id="d9237-111">Retourne la taille de la mémoire tampon, en octets.</span><span class="sxs-lookup"><span data-stu-id="d9237-111">Returns the size of the buffer, in bytes.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9237-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d9237-112">Requirements</span></span>



| <span data-ttu-id="d9237-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d9237-113">Requirement</span></span> | <span data-ttu-id="d9237-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="d9237-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9237-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="d9237-115">Header</span></span><br/>  | <dl> <span data-ttu-id="d9237-116"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d9237-116"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="d9237-117">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d9237-117">Library</span></span><br/> | <dl> <span data-ttu-id="d9237-118"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="d9237-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9237-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d9237-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9237-120">**CMediaSample, classe**</span><span class="sxs-lookup"><span data-stu-id="d9237-120">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




