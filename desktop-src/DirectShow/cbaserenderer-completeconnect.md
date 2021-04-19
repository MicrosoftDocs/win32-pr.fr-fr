---
description: La méthode CompleteConnect termine la connexion de la broche d’entrée à une autre broche.
ms.assetid: 8dfc1a50-bc73-436a-a471-d8d3218410d3
title: Méthode CBaseRenderer. CompleteConnect (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a9d2d35f99a3b3b8dc5b668b8ee9a9f94f0a53dd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106536046"
---
# <a name="cbaserenderercompleteconnect-method"></a><span data-ttu-id="1615a-103">Méthode CBaseRenderer. CompleteConnect</span><span class="sxs-lookup"><span data-stu-id="1615a-103">CBaseRenderer.CompleteConnect method</span></span>

<span data-ttu-id="1615a-104">La `CompleteConnect` méthode termine la connexion de la broche d’entrée à une autre broche.</span><span class="sxs-lookup"><span data-stu-id="1615a-104">The `CompleteConnect` method completes the input pin's connection to another pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="1615a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1615a-105">Syntax</span></span>


```C++
virtual HRESULT CompleteConnect(
   IPin *pReceivePin
);
```



## <a name="parameters"></a><span data-ttu-id="1615a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1615a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1615a-107">*pReceivePin*</span><span class="sxs-lookup"><span data-stu-id="1615a-107">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="1615a-108">Pointeur vers l’interface [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin) de la broche de sortie.</span><span class="sxs-lookup"><span data-stu-id="1615a-108">Pointer to the output pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1615a-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1615a-109">Return value</span></span>

<span data-ttu-id="1615a-110">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1615a-110">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="1615a-111">Notes</span><span class="sxs-lookup"><span data-stu-id="1615a-111">Remarks</span></span>

<span data-ttu-id="1615a-112">La broche d’entrée du filtre appelle cette méthode à l’intérieur de sa propre `CompleteConnect` méthode, qui est appelée pour terminer une connexion de code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="1615a-112">The filter's input pin calls this method from inside its own `CompleteConnect` method, which is called in order to complete a pin connection.</span></span> <span data-ttu-id="1615a-113">(Pour plus d’informations, consultez [**CBasePin :: CompleteConnect**](cbasepin-completeconnect.md).) Le filtre appelle la méthode [**CBaseRenderer :: SetRepaintStatus**](cbaserenderer-setrepaintstatus.md) pour activer les événements de [**\_ redessin ce**](ec-repaint.md) .</span><span class="sxs-lookup"><span data-stu-id="1615a-113">(For more information, see [**CBasePin::CompleteConnect**](cbasepin-completeconnect.md).) The filter calls the [**CBaseRenderer::SetRepaintStatus**](cbaserenderer-setrepaintstatus.md) method to enable [**EC\_REPAINT**](ec-repaint.md) events.</span></span>

## <a name="requirements"></a><span data-ttu-id="1615a-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1615a-114">Requirements</span></span>



| <span data-ttu-id="1615a-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1615a-115">Requirement</span></span> | <span data-ttu-id="1615a-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="1615a-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1615a-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="1615a-117">Header</span></span><br/>  | <dl> <span data-ttu-id="1615a-118"><dt>Renbase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1615a-118"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1615a-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1615a-119">Library</span></span><br/> | <dl> <span data-ttu-id="1615a-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="1615a-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1615a-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1615a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1615a-122">**CBaseRenderer, classe**</span><span class="sxs-lookup"><span data-stu-id="1615a-122">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




