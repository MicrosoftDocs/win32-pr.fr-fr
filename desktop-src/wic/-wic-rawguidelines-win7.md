---
description: Configuration requise pour les codecs BRUTs pour Windows 7
ms.assetid: 3f8bd336-ba03-4ffb-9aa2-ea55a276e3bc
title: Configuration requise pour les codecs BRUTs pour Windows 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e0c4d04175eab1b6e68ac87ed18a648fa4655b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520018"
---
# <a name="raw-codec-requirements-for-windows-7"></a><span data-ttu-id="dd25c-103">Configuration requise pour les codecs BRUTs pour Windows 7</span><span class="sxs-lookup"><span data-stu-id="dd25c-103">RAW Codec Requirements for Windows 7</span></span>

<span data-ttu-id="dd25c-104">Les fonctionnalités de codec suivantes sont requises au minimum :</span><span class="sxs-lookup"><span data-stu-id="dd25c-104">The following codec features are required at a minimum:</span></span>

<span data-ttu-id="dd25c-105">Toutes les fonctionnalités requises pour la prise en charge de l’interpréteur de commandes et de la Galerie de photos Windows Vista : miniature, aperçu et rotation (persistante).</span><span class="sxs-lookup"><span data-stu-id="dd25c-105">All functionality that is required for Windows Vista shell and Photo Gallery support: thumbnail, preview, and (persisted) rotation.</span></span> <span data-ttu-id="dd25c-106">Le traitement brut doit avoir comme valeur par défaut les paramètres appropriés.</span><span class="sxs-lookup"><span data-stu-id="dd25c-106">RAW processing should default to appropriate as-shot settings.</span></span>

<span data-ttu-id="dd25c-107">La prise en charge des métadonnées principales (à la fois en lecture et en écriture), les métadonnées non EXIF, ainsi que les métadonnées EXIF, doit être conservée dans des formats de fichiers BRUTs sans utiliser de fichiers side-car.</span><span class="sxs-lookup"><span data-stu-id="dd25c-107">Support for core metadata (both read and write), Non-EXIF metadata, as well as EXIF metadata, should be persisted inside RAW file formats without use of sidecar files.</span></span>

<span data-ttu-id="dd25c-108">Prise en charge de l’interface [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) .</span><span class="sxs-lookup"><span data-stu-id="dd25c-108">Support for the [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) interface.</span></span> <span data-ttu-id="dd25c-109">Pour Windows 7, WIC (Windows Imaging Component) WIC exige que toutes les interfaces de paramètre exposées par [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) soient implémentées.</span><span class="sxs-lookup"><span data-stu-id="dd25c-109">For Windows 7, Windows Imaging Component (WIC)WIC requires that all parameter interfaces exposed by [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) be implemented.</span></span>

<span data-ttu-id="dd25c-110">Prise en charge de l’état d’orientation :</span><span class="sxs-lookup"><span data-stu-id="dd25c-110">Orientation state support:</span></span>

-   <span data-ttu-id="dd25c-111">les rotations d’image d’une étape de 90 doivent être appliquées à l’aide de la méthode [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)::[**SetRotation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrotation) .</span><span class="sxs-lookup"><span data-stu-id="dd25c-111">90 degree-step Image rotations should be applied by using the [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)::[**SetRotation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrotation) method.</span></span> <span data-ttu-id="dd25c-112">Les applications et Windows utilisent cette méthode pour faire pivoter les images (et les miniatures et les aperçus mis en cache).</span><span class="sxs-lookup"><span data-stu-id="dd25c-112">Applications and Windows use this method to rotate the images (and cached thumbnails and previews).</span></span>
-   <span data-ttu-id="dd25c-113">L’application de la rotation à l’aide de cette API doit également être conservée par le codec (voir plus haut dans ce document).</span><span class="sxs-lookup"><span data-stu-id="dd25c-113">Application of rotation by using this API should also be persisted by the codec (see earlier in this paper).</span></span>
-   <span data-ttu-id="dd25c-114">Les applications peuvent utiliser les fonctionnalités de rotation de l’API [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) , mais le codec ne sérialise pas les paramètres de rotation sur cette API, donc les rotations effectuées à l’aide de [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) ne sont pas conservées.</span><span class="sxs-lookup"><span data-stu-id="dd25c-114">Applications can use the rotation capabilities of the [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) API, but the codec will not serialize any rotation settings on this API, so rotations done using [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) will not be persisted.</span></span>

<span data-ttu-id="dd25c-115">Prise en charge de l’extraction des miniatures et des aperçus rapides.</span><span class="sxs-lookup"><span data-stu-id="dd25c-115">High-speed thumbnail and preview extraction support.</span></span> <span data-ttu-id="dd25c-116">Si la taille de la dimension de pixel maximale de l’aperçu (largeur ou hauteur) est inférieure à 1024 pixels, Windows Vista demande un rendu pour l’aperçu de l’écran :</span><span class="sxs-lookup"><span data-stu-id="dd25c-116">If the preview maximum pixel dimension (width or height) is less than 1024 pixels in size, Windows Vista will request a render for screen preview:</span></span>

-   <span data-ttu-id="dd25c-117">La méthode [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)::[**SetRenderMode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrendermode) doit prendre en charge au moins les modes [**WICRawRenderQualityDraftMode**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawrendermode) et [**WICRawRenderQualityBestQuality**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawrendermode) pour permettre un rendu plus rapide des miniatures et des aperçus que le mode de qualité totale.</span><span class="sxs-lookup"><span data-stu-id="dd25c-117">The [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)::[**SetRenderMode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrendermode) method should support at least the [**WICRawRenderQualityDraftMode**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawrendermode) and [**WICRawRenderQualityBestQuality**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawrendermode) modes to allow faster rendering of thumbnails and previews than the full-quality mode.</span></span>
-   <span data-ttu-id="dd25c-118">Windows appellera [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)::[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) avec la taille de résolution d’écran demandée.</span><span class="sxs-lookup"><span data-stu-id="dd25c-118">Windows will call [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)::[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) with the requested screen resolution size.</span></span>
-   <span data-ttu-id="dd25c-119">Les tailles de résolution d’écran doivent être prises en charge dans l’API ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="dd25c-119">Screen resolution sizes must be supported in the above API.</span></span>
-   <span data-ttu-id="dd25c-120">Un traitement cohérent des images de la miniature, de l’aperçu et des bits d’image complète à partir de [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="dd25c-120">Consistent image processing of thumbnail, preview, and full-image bits from [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) is required.</span></span>

<span data-ttu-id="dd25c-121">Formats de pixel HDR (High dynamique Range).</span><span class="sxs-lookup"><span data-stu-id="dd25c-121">High dynamic range (HDR) pixel formats.</span></span>

<span data-ttu-id="dd25c-122">Impression XPS (XML Paper Specification).</span><span class="sxs-lookup"><span data-stu-id="dd25c-122">XML Paper Specification (XPS) printing.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dd25c-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="dd25c-123">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="dd25c-124">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="dd25c-124">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="dd25c-125">Vue d’ensemble du composant Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="dd25c-125">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="dd25c-126">Recommandations de WIC pour les formats d’image RAW Camera</span><span class="sxs-lookup"><span data-stu-id="dd25c-126">WIC Guidelines for Camera RAW Image Formats</span></span>](-wic-rawguidelines.md)
</dt> <dt>

[<span data-ttu-id="dd25c-127">Comment écrire un CODEC WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="dd25c-127">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



