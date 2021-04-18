---
description: La méthode obtenir une \_ légende récupère le titre de la fenêtre active.
ms.assetid: 51ce9cf8-0b2a-4459-b005-02dc45444fd8
title: Méthode CBaseControlWindow.get_Caption (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_Caption
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b8d743c746f833007d91afd4346f7f48c6218dde
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533012"
---
# <a name="cbasecontrolwindowget_caption-method"></a><span data-ttu-id="d7273-103">CBaseControlWindow. obten, \_ méthode de légende</span><span class="sxs-lookup"><span data-stu-id="d7273-103">CBaseControlWindow.get\_Caption method</span></span>

<span data-ttu-id="d7273-104">La `get_Caption` méthode récupère le titre de la fenêtre active.</span><span class="sxs-lookup"><span data-stu-id="d7273-104">The `get_Caption` method retrieves the current window caption.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7273-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d7273-105">Syntax</span></span>


```C++
HRESULT get_Caption(
   BSTR *pstrCaption
);
```



## <a name="parameters"></a><span data-ttu-id="d7273-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d7273-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7273-107">*pstrCaption*</span><span class="sxs-lookup"><span data-stu-id="d7273-107">*pstrCaption*</span></span> 
</dt> <dd>

<span data-ttu-id="d7273-108">Pointeur vers le titre de la fenêtre active.</span><span class="sxs-lookup"><span data-stu-id="d7273-108">Pointer to the current window caption.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7273-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d7273-109">Return value</span></span>

<span data-ttu-id="d7273-110">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d7273-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7273-111">Notes</span><span class="sxs-lookup"><span data-stu-id="d7273-111">Remarks</span></span>

<span data-ttu-id="d7273-112">La plupart des fenêtres de niveau supérieur sur un bureau Windows ont un titre (légende) qui leur est associé.</span><span class="sxs-lookup"><span data-stu-id="d7273-112">Most top-level windows on a Windows-based desktop have a title (caption) associated with them.</span></span> <span data-ttu-id="d7273-113">Cette propriété peut être interrogée et définie par le biais de l’interface [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) .</span><span class="sxs-lookup"><span data-stu-id="d7273-113">This property can be queried and set through the [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) interface.</span></span> <span data-ttu-id="d7273-114">Tout jeu de légendes est visible uniquement si le style de légende WS est appliqué à la fenêtre \_ .</span><span class="sxs-lookup"><span data-stu-id="d7273-114">Any caption set will be visible only if the window has the WS\_CAPTION style applied.</span></span> <span data-ttu-id="d7273-115">Si ce n’est pas le cas, la légende peut toujours être définie (et Récupérée), bien qu’elle ne soit pas visible par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d7273-115">If it does not, the caption can still be set (and retrieved), although it will not be visible to the user.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7273-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d7273-116">Requirements</span></span>



| <span data-ttu-id="d7273-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d7273-117">Requirement</span></span> | <span data-ttu-id="d7273-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="d7273-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7273-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="d7273-119">Header</span></span><br/>  | <dl> <span data-ttu-id="d7273-120"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d7273-120"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d7273-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d7273-121">Library</span></span><br/> | <dl> <span data-ttu-id="d7273-122"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="d7273-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7273-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d7273-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7273-124">**CBaseControlWindow, classe**</span><span class="sxs-lookup"><span data-stu-id="d7273-124">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




