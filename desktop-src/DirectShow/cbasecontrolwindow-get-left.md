---
description: La \_ méthode obtenir la gauche récupère la coordonnée actuelle de la fenêtre de gauche.
ms.assetid: 9ee71bd3-1ff5-4574-8dcd-5ba6490d9785
title: Méthode CBaseControlWindow.get_Left (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_Left
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 04f586cede24f8ff2017ae4004fc45c584a57f4d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537609"
---
# <a name="cbasecontrolwindowget_left-method"></a><span data-ttu-id="7de90-103">CBaseControlWindow. obtient la \_ méthode Left</span><span class="sxs-lookup"><span data-stu-id="7de90-103">CBaseControlWindow.get\_Left method</span></span>

<span data-ttu-id="7de90-104">La `get_Left` méthode récupère la coordonnée de la fenêtre de gauche actuelle.</span><span class="sxs-lookup"><span data-stu-id="7de90-104">The `get_Left` method retrieves the current left window coordinate.</span></span>

## <a name="syntax"></a><span data-ttu-id="7de90-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7de90-105">Syntax</span></span>


```C++
HRESULT get_Left(
   long *pLeft
);
```



## <a name="parameters"></a><span data-ttu-id="7de90-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7de90-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7de90-107">*pLeft*</span><span class="sxs-lookup"><span data-stu-id="7de90-107">*pLeft*</span></span> 
</dt> <dd>

<span data-ttu-id="7de90-108">Pointeur vers la coordonnée gauche, en pixels.</span><span class="sxs-lookup"><span data-stu-id="7de90-108">Pointer to the left coordinate, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7de90-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7de90-109">Return value</span></span>

<span data-ttu-id="7de90-110">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7de90-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7de90-111">Notes</span><span class="sxs-lookup"><span data-stu-id="7de90-111">Remarks</span></span>

<span data-ttu-id="7de90-112">La fenêtre a une position sur le bureau.</span><span class="sxs-lookup"><span data-stu-id="7de90-112">The window has a position on the desktop.</span></span> <span data-ttu-id="7de90-113">Cette position est exprimée en pixels par quatre coordonnées (gauche, haut, droit et bas).</span><span class="sxs-lookup"><span data-stu-id="7de90-113">This position is expressed in pixels by four coordinates (left, top, right, and bottom).</span></span> <span data-ttu-id="7de90-114">Les interfaces automatisées par OLE expriment généralement cette position à gauche, en haut, à largeur et en hauteur ; Il s’agit de la Convention utilisée dans DirectShow.</span><span class="sxs-lookup"><span data-stu-id="7de90-114">Interfaces that are automated by OLE typically express this position through left, top, width, and height; this is the convention used in DirectShow.</span></span> <span data-ttu-id="7de90-115">Toutes les coordonnées sont exprimées en pixels, et la modification de toute coordonnée met immédiatement à jour la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="7de90-115">All coordinates are expressed in pixels, and changing any coordinate will update the window immediately.</span></span>

<span data-ttu-id="7de90-116">La définition des coordonnées gauche ou supérieure déplace la fenêtre vers la gauche et vers le haut, respectivement ; ces coordonnées n’ont aucun effet sur la largeur et la hauteur de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="7de90-116">Setting the left or top coordinates moves the window left and up, respectively; these coordinates have no effect on the width and height of the window.</span></span> <span data-ttu-id="7de90-117">De même, la définition de la largeur et de la hauteur n’a aucun effet sur les coordonnées gauche et supérieure.</span><span class="sxs-lookup"><span data-stu-id="7de90-117">Likewise, setting the width and height have no effect on the left and top coordinates.</span></span>

## <a name="requirements"></a><span data-ttu-id="7de90-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7de90-118">Requirements</span></span>



| <span data-ttu-id="7de90-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7de90-119">Requirement</span></span> | <span data-ttu-id="7de90-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="7de90-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7de90-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="7de90-121">Header</span></span><br/>  | <dl> <span data-ttu-id="7de90-122"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7de90-122"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7de90-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7de90-123">Library</span></span><br/> | <dl> <span data-ttu-id="7de90-124"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="7de90-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7de90-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7de90-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7de90-126">**CBaseControlWindow, classe**</span><span class="sxs-lookup"><span data-stu-id="7de90-126">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




