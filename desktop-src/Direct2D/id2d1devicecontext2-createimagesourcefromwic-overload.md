---
title: Méthodes ID2D1DeviceContext2 CreateImageSourceFromWic (D2d1 \_ 3. h)
description: Crée un objet source d’image à partir d’une source de bitmap WIC, tout en remplissant la mémoire en pixels dans la source de l’image. L’image est chargée et stockée tout en utilisant une quantité minimale de mémoire.
ms.assetid: af02630d-a9ca-f5b4-6f2a-31a73ef603e5
keywords:
- Méthodes CreateImageSourceFromWic Direct2D
topic_type:
- apiref
api_location:
- d2d1_3.h
api_type:
- HeaderDef
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 20773912886840a185e1b9fc71576f89e9a40fde
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545670"
---
# <a name="id2d1devicecontext2createimagesourcefromwic-methods"></a><span data-ttu-id="14406-105">ID2D1DeviceContext2 :: CreateImageSourceFromWic, méthodes</span><span class="sxs-lookup"><span data-stu-id="14406-105">ID2D1DeviceContext2::CreateImageSourceFromWic methods</span></span>

<span data-ttu-id="14406-106">Crée un objet source d’image à partir d’une source de bitmap WIC, tout en remplissant la mémoire en pixels dans la source de l’image.</span><span class="sxs-lookup"><span data-stu-id="14406-106">Creates an image source object from a WIC bitmap source, while populating all pixel memory within the image source.</span></span> <span data-ttu-id="14406-107">L’image est chargée et stockée tout en utilisant une quantité minimale de mémoire.</span><span class="sxs-lookup"><span data-stu-id="14406-107">The image is loaded and stored while using a minimal amount of memory.</span></span>

### <a name="overload-list"></a><span data-ttu-id="14406-108">Liste de surcharge</span><span class="sxs-lookup"><span data-stu-id="14406-108">Overload list</span></span>



| <span data-ttu-id="14406-109">Méthode</span><span class="sxs-lookup"><span data-stu-id="14406-109">Method</span></span>                                                                                                                                                                                       | <span data-ttu-id="14406-110">Description</span><span class="sxs-lookup"><span data-stu-id="14406-110">Description</span></span>                                                                                                                                                       |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14406-111">[**CreateImageSourceFromWic (IWICBitmapSource \* , d2d1, \_ options de chargement de source d’image \_ \_ \_ , ID2D1ImageSourceFromWic \* \* )**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-createimagesourcefromwic(iwicbitmapsource_d2d1_image_source_loading_options_id2d1imagesourcefromwic))</span><span class="sxs-lookup"><span data-stu-id="14406-111">[**CreateImageSourceFromWic (IWICBitmapSource\*, D2D1\_IMAGE\_SOURCE\_LOADING\_OPTIONS, ID2D1ImageSourceFromWic\*\*)**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-createimagesourcefromwic(iwicbitmapsource_d2d1_image_source_loading_options_id2d1imagesourcefromwic))</span></span>                   | <span data-ttu-id="14406-112">Version de la méthode qui vous permet de spécifier la source de la bitmap WIC, l’objet source de l’image de sortie et les options de chargement avec le mode Alpha par défaut.</span><span class="sxs-lookup"><span data-stu-id="14406-112">Version of the method that allows you to specify the WIC bitmap source, the output image source object, and loading options with default alpha mode.</span></span><br/>   |
| <span data-ttu-id="14406-113">[**CreateImageSourceFromWic (IWICBitmapSource \* , d2d1 \_ , \_ options de chargement de source d’image \_ \_ , d2d1 \_ \_ mode alpha, ID2D1ImageSourceFromWic \* \* )**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-createimagesourcefromwic(iwicbitmapsource_d2d1_image_source_loading_options_d2d1_alpha_mode_id2d1imagesourcefromwic))</span><span class="sxs-lookup"><span data-stu-id="14406-113">[**CreateImageSourceFromWic (IWICBitmapSource\*, D2D1\_IMAGE\_SOURCE\_LOADING\_OPTIONS, D2D1\_ALPHA\_MODE, ID2D1ImageSourceFromWic\*\*)**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-createimagesourcefromwic(iwicbitmapsource_d2d1_image_source_loading_options_d2d1_alpha_mode_id2d1imagesourcefromwic))</span></span> | <span data-ttu-id="14406-114">Version de la méthode qui vous permet de spécifier la source de la bitmap WIC, l’objet source de l’image de sortie et les options de chargement, ainsi que le mode Alpha.</span><span class="sxs-lookup"><span data-stu-id="14406-114">Version of the method that allows you to specify the WIC bitmap source, the output image source object, and loading options, and alpha mode.</span></span><br/>           |
| <span data-ttu-id="14406-115">[**CreateImageSourceFromWic (IWICBitmapSource \* , ID2D1ImageSourceFromWic \* \* )**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-createimagesourcefromwic(iwicbitmapsource_id2d1imagesourcefromwic))</span><span class="sxs-lookup"><span data-stu-id="14406-115">[**CreateImageSourceFromWic (IWICBitmapSource\*, ID2D1ImageSourceFromWic\*\*)**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-createimagesourcefromwic(iwicbitmapsource_id2d1imagesourcefromwic))</span></span>                                                          | <span data-ttu-id="14406-116">Version de la méthode qui vous permet de spécifier la source de la bitmap WIC et l’objet source de l’image de sortie avec le mode de chargement par défaut opitons et le mode Alpha.</span><span class="sxs-lookup"><span data-stu-id="14406-116">Version of the method that allows you to specify the WIC bitmap source and the output image source object with default loading opitons and alpha mode.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="14406-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="14406-117">Requirements</span></span>



| <span data-ttu-id="14406-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="14406-118">Requirement</span></span> | <span data-ttu-id="14406-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="14406-119">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="14406-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="14406-120">Header</span></span><br/> | <dl> <span data-ttu-id="14406-121"><dt>D2d1 \_ 3. h</dt></span><span class="sxs-lookup"><span data-stu-id="14406-121"><dt>D2d1\_3.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14406-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="14406-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14406-123">**ID2D1DeviceContext2**</span><span class="sxs-lookup"><span data-stu-id="14406-123">**ID2D1DeviceContext2**</span></span>](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1devicecontext2)
</dt> </dl>

<span data-ttu-id="14406-124">�</span><span class="sxs-lookup"><span data-stu-id="14406-124">�</span></span>

<span data-ttu-id="14406-125">�</span><span class="sxs-lookup"><span data-stu-id="14406-125">�</span></span>
