---
description: La méthode d’extraction de la \_ hauteur récupère la hauteur de la fenêtre active.
ms.assetid: 841c7d5d-f633-41fb-9cde-6126cd1cab9b
title: Méthode CBaseControlWindow.get_Height (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_Height
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bed7beaac064ce9d97b9c93264eab8d56b27c9df
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537973"
---
# <a name="cbasecontrolwindowget_height-method"></a><span data-ttu-id="3b9ba-103">CBaseControlWindow. obtient la \_ méthode Height</span><span class="sxs-lookup"><span data-stu-id="3b9ba-103">CBaseControlWindow.get\_Height method</span></span>

<span data-ttu-id="3b9ba-104">La `get_Height` méthode récupère la hauteur de la fenêtre actuelle.</span><span class="sxs-lookup"><span data-stu-id="3b9ba-104">The `get_Height` method retrieves the current window height.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b9ba-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3b9ba-105">Syntax</span></span>


```C++
HRESULT get_Height(
   long *pHeight
);
```



## <a name="parameters"></a><span data-ttu-id="3b9ba-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3b9ba-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b9ba-107">*pHeight*</span><span class="sxs-lookup"><span data-stu-id="3b9ba-107">*pHeight*</span></span> 
</dt> <dd>

<span data-ttu-id="3b9ba-108">Pointeur vers la hauteur de la fenêtre active, en pixels.</span><span class="sxs-lookup"><span data-stu-id="3b9ba-108">Pointer to the current window height, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b9ba-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3b9ba-109">Return value</span></span>

<span data-ttu-id="3b9ba-110">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="3b9ba-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3b9ba-111">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3b9ba-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b9ba-112">Notes</span><span class="sxs-lookup"><span data-stu-id="3b9ba-112">Remarks</span></span>

<span data-ttu-id="3b9ba-113">La fenêtre a une position sur le bureau.</span><span class="sxs-lookup"><span data-stu-id="3b9ba-113">The window has a position on the desktop.</span></span> <span data-ttu-id="3b9ba-114">Ce pourcentage est exprimé en pixels par quatre coordonnées (gauche, haut, droit et bas).</span><span class="sxs-lookup"><span data-stu-id="3b9ba-114">This is expressed in pixels by four coordinates (left, top, right, and bottom).</span></span> <span data-ttu-id="3b9ba-115">Les interfaces automatisées par OLE expriment généralement cette position à gauche, en haut, à largeur et en hauteur ; Il s’agit de la Convention utilisée dans DirectShow.</span><span class="sxs-lookup"><span data-stu-id="3b9ba-115">Interfaces that are automated by OLE typically express this position through left, top, width, and height; this is the convention used in DirectShow.</span></span> <span data-ttu-id="3b9ba-116">Toutes les coordonnées sont exprimées en pixels, et la modification de toute coordonnée met immédiatement à jour la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="3b9ba-116">All coordinates are expressed in pixels, and changing any coordinate will update the window immediately.</span></span>

<span data-ttu-id="3b9ba-117">La définition des coordonnées gauche ou supérieure déplace la fenêtre vers la gauche ou vers le haut, respectivement ; ces coordonnées n’ont aucun effet sur la largeur et la hauteur de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="3b9ba-117">Setting the left or top coordinates moves the window left or up, respectively; these coordinates have no effect on the width and height of the window.</span></span> <span data-ttu-id="3b9ba-118">De même, la définition de la largeur et de la hauteur n’affecte pas les coordonnées gauche et supérieure.</span><span class="sxs-lookup"><span data-stu-id="3b9ba-118">Likewise, setting the width and height does not affect the left and top coordinates.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b9ba-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3b9ba-119">Requirements</span></span>



| <span data-ttu-id="3b9ba-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3b9ba-120">Requirement</span></span> | <span data-ttu-id="3b9ba-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="3b9ba-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b9ba-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="3b9ba-122">Header</span></span><br/>  | <dl> <span data-ttu-id="3b9ba-123"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3b9ba-123"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3b9ba-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3b9ba-124">Library</span></span><br/> | <dl> <span data-ttu-id="3b9ba-125"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="3b9ba-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b9ba-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3b9ba-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b9ba-127">**CBaseControlWindow, classe**</span><span class="sxs-lookup"><span data-stu-id="3b9ba-127">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




