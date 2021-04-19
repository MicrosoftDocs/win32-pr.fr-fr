---
description: La méthode PaintWindow provoque la redessin de la fenêtre.
ms.assetid: dce3d782-00e5-4176-9365-378d59d48ebc
title: Méthode CBaseWindow. PaintWindow (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.PaintWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3b0932422f85cb31d587485976dfacbaa51e2bf7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539250"
---
# <a name="cbasewindowpaintwindow-method"></a><span data-ttu-id="aea60-103">Méthode CBaseWindow. PaintWindow</span><span class="sxs-lookup"><span data-stu-id="aea60-103">CBaseWindow.PaintWindow method</span></span>

<span data-ttu-id="aea60-104">La `PaintWindow` méthode permet de redessiner la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="aea60-104">The `PaintWindow` method causes the window to be repainted.</span></span>

## <a name="syntax"></a><span data-ttu-id="aea60-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="aea60-105">Syntax</span></span>


```C++
void PaintWindow(
   BOOL bErase
);
```



## <a name="parameters"></a><span data-ttu-id="aea60-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="aea60-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aea60-107">*bErase*</span><span class="sxs-lookup"><span data-stu-id="aea60-107">*bErase*</span></span> 
</dt> <dd>

<span data-ttu-id="aea60-108">Valeur booléenne qui spécifie si l’arrière-plan est effacé.</span><span class="sxs-lookup"><span data-stu-id="aea60-108">Boolean value that specifies whether the background is erased.</span></span> <span data-ttu-id="aea60-109">Si la valeur est **true**, l’arrière-plan est effacé.</span><span class="sxs-lookup"><span data-stu-id="aea60-109">If the value is **TRUE**, the background is erased.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aea60-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="aea60-110">Return value</span></span>

<span data-ttu-id="aea60-111">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="aea60-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="aea60-112">Notes</span><span class="sxs-lookup"><span data-stu-id="aea60-112">Remarks</span></span>

<span data-ttu-id="aea60-113">Cette méthode génère un \_ message WM Paint en invalidant la zone cliente entière de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="aea60-113">This method generates a WM\_PAINT message by invalidating the window's entire client area.</span></span>

## <a name="requirements"></a><span data-ttu-id="aea60-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="aea60-114">Requirements</span></span>



| <span data-ttu-id="aea60-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="aea60-115">Requirement</span></span> | <span data-ttu-id="aea60-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="aea60-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aea60-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="aea60-117">Header</span></span><br/>  | <dl> <span data-ttu-id="aea60-118"><dt>Winutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="aea60-118"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="aea60-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="aea60-119">Library</span></span><br/> | <dl> <span data-ttu-id="aea60-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="aea60-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aea60-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aea60-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aea60-122">**CBaseWindow, classe**</span><span class="sxs-lookup"><span data-stu-id="aea60-122">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




