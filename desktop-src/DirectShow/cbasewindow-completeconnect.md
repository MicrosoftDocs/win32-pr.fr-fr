---
description: La méthode CompleteConnect notifie la fenêtre que la broche d’entrée du convertisseur a été connectée.
ms.assetid: 82347ded-eb37-4360-9333-7c837d532115
title: Méthode CBaseWindow. CompleteConnect (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 15d5719ab78c3e95cd0128d4075797221af1f4c2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528417"
---
# <a name="cbasewindowcompleteconnect-method"></a><span data-ttu-id="e6a10-103">Méthode CBaseWindow. CompleteConnect</span><span class="sxs-lookup"><span data-stu-id="e6a10-103">CBaseWindow.CompleteConnect method</span></span>

<span data-ttu-id="e6a10-104">La `CompleteConnect` méthode notifie la fenêtre que la broche d’entrée du convertisseur a été connectée.</span><span class="sxs-lookup"><span data-stu-id="e6a10-104">The `CompleteConnect` method notifies the window that the renderer's input pin has been connected.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6a10-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e6a10-105">Syntax</span></span>


```C++
HRESULT CompleteConnect();
```



## <a name="parameters"></a><span data-ttu-id="e6a10-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e6a10-106">Parameters</span></span>

<span data-ttu-id="e6a10-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="e6a10-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e6a10-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e6a10-108">Return value</span></span>

<span data-ttu-id="e6a10-109">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e6a10-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6a10-110">Notes</span><span class="sxs-lookup"><span data-stu-id="e6a10-110">Remarks</span></span>

<span data-ttu-id="e6a10-111">Cette méthode réinitialise l’indicateur d’activation de la fenêtre ([**CBaseWindow :: m \_ bActivated**](cbasewindow-m-bactivated.md)) sur **false**.</span><span class="sxs-lookup"><span data-stu-id="e6a10-111">This method resets the window activation flag ([**CBaseWindow::m\_bActivated**](cbasewindow-m-bactivated.md)) to **FALSE**.</span></span> <span data-ttu-id="e6a10-112">Lorsqu’un convertisseur vidéo termine une connexion de code confidentiel, il peut appeler la méthode [**CBaseWindow :: ActivateWindow**](cbasewindow-activatewindow.md) pour définir la taille et la position de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="e6a10-112">When a video renderer completes a pin connection, it might call the [**CBaseWindow::ActivateWindow**](cbasewindow-activatewindow.md) method to set the window's size and position.</span></span> <span data-ttu-id="e6a10-113">Pour forcer **ActivateWindow** à recalculer ces attributs, appelez d’abord la `CompleteConnect` méthode.</span><span class="sxs-lookup"><span data-stu-id="e6a10-113">To force **ActivateWindow** to recalculate these attributes, first call the `CompleteConnect` method.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6a10-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e6a10-114">Requirements</span></span>



| <span data-ttu-id="e6a10-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e6a10-115">Requirement</span></span> | <span data-ttu-id="e6a10-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="e6a10-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6a10-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="e6a10-117">Header</span></span><br/>  | <dl> <span data-ttu-id="e6a10-118"><dt>Winutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e6a10-118"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e6a10-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e6a10-119">Library</span></span><br/> | <dl> <span data-ttu-id="e6a10-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="e6a10-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6a10-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e6a10-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6a10-122">**CBaseWindow, classe**</span><span class="sxs-lookup"><span data-stu-id="e6a10-122">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




