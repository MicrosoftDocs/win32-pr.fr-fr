---
description: 'Méthode CTransformOutputPin. BreakConnect : la méthode BreakConnect libère le code confidentiel d’une connexion.'
ms.assetid: bf68aca3-93e5-4f9d-9980-1a5eed1513f5
title: Méthode CTransformOutputPin. BreakConnect (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.BreakConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 92854041e1d553945d0a1ab1755ef3557bd4a8b2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084957"
---
# <a name="ctransformoutputpinbreakconnect-method"></a><span data-ttu-id="08d46-103">Méthode CTransformOutputPin. BreakConnect</span><span class="sxs-lookup"><span data-stu-id="08d46-103">CTransformOutputPin.BreakConnect method</span></span>

<span data-ttu-id="08d46-104">La `BreakConnect` méthode libère le code confidentiel d’une connexion.</span><span class="sxs-lookup"><span data-stu-id="08d46-104">The `BreakConnect` method releases the pin from a connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="08d46-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="08d46-105">Syntax</span></span>


```C++
HRESULT BreakConnect();
```



## <a name="parameters"></a><span data-ttu-id="08d46-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="08d46-106">Parameters</span></span>

<span data-ttu-id="08d46-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="08d46-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="08d46-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="08d46-108">Return value</span></span>

<span data-ttu-id="08d46-109">Retourne S \_ OK ou une autre valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="08d46-109">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="08d46-110">Notes </span><span class="sxs-lookup"><span data-stu-id="08d46-110">Remarks</span></span>

<span data-ttu-id="08d46-111">Cette méthode remplace la méthode [**CBaseOutputPin :: BreakConnect**](cbaseoutputpin-breakconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="08d46-111">This method overrides the [**CBaseOutputPin::BreakConnect**](cbaseoutputpin-breakconnect.md) method.</span></span> <span data-ttu-id="08d46-112">Elle appelle la méthode [**CTransformFilter :: BreakConnect**](ctransformfilter-breakconnect.md) du filtre, qui retourne la valeur \_ OK dans la classe de base.</span><span class="sxs-lookup"><span data-stu-id="08d46-112">It calls the filter's [**CTransformFilter::BreakConnect**](ctransformfilter-breakconnect.md) method, which returns S\_OK in the base class.</span></span> <span data-ttu-id="08d46-113">La classe dérivée peut substituer la méthode **CTransformFilter :: BreakConnect** .</span><span class="sxs-lookup"><span data-stu-id="08d46-113">The derived class can override the **CTransformFilter::BreakConnect** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="08d46-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="08d46-114">Requirements</span></span>



| <span data-ttu-id="08d46-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="08d46-115">Requirement</span></span> | <span data-ttu-id="08d46-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="08d46-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08d46-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="08d46-117">Header</span></span><br/>  | <dl> <span data-ttu-id="08d46-118"><dt>Transfrm. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="08d46-118"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="08d46-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="08d46-119">Library</span></span><br/> | <dl> <span data-ttu-id="08d46-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="08d46-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




