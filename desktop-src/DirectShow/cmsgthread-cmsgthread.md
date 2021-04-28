---
description: Méthode constructeur CMsgThread. CMsgThread.
ms.assetid: 3f758c45-21ec-4728-ba7d-41da7b2fa02f
title: Constructeur CMsgThread. CMsgThread (Msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.CMsgThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 08d76ebecd09d95b7ba0fca22b300c1e402f5302
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095367"
---
# <a name="cmsgthreadcmsgthread-constructor"></a><span data-ttu-id="4ed10-103">Constructeur CMsgThread. CMsgThread</span><span class="sxs-lookup"><span data-stu-id="4ed10-103">CMsgThread.CMsgThread constructor</span></span>

<span data-ttu-id="4ed10-104">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="4ed10-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ed10-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4ed10-105">Syntax</span></span>


```C++
CMsgThread();
```



## <a name="parameters"></a><span data-ttu-id="4ed10-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4ed10-106">Parameters</span></span>

<span data-ttu-id="4ed10-107">Ce constructeur n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="4ed10-107">This constructor has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ed10-108">Notes </span><span class="sxs-lookup"><span data-stu-id="4ed10-108">Remarks</span></span>

<span data-ttu-id="4ed10-109">La construction d’un objet de thread de message ne crée pas automatiquement le thread.</span><span class="sxs-lookup"><span data-stu-id="4ed10-109">Constructing a message thread object does not automatically create the thread.</span></span> <span data-ttu-id="4ed10-110">Vous devez appeler la fonction membre [**CMsgThread :: CreateThread**](cmsgthread-createthread.md) pour créer le thread.</span><span class="sxs-lookup"><span data-stu-id="4ed10-110">You must call the [**CMsgThread::CreateThread**](cmsgthread-createthread.md) member function to create the thread.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ed10-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4ed10-111">Requirements</span></span>



| <span data-ttu-id="4ed10-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4ed10-112">Requirement</span></span> | <span data-ttu-id="4ed10-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="4ed10-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ed10-114">En-tête</span><span class="sxs-lookup"><span data-stu-id="4ed10-114">Header</span></span><br/>  | <dl> <span data-ttu-id="4ed10-115"><dt>Msgthrd. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4ed10-115"><dt>Msgthrd.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="4ed10-116">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4ed10-116">Library</span></span><br/> | <dl> <span data-ttu-id="4ed10-117"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="4ed10-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ed10-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4ed10-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ed10-119">**CMsgThread, classe**</span><span class="sxs-lookup"><span data-stu-id="4ed10-119">**CMsgThread Class**</span></span>](cmsgthread.md)
</dt> </dl>

 

 




