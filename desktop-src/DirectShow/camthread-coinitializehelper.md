---
description: La méthode CoInitializeHelper appelle la fonction CoInitializeEx au début du thread.
ms.assetid: 1a981e1e-c059-4e51-81d8-33bcb39ee580
title: Méthode CAMThread. CoInitializeHelper (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.CoInitializeHelper
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a6c3eb7fbcb9e4abada43098339a29d208ded0d4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539622"
---
# <a name="camthreadcoinitializehelper-method"></a><span data-ttu-id="35ed6-103">Méthode CAMThread. CoInitializeHelper</span><span class="sxs-lookup"><span data-stu-id="35ed6-103">CAMThread.CoInitializeHelper method</span></span>

<span data-ttu-id="35ed6-104">La `CoInitializeHelper` méthode appelle la fonction CoInitializeEx au début du thread.</span><span class="sxs-lookup"><span data-stu-id="35ed6-104">The `CoInitializeHelper` method calls the CoInitializeEx function at the start of the thread.</span></span>

## <a name="syntax"></a><span data-ttu-id="35ed6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="35ed6-105">Syntax</span></span>


```C++
static HRESULT CoInitializeHelper();
```



## <a name="parameters"></a><span data-ttu-id="35ed6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="35ed6-106">Parameters</span></span>

<span data-ttu-id="35ed6-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="35ed6-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="35ed6-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="35ed6-108">Return value</span></span>

<span data-ttu-id="35ed6-109">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="35ed6-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="35ed6-110">Les valeurs possibles sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="35ed6-110">The following are possible values.</span></span>



| <span data-ttu-id="35ed6-111">Code de retour</span><span class="sxs-lookup"><span data-stu-id="35ed6-111">Return code</span></span>                                                                             | <span data-ttu-id="35ed6-112">Description</span><span class="sxs-lookup"><span data-stu-id="35ed6-112">Description</span></span>                                              |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="35ed6-113"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="35ed6-113"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="35ed6-114">La fonction CoInitializeEx n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="35ed6-114">The CoInitializeEx function is not available.</span></span><br/> |
| <dl> <span data-ttu-id="35ed6-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="35ed6-115"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="35ed6-116">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="35ed6-116">Success.</span></span><br/>                                      |
| <dl> <span data-ttu-id="35ed6-117"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="35ed6-117"><dt>**E\_FAIL**</dt></span></span> </dl>  | <span data-ttu-id="35ed6-118">Échec.</span><span class="sxs-lookup"><span data-stu-id="35ed6-118">Failure.</span></span><br/>                                      |



 

## <a name="remarks"></a><span data-ttu-id="35ed6-119">Notes</span><span class="sxs-lookup"><span data-stu-id="35ed6-119">Remarks</span></span>

<span data-ttu-id="35ed6-120">La méthode [**CAMThread :: InitialThreadProc**](camthread-initialthreadproc.md) appelle cette méthode d’assistance, qui appelle la fonction CoInitializeEx.</span><span class="sxs-lookup"><span data-stu-id="35ed6-120">The [**CAMThread::InitialThreadProc**](camthread-initialthreadproc.md) method calls this helper method, which calls the CoInitializeEx function.</span></span> <span data-ttu-id="35ed6-121">Elle utilise l’indicateur coinit \_ Disable \_ OLE1DDE pour désactiver l’échange dynamique de données (DDE).</span><span class="sxs-lookup"><span data-stu-id="35ed6-121">It uses the COINIT\_DISABLE\_OLE1DDE flag, to disable Dynamic Data Exchange (DDE).</span></span> <span data-ttu-id="35ed6-122">Pour plus d’informations, consultez le kit de développement Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="35ed6-122">For more information, see the Platform SDK.</span></span>

## <a name="requirements"></a><span data-ttu-id="35ed6-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="35ed6-123">Requirements</span></span>



| <span data-ttu-id="35ed6-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="35ed6-124">Requirement</span></span> | <span data-ttu-id="35ed6-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="35ed6-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35ed6-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="35ed6-126">Header</span></span><br/>  | <dl> <span data-ttu-id="35ed6-127"><dt>Wxutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="35ed6-127"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="35ed6-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="35ed6-128">Library</span></span><br/> | <dl> <span data-ttu-id="35ed6-129"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="35ed6-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35ed6-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="35ed6-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35ed6-131">**CAMThread, classe**</span><span class="sxs-lookup"><span data-stu-id="35ed6-131">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




