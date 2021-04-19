---
description: Méthode de constructeur.
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
ms.openlocfilehash: e77d3a84e349ab370b6319cd973f6ba86d632366
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525280"
---
# <a name="cmsgthreadcmsgthread-constructor"></a><span data-ttu-id="9f1d2-103">Constructeur CMsgThread. CMsgThread</span><span class="sxs-lookup"><span data-stu-id="9f1d2-103">CMsgThread.CMsgThread constructor</span></span>

<span data-ttu-id="9f1d2-104">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="9f1d2-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f1d2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9f1d2-105">Syntax</span></span>


```C++
CMsgThread();
```



## <a name="parameters"></a><span data-ttu-id="9f1d2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9f1d2-106">Parameters</span></span>

<span data-ttu-id="9f1d2-107">Ce constructeur n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="9f1d2-107">This constructor has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f1d2-108">Notes</span><span class="sxs-lookup"><span data-stu-id="9f1d2-108">Remarks</span></span>

<span data-ttu-id="9f1d2-109">La construction d’un objet de thread de message ne crée pas automatiquement le thread.</span><span class="sxs-lookup"><span data-stu-id="9f1d2-109">Constructing a message thread object does not automatically create the thread.</span></span> <span data-ttu-id="9f1d2-110">Vous devez appeler la fonction membre [**CMsgThread :: CreateThread**](cmsgthread-createthread.md) pour créer le thread.</span><span class="sxs-lookup"><span data-stu-id="9f1d2-110">You must call the [**CMsgThread::CreateThread**](cmsgthread-createthread.md) member function to create the thread.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f1d2-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9f1d2-111">Requirements</span></span>



| <span data-ttu-id="9f1d2-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9f1d2-112">Requirement</span></span> | <span data-ttu-id="9f1d2-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="9f1d2-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f1d2-114">En-tête</span><span class="sxs-lookup"><span data-stu-id="9f1d2-114">Header</span></span><br/>  | <dl> <span data-ttu-id="9f1d2-115"><dt>Msgthrd. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9f1d2-115"><dt>Msgthrd.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="9f1d2-116">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9f1d2-116">Library</span></span><br/> | <dl> <span data-ttu-id="9f1d2-117"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="9f1d2-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f1d2-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9f1d2-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f1d2-119">**CMsgThread, classe**</span><span class="sxs-lookup"><span data-stu-id="9f1d2-119">**CMsgThread Class**</span></span>](cmsgthread.md)
</dt> </dl>

 

 




