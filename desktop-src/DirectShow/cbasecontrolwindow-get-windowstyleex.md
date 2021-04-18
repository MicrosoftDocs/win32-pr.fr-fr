---
description: La \_ méthode obtenir WindowStyleEx récupère les styles de fenêtre étendus.
ms.assetid: 72955958-bbda-4b8f-9c28-6d3f5eb56a82
title: Méthode CBaseControlWindow.get_WindowStyleEx (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_WindowStyleEx
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c59336ab57e92e99366494a272f2b995191b494b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528985"
---
# <a name="cbasecontrolwindowget_windowstyleex-method"></a><span data-ttu-id="5fa35-103">Méthode CBaseControlWindow. obten \_ WindowStyleEx</span><span class="sxs-lookup"><span data-stu-id="5fa35-103">CBaseControlWindow.get\_WindowStyleEx method</span></span>

<span data-ttu-id="5fa35-104">La `get_WindowStyleEx` méthode récupère les styles de fenêtre étendus.</span><span class="sxs-lookup"><span data-stu-id="5fa35-104">The `get_WindowStyleEx` method retrieves the extended window styles.</span></span>

## <a name="syntax"></a><span data-ttu-id="5fa35-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5fa35-105">Syntax</span></span>


```C++
HRESULT get_WindowStyleEx(
   long *pWindowStyleEx
);
```



## <a name="parameters"></a><span data-ttu-id="5fa35-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5fa35-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5fa35-107">*pWindowStyleEx*</span><span class="sxs-lookup"><span data-stu-id="5fa35-107">*pWindowStyleEx*</span></span> 
</dt> <dd>

<span data-ttu-id="5fa35-108">Pointeur vers les styles de fenêtre étendus.</span><span class="sxs-lookup"><span data-stu-id="5fa35-108">Pointer to extended window styles.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5fa35-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5fa35-109">Return value</span></span>

<span data-ttu-id="5fa35-110">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5fa35-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5fa35-111">Notes</span><span class="sxs-lookup"><span data-stu-id="5fa35-111">Remarks</span></span>

<span data-ttu-id="5fa35-112">Cette fonction membre récupère les styles de fenêtre étendus.</span><span class="sxs-lookup"><span data-stu-id="5fa35-112">This member function retrieves the extended window styles.</span></span> <span data-ttu-id="5fa35-113">Elle appelle la fonction membre [**CBaseControlWindow ::D ogetwindowstyle**](cbasecontrolwindow-dogetwindowstyle.md) .</span><span class="sxs-lookup"><span data-stu-id="5fa35-113">It calls the [**CBaseControlWindow::DoGetWindowStyle**](cbasecontrolwindow-dogetwindowstyle.md) member function.</span></span>

## <a name="requirements"></a><span data-ttu-id="5fa35-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5fa35-114">Requirements</span></span>



| <span data-ttu-id="5fa35-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5fa35-115">Requirement</span></span> | <span data-ttu-id="5fa35-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="5fa35-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5fa35-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="5fa35-117">Header</span></span><br/>  | <dl> <span data-ttu-id="5fa35-118"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5fa35-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5fa35-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5fa35-119">Library</span></span><br/> | <dl> <span data-ttu-id="5fa35-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="5fa35-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5fa35-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5fa35-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5fa35-122">**CBaseControlWindow, classe**</span><span class="sxs-lookup"><span data-stu-id="5fa35-122">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




