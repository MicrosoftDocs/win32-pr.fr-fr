---
description: 'Méthode CTransformInputPin. BreakConnect : la méthode BreakConnect libère le code confidentiel d’une connexion.'
ms.assetid: 9874717d-f4d8-426d-a717-9f5d83b4683c
title: Méthode CTransformInputPin. BreakConnect (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.BreakConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fe425ba617909dcfb1d66dbb4777b579139d436b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085017"
---
# <a name="ctransforminputpinbreakconnect-method"></a><span data-ttu-id="3dc8f-103">Méthode CTransformInputPin. BreakConnect</span><span class="sxs-lookup"><span data-stu-id="3dc8f-103">CTransformInputPin.BreakConnect method</span></span>

<span data-ttu-id="3dc8f-104">La `BreakConnect` méthode libère le code confidentiel d’une connexion.</span><span class="sxs-lookup"><span data-stu-id="3dc8f-104">The `BreakConnect` method releases the pin from a connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="3dc8f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3dc8f-105">Syntax</span></span>


```C++
HRESULT BreakConnect();
```



## <a name="parameters"></a><span data-ttu-id="3dc8f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3dc8f-106">Parameters</span></span>

<span data-ttu-id="3dc8f-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="3dc8f-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3dc8f-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="3dc8f-108">Return value</span></span>

<span data-ttu-id="3dc8f-109">Retourne S \_ OK ou une autre valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3dc8f-109">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3dc8f-110">Notes </span><span class="sxs-lookup"><span data-stu-id="3dc8f-110">Remarks</span></span>

<span data-ttu-id="3dc8f-111">Cette méthode remplace la méthode [**CBaseInputPin :: BreakConnect**](cbaseinputpin-breakconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="3dc8f-111">This method overrides the [**CBaseInputPin::BreakConnect**](cbaseinputpin-breakconnect.md) method.</span></span> <span data-ttu-id="3dc8f-112">Elle appelle la méthode [**CTransformFilter :: BreakConnect**](ctransformfilter-breakconnect.md) du filtre, qui retourne la valeur \_ OK dans la classe de base.</span><span class="sxs-lookup"><span data-stu-id="3dc8f-112">It calls the filter's [**CTransformFilter::BreakConnect**](ctransformfilter-breakconnect.md) method, which returns S\_OK in the base class.</span></span> <span data-ttu-id="3dc8f-113">La classe dérivée peut substituer la méthode **CTransformFilter :: BreakConnect** .</span><span class="sxs-lookup"><span data-stu-id="3dc8f-113">The derived class can override the **CTransformFilter::BreakConnect** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="3dc8f-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3dc8f-114">Requirements</span></span>



| <span data-ttu-id="3dc8f-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3dc8f-115">Requirement</span></span> | <span data-ttu-id="3dc8f-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="3dc8f-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3dc8f-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="3dc8f-117">Header</span></span><br/>  | <dl> <span data-ttu-id="3dc8f-118"><dt>Transfrm. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3dc8f-118"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="3dc8f-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3dc8f-119">Library</span></span><br/> | <dl> <span data-ttu-id="3dc8f-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="3dc8f-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




