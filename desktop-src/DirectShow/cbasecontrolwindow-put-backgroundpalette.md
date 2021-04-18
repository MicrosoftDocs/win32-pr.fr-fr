---
description: La \_ méthode put BackgroundPalette définit un indicateur pour réaliser la palette en arrière-plan.
ms.assetid: db420e75-e300-41fa-bae4-fb267cc99c7c
title: Méthode CBaseControlWindow.put_BackgroundPalette (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_BackgroundPalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 04aeb445be91426e7995ecd01c9326cda586a447
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533079"
---
# <a name="cbasecontrolwindowput_backgroundpalette-method"></a><span data-ttu-id="26c09-103">CBaseControlWindow. put \_ BackgroundPalette, méthode</span><span class="sxs-lookup"><span data-stu-id="26c09-103">CBaseControlWindow.put\_BackgroundPalette method</span></span>

<span data-ttu-id="26c09-104">La `put_BackgroundPalette` méthode définit un indicateur pour réaliser la palette en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="26c09-104">The `put_BackgroundPalette` method sets a flag to realize the palette in the background.</span></span>

## <a name="syntax"></a><span data-ttu-id="26c09-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="26c09-105">Syntax</span></span>


```C++
HRESULT put_BackgroundPalette(
   long BackgroundPalette
);
```



## <a name="parameters"></a><span data-ttu-id="26c09-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="26c09-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26c09-107">*BackgroundPalette*</span><span class="sxs-lookup"><span data-stu-id="26c09-107">*BackgroundPalette*</span></span> 
</dt> <dd>

<span data-ttu-id="26c09-108">Indicateur booléen Automation (0 est désactivé, 1 est activé).</span><span class="sxs-lookup"><span data-stu-id="26c09-108">Automation Boolean flag (0 is off,  1 is on).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26c09-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="26c09-109">Return value</span></span>

<span data-ttu-id="26c09-110">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="26c09-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="26c09-111">Notes</span><span class="sxs-lookup"><span data-stu-id="26c09-111">Remarks</span></span>

<span data-ttu-id="26c09-112">Pour lire une vidéo dans une autre application ou un autre document, l’application peut utiliser sa propre palette.</span><span class="sxs-lookup"><span data-stu-id="26c09-112">To play a video within another application or document, the application might want to use its own palette.</span></span> <span data-ttu-id="26c09-113">Il peut demander à la vidéo d’utiliser la palette de premier plan actuelle plutôt que sa propre palette en affectant la valeur 1 à cet indicateur.</span><span class="sxs-lookup"><span data-stu-id="26c09-113">It can ask that the video use the current foreground palette rather than its own as the background palette by setting this flag to  1.</span></span> <span data-ttu-id="26c09-114">Si cette valeur est définie sur 0, la fenêtre installe et réalise sa propre palette par défaut.</span><span class="sxs-lookup"><span data-stu-id="26c09-114">If this is set to 0, the window will install and realize its own preferred palette.</span></span> <span data-ttu-id="26c09-115">Si vous demandez à la fenêtre d’utiliser une palette différente, vous risquez de nuire aux performances.</span><span class="sxs-lookup"><span data-stu-id="26c09-115">Asking the window to use a different palette will cause severe performance penalties.</span></span>

## <a name="requirements"></a><span data-ttu-id="26c09-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="26c09-116">Requirements</span></span>



| <span data-ttu-id="26c09-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="26c09-117">Requirement</span></span> | <span data-ttu-id="26c09-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="26c09-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26c09-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="26c09-119">Header</span></span><br/>  | <dl> <span data-ttu-id="26c09-120"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="26c09-120"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="26c09-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="26c09-121">Library</span></span><br/> | <dl> <span data-ttu-id="26c09-122"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="26c09-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26c09-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="26c09-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26c09-124">**CBaseControlWindow, classe**</span><span class="sxs-lookup"><span data-stu-id="26c09-124">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




