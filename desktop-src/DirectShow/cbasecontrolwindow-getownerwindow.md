---
description: La méthode GetOwnerWindow récupère le handle de fenêtre propriétaire, m \_ hwndOwner.
ms.assetid: fa576b42-b4a7-4374-8ba4-7d21e86d9d61
title: Méthode CBaseControlWindow. GetOwnerWindow (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.GetOwnerWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4e4d3811f85abd68bcd7d625dce0e9e8963be39a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533069"
---
# <a name="cbasecontrolwindowgetownerwindow-method"></a><span data-ttu-id="0784e-103">Méthode CBaseControlWindow. GetOwnerWindow</span><span class="sxs-lookup"><span data-stu-id="0784e-103">CBaseControlWindow.GetOwnerWindow method</span></span>

<span data-ttu-id="0784e-104">La `GetOwnerWindow` méthode récupère le handle de fenêtre propriétaire, **m \_ hwndOwner**.</span><span class="sxs-lookup"><span data-stu-id="0784e-104">The `GetOwnerWindow` method retrieves the owning window handle, **m\_hwndOwner**.</span></span>

## <a name="syntax"></a><span data-ttu-id="0784e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0784e-105">Syntax</span></span>


```C++
HWND GetOwnerWindow();
```



## <a name="parameters"></a><span data-ttu-id="0784e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0784e-106">Parameters</span></span>

<span data-ttu-id="0784e-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="0784e-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0784e-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0784e-108">Return value</span></span>

<span data-ttu-id="0784e-109">Retourne la fenêtre propriétaire.</span><span class="sxs-lookup"><span data-stu-id="0784e-109">Returns the owner window.</span></span>

## <a name="remarks"></a><span data-ttu-id="0784e-110">Notes</span><span class="sxs-lookup"><span data-stu-id="0784e-110">Remarks</span></span>

<span data-ttu-id="0784e-111">Récupère la fenêtre propriétaire sans appeler la méthode d’interface.</span><span class="sxs-lookup"><span data-stu-id="0784e-111">Retrieves the owning window without calling the interface method.</span></span> <span data-ttu-id="0784e-112">Utilisez cette fonction membre à la place de [**CBaseControlWindow :: obten \_ owner**](cbasecontrolwindow-get-owner.md), sauf si vous appelez cette méthode en externe par le biais de la méthode [**IVideoWindow :: d’extraction de \_ propriétaire**](/windows/desktop/api/Control/nf-control-ivideowindow-get_owner) .</span><span class="sxs-lookup"><span data-stu-id="0784e-112">Use this member function instead of [**CBaseControlWindow::get\_Owner**](cbasecontrolwindow-get-owner.md), unless you are calling this externally through the [**IVideoWindow::get\_Owner**](/windows/desktop/api/Control/nf-control-ivideowindow-get_owner) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="0784e-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0784e-113">Requirements</span></span>



| <span data-ttu-id="0784e-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0784e-114">Requirement</span></span> | <span data-ttu-id="0784e-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="0784e-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0784e-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="0784e-116">Header</span></span><br/>  | <dl> <span data-ttu-id="0784e-117"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0784e-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0784e-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0784e-118">Library</span></span><br/> | <dl> <span data-ttu-id="0784e-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="0784e-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0784e-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0784e-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0784e-121">**CBaseControlWindow, classe**</span><span class="sxs-lookup"><span data-stu-id="0784e-121">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




