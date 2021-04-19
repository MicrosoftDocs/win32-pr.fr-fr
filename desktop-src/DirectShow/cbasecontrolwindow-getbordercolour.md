---
description: La méthode GetBorderColour récupère la couleur de bordure de la fenêtre active, m \_ BorderColour.
ms.assetid: 5cd9b834-5438-475e-9671-ee9917f9a485
title: Méthode CBaseControlWindow. GetBorderColour (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.GetBorderColour
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0ba6e1be9babf96d03235c49d9cde0f11cae1b83
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528805"
---
# <a name="cbasecontrolwindowgetbordercolour-method"></a><span data-ttu-id="5e718-103">Méthode CBaseControlWindow. GetBorderColour</span><span class="sxs-lookup"><span data-stu-id="5e718-103">CBaseControlWindow.GetBorderColour method</span></span>

<span data-ttu-id="5e718-104">La `GetBorderColour` méthode récupère la couleur de bordure de la fenêtre active, **m \_ BorderColour**.</span><span class="sxs-lookup"><span data-stu-id="5e718-104">The `GetBorderColour` method retrieves the current window border color, **m\_BorderColour**.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e718-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5e718-105">Syntax</span></span>


```C++
COLORREF GetBorderColour();
```



## <a name="parameters"></a><span data-ttu-id="5e718-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5e718-106">Parameters</span></span>

<span data-ttu-id="5e718-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="5e718-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5e718-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5e718-108">Return value</span></span>

<span data-ttu-id="5e718-109">Retourne la couleur de la bordure.</span><span class="sxs-lookup"><span data-stu-id="5e718-109">Returns the color of the border.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e718-110">Notes</span><span class="sxs-lookup"><span data-stu-id="5e718-110">Remarks</span></span>

<span data-ttu-id="5e718-111">Une application peut définir un rectangle de destination pour afficher la vidéo.</span><span class="sxs-lookup"><span data-stu-id="5e718-111">An application can set a destination rectangle to display the video.</span></span> <span data-ttu-id="5e718-112">Ce rectangle doit être relatif à la zone cliente pour la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="5e718-112">This rectangle should be relative to the client area for the window.</span></span> <span data-ttu-id="5e718-113">Si cette opération est effectuée (la valeur par défaut consiste à toujours peindre la totalité de la fenêtre), il y a une zone qui entoure la vidéo ; autrement dit, la bordure.</span><span class="sxs-lookup"><span data-stu-id="5e718-113">If this is done (the default is to always paint the entire window), there is an area that surrounds the video; that is, the border.</span></span> <span data-ttu-id="5e718-114">La couleur de bordure peut être définie à l’aide de la fonction membre [**CBaseControlWindow ::p ut \_ BorderColor**](cbasecontrolwindow-put-bordercolor.md) .</span><span class="sxs-lookup"><span data-stu-id="5e718-114">The border color can be set through the [**CBaseControlWindow::put\_BorderColor**](cbasecontrolwindow-put-bordercolor.md) member function.</span></span> <span data-ttu-id="5e718-115">Cette propriété affecte la couleur de la bordure.</span><span class="sxs-lookup"><span data-stu-id="5e718-115">This property affects the color of the border.</span></span> <span data-ttu-id="5e718-116">Utilisez cette fonction membre à la place de [**CBaseControlWindow :: obten \_ BorderColor**](cbasecontrolwindow-get-bordercolor.md), sauf si vous appelez cette méthode en externe via la méthode [**IVideoWindow :: obten \_ BorderColor**](/windows/desktop/api/Control/nf-control-ivideowindow-get_bordercolor) .</span><span class="sxs-lookup"><span data-stu-id="5e718-116">Use this member function instead of [**CBaseControlWindow::get\_BorderColor**](cbasecontrolwindow-get-bordercolor.md), unless you are calling this externally through the [**IVideoWindow::get\_BorderColor**](/windows/desktop/api/Control/nf-control-ivideowindow-get_bordercolor) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e718-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5e718-117">Requirements</span></span>



| <span data-ttu-id="5e718-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5e718-118">Requirement</span></span> | <span data-ttu-id="5e718-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="5e718-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e718-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="5e718-120">Header</span></span><br/>  | <dl> <span data-ttu-id="5e718-121"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5e718-121"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5e718-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5e718-122">Library</span></span><br/> | <dl> <span data-ttu-id="5e718-123"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="5e718-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e718-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5e718-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e718-125">**CBaseControlWindow, classe**</span><span class="sxs-lookup"><span data-stu-id="5e718-125">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




