---
description: La méthode CancelNotification annule l’événement du minuteur qui planifie le rendu.
ms.assetid: 56ddf692-a2e3-40f2-848f-2d592601ec00
title: Méthode CBaseRenderer. CancelNotification (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.CancelNotification
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3330f369c5fcc45fe051a1964a504d5d40fcd091
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532677"
---
# <a name="cbaserenderercancelnotification-method"></a><span data-ttu-id="5302a-103">Méthode CBaseRenderer. CancelNotification</span><span class="sxs-lookup"><span data-stu-id="5302a-103">CBaseRenderer.CancelNotification method</span></span>

<span data-ttu-id="5302a-104">La `CancelNotification` méthode annule l’événement de minuterie qui planifie le rendu.</span><span class="sxs-lookup"><span data-stu-id="5302a-104">The `CancelNotification` method cancels the timer event that schedules rendering.</span></span>

## <a name="syntax"></a><span data-ttu-id="5302a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5302a-105">Syntax</span></span>


```C++
virtual HRESULT CancelNotification();
```



## <a name="parameters"></a><span data-ttu-id="5302a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5302a-106">Parameters</span></span>

<span data-ttu-id="5302a-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="5302a-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5302a-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5302a-108">Return value</span></span>

<span data-ttu-id="5302a-109">Retourne l’une des valeurs **HRESULT** indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="5302a-109">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="5302a-110">Code de retour</span><span class="sxs-lookup"><span data-stu-id="5302a-110">Return code</span></span>                                                                             | <span data-ttu-id="5302a-111">Description</span><span class="sxs-lookup"><span data-stu-id="5302a-111">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="5302a-112"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="5302a-112"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="5302a-113">Aucun événement de minuterie en attente.</span><span class="sxs-lookup"><span data-stu-id="5302a-113">There was no pending timer event.</span></span><br/> |
| <dl> <span data-ttu-id="5302a-114"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="5302a-114"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="5302a-115">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="5302a-115">Success.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="5302a-116">Notes</span><span class="sxs-lookup"><span data-stu-id="5302a-116">Remarks</span></span>

<span data-ttu-id="5302a-117">Le filtre appelle cette méthode lorsque la diffusion en continu s’arrête.</span><span class="sxs-lookup"><span data-stu-id="5302a-117">The filter calls this method when streaming stops.</span></span> <span data-ttu-id="5302a-118">La méthode annule tout rendu planifié.</span><span class="sxs-lookup"><span data-stu-id="5302a-118">The method cancels any scheduled rendering.</span></span>

## <a name="requirements"></a><span data-ttu-id="5302a-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5302a-119">Requirements</span></span>



| <span data-ttu-id="5302a-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5302a-120">Requirement</span></span> | <span data-ttu-id="5302a-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="5302a-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5302a-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="5302a-122">Header</span></span><br/>  | <dl> <span data-ttu-id="5302a-123"><dt>Renbase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5302a-123"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5302a-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5302a-124">Library</span></span><br/> | <dl> <span data-ttu-id="5302a-125"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="5302a-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5302a-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5302a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5302a-127">**CBaseRenderer, classe**</span><span class="sxs-lookup"><span data-stu-id="5302a-127">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




