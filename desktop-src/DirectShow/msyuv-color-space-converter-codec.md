---
description: MSYUV est un codec de convertisseur d’espace colorimétrique YUV-à-RVB.
ms.assetid: 77b00937-ac63-4b23-b546-c0896b3c57ba
title: Codec de convertisseur d’espace de couleurs MSYUV
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 838e7cd749042b2fb97adaf0b2b4cd0378a81c07
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540056"
---
# <a name="msyuv-color-space-converter-codec"></a><span data-ttu-id="0a030-103">Codec de convertisseur d’espace de couleurs MSYUV</span><span class="sxs-lookup"><span data-stu-id="0a030-103">MSYUV Color Space Converter Codec</span></span>

<span data-ttu-id="0a030-104">MSYUV est un codec de convertisseur d’espace colorimétrique YUV-à-RVB.</span><span class="sxs-lookup"><span data-stu-id="0a030-104">MSYUV is a YUV-to-RGB color space converter codec.</span></span> <span data-ttu-id="0a030-105">Il permet la lecture de données sources vidéo dans des formats YUV sur les clients dont la carte vidéo ne peut pas être utilisée pour les conversions YUV-à-RGB dans le matériel.</span><span class="sxs-lookup"><span data-stu-id="0a030-105">It enables playback of video source data in YUV formats on clients whose video display adapter cannot be used for YUV-to-RGB conversions in hardware.</span></span> <span data-ttu-id="0a030-106">Le codec participe aux graphiques de filtres via le filtre de wrapper de [décompresseur AVI](avi-decompressor-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="0a030-106">The codec participates in filter graphs through the [AVI Decompressor](avi-decompressor-filter.md) wrapper filter.</span></span>

<span data-ttu-id="0a030-107">Les caméras de conférence numérique avec des interfaces 1394 ou USB peuvent produire des données d’image dans différents formats YUV.</span><span class="sxs-lookup"><span data-stu-id="0a030-107">Digital conferencing cameras with 1394 or USB interfaces can produce image data in various YUV formats.</span></span> <span data-ttu-id="0a030-108">Si le matériel d’affichage ne prend pas en charge la conversion YUV-à-RGB intégrée, ou si la fonctionnalité de conversion matérielle ne peut pas être utilisée pour une autre raison, les données de l’image YUV doivent être converties au format RVB avant d’être envoyées au convertisseur vidéo.</span><span class="sxs-lookup"><span data-stu-id="0a030-108">If the display hardware does not support on-board YUV-to-RGB conversion, or if the hardware conversion capability cannot be used for some other reason, then the YUV image data must be converted to RGB format before it is sent to the Video Renderer.</span></span>

<span data-ttu-id="0a030-109">En raison de la nécessité du [convertisseur vidéo](video-renderer-filter.md)pour un type d’entrée RVB au moment de la connexion, ce filtre peut être inséré dans un graphique en amont du convertisseur vidéo pendant la génération automatique de graphiques.</span><span class="sxs-lookup"><span data-stu-id="0a030-109">Because of the [Video Renderer](video-renderer-filter.md)'s requirement for an RGB input type at connection time, this filter might be inserted into a graph upstream from the Video Renderer during automatic graph building.</span></span> <span data-ttu-id="0a030-110">Plus précisément, si le générateur de graphiques détecte un format YUV dans le type de média de la broche de sortie du filtre en amont, le générateur de graphiques insère le décompresseur AVI, qui charge ensuite le codec MSYUV et le configure initialement pour effectuer la conversion en RVB.</span><span class="sxs-lookup"><span data-stu-id="0a030-110">Specifically, if the Graph Builder detects a YUV format in the media type of the upstream filter's output pin, the Graph Builder will insert the AVI Decompressor, which will then load the MSYUV codec and configure it initially to perform the conversion to RGB.</span></span> <span data-ttu-id="0a030-111">Une fois que le graphique a d’abord effectué une transition vers un État exécution ou suspendu, le filtre de convertisseur vidéo peut détecter si la carte vidéo peut effectuer la conversion dans le matériel.</span><span class="sxs-lookup"><span data-stu-id="0a030-111">After the graph first transitions to a run or paused state, the Video Renderer filter can detect whether the video display adapter can perform the conversion in hardware.</span></span> <span data-ttu-id="0a030-112">Si tel est le cas, le décompresseur AVI est notifié et RECONFIGURE MSYUV pour qu’il fonctionne en « mode pass-through », ce qui amène le codec à ignorer la conversion et à copier les données de l’image YUV directement sur une surface de superposition DirectDraw dans la mémoire vidéo.</span><span class="sxs-lookup"><span data-stu-id="0a030-112">If it can, then the AVI Decompressor is notified and it reconfigures MSYUV to operate in "pass-through mode," which causes the codec to skip the conversion and copy the YUV image data directly onto a DirectDraw overlay surface in video memory.</span></span>

<span data-ttu-id="0a030-113">Étant donné que les convertisseurs de mixage vidéo (VMR-7 et VMR-9) n’utilisent jamais GDI, ils n’ont pas besoin d’un type RVB au moment de la connexion, et le convertisseur d’espace de couleurs MSYUV n’est jamais inséré avant le VMR dans un graphique.</span><span class="sxs-lookup"><span data-stu-id="0a030-113">Because the Video Mixing Renderers (VMR-7 and VMR-9) never use GDI, they do not require an RGB type at connect time, and the MSYUV Color Space Converter is never inserted before the VMR in a graph.</span></span>

<span data-ttu-id="0a030-114">MSYUV convertit les formats YUV compressés en RGB, comme illustré dans la liste suivante :</span><span class="sxs-lookup"><span data-stu-id="0a030-114">MSYUV converts packed YUV formats to RGB, as shown in the following list:</span></span>

-   <span data-ttu-id="0a030-115">Formats d’entrée : UYVY, YUY2, YVYU</span><span class="sxs-lookup"><span data-stu-id="0a030-115">Input formats: UYVY, YUY2, YVYU</span></span>
-   <span data-ttu-id="0a030-116">Formats de sortie : RVB 8, RVB 16, RVB 24, RVB 32</span><span class="sxs-lookup"><span data-stu-id="0a030-116">Output formats: RGB 8, RGB 16, RGB 24, RGB 32</span></span>

<span data-ttu-id="0a030-117">Le codec de convertisseur d’espace de couleurs MSYUV est un codec VCM (Video Compression Manager).</span><span class="sxs-lookup"><span data-stu-id="0a030-117">The MSYUV Color Space Converter Codec is a Video Compression Manager (VCM) codec.</span></span> <span data-ttu-id="0a030-118">Il est utilisé dans DirectShow via le filtre de [décompresseur AVI](avi-decompressor-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="0a030-118">It is used in DirectShow through the [AVI Decompressor](avi-decompressor-filter.md) filter.</span></span> <span data-ttu-id="0a030-119">Pour obtenir un convertisseur de couleurs plus général, utilisez le [**convertisseur de couleurs DSP**](../medfound/colorconverter.md).</span><span class="sxs-lookup"><span data-stu-id="0a030-119">For a more general-purpose color converter, use the [**Color Converter DSP**](../medfound/colorconverter.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0a030-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0a030-120">Requirements</span></span>



| <span data-ttu-id="0a030-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0a030-121">Requirement</span></span> | <span data-ttu-id="0a030-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="0a030-122">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="0a030-123">DLL</span><span class="sxs-lookup"><span data-stu-id="0a030-123">DLL</span></span><br/> | <dl> <span data-ttu-id="0a030-124"><dt>Msyuv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0a030-124"><dt>Msyuv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a030-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0a030-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a030-126">Filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="0a030-126">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 
