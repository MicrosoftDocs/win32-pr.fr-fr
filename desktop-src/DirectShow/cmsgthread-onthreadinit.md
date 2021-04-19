---
description: Fournit l’initialisation sur un thread.
ms.assetid: a9c330bb-0a2b-45bf-9b24-d03dd61d7dbf
title: Méthode CMsgThread. OnThreadInit (Msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.OnThreadInit
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 80e15d6430da77c0f22f5566375394b8fe6994ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542496"
---
# <a name="cmsgthreadonthreadinit-method"></a><span data-ttu-id="b5b3c-103">Méthode CMsgThread. OnThreadInit</span><span class="sxs-lookup"><span data-stu-id="b5b3c-103">CMsgThread.OnThreadInit method</span></span>

<span data-ttu-id="b5b3c-104">Fournit l’initialisation sur un thread.</span><span class="sxs-lookup"><span data-stu-id="b5b3c-104">Provides initialization on a thread.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5b3c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b5b3c-105">Syntax</span></span>


```C++
virtual void OnThreadInit();
```



## <a name="parameters"></a><span data-ttu-id="b5b3c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b5b3c-106">Parameters</span></span>

<span data-ttu-id="b5b3c-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="b5b3c-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b5b3c-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b5b3c-108">Return value</span></span>

<span data-ttu-id="b5b3c-109">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="b5b3c-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5b3c-110">Notes</span><span class="sxs-lookup"><span data-stu-id="b5b3c-110">Remarks</span></span>

<span data-ttu-id="b5b3c-111">Substituez cette fonction si vous souhaitez effectuer votre propre initialisation spécifique au démarrage du thread.</span><span class="sxs-lookup"><span data-stu-id="b5b3c-111">Override this function if you want to do your own specific initialization on thread startup.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5b3c-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b5b3c-112">Requirements</span></span>



| <span data-ttu-id="b5b3c-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b5b3c-113">Requirement</span></span> | <span data-ttu-id="b5b3c-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="b5b3c-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5b3c-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="b5b3c-115">Header</span></span><br/>  | <dl> <span data-ttu-id="b5b3c-116"><dt>Msgthrd. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b5b3c-116"><dt>Msgthrd.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b5b3c-117">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b5b3c-117">Library</span></span><br/> | <dl> <span data-ttu-id="b5b3c-118"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="b5b3c-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5b3c-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b5b3c-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5b3c-120">**CMsgThread, classe**</span><span class="sxs-lookup"><span data-stu-id="b5b3c-120">**CMsgThread Class**</span></span>](cmsgthread.md)
</dt> </dl>

 

 




