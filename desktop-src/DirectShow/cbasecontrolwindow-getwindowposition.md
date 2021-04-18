---
description: La méthode GetWindowPosition récupère les coordonnées actuelles de la fenêtre.
ms.assetid: a2f46a87-b2cd-450f-8d2b-0f8695432fda
title: Méthode CBaseControlWindow. GetWindowPosition (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.GetWindowPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: af2b1bdb8b2c839644e8c0629e3e272c123d3c21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526088"
---
# <a name="cbasecontrolwindowgetwindowposition-method"></a><span data-ttu-id="5d46c-103">Méthode CBaseControlWindow. GetWindowPosition</span><span class="sxs-lookup"><span data-stu-id="5d46c-103">CBaseControlWindow.GetWindowPosition method</span></span>

<span data-ttu-id="5d46c-104">La `GetWindowPosition` méthode récupère les coordonnées actuelles de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="5d46c-104">The `GetWindowPosition` method retrieves the current coordinates for the window.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d46c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5d46c-105">Syntax</span></span>


```C++
HRESULT GetWindowPosition(
   long *pLeft,
   long *pTop,
   long *pWidth,
   long *pHeight
);
```



## <a name="parameters"></a><span data-ttu-id="5d46c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5d46c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d46c-107">*pLeft*</span><span class="sxs-lookup"><span data-stu-id="5d46c-107">*pLeft*</span></span> 
</dt> <dd>

<span data-ttu-id="5d46c-108">Pointeur vers la coordonnée gauche, en coordonnées d’écran.</span><span class="sxs-lookup"><span data-stu-id="5d46c-108">Pointer to the left coordinate, in screen coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="5d46c-109">*pTop*</span><span class="sxs-lookup"><span data-stu-id="5d46c-109">*pTop*</span></span> 
</dt> <dd>

<span data-ttu-id="5d46c-110">Pointeur vers la coordonnée supérieure, en coordonnées d’écran.</span><span class="sxs-lookup"><span data-stu-id="5d46c-110">Pointer to the top coordinate, in screen coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="5d46c-111">*pWidth*</span><span class="sxs-lookup"><span data-stu-id="5d46c-111">*pWidth*</span></span> 
</dt> <dd>

<span data-ttu-id="5d46c-112">Pointeur vers la largeur de la fenêtre, en coordonnées d’écran.</span><span class="sxs-lookup"><span data-stu-id="5d46c-112">Pointer to the window width, in screen coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="5d46c-113">*pHeight*</span><span class="sxs-lookup"><span data-stu-id="5d46c-113">*pHeight*</span></span> 
</dt> <dd>

<span data-ttu-id="5d46c-114">Pointeur vers la hauteur de la fenêtre, en coordonnées d’écran.</span><span class="sxs-lookup"><span data-stu-id="5d46c-114">Pointer to the window height, in screen coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d46c-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5d46c-115">Return value</span></span>

<span data-ttu-id="5d46c-116">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5d46c-116">Returns an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d46c-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5d46c-117">Requirements</span></span>



| <span data-ttu-id="5d46c-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5d46c-118">Requirement</span></span> | <span data-ttu-id="5d46c-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="5d46c-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d46c-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="5d46c-120">Header</span></span><br/>  | <dl> <span data-ttu-id="5d46c-121"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5d46c-121"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5d46c-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5d46c-122">Library</span></span><br/> | <dl> <span data-ttu-id="5d46c-123"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="5d46c-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d46c-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5d46c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d46c-125">**CBaseControlWindow, classe**</span><span class="sxs-lookup"><span data-stu-id="5d46c-125">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




