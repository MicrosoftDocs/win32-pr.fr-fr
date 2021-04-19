---
description: La méthode OnClose gère les \_ messages de fermeture WM.
ms.assetid: e562add4-752e-4665-a75e-a5526fb7f045
title: CBaseWindow. OnClose, méthode (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.OnClose
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 189b08c116f66ff864ffe308befb990973c6ce43
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537401"
---
# <a name="cbasewindowonclose-method"></a><span data-ttu-id="2981c-103">CBaseWindow. OnClose, méthode</span><span class="sxs-lookup"><span data-stu-id="2981c-103">CBaseWindow.OnClose method</span></span>

<span data-ttu-id="2981c-104">La `OnClose` méthode gère les \_ messages de fermeture WM.</span><span class="sxs-lookup"><span data-stu-id="2981c-104">The `OnClose` method handles WM\_CLOSE messages.</span></span>

## <a name="syntax"></a><span data-ttu-id="2981c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2981c-105">Syntax</span></span>


```C++
virtual BOOL OnClose();
```



## <a name="parameters"></a><span data-ttu-id="2981c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2981c-106">Parameters</span></span>

<span data-ttu-id="2981c-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="2981c-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2981c-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2981c-108">Return value</span></span>

<span data-ttu-id="2981c-109">Retourne la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="2981c-109">Returns **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="2981c-110">Notes</span><span class="sxs-lookup"><span data-stu-id="2981c-110">Remarks</span></span>

<span data-ttu-id="2981c-111">Dans la classe de base, cette méthode masque simplement la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="2981c-111">In the base class, this method simply hides the window.</span></span> <span data-ttu-id="2981c-112">En règle générale, une classe dérivée remplace cette méthode afin qu’elle envoie également un événement [**EC \_ USERABORT**](ec-userabort.md) .</span><span class="sxs-lookup"><span data-stu-id="2981c-112">Typically, a derived class will override this method so that it sends an [**EC\_USERABORT**](ec-userabort.md) event as well.</span></span> <span data-ttu-id="2981c-113">Ne substituez pas la méthode pour détruire la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="2981c-113">Do not override the method to destroy the window.</span></span> <span data-ttu-id="2981c-114">Au lieu de cela, appelez la méthode [**CBaseWindow ::D onewithwindow**](cbasewindow-donewithwindow.md) lorsque le filtre propriétaire est détruit.</span><span class="sxs-lookup"><span data-stu-id="2981c-114">Instead, call the [**CBaseWindow::DoneWithWindow**](cbasewindow-donewithwindow.md) method when the owning filter is destroyed.</span></span>

## <a name="requirements"></a><span data-ttu-id="2981c-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2981c-115">Requirements</span></span>



| <span data-ttu-id="2981c-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2981c-116">Requirement</span></span> | <span data-ttu-id="2981c-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="2981c-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2981c-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="2981c-118">Header</span></span><br/>  | <dl> <span data-ttu-id="2981c-119"><dt>Winutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2981c-119"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2981c-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="2981c-120">Library</span></span><br/> | <dl> <span data-ttu-id="2981c-121"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="2981c-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2981c-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2981c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2981c-123">**CBaseWindow, classe**</span><span class="sxs-lookup"><span data-stu-id="2981c-123">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




