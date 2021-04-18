---
description: La méthode DoneWithWindow détruit la fenêtre.
ms.assetid: 03c97884-7d91-4b59-b867-dda231d2a184
title: Méthode CBaseWindow. DoneWithWindow (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.DoneWithWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cc31e893a4015aa8b4356d265ca4065ee336c3ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540349"
---
# <a name="cbasewindowdonewithwindow-method"></a><span data-ttu-id="c5913-103">Méthode CBaseWindow. DoneWithWindow</span><span class="sxs-lookup"><span data-stu-id="c5913-103">CBaseWindow.DoneWithWindow method</span></span>

<span data-ttu-id="c5913-104">La `DoneWithWindow` méthode détruit la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="c5913-104">The `DoneWithWindow` method destroys the window.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5913-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c5913-105">Syntax</span></span>


```C++
virtual HRESULT DoneWithWindow();
```



## <a name="parameters"></a><span data-ttu-id="c5913-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c5913-106">Parameters</span></span>

<span data-ttu-id="c5913-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="c5913-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c5913-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c5913-108">Return value</span></span>

<span data-ttu-id="c5913-109">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c5913-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="c5913-110">Notes</span><span class="sxs-lookup"><span data-stu-id="c5913-110">Remarks</span></span>

<span data-ttu-id="c5913-111">Appelez cette méthode à partir de la méthode de destructeur de l’objet dérivé.</span><span class="sxs-lookup"><span data-stu-id="c5913-111">Call this method from the derived object's destructor method.</span></span>

<span data-ttu-id="c5913-112">Si cette méthode est appelée à partir du même thread que celui qui a créé la fenêtre, la méthode effectue les actions suivantes :</span><span class="sxs-lookup"><span data-stu-id="c5913-112">If this method is called from the same thread that created the window, the method performs the following actions:</span></span>

-   <span data-ttu-id="c5913-113">Appelle la méthode [**CBaseWindow :: InactivateWindow**](cbasewindow-inactivatewindow.md) , qui désactive la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="c5913-113">Calls the [**CBaseWindow::InactivateWindow**](cbasewindow-inactivatewindow.md) method, which deactivates the window.</span></span>
-   <span data-ttu-id="c5913-114">Appelle la méthode [**CBaseWindow :: UninitialiseWindow**](cbasewindow-uninitialisewindow.md) , qui libère les ressources utilisées par la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="c5913-114">Calls the [**CBaseWindow::UninitialiseWindow**](cbasewindow-uninitialisewindow.md) method, which releases resources used by the window.</span></span>
-   <span data-ttu-id="c5913-115">Détruit la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="c5913-115">Destroys the window.</span></span>

<span data-ttu-id="c5913-116">Si le thread appelant `DoneWithWindow` n’est pas le thread qui a créé la fenêtre, la méthode envoie un message « détruire » privé à la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="c5913-116">If the thread calling `DoneWithWindow` is not the thread that created the window, the method sends a private "destroy" message to the window.</span></span> <span data-ttu-id="c5913-117">Quand la fenêtre reçoit ce message, elle appelle `DoneWithWindow` lui-même.</span><span class="sxs-lookup"><span data-stu-id="c5913-117">When the window receives this message, it calls `DoneWithWindow` on itself.</span></span> <span data-ttu-id="c5913-118">(Si [**CBaseWindow :: m \_ bDoPostToDestroy**](cbasewindow-m-bdoposttodestroy.md) a la **valeur true**, la fenêtre publie le message.)</span><span class="sxs-lookup"><span data-stu-id="c5913-118">(If [**CBaseWindow::m\_bDoPostToDestroy**](cbasewindow-m-bdoposttodestroy.md) is **TRUE**, the window posts the message.)</span></span>

## <a name="requirements"></a><span data-ttu-id="c5913-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c5913-119">Requirements</span></span>



| <span data-ttu-id="c5913-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c5913-120">Requirement</span></span> | <span data-ttu-id="c5913-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="c5913-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5913-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="c5913-122">Header</span></span><br/>  | <dl> <span data-ttu-id="c5913-123"><dt>Winutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c5913-123"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c5913-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c5913-124">Library</span></span><br/> | <dl> <span data-ttu-id="c5913-125"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="c5913-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5913-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c5913-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5913-127">**CBaseWindow, classe**</span><span class="sxs-lookup"><span data-stu-id="c5913-127">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




