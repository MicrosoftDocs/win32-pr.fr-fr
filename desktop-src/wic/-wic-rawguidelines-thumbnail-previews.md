---
description: Miniatures et aperçus
ms.assetid: e45f025e-a1ac-47c8-b794-ab1402ab35fb
title: Miniatures et aperçus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e279da9771a43eb75bb94faff23d2e6aa29c4ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534027"
---
# <a name="thumbnails-and-previews"></a><span data-ttu-id="6b3cf-103">Miniatures et aperçus</span><span class="sxs-lookup"><span data-stu-id="6b3cf-103">Thumbnails and Previews</span></span>

<span data-ttu-id="6b3cf-104">Windows Vista et la Galerie de photos Windows s’appuient sur le composant WIC (Windows Imaging Component) pour afficher des miniatures et des aperçus rapides des images.</span><span class="sxs-lookup"><span data-stu-id="6b3cf-104">Windows Vista and the Windows Photo Gallery rely on Windows Imaging Component (WIC) to render fast thumbnails and previews of images.</span></span> <span data-ttu-id="6b3cf-105">Pour prendre en charge le rendu rapide miniature et aperçu, les codecs BRUTs doivent implémenter les interfaces WIC [**miniature**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) et [**GetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) .</span><span class="sxs-lookup"><span data-stu-id="6b3cf-105">To support fast thumbnail and preview rendering, RAW codecs must implement the WIC [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) and [**GetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) interfaces.</span></span> <span data-ttu-id="6b3cf-106">Pour prendre en charge une expérience utilisateur réactive, il est fortement souhaitable que ces interfaces retournent un [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) à l’appelant en 200 millisecondes ou moins.</span><span class="sxs-lookup"><span data-stu-id="6b3cf-106">To support a responsive user experience, it is highly desirable that these interfaces return an [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) to the caller in 200 milliseconds or less.</span></span>

<span data-ttu-id="6b3cf-107">Microsoft recommande vivement que les propriétaires de format de fichier brut génèrent un aperçu prérendu et le cache dans le fichier image.</span><span class="sxs-lookup"><span data-stu-id="6b3cf-107">Microsoft strongly recommends that RAW file format owners generate a prerendered preview and cache this in the image file.</span></span> <span data-ttu-id="6b3cf-108">Pour un format de périphérique, cette opération est généralement effectuée au moment de la capture.</span><span class="sxs-lookup"><span data-stu-id="6b3cf-108">For an in-device format, this is usually done at capture time.</span></span> <span data-ttu-id="6b3cf-109">Toutefois, les préversions peuvent également être régénérées et stockées dans le fichier image chaque fois que les propriétés de l’interface [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) sont modifiées, si elles ne prennent pas trop de temps pour effectuer cette opération.</span><span class="sxs-lookup"><span data-stu-id="6b3cf-109">However, previews could also be regenerated and stored in the image file whenever [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) interface properties are changed-if it does not take too much work to do so.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6b3cf-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6b3cf-110">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="6b3cf-111">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="6b3cf-111">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="6b3cf-112">Vue d’ensemble du composant Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="6b3cf-112">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="6b3cf-113">Recommandations de WIC pour les formats d’image RAW Camera</span><span class="sxs-lookup"><span data-stu-id="6b3cf-113">WIC Guidelines for Camera RAW Image Formats</span></span>](-wic-rawguidelines.md)
</dt> <dt>

[<span data-ttu-id="6b3cf-114">Comment écrire un CODEC WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="6b3cf-114">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



