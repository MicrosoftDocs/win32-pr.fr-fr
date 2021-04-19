---
description: La méthode GetWindowHDC récupère un handle vers le contexte de périphérique (DC) de la fenêtre.
ms.assetid: 35ee2a66-ee56-44dc-ad59-fd467bb4aa63
title: Méthode CBaseWindow. GetWindowHDC (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.GetWindowHDC
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 16c2502b3a9de587e91ff43ddc45a84ae08492db
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528512"
---
# <a name="cbasewindowgetwindowhdc-method"></a><span data-ttu-id="c664b-103">Méthode CBaseWindow. GetWindowHDC</span><span class="sxs-lookup"><span data-stu-id="c664b-103">CBaseWindow.GetWindowHDC method</span></span>

<span data-ttu-id="c664b-104">La `GetWindowHDC` méthode récupère un handle vers le contexte de périphérique (DC) de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="c664b-104">The `GetWindowHDC` method retrieves a handle to the window's device context (DC).</span></span>

## <a name="syntax"></a><span data-ttu-id="c664b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c664b-105">Syntax</span></span>


```C++
HDC GetWindowHDC();
```



## <a name="parameters"></a><span data-ttu-id="c664b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c664b-106">Parameters</span></span>

<span data-ttu-id="c664b-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="c664b-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c664b-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c664b-108">Return value</span></span>

<span data-ttu-id="c664b-109">Retourne un handle vers le DC.</span><span class="sxs-lookup"><span data-stu-id="c664b-109">Returns a handle to the DC.</span></span>

## <a name="requirements"></a><span data-ttu-id="c664b-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c664b-110">Requirements</span></span>



| <span data-ttu-id="c664b-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c664b-111">Requirement</span></span> | <span data-ttu-id="c664b-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="c664b-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c664b-113">En-tête</span><span class="sxs-lookup"><span data-stu-id="c664b-113">Header</span></span><br/>  | <dl> <span data-ttu-id="c664b-114"><dt>Winutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c664b-114"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c664b-115">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c664b-115">Library</span></span><br/> | <dl> <span data-ttu-id="c664b-116"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="c664b-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c664b-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c664b-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c664b-118">**CBaseWindow, classe**</span><span class="sxs-lookup"><span data-stu-id="c664b-118">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




