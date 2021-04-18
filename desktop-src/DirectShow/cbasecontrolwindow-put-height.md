---
description: La \_ méthode put Height définit la hauteur de la fenêtre.
ms.assetid: 11026ee5-e83a-4d82-9069-a302d55a2d46
title: Méthode CBaseControlWindow.put_Height (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_Height
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 798719c60b830caebee348032abce3e39a742e38
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526419"
---
# <a name="cbasecontrolwindowput_height-method"></a><span data-ttu-id="5e2c4-103">CBaseControlWindow. put \_ Height, méthode</span><span class="sxs-lookup"><span data-stu-id="5e2c4-103">CBaseControlWindow.put\_Height method</span></span>

<span data-ttu-id="5e2c4-104">La `put_Height` méthode définit la hauteur de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="5e2c4-104">The `put_Height` method sets the window height.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e2c4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5e2c4-105">Syntax</span></span>


```C++
HRESULT put_Height(
   long Height
);
```



## <a name="parameters"></a><span data-ttu-id="5e2c4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5e2c4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e2c4-107">*Height*</span><span class="sxs-lookup"><span data-stu-id="5e2c4-107">*Height*</span></span> 
</dt> <dd>

<span data-ttu-id="5e2c4-108">Nouvelle hauteur de la fenêtre, en pixels.</span><span class="sxs-lookup"><span data-stu-id="5e2c4-108">New window height, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e2c4-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5e2c4-109">Return value</span></span>

<span data-ttu-id="5e2c4-110">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5e2c4-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e2c4-111">Notes</span><span class="sxs-lookup"><span data-stu-id="5e2c4-111">Remarks</span></span>

<span data-ttu-id="5e2c4-112">La fenêtre a une position sur le bureau.</span><span class="sxs-lookup"><span data-stu-id="5e2c4-112">The window has a position on the desktop.</span></span> <span data-ttu-id="5e2c4-113">Ce pourcentage est exprimé en pixels par quatre coordonnées (gauche, haut, droit et bas).</span><span class="sxs-lookup"><span data-stu-id="5e2c4-113">This is expressed in pixels by four coordinates (left, top, right, and bottom).</span></span> <span data-ttu-id="5e2c4-114">Les interfaces automatisées par OLE expriment généralement cette position à gauche, en haut, à largeur et en hauteur ; Il s’agit de la Convention utilisée dans DirectShow.</span><span class="sxs-lookup"><span data-stu-id="5e2c4-114">Interfaces that are automated by OLE typically express this position through left, top, width, and height; this is the convention used in DirectShow.</span></span> <span data-ttu-id="5e2c4-115">Toutes les coordonnées sont exprimées en pixels, et la modification de toute coordonnée met immédiatement à jour la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="5e2c4-115">All coordinates are expressed in pixels, and changing any coordinate will update the window immediately.</span></span>

<span data-ttu-id="5e2c4-116">La définition des coordonnées gauche ou supérieure déplace la fenêtre vers la gauche ou vers le haut, respectivement ; ces coordonnées n’ont aucun effet sur la largeur et la hauteur de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="5e2c4-116">Setting the left or top coordinates moves the window left or up, respectively; these coordinates have no effect on the width and height of the window.</span></span> <span data-ttu-id="5e2c4-117">De même, la définition de la largeur et de la hauteur n’affecte pas les coordonnées gauche et supérieure.</span><span class="sxs-lookup"><span data-stu-id="5e2c4-117">Likewise, setting the width and height does not affect the left and top coordinates.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e2c4-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5e2c4-118">Requirements</span></span>



| <span data-ttu-id="5e2c4-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5e2c4-119">Requirement</span></span> | <span data-ttu-id="5e2c4-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="5e2c4-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e2c4-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="5e2c4-121">Header</span></span><br/>  | <dl> <span data-ttu-id="5e2c4-122"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5e2c4-122"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5e2c4-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5e2c4-123">Library</span></span><br/> | <dl> <span data-ttu-id="5e2c4-124"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="5e2c4-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e2c4-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5e2c4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e2c4-126">**CBaseControlWindow, classe**</span><span class="sxs-lookup"><span data-stu-id="5e2c4-126">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




