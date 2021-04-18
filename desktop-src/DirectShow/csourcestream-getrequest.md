---
description: La méthode GetRequest attend la demande de thread suivante.
ms.assetid: 2938374b-174f-4276-98a2-20a084bd9bbd
title: Méthode CSourceStream. GetRequest (source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.GetRequest
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3f45e6f6cf269f7aca6741d8e1c150c7054b07f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528886"
---
# <a name="csourcestreamgetrequest-method"></a><span data-ttu-id="47d18-103">Méthode CSourceStream. GetRequest</span><span class="sxs-lookup"><span data-stu-id="47d18-103">CSourceStream.GetRequest method</span></span>

<span data-ttu-id="47d18-104">La `GetRequest` méthode attend la demande de thread suivante.</span><span class="sxs-lookup"><span data-stu-id="47d18-104">The `GetRequest` method waits for the next thread request.</span></span>

## <a name="syntax"></a><span data-ttu-id="47d18-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="47d18-105">Syntax</span></span>


```C++
Command GetRequest();
```



## <a name="parameters"></a><span data-ttu-id="47d18-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="47d18-106">Parameters</span></span>

<span data-ttu-id="47d18-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="47d18-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="47d18-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="47d18-108">Return value</span></span>

<span data-ttu-id="47d18-109">Retourne la requête de thread suivante.</span><span class="sxs-lookup"><span data-stu-id="47d18-109">Returns the next thread request.</span></span>

## <a name="remarks"></a><span data-ttu-id="47d18-110">Notes</span><span class="sxs-lookup"><span data-stu-id="47d18-110">Remarks</span></span>

<span data-ttu-id="47d18-111">Cette méthode remplace la méthode [**CAMThread :: GetRequest**](camthread-getrequest.md) .</span><span class="sxs-lookup"><span data-stu-id="47d18-111">This method overrides the [**CAMThread::GetRequest**](camthread-getrequest.md) method.</span></span> <span data-ttu-id="47d18-112">La valeur de retour est convertie vers le type énuméré suivant :</span><span class="sxs-lookup"><span data-stu-id="47d18-112">The return value is cast to the following enumerated type:</span></span>


```C++
enum Command {CMD_INIT, CMD_PAUSE, CMD_RUN, CMD_STOP, CMD_EXIT};
```



## <a name="requirements"></a><span data-ttu-id="47d18-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="47d18-113">Requirements</span></span>



| <span data-ttu-id="47d18-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="47d18-114">Requirement</span></span> | <span data-ttu-id="47d18-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="47d18-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47d18-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="47d18-116">Header</span></span><br/>  | <dl> <span data-ttu-id="47d18-117"><dt>Source. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="47d18-117"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="47d18-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="47d18-118">Library</span></span><br/> | <dl> <span data-ttu-id="47d18-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="47d18-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47d18-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="47d18-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47d18-121">**CSourceStream, classe**</span><span class="sxs-lookup"><span data-stu-id="47d18-121">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




