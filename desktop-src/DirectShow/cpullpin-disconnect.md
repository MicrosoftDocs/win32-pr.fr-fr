---
description: La méthode Disconnect interrompt la connexion avec la broche de sortie.
ms.assetid: 6e362e32-7b74-4392-b46f-1ab47a30a07b
title: CPullPin. Disconnect, méthode (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.Disconnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ec13a7f29a06bab4f79ddb58932796f8363adadc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540005"
---
# <a name="cpullpindisconnect-method"></a><span data-ttu-id="65187-103">CPullPin. Disconnect, méthode</span><span class="sxs-lookup"><span data-stu-id="65187-103">CPullPin.Disconnect method</span></span>

<span data-ttu-id="65187-104">La `Disconnect` méthode interrompt la connexion avec la broche de sortie.</span><span class="sxs-lookup"><span data-stu-id="65187-104">The `Disconnect` method breaks the connection with the output pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="65187-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="65187-105">Syntax</span></span>


```C++
HRESULT Disconnect();
```



## <a name="parameters"></a><span data-ttu-id="65187-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="65187-106">Parameters</span></span>

<span data-ttu-id="65187-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="65187-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="65187-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="65187-108">Return value</span></span>

<span data-ttu-id="65187-109">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="65187-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="65187-110">Notes</span><span class="sxs-lookup"><span data-stu-id="65187-110">Remarks</span></span>

<span data-ttu-id="65187-111">Cette méthode interrompt toute connexion effectuée dans la méthode [**CPullPin :: Connect**](cpullpin-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="65187-111">This method breaks any connection made in the [**CPullPin::Connect**](cpullpin-connect.md) method.</span></span> <span data-ttu-id="65187-112">Appelez cette méthode à l’intérieur de votre méthode [**IPIN ::D éconnecter**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect) .</span><span class="sxs-lookup"><span data-stu-id="65187-112">Call this method inside your [**IPin::Disconnect**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect) method.</span></span> <span data-ttu-id="65187-113">(Si votre code confidentiel est dérivé de [**CBasePin**](cbasepin.md), remplacez [**CBasePin :: BreakConnect**](cbasepin-breakconnect.md) pour appeler cette méthode.)</span><span class="sxs-lookup"><span data-stu-id="65187-113">(If your pin derives from [**CBasePin**](cbasepin.md), override [**CBasePin::BreakConnect**](cbasepin-breakconnect.md) to call this method.)</span></span>

## <a name="requirements"></a><span data-ttu-id="65187-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="65187-114">Requirements</span></span>



| <span data-ttu-id="65187-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="65187-115">Requirement</span></span> | <span data-ttu-id="65187-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="65187-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65187-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="65187-117">Header</span></span><br/>  | <dl> <span data-ttu-id="65187-118"><dt>Pullpin. h</dt></span><span class="sxs-lookup"><span data-stu-id="65187-118"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="65187-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="65187-119">Library</span></span><br/> | <dl> <span data-ttu-id="65187-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="65187-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65187-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="65187-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65187-122">**CPullPin, classe**</span><span class="sxs-lookup"><span data-stu-id="65187-122">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 




