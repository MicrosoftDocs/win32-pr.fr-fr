---
description: La méthode Seek définit les positions de début et de fin du flux.
ms.assetid: d84476f5-688c-429d-a51b-7020a6316e35
title: CPullPin. Seek, méthode (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.Seek
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6f1a82ec549b5ceb888acc194a7abc2cd3eace47
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526385"
---
# <a name="cpullpinseek-method"></a><span data-ttu-id="7ffde-103">CPullPin. Seek, méthode</span><span class="sxs-lookup"><span data-stu-id="7ffde-103">CPullPin.Seek method</span></span>

<span data-ttu-id="7ffde-104">La `Seek` méthode définit les positions de début et de fin du flux.</span><span class="sxs-lookup"><span data-stu-id="7ffde-104">The `Seek` method sets the start and stop positions of the stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ffde-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7ffde-105">Syntax</span></span>


```C++
HRESULT Seek(
   REFERENCE_TIME tStart,
   REFERENCE_TIME tStop
);
```



## <a name="parameters"></a><span data-ttu-id="7ffde-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7ffde-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ffde-107">*tStart*</span><span class="sxs-lookup"><span data-stu-id="7ffde-107">*tStart*</span></span> 
</dt> <dd>

<span data-ttu-id="7ffde-108">Spécifie la position de départ, en octets, multipliée par 10 millions.</span><span class="sxs-lookup"><span data-stu-id="7ffde-108">Specifies the start position, in bytes multiplied by 10,000,000.</span></span>

</dd> <dt>

<span data-ttu-id="7ffde-109">*tStop*</span><span class="sxs-lookup"><span data-stu-id="7ffde-109">*tStop*</span></span> 
</dt> <dd>

<span data-ttu-id="7ffde-110">Spécifie la position d’arrêt, en octets, multipliée par 10 millions.</span><span class="sxs-lookup"><span data-stu-id="7ffde-110">Specifies the stop position, in bytes multiplied by 10,000,000.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ffde-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7ffde-111">Return value</span></span>

<span data-ttu-id="7ffde-112">Retourne S \_ OK si la méthode est réussie, ou un code d’erreur dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="7ffde-112">Returns S\_OK if the method succeeds, or an error code otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="7ffde-113">Notes</span><span class="sxs-lookup"><span data-stu-id="7ffde-113">Remarks</span></span>

<span data-ttu-id="7ffde-114">Si le thread de travail est en cours d’exécution, la méthode suspend le thread, vide le graphique de filtre et reprend le thread.</span><span class="sxs-lookup"><span data-stu-id="7ffde-114">If the worker thread is running, the method pauses the thread, flushes the filter graph, and resumes the thread.</span></span> <span data-ttu-id="7ffde-115">Le thread commence à extraire les données à partir de la nouvelle position de départ.</span><span class="sxs-lookup"><span data-stu-id="7ffde-115">The thread begins pulling data from the new start position.</span></span> <span data-ttu-id="7ffde-116">Dans le cas contraire, les nouvelles valeurs de position prennent effet à chaque démarrage du thread.</span><span class="sxs-lookup"><span data-stu-id="7ffde-116">Otherwise, the new position values become effective whenever the thread is started.</span></span>

<span data-ttu-id="7ffde-117">Les positions sont relatives au début de la source d’origine.</span><span class="sxs-lookup"><span data-stu-id="7ffde-117">Positions are relative to the start of the original source.</span></span> <span data-ttu-id="7ffde-118">Multipliez les décalages d’octets souhaités par les unités constantes, qui sont définies dans la bibliothèque de classes de base sous la forme 10 millions.</span><span class="sxs-lookup"><span data-stu-id="7ffde-118">Multiply the desired byte offsets by the constant UNITS, which is defined in the base class library as 10,000,000.</span></span>

<span data-ttu-id="7ffde-119">Lorsque le code confidentiel se connecte pour la première fois, les positions arrêter et démarrer sont représentées par défaut au début et à la fin du flux.</span><span class="sxs-lookup"><span data-stu-id="7ffde-119">When the pin first connects, the stop and start positions default to the beginning and end of the stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ffde-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7ffde-120">Requirements</span></span>



| <span data-ttu-id="7ffde-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7ffde-121">Requirement</span></span> | <span data-ttu-id="7ffde-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="7ffde-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ffde-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="7ffde-123">Header</span></span><br/>  | <dl> <span data-ttu-id="7ffde-124"><dt>Pullpin. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ffde-124"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="7ffde-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7ffde-125">Library</span></span><br/> | <dl> <span data-ttu-id="7ffde-126"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="7ffde-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ffde-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7ffde-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ffde-128">**CPullPin, classe**</span><span class="sxs-lookup"><span data-stu-id="7ffde-128">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 




