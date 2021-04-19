---
description: La méthode GetRestorePosition récupère la position vers laquelle la fenêtre sera restaurée lorsqu’elle n’est pas agrandie ou réduite.
ms.assetid: 5f129be3-c4d8-4583-bbc8-870e0bcafd80
title: Méthode CBaseControlWindow. GetRestorePosition (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.GetRestorePosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f922a97f69f4dae03d4e61a54bd99c52d69a984a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530311"
---
# <a name="cbasecontrolwindowgetrestoreposition-method"></a><span data-ttu-id="786ae-103">Méthode CBaseControlWindow. GetRestorePosition</span><span class="sxs-lookup"><span data-stu-id="786ae-103">CBaseControlWindow.GetRestorePosition method</span></span>

<span data-ttu-id="786ae-104">La `GetRestorePosition` méthode récupère la position vers laquelle la fenêtre sera restaurée lorsqu’elle n’est pas agrandie ou réduite.</span><span class="sxs-lookup"><span data-stu-id="786ae-104">The `GetRestorePosition` method retrieves the position to which the window will be restored when it is not maximized or minimized.</span></span>

## <a name="syntax"></a><span data-ttu-id="786ae-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="786ae-105">Syntax</span></span>


```C++
HRESULT GetRestorePosition(
   long *pLeft,
   long *pTop,
   long *pWidth,
   long *pHeight
);
```



## <a name="parameters"></a><span data-ttu-id="786ae-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="786ae-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="786ae-107">*pLeft*</span><span class="sxs-lookup"><span data-stu-id="786ae-107">*pLeft*</span></span> 
</dt> <dd>

<span data-ttu-id="786ae-108">Pointeur vers la valeur de la coordonnée la plus à gauche.</span><span class="sxs-lookup"><span data-stu-id="786ae-108">Pointer to the value for leftmost coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="786ae-109">*pTop*</span><span class="sxs-lookup"><span data-stu-id="786ae-109">*pTop*</span></span> 
</dt> <dd>

<span data-ttu-id="786ae-110">Pointeur vers la valeur pour le haut de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="786ae-110">Pointer to the value for top of the window.</span></span>

</dd> <dt>

<span data-ttu-id="786ae-111">*pWidth*</span><span class="sxs-lookup"><span data-stu-id="786ae-111">*pWidth*</span></span> 
</dt> <dd>

<span data-ttu-id="786ae-112">Pointeur vers la valeur pour la largeur de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="786ae-112">Pointer to the value for width of the window.</span></span>

</dd> <dt>

<span data-ttu-id="786ae-113">*pHeight*</span><span class="sxs-lookup"><span data-stu-id="786ae-113">*pHeight*</span></span> 
</dt> <dd>

<span data-ttu-id="786ae-114">Pointeur vers la valeur de la hauteur de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="786ae-114">Pointer to the value for height of window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="786ae-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="786ae-115">Return value</span></span>

<span data-ttu-id="786ae-116">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="786ae-116">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="786ae-117">Notes</span><span class="sxs-lookup"><span data-stu-id="786ae-117">Remarks</span></span>

<span data-ttu-id="786ae-118">Il s’agit des mêmes valeurs que celles retournées par la fonction [**CBaseControlWindow :: GetWindowPosition**](cbasecontrolwindow-getwindowposition.md) lorsque la fenêtre n’est ni agrandie, ni réduite.</span><span class="sxs-lookup"><span data-stu-id="786ae-118">This is the same as the values returned by the [**CBaseControlWindow::GetWindowPosition**](cbasecontrolwindow-getwindowposition.md) function when the window is neither maximized nor minimized.</span></span>

## <a name="requirements"></a><span data-ttu-id="786ae-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="786ae-119">Requirements</span></span>



| <span data-ttu-id="786ae-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="786ae-120">Requirement</span></span> | <span data-ttu-id="786ae-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="786ae-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="786ae-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="786ae-122">Header</span></span><br/>  | <dl> <span data-ttu-id="786ae-123"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="786ae-123"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="786ae-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="786ae-124">Library</span></span><br/> | <dl> <span data-ttu-id="786ae-125"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="786ae-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="786ae-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="786ae-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="786ae-127">**CBaseControlWindow, classe**</span><span class="sxs-lookup"><span data-stu-id="786ae-127">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




