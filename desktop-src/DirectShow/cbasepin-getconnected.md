---
description: La méthode GetConnected récupère le pin connecté à ce code confidentiel.
ms.assetid: 7b47aa8e-55a9-45f8-aa32-902fee037c72
title: Méthode CBasePin. GetConnected (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.GetConnected
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e5c583b06a9c25126a611736002c455a2c93ed90
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537530"
---
# <a name="cbasepingetconnected-method"></a><span data-ttu-id="bd1da-103">Méthode CBasePin. GetConnected</span><span class="sxs-lookup"><span data-stu-id="bd1da-103">CBasePin.GetConnected method</span></span>

<span data-ttu-id="bd1da-104">La `GetConnected` méthode récupère le code confidentiel connecté à ce code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="bd1da-104">The `GetConnected` method retrieves the pin connected to this pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd1da-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bd1da-105">Syntax</span></span>


```C++
IPin* GetConnected();
```



## <a name="parameters"></a><span data-ttu-id="bd1da-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bd1da-106">Parameters</span></span>

<span data-ttu-id="bd1da-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="bd1da-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bd1da-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bd1da-108">Return value</span></span>

<span data-ttu-id="bd1da-109">Retourne un pointeur vers l’interface [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin) de l’autre pin.</span><span class="sxs-lookup"><span data-stu-id="bd1da-109">Returns a pointer to the other pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd1da-110">Notes</span><span class="sxs-lookup"><span data-stu-id="bd1da-110">Remarks</span></span>

<span data-ttu-id="bd1da-111">Si le code pin n’est pas connecté, cette méthode retourne la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="bd1da-111">If the pin is not connected, this method returns **NULL**.</span></span> <span data-ttu-id="bd1da-112">Appelez la méthode [**CBasePin :: IsConnected**](cbasepin-isconnected.md) pour déterminer si le code PIN est connecté.</span><span class="sxs-lookup"><span data-stu-id="bd1da-112">Call the [**CBasePin::IsConnected**](cbasepin-isconnected.md) method to determine whether the pin is connected.</span></span>

<span data-ttu-id="bd1da-113">La méthode n’appelle pas **AddRef** sur l’interface **IPIN** , de sorte que l’appelant ne doit pas libérer l’interface.</span><span class="sxs-lookup"><span data-stu-id="bd1da-113">The method does not call **AddRef** on the **IPin** interface, so the caller should not release the interface.</span></span>

## <a name="examples"></a><span data-ttu-id="bd1da-114">Exemples</span><span class="sxs-lookup"><span data-stu-id="bd1da-114">Examples</span></span>

<span data-ttu-id="bd1da-115">Étant donné que le décompte de références n’est pas incrémenté sur le pointeur retourné, vous pouvez chaîner des appels de méthode ensemble :</span><span class="sxs-lookup"><span data-stu-id="bd1da-115">Because the reference count is not incremented on the returned pointer, you can chain method calls together:</span></span>


```C++
if (m_MyPin->IsConnected())
{
    m_MyPin->GetConnected()->EndOfStream();
}
```



<span data-ttu-id="bd1da-116">Ce modèle de codage est très pratique ; mais comme l’illustre l’exemple, vous devez veiller à ne pas déréférencer un pointeur **null** lorsque le code confidentiel n’est pas connecté.</span><span class="sxs-lookup"><span data-stu-id="bd1da-116">This coding pattern is very convenient; but as the example shows, you must be careful not to dereference a **NULL** pointer when the pin is unconnected.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd1da-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bd1da-117">Requirements</span></span>



| <span data-ttu-id="bd1da-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bd1da-118">Requirement</span></span> | <span data-ttu-id="bd1da-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="bd1da-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd1da-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="bd1da-120">Header</span></span><br/>  | <dl> <span data-ttu-id="bd1da-121"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bd1da-121"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="bd1da-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="bd1da-122">Library</span></span><br/> | <dl> <span data-ttu-id="bd1da-123"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="bd1da-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd1da-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bd1da-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd1da-125">**CBasePin, classe**</span><span class="sxs-lookup"><span data-stu-id="bd1da-125">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




