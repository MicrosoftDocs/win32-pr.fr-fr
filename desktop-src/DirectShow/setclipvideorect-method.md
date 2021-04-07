---
description: La méthode SetClipVideoRect fait un zoom de l’affichage vidéo sur le sous-rectangle spécifié.
ms.assetid: 3940a382-8d53-4ff9-b024-38de1aa00f54
title: Méthode SetClipVideoRect
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ff7f4b003ef20b82f1e783ebf074e8bbd5cc793
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746293"
---
# <a name="setclipvideorect-method"></a><span data-ttu-id="ca114-103">Méthode SetClipVideoRect</span><span class="sxs-lookup"><span data-stu-id="ca114-103">SetClipVideoRect Method</span></span>

> [!Note]  
> <span data-ttu-id="ca114-104">Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="ca114-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="ca114-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="ca114-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="ca114-106">La `SetClipVideoRect` méthode effectue un zoom de l’affichage vidéo sur le sous-rectangle spécifié.</span><span class="sxs-lookup"><span data-stu-id="ca114-106">The `SetClipVideoRect` method zooms the video display to the specified subrectangle.</span></span>

``` syntax
MSWebDVD.SetClipVideoRect(oRect)
```

## <a name="parameters"></a><span data-ttu-id="ca114-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ca114-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca114-108"><span id="oRect"></span><span id="orect"></span><span id="ORECT"></span>*oRect*</span><span class="sxs-lookup"><span data-stu-id="ca114-108"><span id="oRect"></span><span id="orect"></span><span id="ORECT"></span>*oRect*</span></span>
</dt> <dd>

<span data-ttu-id="ca114-109">Spécifie un objet [DVDRect](dvdrect-object.md) , qui contient le rectangle de découpage.</span><span class="sxs-lookup"><span data-stu-id="ca114-109">Specifies a [DVDRect](dvdrect-object.md) object, which contains the clipping rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca114-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ca114-110">Return Value</span></span>

<span data-ttu-id="ca114-111">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="ca114-111">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ca114-112">Notes</span><span class="sxs-lookup"><span data-stu-id="ca114-112">Remarks</span></span>

<span data-ttu-id="ca114-113">Lorsque vous définissez un nouveau rectangle de découpage, l’objet agrandit cette zone pour s’ajuster aux dimensions d’affichage globales de l’application.</span><span class="sxs-lookup"><span data-stu-id="ca114-113">When you set a new clipping rectangle, the object enlarges that area to fit within the application's overall display dimensions.</span></span> <span data-ttu-id="ca114-114">Cela crée l’effet de zoom avant sur une zone particulière de l’écran.</span><span class="sxs-lookup"><span data-stu-id="ca114-114">This creates the effect zooming in on a particular area of the screen.</span></span> <span data-ttu-id="ca114-115">Pour spécifier le rectangle, créez un nouvel objet [DVDRect](dvdrect-object.md) et renseignez ses propriétés.</span><span class="sxs-lookup"><span data-stu-id="ca114-115">To specify the rectangle, create a new [DVDRect](dvdrect-object.md) object and fill in its properties.</span></span>

<span data-ttu-id="ca114-116">Le rectangle le plus courant pour l’affichage vidéo est 720 x 540.</span><span class="sxs-lookup"><span data-stu-id="ca114-116">The most common rectangle for video display is 720 x 540.</span></span>

## <a name="see-also"></a><span data-ttu-id="ca114-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ca114-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca114-118">**GetClipVideoRect**</span><span class="sxs-lookup"><span data-stu-id="ca114-118">**GetClipVideoRect**</span></span>](getclipvideorect-method.md)
</dt> </dl>

 

 



