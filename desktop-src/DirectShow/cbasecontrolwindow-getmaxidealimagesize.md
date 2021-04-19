---
description: La méthode GetMaxIdealImageSize récupère la taille d’image maximale idéale.
ms.assetid: 881c1c3d-7505-44a2-964d-3255e2072f6b
title: Méthode CBaseControlWindow. GetMaxIdealImageSize (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.GetMaxIdealImageSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bc8ac53dd30c62f3ebb50585677f83f356b593f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541117"
---
# <a name="cbasecontrolwindowgetmaxidealimagesize-method"></a><span data-ttu-id="10cdf-103">Méthode CBaseControlWindow. GetMaxIdealImageSize</span><span class="sxs-lookup"><span data-stu-id="10cdf-103">CBaseControlWindow.GetMaxIdealImageSize method</span></span>

<span data-ttu-id="10cdf-104">La `GetMaxIdealImageSize` méthode récupère la taille d’image idéale maximale.</span><span class="sxs-lookup"><span data-stu-id="10cdf-104">The `GetMaxIdealImageSize` method retrieves the maximum ideal image size.</span></span>

## <a name="syntax"></a><span data-ttu-id="10cdf-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="10cdf-105">Syntax</span></span>


```C++
HRESULT GetMaxIdealImageSize(
   long *pWidth,
   long *pHeight
);
```



## <a name="parameters"></a><span data-ttu-id="10cdf-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="10cdf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10cdf-107">*pWidth*</span><span class="sxs-lookup"><span data-stu-id="10cdf-107">*pWidth*</span></span> 
</dt> <dd>

<span data-ttu-id="10cdf-108">Pointeur vers la largeur idéale maximale, en pixels.</span><span class="sxs-lookup"><span data-stu-id="10cdf-108">Pointer to the maximum ideal width, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="10cdf-109">*pHeight*</span><span class="sxs-lookup"><span data-stu-id="10cdf-109">*pHeight*</span></span> 
</dt> <dd>

<span data-ttu-id="10cdf-110">Pointeur vers la hauteur maximale idéale, en pixels.</span><span class="sxs-lookup"><span data-stu-id="10cdf-110">Pointer to the maximum ideal height, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10cdf-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="10cdf-111">Return value</span></span>

<span data-ttu-id="10cdf-112">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="10cdf-112">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="10cdf-113">Notes</span><span class="sxs-lookup"><span data-stu-id="10cdf-113">Remarks</span></span>

<span data-ttu-id="10cdf-114">Différents convertisseurs présentent des restrictions de performances quant à la taille des images qu’ils peuvent afficher.</span><span class="sxs-lookup"><span data-stu-id="10cdf-114">Various renderers have performance restrictions on the size of images they can display.</span></span> <span data-ttu-id="10cdf-115">Bien qu’ils doivent toujours fonctionner correctement lorsqu’ils sont invités à afficher des images plus volumineuses que la valeur maximale spécifiée, les convertisseurs peuvent désigner les tailles idéales minimales et maximales par le biais de l’interface [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) .</span><span class="sxs-lookup"><span data-stu-id="10cdf-115">Although they should still function properly when requested to display images larger than the specified maximum, renderers can nominate the minimum and maximum ideal sizes through the [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) interface.</span></span> <span data-ttu-id="10cdf-116">Cette interface peut être appelée uniquement lorsque le graphique de filtre est suspendu ou en cours d’exécution, car ce n’est pas jusqu’à ce que les ressources soient allouées et que le convertisseur puisse reconnaître ses restrictions.</span><span class="sxs-lookup"><span data-stu-id="10cdf-116">This interface can be called only when the filter graph is paused or running, because it is not until then that resources are allocated and the renderer can recognize its restrictions.</span></span> <span data-ttu-id="10cdf-117">S’il n’existe aucune restriction, le convertisseur remplit les paramètres *pWidth* et *pHeight* avec les dimensions Native Video et retourne S \_ false.</span><span class="sxs-lookup"><span data-stu-id="10cdf-117">If no restrictions exist, the renderer fills in the *pWidth* and *pHeight* parameters with the native video dimensions and returns S\_FALSE.</span></span> <span data-ttu-id="10cdf-118">S’il existe des restrictions, la largeur et la hauteur restreintes sont entrées, et la fonction membre retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="10cdf-118">If restrictions do exist, the restricted width and height are entered, and the member function returns S\_OK.</span></span>

<span data-ttu-id="10cdf-119">Les dimensions s’appliquent à la taille de la vidéo de destination et non à la taille globale de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="10cdf-119">The dimensions apply to the size of the destination video and not to the overall window size.</span></span> <span data-ttu-id="10cdf-120">Ainsi, lors du calcul de la taille de la fenêtre à définir, comptez pour les styles de fenêtre actuels (par exemple, WS \_ Caption et WS \_ Border).</span><span class="sxs-lookup"><span data-stu-id="10cdf-120">So, when calculating the size of the window to set, account for the current window styles (for example, WS\_CAPTION and WS\_BORDER).</span></span>

## <a name="requirements"></a><span data-ttu-id="10cdf-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="10cdf-121">Requirements</span></span>



| <span data-ttu-id="10cdf-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="10cdf-122">Requirement</span></span> | <span data-ttu-id="10cdf-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="10cdf-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10cdf-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="10cdf-124">Header</span></span><br/>  | <dl> <span data-ttu-id="10cdf-125"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="10cdf-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="10cdf-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="10cdf-126">Library</span></span><br/> | <dl> <span data-ttu-id="10cdf-127"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="10cdf-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10cdf-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="10cdf-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10cdf-129">**CBaseControlWindow, classe**</span><span class="sxs-lookup"><span data-stu-id="10cdf-129">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




