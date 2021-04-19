---
description: La méthode CheckStreaming détermine si le code pin peut accepter des exemples.
ms.assetid: fa063966-4c72-466e-933c-def6a6818621
title: Méthode CTransformInputPin. CheckStreaming (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.CheckStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0e5c49a00054547193e3f492f0731f77af8331a2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106536021"
---
# <a name="ctransforminputpincheckstreaming-method"></a><span data-ttu-id="0952f-103">Méthode CTransformInputPin. CheckStreaming</span><span class="sxs-lookup"><span data-stu-id="0952f-103">CTransformInputPin.CheckStreaming method</span></span>

<span data-ttu-id="0952f-104">La `CheckStreaming` méthode détermine si le code pin peut accepter des exemples.</span><span class="sxs-lookup"><span data-stu-id="0952f-104">The `CheckStreaming` method determines whether the pin can accept samples.</span></span>

## <a name="syntax"></a><span data-ttu-id="0952f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0952f-105">Syntax</span></span>


```C++
HRESULT CheckStreaming();
```



## <a name="parameters"></a><span data-ttu-id="0952f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0952f-106">Parameters</span></span>

<span data-ttu-id="0952f-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="0952f-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0952f-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0952f-108">Return value</span></span>

<span data-ttu-id="0952f-109">Retourne l’une des valeurs **HRESULT** listées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="0952f-109">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="0952f-110">Code de retour</span><span class="sxs-lookup"><span data-stu-id="0952f-110">Return code</span></span>                                                                                           | <span data-ttu-id="0952f-111">Description</span><span class="sxs-lookup"><span data-stu-id="0952f-111">Description</span></span>                                 |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <span data-ttu-id="0952f-112"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0952f-112"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="0952f-113">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="0952f-113">Success.</span></span><br/>                         |
| <dl> <span data-ttu-id="0952f-114"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="0952f-114"><dt>**S\_FALSE**</dt></span></span> </dl>               | <span data-ttu-id="0952f-115">Le code PIN est en cours de vidage.</span><span class="sxs-lookup"><span data-stu-id="0952f-115">Pin is currently flushing.</span></span><br/>       |
| <dl> <span data-ttu-id="0952f-116"><dt>**VFW \_ E \_ non \_ connecté**</dt></span><span class="sxs-lookup"><span data-stu-id="0952f-116"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="0952f-117">La broche de sortie n’est pas connectée.</span><span class="sxs-lookup"><span data-stu-id="0952f-117">The output pin is not connected.</span></span><br/> |
| <dl> <span data-ttu-id="0952f-118"><dt>**\_erreur d' \_ exécution VFW E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0952f-118"><dt>**VFW\_E\_RUNTIME\_ERROR**</dt></span></span> </dl> | <span data-ttu-id="0952f-119">Une erreur d’exécution s’est produite.</span><span class="sxs-lookup"><span data-stu-id="0952f-119">A run-time error occurred.</span></span><br/>       |
| <dl> <span data-ttu-id="0952f-120"><dt>**VFW \_ E \_ état incorrect \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0952f-120"><dt>**VFW\_E\_WRONG\_STATE**</dt></span></span> </dl>   | <span data-ttu-id="0952f-121">Le code PIN est arrêté.</span><span class="sxs-lookup"><span data-stu-id="0952f-121">The pin is stopped.</span></span><br/>              |



 

## <a name="remarks"></a><span data-ttu-id="0952f-122">Notes</span><span class="sxs-lookup"><span data-stu-id="0952f-122">Remarks</span></span>

<span data-ttu-id="0952f-123">Cette méthode remplace la méthode [**CBaseInputPin :: CheckStreaming**](cbaseinputpin-checkstreaming.md) .</span><span class="sxs-lookup"><span data-stu-id="0952f-123">This method overrides the [**CBaseInputPin::CheckStreaming**](cbaseinputpin-checkstreaming.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="0952f-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0952f-124">Requirements</span></span>



| <span data-ttu-id="0952f-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0952f-125">Requirement</span></span> | <span data-ttu-id="0952f-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="0952f-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0952f-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="0952f-127">Header</span></span><br/>  | <dl> <span data-ttu-id="0952f-128"><dt>Transfrm. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0952f-128"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="0952f-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0952f-129">Library</span></span><br/> | <dl> <span data-ttu-id="0952f-130"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="0952f-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




