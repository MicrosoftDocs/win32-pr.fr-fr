---
description: La méthode active crée un thread de travail qui extrait les données de la broche de sortie. Cette méthode valide également l’allocateur.
ms.assetid: 9efa20f3-7909-4d87-bfa8-314d055b80f8
title: CPullPin. active, méthode (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.Active
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 461f6554f828dc096029ee1e7a1832e12a7c262a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533494"
---
# <a name="cpullpinactive-method"></a><span data-ttu-id="51605-104">CPullPin. active, méthode</span><span class="sxs-lookup"><span data-stu-id="51605-104">CPullPin.Active method</span></span>

<span data-ttu-id="51605-105">La méthode **active** crée un thread de travail qui extrait les données de la broche de sortie.</span><span class="sxs-lookup"><span data-stu-id="51605-105">The **Active** method creates a worker thread that pulls data from the output pin.</span></span> <span data-ttu-id="51605-106">Cette méthode valide également l’allocateur.</span><span class="sxs-lookup"><span data-stu-id="51605-106">This method also commits the allocator.</span></span>

## <a name="syntax"></a><span data-ttu-id="51605-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="51605-107">Syntax</span></span>


```C++
HRESULT Active();
```



## <a name="parameters"></a><span data-ttu-id="51605-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="51605-108">Parameters</span></span>

<span data-ttu-id="51605-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="51605-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="51605-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="51605-110">Return value</span></span>

<span data-ttu-id="51605-111">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="51605-111">Returns an **HRESULT** value.</span></span> <span data-ttu-id="51605-112">Les valeurs possibles sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="51605-112">Possible values include the following.</span></span>



| <span data-ttu-id="51605-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="51605-113">Return code</span></span>                                                                                  | <span data-ttu-id="51605-114">Description</span><span class="sxs-lookup"><span data-stu-id="51605-114">Description</span></span>                                                           |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <span data-ttu-id="51605-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="51605-115"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="51605-116">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="51605-116">Success.</span></span><br/>                                                   |
| <dl> <span data-ttu-id="51605-117"><dt>**E \_ inattendu**</dt></span><span class="sxs-lookup"><span data-stu-id="51605-117"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="51605-118">La connexion de code confidentiel n’a pas été établie correctement.</span><span class="sxs-lookup"><span data-stu-id="51605-118">The pin connection was not established correctly.</span></span><br/>          |
| <dl> <span data-ttu-id="51605-119"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="51605-119"><dt>**E\_FAIL**</dt></span></span> </dl>       | <span data-ttu-id="51605-120">Impossible de créer le thread ou le thread existe déjà.</span><span class="sxs-lookup"><span data-stu-id="51605-120">Could not create the thread, or the thread already exists.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="51605-121">Notes</span><span class="sxs-lookup"><span data-stu-id="51605-121">Remarks</span></span>

<span data-ttu-id="51605-122">Appelez cette méthode lorsque le filtre propriétaire devient actif.</span><span class="sxs-lookup"><span data-stu-id="51605-122">Call this method when the owning filter becomes active.</span></span> <span data-ttu-id="51605-123">(Si votre broche d’entrée dérive de [**CBasePin**](cbasepin.md), remplacez la méthode [**CBasePin :: active**](cbasepin-active.md) .)</span><span class="sxs-lookup"><span data-stu-id="51605-123">(If your input pin derives from [**CBasePin**](cbasepin.md), override the [**CBasePin::Active**](cbasepin-active.md) method.)</span></span>

<span data-ttu-id="51605-124">Avant d’appeler cette méthode, appelez la méthode [**CPullPin :: Connect**](cpullpin-connect.md) pour établir la connexion avec la broche de sortie.</span><span class="sxs-lookup"><span data-stu-id="51605-124">Before calling this method, call the [**CPullPin::Connect**](cpullpin-connect.md) method to establish the connection with the output pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="51605-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="51605-125">Requirements</span></span>



| <span data-ttu-id="51605-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="51605-126">Requirement</span></span> | <span data-ttu-id="51605-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="51605-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51605-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="51605-128">Header</span></span><br/>  | <dl> <span data-ttu-id="51605-129"><dt>Pullpin. h</dt></span><span class="sxs-lookup"><span data-stu-id="51605-129"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="51605-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="51605-130">Library</span></span><br/> | <dl> <span data-ttu-id="51605-131"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="51605-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51605-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="51605-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51605-133">**CPullPin, classe**</span><span class="sxs-lookup"><span data-stu-id="51605-133">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 




