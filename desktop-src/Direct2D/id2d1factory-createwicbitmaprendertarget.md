---
title: Méthodes ID2D1Factory CreateWicBitmapRenderTarget
description: Crée une cible de rendu qui est rendue en bitmap WIC (Microsoft Windows Imaging Component).
ms.assetid: 93141743-c11d-40b4-83c5-07c9066836c7
keywords:
- Méthodes CreateWicBitmapRenderTarget Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 4025028582c254e7a5724a575ef0d7f1c7d91570
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545386"
---
# <a name="id2d1factorycreatewicbitmaprendertarget-methods"></a><span data-ttu-id="ff51c-104">ID2D1Factory :: CreateWicBitmapRenderTarget, méthodes</span><span class="sxs-lookup"><span data-stu-id="ff51c-104">ID2D1Factory::CreateWicBitmapRenderTarget methods</span></span>

<span data-ttu-id="ff51c-105">Crée une cible de rendu qui est rendue en bitmap WIC (Microsoft Windows Imaging Component).</span><span class="sxs-lookup"><span data-stu-id="ff51c-105">Creates a render target that renders to a Microsoft Windows Imaging Component (WIC) bitmap.</span></span>

### <a name="overload-list"></a><span data-ttu-id="ff51c-106">Liste de surcharge</span><span class="sxs-lookup"><span data-stu-id="ff51c-106">Overload list</span></span>



| <span data-ttu-id="ff51c-107">Méthode</span><span class="sxs-lookup"><span data-stu-id="ff51c-107">Method</span></span>                                                                                                                                                                                                                            | <span data-ttu-id="ff51c-108">Description</span><span class="sxs-lookup"><span data-stu-id="ff51c-108">Description</span></span>                                                                                            |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff51c-109">[**CreateWicBitmapRenderTarget (IWICBitmap \* , d2d1 \_ Propriétés de la \_ cible \_ de rendu \* , ID2D1RenderTarget \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createwicbitmaprendertarget(iwicbitmap_constd2d1_render_target_properties_id2d1rendertarget))</span><span class="sxs-lookup"><span data-stu-id="ff51c-109">[**CreateWicBitmapRenderTarget(IWICBitmap\*,D2D1\_RENDER\_TARGET\_PROPERTIES\*,ID2D1RenderTarget\*\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createwicbitmaprendertarget(iwicbitmap_constd2d1_render_target_properties_id2d1rendertarget))</span></span> | <span data-ttu-id="ff51c-110">Crée une cible de rendu qui est rendue en bitmap WIC (Microsoft Windows Imaging Component).</span><span class="sxs-lookup"><span data-stu-id="ff51c-110">Creates a render target that renders to a Microsoft Windows Imaging Component (WIC) bitmap.</span></span><br/> |
| <span data-ttu-id="ff51c-111">[**CreateWicBitmapRenderTarget (IWICBitmap \* , d2d1 \_ Propriétés de la cible de rendu \_ \_&, ID2D1RenderTarget \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createwicbitmaprendertarget(iwicbitmap_constd2d1_render_target_properties__id2d1rendertarget))</span><span class="sxs-lookup"><span data-stu-id="ff51c-111">[**CreateWicBitmapRenderTarget(IWICBitmap\*,D2D1\_RENDER\_TARGET\_PROPERTIES&,ID2D1RenderTarget\*\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createwicbitmaprendertarget(iwicbitmap_constd2d1_render_target_properties__id2d1rendertarget))</span></span>  | <span data-ttu-id="ff51c-112">Crée une cible de rendu qui est rendue en bitmap WIC (Microsoft Windows Imaging Component).</span><span class="sxs-lookup"><span data-stu-id="ff51c-112">Creates a render target that renders to a Microsoft Windows Imaging Component (WIC) bitmap.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="ff51c-113">Notes</span><span class="sxs-lookup"><span data-stu-id="ff51c-113">Remarks</span></span>

<span data-ttu-id="ff51c-114">Votre application doit créer des cibles de rendu une seule fois et les conserver pendant toute la durée de vie de l’application ou jusqu’à ce que l’erreur de [**\_ recréation de la \_ cible D2DERR**](direct2d-error-codes.md) soit reçue.</span><span class="sxs-lookup"><span data-stu-id="ff51c-114">Your application should create render targets once and hold onto them for the life of the application or until the [**D2DERR\_RECREATE\_TARGET**](direct2d-error-codes.md) error is received.</span></span> <span data-ttu-id="ff51c-115">Lorsque vous recevez cette erreur, vous devez recréer la cible de rendu (et toutes les ressources qu’elle a créées).</span><span class="sxs-lookup"><span data-stu-id="ff51c-115">When you receive this error, you need to recreate the render target (and any resources it created).</span></span>

<span data-ttu-id="ff51c-116">**Remarque**   Cette méthode n’est pas prise en charge sur les Windows Phone et échoue quand elle est appelée sur un appareil avec le code d’erreur 0x8899000b (aucun périphérique de rendu matériel n’est disponible pour cette opération).</span><span class="sxs-lookup"><span data-stu-id="ff51c-116">**Note**   This method isn't supported on Windows Phone and will fail when called on a device with error code 0x8899000b ( There is no hardware rendering device available for this operation ).</span></span> <span data-ttu-id="ff51c-117">Étant donné que l’émulateur Windows Phone prend en charge le rendu de distorsion, cette méthode échoue quand elle est appelée sur l’émulateur avec un code d’erreur différent, 0x88982f80 (wincodec \_ Err \_ unsupportedpixelformat).</span><span class="sxs-lookup"><span data-stu-id="ff51c-117">Because the Windows Phone Emulator supports WARP rendering, this method will fail when called on the emulator with a different error code, 0x88982f80 (wincodec\_err\_unsupportedpixelformat).</span></span>

## <a name="requirements"></a><span data-ttu-id="ff51c-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ff51c-118">Requirements</span></span>



| <span data-ttu-id="ff51c-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ff51c-119">Requirement</span></span> | <span data-ttu-id="ff51c-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="ff51c-120">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ff51c-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ff51c-121">Library</span></span><br/> | <dl> <span data-ttu-id="ff51c-122"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ff51c-122"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="ff51c-123">DLL</span><span class="sxs-lookup"><span data-stu-id="ff51c-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="ff51c-124"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ff51c-124"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff51c-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ff51c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff51c-126">**ID2D1Factory**</span><span class="sxs-lookup"><span data-stu-id="ff51c-126">**ID2D1Factory**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)
</dt> </dl>

 

