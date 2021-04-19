---
description: La \_ méthode put Left définit la coordonnée gauche de la fenêtre.
ms.assetid: 4ba6b243-e7a7-4c41-a2c5-248b05b42f4f
title: Méthode CBaseControlWindow.put_Left (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_Left
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e1dcd56bc10e60d263ce385246a6ea01aee721bf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106538001"
---
# <a name="cbasecontrolwindowput_left-method"></a><span data-ttu-id="0109e-103">CBaseControlWindow. put \_ Left, méthode</span><span class="sxs-lookup"><span data-stu-id="0109e-103">CBaseControlWindow.put\_Left method</span></span>

<span data-ttu-id="0109e-104">La `put_Left` méthode définit la coordonnée gauche de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="0109e-104">The `put_Left` method sets the left coordinate for the window.</span></span>

## <a name="syntax"></a><span data-ttu-id="0109e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0109e-105">Syntax</span></span>


```C++
HRESULT put_Left(
   long Left
);
```



## <a name="parameters"></a><span data-ttu-id="0109e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0109e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0109e-107">*Left*</span><span class="sxs-lookup"><span data-stu-id="0109e-107">*Left*</span></span> 
</dt> <dd>

<span data-ttu-id="0109e-108">Nouvelle coordonnée gauche, en pixels.</span><span class="sxs-lookup"><span data-stu-id="0109e-108">New left coordinate, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0109e-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0109e-109">Return value</span></span>

<span data-ttu-id="0109e-110">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0109e-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0109e-111">Notes</span><span class="sxs-lookup"><span data-stu-id="0109e-111">Remarks</span></span>

<span data-ttu-id="0109e-112">La fenêtre a une position sur le bureau.</span><span class="sxs-lookup"><span data-stu-id="0109e-112">The window has a position on the desktop.</span></span> <span data-ttu-id="0109e-113">Ce pourcentage est exprimé en pixels par quatre coordonnées (gauche, haut, droit et bas).</span><span class="sxs-lookup"><span data-stu-id="0109e-113">This is expressed in pixels by four coordinates (left, top, right, and bottom).</span></span> <span data-ttu-id="0109e-114">Les interfaces automatisées par OLE expriment généralement cette position à gauche, en haut, à largeur et en hauteur ; Il s’agit de la Convention utilisée dans DirectShow.</span><span class="sxs-lookup"><span data-stu-id="0109e-114">Interfaces that are automated by OLE typically express this position through left, top, width, and height; this is the convention used in DirectShow.</span></span> <span data-ttu-id="0109e-115">Toutes les coordonnées sont exprimées en pixels, et la modification de toute coordonnée met immédiatement à jour la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="0109e-115">All coordinates are expressed in pixels, and changing any coordinate will update the window immediately.</span></span>

<span data-ttu-id="0109e-116">La définition des coordonnées gauche ou supérieure déplace la fenêtre vers la gauche ou vers le haut, respectivement ; ces coordonnées n’ont aucun effet sur la largeur et la hauteur de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="0109e-116">Setting the left or top coordinates moves the window left or up, respectively; these coordinates have no effect on the width and height of the window.</span></span> <span data-ttu-id="0109e-117">De même, la définition de la largeur et de la hauteur n’affecte pas les coordonnées gauche et supérieure.</span><span class="sxs-lookup"><span data-stu-id="0109e-117">Likewise, setting the width and height does not affect the left and top coordinates.</span></span>

## <a name="requirements"></a><span data-ttu-id="0109e-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0109e-118">Requirements</span></span>



| <span data-ttu-id="0109e-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0109e-119">Requirement</span></span> | <span data-ttu-id="0109e-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="0109e-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0109e-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="0109e-121">Header</span></span><br/>  | <dl> <span data-ttu-id="0109e-122"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0109e-122"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0109e-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0109e-123">Library</span></span><br/> | <dl> <span data-ttu-id="0109e-124"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="0109e-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0109e-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0109e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0109e-126">**CBaseControlWindow, classe**</span><span class="sxs-lookup"><span data-stu-id="0109e-126">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




