---
description: La méthode de vidage indique à la classe de base que le code pin a démarré ou a arrêté le vidage.
ms.assetid: a3c000e1-18a1-48f7-9e2e-fe63cf13fc5c
title: CBaseStreamControl. Flush, méthode (Strmctl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.Flushing
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5d4a3a2375ca799f5dd35def03295f29f61c0583
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525549"
---
# <a name="cbasestreamcontrolflushing-method"></a><span data-ttu-id="1807e-103">CBaseStreamControl. Flush, méthode</span><span class="sxs-lookup"><span data-stu-id="1807e-103">CBaseStreamControl.Flushing method</span></span>

<span data-ttu-id="1807e-104">La `Flushing` méthode notifie la classe de base que le code confidentiel a démarré ou a arrêté le vidage.</span><span class="sxs-lookup"><span data-stu-id="1807e-104">The `Flushing` method notifies the base class that the pin has started or stopped flushing.</span></span>

## <a name="syntax"></a><span data-ttu-id="1807e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1807e-105">Syntax</span></span>


```C++
void Flushing(
   BOOL bInProgress
);
```



## <a name="parameters"></a><span data-ttu-id="1807e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1807e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1807e-107">*bInProgress*</span><span class="sxs-lookup"><span data-stu-id="1807e-107">*bInProgress*</span></span> 
</dt> <dd>

<span data-ttu-id="1807e-108">Spécifie une valeur booléenne qui indique si le code PIN est vidé.</span><span class="sxs-lookup"><span data-stu-id="1807e-108">Specifies a Boolean value that indicates whether the pin is flushing.</span></span> <span data-ttu-id="1807e-109">Utilisez la valeur **true** lorsque le code PIN commence une opération de vidage, et **false** lorsque le code PIN met fin à une opération de vidage.</span><span class="sxs-lookup"><span data-stu-id="1807e-109">Use the value **TRUE** when the pin begins a flush operation, and **FALSE** when the pin ends a flush operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1807e-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1807e-110">Return value</span></span>

<span data-ttu-id="1807e-111">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="1807e-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1807e-112">Notes</span><span class="sxs-lookup"><span data-stu-id="1807e-112">Remarks</span></span>

<span data-ttu-id="1807e-113">Le code confidentiel doit appeler cette méthode à partir de ses méthodes [**IPIN :: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) et [**IPIN :: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) .</span><span class="sxs-lookup"><span data-stu-id="1807e-113">The pin must call this method from within its [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) and [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) methods.</span></span> <span data-ttu-id="1807e-114">Spécifiez **true** dans **BeginFlush** et **false** dans **EndFlush**.</span><span class="sxs-lookup"><span data-stu-id="1807e-114">Specify **TRUE** in **BeginFlush** and **FALSE** in **EndFlush**.</span></span>

<span data-ttu-id="1807e-115">Cette méthode provoque l’arrêt de l’attente de la méthode [**CBaseStreamControl :: CheckStreamState**](cbasestreamcontrol-checkstreamstate.md) .</span><span class="sxs-lookup"><span data-stu-id="1807e-115">This method causes the [**CBaseStreamControl::CheckStreamState**](cbasestreamcontrol-checkstreamstate.md) method to stop waiting.</span></span> <span data-ttu-id="1807e-116">Pendant le vidage du code PIN, **CheckStreamState** retourne toujours le flux \_ ignoré.</span><span class="sxs-lookup"><span data-stu-id="1807e-116">While the pin is flushing, **CheckStreamState** always returns STREAM\_DISCARDING.</span></span>

## <a name="requirements"></a><span data-ttu-id="1807e-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1807e-117">Requirements</span></span>



| <span data-ttu-id="1807e-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1807e-118">Requirement</span></span> | <span data-ttu-id="1807e-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="1807e-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1807e-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="1807e-120">Header</span></span><br/>  | <dl> <span data-ttu-id="1807e-121"><dt>Strmctl. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1807e-121"><dt>Strmctl.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1807e-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1807e-122">Library</span></span><br/> | <dl> <span data-ttu-id="1807e-123"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="1807e-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1807e-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1807e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1807e-125">**CBaseStreamControl, classe**</span><span class="sxs-lookup"><span data-stu-id="1807e-125">**CBaseStreamControl Class**</span></span>](cbasestreamcontrol.md)
</dt> </dl>

 

 




