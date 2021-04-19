---
description: La méthode GetRequestParam récupère la dernière requête.
ms.assetid: f5bf4935-29ea-45b9-a57e-9fdcd9cde20a
title: Méthode CAMThread. GetRequestParam (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.GetRequestParam
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2dd6584123663bb36f1db4771fb3f86d7ac4f5cd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542672"
---
# <a name="camthreadgetrequestparam-method"></a><span data-ttu-id="3a669-103">Méthode CAMThread. GetRequestParam</span><span class="sxs-lookup"><span data-stu-id="3a669-103">CAMThread.GetRequestParam method</span></span>

<span data-ttu-id="3a669-104">La `GetRequestParam` méthode récupère la dernière requête.</span><span class="sxs-lookup"><span data-stu-id="3a669-104">The `GetRequestParam` method retrieves the latest request.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a669-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3a669-105">Syntax</span></span>


```C++
DWORD GetRequestParam() const;
```



## <a name="parameters"></a><span data-ttu-id="3a669-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3a669-106">Parameters</span></span>

<span data-ttu-id="3a669-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="3a669-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3a669-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3a669-108">Return value</span></span>

<span data-ttu-id="3a669-109">Retourne la valeur du paramètre passé le plus récemment à la méthode [**CAMThread :: CallWorker**](camthread-callworker.md) .</span><span class="sxs-lookup"><span data-stu-id="3a669-109">Returns the value of the parameter that was passed most recently to the [**CAMThread::CallWorker**](camthread-callworker.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a669-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3a669-110">Requirements</span></span>



| <span data-ttu-id="3a669-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3a669-111">Requirement</span></span> | <span data-ttu-id="3a669-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="3a669-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a669-113">En-tête</span><span class="sxs-lookup"><span data-stu-id="3a669-113">Header</span></span><br/>  | <dl> <span data-ttu-id="3a669-114"><dt>Wxutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3a669-114"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="3a669-115">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3a669-115">Library</span></span><br/> | <dl> <span data-ttu-id="3a669-116"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="3a669-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a669-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3a669-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a669-118">**CAMThread, classe**</span><span class="sxs-lookup"><span data-stu-id="3a669-118">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




