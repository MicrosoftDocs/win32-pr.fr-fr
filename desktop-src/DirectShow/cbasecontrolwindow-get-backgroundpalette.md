---
description: La \_ méthode obtenir BackgroundPalette récupère la palette réalisée dans l’indicateur d’arrière-plan.
ms.assetid: cc649dbd-d049-4993-b187-4e297bef5152
title: Méthode CBaseControlWindow.get_BackgroundPalette (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_BackgroundPalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dd06bcec9b3c435370ec3f12340c1c3aede3904c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528647"
---
# <a name="cbasecontrolwindowget_backgroundpalette-method"></a><span data-ttu-id="2f200-103">Méthode CBaseControlWindow. obten \_ BackgroundPalette</span><span class="sxs-lookup"><span data-stu-id="2f200-103">CBaseControlWindow.get\_BackgroundPalette method</span></span>

<span data-ttu-id="2f200-104">La `get_BackgroundPalette` méthode récupère la palette réalisée dans l’indicateur d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="2f200-104">The `get_BackgroundPalette` method retrieves the realized palette in the background flag.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f200-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2f200-105">Syntax</span></span>


```C++
HRESULT get_BackgroundPalette(
   long *pBackgroundPalette
);
```



## <a name="parameters"></a><span data-ttu-id="2f200-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2f200-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f200-107">*pBackgroundPalette*</span><span class="sxs-lookup"><span data-stu-id="2f200-107">*pBackgroundPalette*</span></span> 
</dt> <dd>

<span data-ttu-id="2f200-108">Pointeur vers un indicateur booléen Automation (0 est désactivé, 1 est activé).</span><span class="sxs-lookup"><span data-stu-id="2f200-108">Pointer to an Automation Boolean flag (0 is off,  1 is on).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f200-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2f200-109">Return value</span></span>

<span data-ttu-id="2f200-110">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2f200-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f200-111">Notes</span><span class="sxs-lookup"><span data-stu-id="2f200-111">Remarks</span></span>

<span data-ttu-id="2f200-112">Cette fonction membre implémente la méthode [**IVideoWindow :: obten \_ BackgroundPalette**](/windows/desktop/api/Control/nf-control-ivideowindow-get_backgroundpalette) .</span><span class="sxs-lookup"><span data-stu-id="2f200-112">This member function implements the [**IVideoWindow::get\_BackgroundPalette**](/windows/desktop/api/Control/nf-control-ivideowindow-get_backgroundpalette) method.</span></span> <span data-ttu-id="2f200-113">Si une vidéo est lue dans une autre application ou un autre document, l’application peut utiliser sa propre palette.</span><span class="sxs-lookup"><span data-stu-id="2f200-113">If a video will be played within another application or document, the application might want to use its own palette.</span></span> <span data-ttu-id="2f200-114">Elle peut demander à ce que la vidéo utilise la palette de premier plan actuelle plutôt que sa propre, en affectant la valeur 1 à cet indicateur.</span><span class="sxs-lookup"><span data-stu-id="2f200-114">It can ask that the video use the current foreground palette rather than its own by setting this flag to  1.</span></span> <span data-ttu-id="2f200-115">Si cette valeur est définie sur 0, la fenêtre installe et réalise sa propre palette par défaut.</span><span class="sxs-lookup"><span data-stu-id="2f200-115">If this is set to 0, the window will install and realize its own preferred palette.</span></span> <span data-ttu-id="2f200-116">Notez que le fait de demander à la fenêtre d’utiliser une palette différente entraîne des pénalités de performances graves.</span><span class="sxs-lookup"><span data-stu-id="2f200-116">Note that asking the window to use a different palette will cause severe performance penalties.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f200-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2f200-117">Requirements</span></span>



| <span data-ttu-id="2f200-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2f200-118">Requirement</span></span> | <span data-ttu-id="2f200-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="2f200-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f200-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="2f200-120">Header</span></span><br/>  | <dl> <span data-ttu-id="2f200-121"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2f200-121"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2f200-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="2f200-122">Library</span></span><br/> | <dl> <span data-ttu-id="2f200-123"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="2f200-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f200-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2f200-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f200-125">**CBaseControlWindow, classe**</span><span class="sxs-lookup"><span data-stu-id="2f200-125">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




