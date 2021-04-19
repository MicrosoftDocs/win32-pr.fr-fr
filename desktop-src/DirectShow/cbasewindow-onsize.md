---
description: La méthode OnSize gère les \_ messages de taille WM.
ms.assetid: 21d867a4-4321-478a-9beb-5d3053569369
title: Méthode CBaseWindow. OnSize (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.OnSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c9020510030d3b3d4b30e066adfe67367618fb3d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535895"
---
# <a name="cbasewindowonsize-method"></a><span data-ttu-id="5914b-103">Méthode CBaseWindow. OnSize</span><span class="sxs-lookup"><span data-stu-id="5914b-103">CBaseWindow.OnSize method</span></span>

<span data-ttu-id="5914b-104">La `OnSize` méthode gère les \_ messages de taille WM.</span><span class="sxs-lookup"><span data-stu-id="5914b-104">The `OnSize` method handles WM\_SIZE messages.</span></span>

## <a name="syntax"></a><span data-ttu-id="5914b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5914b-105">Syntax</span></span>


```C++
virtual BOOL OnSize(
   LONG Width,
   LONG Height
);
```



## <a name="parameters"></a><span data-ttu-id="5914b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5914b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5914b-107">*Width*</span><span class="sxs-lookup"><span data-stu-id="5914b-107">*Width*</span></span> 
</dt> <dd>

<span data-ttu-id="5914b-108">Largeur de la zone cliente, en pixels.</span><span class="sxs-lookup"><span data-stu-id="5914b-108">Width of the client area, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="5914b-109">*Height*</span><span class="sxs-lookup"><span data-stu-id="5914b-109">*Height*</span></span> 
</dt> <dd>

<span data-ttu-id="5914b-110">Hauteur de la zone cliente, en pixels.</span><span class="sxs-lookup"><span data-stu-id="5914b-110">Height of the client area, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5914b-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5914b-111">Return value</span></span>

<span data-ttu-id="5914b-112">Retourne la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="5914b-112">Returns **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="5914b-113">Notes</span><span class="sxs-lookup"><span data-stu-id="5914b-113">Remarks</span></span>

<span data-ttu-id="5914b-114">Cette méthode stocke les nouvelles largeur et hauteur.</span><span class="sxs-lookup"><span data-stu-id="5914b-114">This method stores the new width and height.</span></span> <span data-ttu-id="5914b-115">Pour récupérer ces valeurs, appelez les méthodes [**CBaseWindow :: GetWindowHeight**](cbasewindow-getwindowheight.md) et [**CBaseWindow :: GetWindowWidth**](cbasewindow-getwindowwidth.md) .</span><span class="sxs-lookup"><span data-stu-id="5914b-115">To retrieve these values, call the [**CBaseWindow::GetWindowHeight**](cbasewindow-getwindowheight.md) and [**CBaseWindow::GetWindowWidth**](cbasewindow-getwindowwidth.md) methods.</span></span>

## <a name="requirements"></a><span data-ttu-id="5914b-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5914b-116">Requirements</span></span>



| <span data-ttu-id="5914b-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5914b-117">Requirement</span></span> | <span data-ttu-id="5914b-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="5914b-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5914b-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="5914b-119">Header</span></span><br/>  | <dl> <span data-ttu-id="5914b-120"><dt>Winutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5914b-120"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5914b-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5914b-121">Library</span></span><br/> | <dl> <span data-ttu-id="5914b-122"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="5914b-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5914b-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5914b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5914b-124">**CBaseWindow, classe**</span><span class="sxs-lookup"><span data-stu-id="5914b-124">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




