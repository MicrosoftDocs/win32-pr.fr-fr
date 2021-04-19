---
description: La méthode SetRealize spécifie si la fenêtre réalise des palettes.
ms.assetid: ab4a6069-c11f-4126-93bf-6de5277970a1
title: Méthode CBaseWindow. SetRealize (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.SetRealize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 587e54cdbbbf57ddb4cf52e2d5dfb916acaee22d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541761"
---
# <a name="cbasewindowsetrealize-method"></a><span data-ttu-id="60b0f-103">Méthode CBaseWindow. SetRealize</span><span class="sxs-lookup"><span data-stu-id="60b0f-103">CBaseWindow.SetRealize method</span></span>

<span data-ttu-id="60b0f-104">La `SetRealize` méthode spécifie si la fenêtre réalise des palettes.</span><span class="sxs-lookup"><span data-stu-id="60b0f-104">The `SetRealize` method specifies whether the window realizes palettes.</span></span>

## <a name="syntax"></a><span data-ttu-id="60b0f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="60b0f-105">Syntax</span></span>


```C++
void SetRealize(
   BOOL bRealize
);
```



## <a name="parameters"></a><span data-ttu-id="60b0f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="60b0f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60b0f-107">*bRealize*</span><span class="sxs-lookup"><span data-stu-id="60b0f-107">*bRealize*</span></span> 
</dt> <dd>

<span data-ttu-id="60b0f-108">Valeur booléenne qui spécifie s’il faut réaliser des palettes.</span><span class="sxs-lookup"><span data-stu-id="60b0f-108">Boolean value that specifies whether to realize palettes.</span></span> <span data-ttu-id="60b0f-109">Si la **valeur est true**, la méthode [**CBaseWindow :: SetPalette**](cbasewindow-setpalette.md) réalise des palettes.</span><span class="sxs-lookup"><span data-stu-id="60b0f-109">If **TRUE**, the [**CBaseWindow::SetPalette**](cbasewindow-setpalette.md) method realizes palettes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60b0f-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="60b0f-110">Return value</span></span>

<span data-ttu-id="60b0f-111">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="60b0f-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="60b0f-112">Notes</span><span class="sxs-lookup"><span data-stu-id="60b0f-112">Remarks</span></span>

<span data-ttu-id="60b0f-113">Par défaut, la méthode **SetPalette** réalise la palette spécifiée.</span><span class="sxs-lookup"><span data-stu-id="60b0f-113">By default, the **SetPalette** method realizes the specified palette.</span></span> <span data-ttu-id="60b0f-114">Appelez cette méthode pour modifier le comportement par défaut, afin que les palettes soient sélectionnées mais pas réalisées.</span><span class="sxs-lookup"><span data-stu-id="60b0f-114">Call this method to change the default behavior, so that palettes are selected but not realized.</span></span> <span data-ttu-id="60b0f-115">Cette méthode définit la variable de membre [**CBaseWindow :: m \_ bNoRealize**](cbasewindow-m-bnorealize.md) .</span><span class="sxs-lookup"><span data-stu-id="60b0f-115">This method sets the [**CBaseWindow::m\_bNoRealize**](cbasewindow-m-bnorealize.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="60b0f-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="60b0f-116">Requirements</span></span>



| <span data-ttu-id="60b0f-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="60b0f-117">Requirement</span></span> | <span data-ttu-id="60b0f-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="60b0f-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60b0f-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="60b0f-119">Header</span></span><br/>  | <dl> <span data-ttu-id="60b0f-120"><dt>Winutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="60b0f-120"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="60b0f-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="60b0f-121">Library</span></span><br/> | <dl> <span data-ttu-id="60b0f-122"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="60b0f-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60b0f-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="60b0f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60b0f-124">**CBaseWindow, classe**</span><span class="sxs-lookup"><span data-stu-id="60b0f-124">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




