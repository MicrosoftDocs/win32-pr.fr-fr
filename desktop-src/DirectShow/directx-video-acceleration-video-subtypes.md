---
description: Les sous-types suivants sont utilisés par les décodeurs qui utilisent DirectX Video Acceleration (DXVA).
ms.assetid: 031b076b-cdfa-407f-8efa-391bce3075ef
title: Sous-types vidéo DirectX Video Acceleration (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0df0f079e795638c6802570c95e2468209a7256
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525269"
---
# <a name="directx-video-acceleration-video-subtypes"></a><span data-ttu-id="e3f48-103">Sous-types vidéo DirectX Video Acceleration</span><span class="sxs-lookup"><span data-stu-id="e3f48-103">DirectX Video Acceleration Video Subtypes</span></span>

<span data-ttu-id="e3f48-104">Les sous-types suivants sont utilisés par les décodeurs qui utilisent DirectX Video Acceleration (DXVA).</span><span class="sxs-lookup"><span data-stu-id="e3f48-104">The following subtypes are used by decoders that are using DirectX Video Acceleration (DXVA).</span></span> <span data-ttu-id="e3f48-105">AI44 et IA44 sont des surfaces avec une valeur de bits par pixel de 8.</span><span class="sxs-lookup"><span data-stu-id="e3f48-105">AI44 and IA44 are surfaces with a bits-per-pixel value of 8.</span></span> <span data-ttu-id="e3f48-106">Il y a 4 bits d’I et 4 bits de *a*. *Je* représente un index dans une palette YUV à 16 entrées.</span><span class="sxs-lookup"><span data-stu-id="e3f48-106">There are 4 bits of I and 4 bits of *A*. *I* represents an index into a 16-entry YUV palette.</span></span> <span data-ttu-id="e3f48-107">*Un* représente 4 bits d’informations de transparence (également appelées par pixel-alpha).</span><span class="sxs-lookup"><span data-stu-id="e3f48-107">*A* represents 4 bits of transparency information (also known as per-pixel-alpha).</span></span> <span data-ttu-id="e3f48-108">Par conséquent, les surfaces AI44 et IA44 autorisent 16 couleurs différentes à 16 valeurs de transparence différentes, ou 256 représentations de pixels différentes.</span><span class="sxs-lookup"><span data-stu-id="e3f48-108">Therefore, AI44 and IA44 surfaces allow for 16 different colors at 16 different transparency values, or 256 different pixel representations.</span></span> <span data-ttu-id="e3f48-109">Avec AI44, l’alpha est stocké dans le grignot-Quartet, en IA44, le alpha est stocké dans le grignot-Quartet.</span><span class="sxs-lookup"><span data-stu-id="e3f48-109">With AI44 the alpha is stored in the hi-nibble, in IA44 the alpha is stored in the lo-nibble.</span></span> <span data-ttu-id="e3f48-110">Les deux formats sont très utiles pour les images de sous-image de DVD et les images Line21 et Teletext.</span><span class="sxs-lookup"><span data-stu-id="e3f48-110">Both formats are very useful for DVD sub-picture images and Line21 and Teletext images.</span></span> <span data-ttu-id="e3f48-111">Microsoft préfère la version AI44, car il est légèrement plus facile de générer du texte à l’aide de ce format.</span><span class="sxs-lookup"><span data-stu-id="e3f48-111">Microsoft prefers the AI44 version because it is slightly easier to generate text using this format.</span></span>

| <span data-ttu-id="e3f48-112">Subtype</span><span class="sxs-lookup"><span data-stu-id="e3f48-112">Subtype</span></span>            | <span data-ttu-id="e3f48-113">Description</span><span class="sxs-lookup"><span data-stu-id="e3f48-113">Description</span></span>                                                 |
|--------------------|-------------------------------------------------------------|
| <span data-ttu-id="e3f48-114">MEDIASUBTYPE \_ AI44</span><span class="sxs-lookup"><span data-stu-id="e3f48-114">MEDIASUBTYPE\_AI44</span></span> | <span data-ttu-id="e3f48-115">Pour les superpositions de sous-image et de texte.</span><span class="sxs-lookup"><span data-stu-id="e3f48-115">For subpicture and text overlays.</span></span> <span data-ttu-id="e3f48-116">Consultez la description précédente.</span><span class="sxs-lookup"><span data-stu-id="e3f48-116">See previous description.</span></span> |
| <span data-ttu-id="e3f48-117">MEDIASUBTYPE \_ IA44</span><span class="sxs-lookup"><span data-stu-id="e3f48-117">MEDIASUBTYPE\_IA44</span></span> | <span data-ttu-id="e3f48-118">Pour les superpositions de sous-image et de texte.</span><span class="sxs-lookup"><span data-stu-id="e3f48-118">For subpicture and text overlays.</span></span> <span data-ttu-id="e3f48-119">Consultez la description précédente.</span><span class="sxs-lookup"><span data-stu-id="e3f48-119">See previous description.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="e3f48-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e3f48-120">Requirements</span></span>



| <span data-ttu-id="e3f48-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e3f48-121">Requirement</span></span> | <span data-ttu-id="e3f48-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="e3f48-122">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e3f48-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="e3f48-123">Header</span></span><br/> | <dl> <span data-ttu-id="e3f48-124"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3f48-124"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3f48-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e3f48-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3f48-126">Sous-types de vidéos</span><span class="sxs-lookup"><span data-stu-id="e3f48-126">Video Subtypes</span></span>](video-subtypes.md)
</dt> </dl>

 

 




