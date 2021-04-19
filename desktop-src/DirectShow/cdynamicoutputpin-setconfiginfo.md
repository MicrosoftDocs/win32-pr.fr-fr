---
description: La méthode SetConfigInfo spécifie le pointeur IGraphConfig et l’événement stop.
ms.assetid: 938fe8be-5622-4954-9ba3-31fc68fbfa31
title: Méthode CDynamicOutputPin. SetConfigInfo (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.SetConfigInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b0c14342a629a38a878649ac59d8f1f814874f12
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106522796"
---
# <a name="cdynamicoutputpinsetconfiginfo-method"></a><span data-ttu-id="1b00e-103">Méthode CDynamicOutputPin. SetConfigInfo</span><span class="sxs-lookup"><span data-stu-id="1b00e-103">CDynamicOutputPin.SetConfigInfo method</span></span>

<span data-ttu-id="1b00e-104">La `SetConfigInfo` méthode spécifie le pointeur [**IGraphConfig**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig) et l’événement stop.</span><span class="sxs-lookup"><span data-stu-id="1b00e-104">The `SetConfigInfo` method specifies the [**IGraphConfig**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig) pointer and the stop event.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b00e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1b00e-105">Syntax</span></span>


```C++
void SetConfigInfo(
   IGraphConfig *pGraphConfig,
   HANDLE       hStopEvent
);
```



## <a name="parameters"></a><span data-ttu-id="1b00e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1b00e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b00e-107">*pGraphConfig*</span><span class="sxs-lookup"><span data-stu-id="1b00e-107">*pGraphConfig*</span></span> 
</dt> <dd>

<span data-ttu-id="1b00e-108">Pointeur vers l’interface [**IGraphConfig**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig) , ou **null**.</span><span class="sxs-lookup"><span data-stu-id="1b00e-108">Pointer to the [**IGraphConfig**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig) interface, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="1b00e-109">*hStopEvent*</span><span class="sxs-lookup"><span data-stu-id="1b00e-109">*hStopEvent*</span></span> 
</dt> <dd>

<span data-ttu-id="1b00e-110">Handle vers un événement qui est signalé lorsque le filtre s’arrête, ou **null**.</span><span class="sxs-lookup"><span data-stu-id="1b00e-110">Handle to an event that is signaled when the filter stops, or **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b00e-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1b00e-111">Return value</span></span>

<span data-ttu-id="1b00e-112">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="1b00e-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1b00e-113">Notes</span><span class="sxs-lookup"><span data-stu-id="1b00e-113">Remarks</span></span>

<span data-ttu-id="1b00e-114">Le filtre doit appeler cette méthode lorsqu’il rejoint le graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="1b00e-114">The filter must call this method when it joins the filter graph.</span></span> <span data-ttu-id="1b00e-115">Le gestionnaire de graphes de filtres prend en charge **IGraphConfig**.</span><span class="sxs-lookup"><span data-stu-id="1b00e-115">The filter graph manager supports **IGraphConfig**.</span></span> <span data-ttu-id="1b00e-116">Pour le paramètre *hStopEvent* , créez un événement de réinitialisation manuelle.</span><span class="sxs-lookup"><span data-stu-id="1b00e-116">For the *hStopEvent* parameter, create a manual-reset event.</span></span> <span data-ttu-id="1b00e-117">Lorsque le filtre quitte le graphique de filtre, appelez à nouveau cette méthode avec la **valeur null** pour les deux paramètres.</span><span class="sxs-lookup"><span data-stu-id="1b00e-117">When the filter leaves the filter graph, call this method again with **NULL** for both parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b00e-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1b00e-118">Requirements</span></span>



| <span data-ttu-id="1b00e-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1b00e-119">Requirement</span></span> | <span data-ttu-id="1b00e-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="1b00e-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b00e-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="1b00e-121">Header</span></span><br/>  | <dl> <span data-ttu-id="1b00e-122"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1b00e-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="1b00e-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1b00e-123">Library</span></span><br/> | <dl> <span data-ttu-id="1b00e-124"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="1b00e-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b00e-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1b00e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b00e-126">**CDynamicOutputPin, classe**</span><span class="sxs-lookup"><span data-stu-id="1b00e-126">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




