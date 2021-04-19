---
description: La méthode GetMemoryHDC récupère un handle vers le contexte de périphérique (DC) de mémoire.
ms.assetid: 2c22015f-5948-4e1a-92c7-36f232816175
title: Méthode CBaseWindow. GetMemoryHDC (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.GetMemoryHDC
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c255ac8734f364597c09fc15b4aa543b1ec0a0da
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542575"
---
# <a name="cbasewindowgetmemoryhdc-method"></a><span data-ttu-id="a69bf-103">Méthode CBaseWindow. GetMemoryHDC</span><span class="sxs-lookup"><span data-stu-id="a69bf-103">CBaseWindow.GetMemoryHDC method</span></span>

<span data-ttu-id="a69bf-104">La `GetMemoryHDC` méthode récupère un handle vers le contexte de périphérique (DC) de mémoire.</span><span class="sxs-lookup"><span data-stu-id="a69bf-104">The `GetMemoryHDC` method retrieves a handle to the memory device context (DC).</span></span>

## <a name="syntax"></a><span data-ttu-id="a69bf-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a69bf-105">Syntax</span></span>


```C++
virtual HDC GetMemoryHDC();
```



## <a name="parameters"></a><span data-ttu-id="a69bf-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a69bf-106">Parameters</span></span>

<span data-ttu-id="a69bf-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="a69bf-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a69bf-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a69bf-108">Return value</span></span>

<span data-ttu-id="a69bf-109">Retourne un handle vers le DC de mémoire.</span><span class="sxs-lookup"><span data-stu-id="a69bf-109">Returns a handle to the memory DC.</span></span>

## <a name="requirements"></a><span data-ttu-id="a69bf-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a69bf-110">Requirements</span></span>



| <span data-ttu-id="a69bf-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a69bf-111">Requirement</span></span> | <span data-ttu-id="a69bf-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="a69bf-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a69bf-113">En-tête</span><span class="sxs-lookup"><span data-stu-id="a69bf-113">Header</span></span><br/>  | <dl> <span data-ttu-id="a69bf-114"><dt>Winutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a69bf-114"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a69bf-115">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a69bf-115">Library</span></span><br/> | <dl> <span data-ttu-id="a69bf-116"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="a69bf-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a69bf-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a69bf-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a69bf-118">**CBaseWindow, classe**</span><span class="sxs-lookup"><span data-stu-id="a69bf-118">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




