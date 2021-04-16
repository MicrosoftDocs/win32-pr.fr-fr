---
description: La méthode zoom fait un zoom avant ou arrière sur un ensemble donné de coordonnées d’écran.
ms.assetid: 050f1264-8fbe-4322-970c-184275d5b219
title: Zoom, méthode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2625e6c4facf006a0d904e49068853720e20c29e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485640"
---
# <a name="zoom-method"></a><span data-ttu-id="1bcfc-103">Zoom, méthode</span><span class="sxs-lookup"><span data-stu-id="1bcfc-103">Zoom Method</span></span>

> [!Note]  
> <span data-ttu-id="1bcfc-104">Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="1bcfc-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="1bcfc-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="1bcfc-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="1bcfc-106">La `Zoom` méthode effectue un zoom avant ou arrière sur un ensemble donné de coordonnées d’écran.</span><span class="sxs-lookup"><span data-stu-id="1bcfc-106">The `Zoom` method zooms the video display in or out, centered on a given set of screen coordinates.</span></span>

``` syntax
MSWebDVD.Zoom(iXPos, iYPos, iZoomRatio)
```

## <a name="parameters"></a><span data-ttu-id="1bcfc-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1bcfc-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1bcfc-108"><span id="iXPos"></span><span id="ixpos"></span><span id="IXPOS"></span>*iXPos*</span><span class="sxs-lookup"><span data-stu-id="1bcfc-108"><span id="iXPos"></span><span id="ixpos"></span><span id="IXPOS"></span>*iXPos*</span></span>
</dt> <dd>

<span data-ttu-id="1bcfc-109">Spécifie la coordonnée x au centre de la zone de zoom rectangulaire sous la forme d’un entier.</span><span class="sxs-lookup"><span data-stu-id="1bcfc-109">Specifies the x-coordinate at the center of the rectangular zoom area as an Integer.</span></span>

</dd> <dt>

<span data-ttu-id="1bcfc-110"><span id="iYPos"></span><span id="iypos"></span><span id="IYPOS"></span>*iYPos*</span><span class="sxs-lookup"><span data-stu-id="1bcfc-110"><span id="iYPos"></span><span id="iypos"></span><span id="IYPOS"></span>*iYPos*</span></span>
</dt> <dd>

<span data-ttu-id="1bcfc-111">Spécifie la coordonnée y au centre du rectangle à faire faire un zoom sous la forme d’un entier.</span><span class="sxs-lookup"><span data-stu-id="1bcfc-111">Specifies the y-coordinate at the center of the rectangle to be zoomed as an Integer.</span></span>

</dd> <dt>

<span data-ttu-id="1bcfc-112"><span id="iZoomRatio"></span><span id="izoomratio"></span><span id="IZOOMRATIO"></span>*iZoomRatio*</span><span class="sxs-lookup"><span data-stu-id="1bcfc-112"><span id="iZoomRatio"></span><span id="izoomratio"></span><span id="IZOOMRATIO"></span>*iZoomRatio*</span></span>
</dt> <dd>

<span data-ttu-id="1bcfc-113">Spécifie le facteur d’agrandissement appliqué à la valeur de zoom actuelle sous la forme d’un entier.</span><span class="sxs-lookup"><span data-stu-id="1bcfc-113">Specifies the magnification factor applied to the current zoom value as an Integer.</span></span> <span data-ttu-id="1bcfc-114">La valeur maximale totale dépend de ce que la superposition matérielle peut prendre en charge ; Il s’agit généralement d’un facteur de 32 à 64 fois la taille d’origine.</span><span class="sxs-lookup"><span data-stu-id="1bcfc-114">The total maximum value depends on what the hardware overlay can support; this is typically a factor of 32 to 64 times the original size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1bcfc-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="1bcfc-115">Return Value</span></span>

<span data-ttu-id="1bcfc-116">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="1bcfc-116">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1bcfc-117">Notes</span><span class="sxs-lookup"><span data-stu-id="1bcfc-117">Remarks</span></span>

<span data-ttu-id="1bcfc-118">Le nouveau facteur de zoom reste en vigueur jusqu’à ce qu’il soit rétabli à sa taille d’origine ou qu’il soit de nouveau modifié.</span><span class="sxs-lookup"><span data-stu-id="1bcfc-118">The new zoom ratio stays in effect until it is restored to the original size or changed again.</span></span> <span data-ttu-id="1bcfc-119">En d’autres termes, deux appels à cette méthode spécifiant un *iZoomRatio* de deux entraînent un ratio de zoom quatre fois supérieur à la taille vidéo d’origine.</span><span class="sxs-lookup"><span data-stu-id="1bcfc-119">In other words, two calls to this method specifying an *iZoomRatio* of two will result in a zoom ratio four times larger than the original video size.</span></span> <span data-ttu-id="1bcfc-120">Si l’utilisateur tente d’effectuer un zoom au-delà de ce que le matériel peut prendre en charge, cette méthode fonctionnera, mais ne fera rien.</span><span class="sxs-lookup"><span data-stu-id="1bcfc-120">If the user tries to zoom beyond what the hardware can support, this method will succeed but do nothing.</span></span>

<span data-ttu-id="1bcfc-121">La méthode [**SetClipVideoRect**](setclipvideorect-method.md) est une autre façon d’effectuer un zoom avant. la seule différence entre les deux méthodes est la façon dont le rectangle de zoom est spécifié.</span><span class="sxs-lookup"><span data-stu-id="1bcfc-121">The [**SetClipVideoRect**](setclipvideorect-method.md) method is another way to zoom in; the only difference between the two methods is the way in which the zoom rectangle is specified.</span></span>

 

 



