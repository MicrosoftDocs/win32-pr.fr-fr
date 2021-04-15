---
title: Guide de programmation WIC
description: Décrit comment utiliser les API WIC.
ms.assetid: ed7987f0-5983-4bb5-8640-0830a87c8f2e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bb6675ef7f5c065d2d3e00ab470cb334af25525
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104393679"
---
# <a name="wic-programming-guide"></a><span data-ttu-id="83d71-103">Guide de programmation WIC</span><span class="sxs-lookup"><span data-stu-id="83d71-103">WIC programming guide</span></span>

<span data-ttu-id="83d71-104">Cette section contient des rubriques conceptuelles qui décrivent comment utiliser les API WIC (Windows Imaging Component).</span><span class="sxs-lookup"><span data-stu-id="83d71-104">This section contains conceptual topics that describe how to use the Windows Imaging Component (WIC) APIs.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="83d71-105">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="83d71-105">In this section</span></span>



| <span data-ttu-id="83d71-106">Rubrique</span><span class="sxs-lookup"><span data-stu-id="83d71-106">Topic</span></span>                                                                                 | <span data-ttu-id="83d71-107">Description</span><span class="sxs-lookup"><span data-stu-id="83d71-107">Description</span></span>                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="83d71-108">Vue d’ensemble du composant Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="83d71-108">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)<br/> | <span data-ttu-id="83d71-109">Le WIC fournit une infrastructure extensible pour l’utilisation des images et des métadonnées d’image.</span><span class="sxs-lookup"><span data-stu-id="83d71-109">The WIC provides an extensible framework for working with images and image metadata.</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="83d71-110">Vue d’ensemble de l’API WIC</span><span class="sxs-lookup"><span data-stu-id="83d71-110">WIC API Overview</span></span>](-wic-api.md)<br/>                                           | <span data-ttu-id="83d71-111">Le WIC fournit une API COM (Component Object Model) à utiliser en C et C++.</span><span class="sxs-lookup"><span data-stu-id="83d71-111">The WIC provides a Component Object Model (COM) based API for use in C and C++.</span></span><br/>                                                                                                                            |
| [<span data-ttu-id="83d71-112">Décodage d’images numériques</span><span class="sxs-lookup"><span data-stu-id="83d71-112">Decoding Digital Images</span></span>](-wic-decoder-portal.md)<br/>                         | <span data-ttu-id="83d71-113">Cette section contient des rubriques conceptuelles et des procédures qui décrivent les décodeurs de bitmap WIC utilisés lors du décodage d’images numériques.</span><span class="sxs-lookup"><span data-stu-id="83d71-113">This section contains conceptual and how-to topics that describe WIC bitmap decoders which are used in decoding digital images.</span></span><br/>                                                                            |
| [<span data-ttu-id="83d71-114">Utilisation des données image</span><span class="sxs-lookup"><span data-stu-id="83d71-114">Using Image Data</span></span>](-wic-bitmapsources-portal.md)<br/>                          | <span data-ttu-id="83d71-115">Cette section contient des rubriques conceptuelles et des procédures qui décrivent les sources bitmap WIC et comment les manipuler.</span><span class="sxs-lookup"><span data-stu-id="83d71-115">This section contains conceptual and how-to topics that describe WIC bitmap sources and how to manipulate them.</span></span><br/>                                                                                            |
| [<span data-ttu-id="83d71-116">Encodage de données image</span><span class="sxs-lookup"><span data-stu-id="83d71-116">Encoding Image Data</span></span>](encoding-bitmaps-to-digital-images.md)<br/>              | <span data-ttu-id="83d71-117">Cette section contient des rubriques conceptuelles et des procédures qui décrivent des encodeurs de bitmap WIC utilisés pour encoder des images numériques.</span><span class="sxs-lookup"><span data-stu-id="83d71-117">This section contains conceptual and how-to topics that describe WIC bitmap encoders which are used to encode digital images.</span></span><br/>                                                                              |
| [<span data-ttu-id="83d71-118">Codecs WIC natifs</span><span class="sxs-lookup"><span data-stu-id="83d71-118">Native WIC Codecs</span></span>](native-wic-codecs.md)<br/>                                 | <span data-ttu-id="83d71-119">Cette section contient des informations sur les codecs de création d’images natives disponibles dans WIC.</span><span class="sxs-lookup"><span data-stu-id="83d71-119">This section contains information about the native imaging codecs available in WIC.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="83d71-120">Traitement des métadonnées de l’image</span><span class="sxs-lookup"><span data-stu-id="83d71-120">Processing Image Metadata</span></span>](-wic-metadata-portal.md)<br/>                      | <span data-ttu-id="83d71-121">Cette section contient des rubriques conceptuelles qui décrivent le système de métadonnées WIC.</span><span class="sxs-lookup"><span data-stu-id="83d71-121">This section contains conceptual topics that describe the WIC metadata system.</span></span><br/>                                                                                                                             |
| [<span data-ttu-id="83d71-122">Prise en charge d’JPEG YCbCr</span><span class="sxs-lookup"><span data-stu-id="83d71-122">JPEG YCbCr Support</span></span>](jpeg-ycbcr-support.md)<br/>                               | <span data-ttu-id="83d71-123">À partir de Windows 8.1, le codec [Windows Imaging Component (WIC)](-wic-about-windows-imaging-codec.md) JPEG prend en charge la lecture et l’écriture des données d’image dans son format natif YC<sub>b</sub>C<sub>r</sub> .</span><span class="sxs-lookup"><span data-stu-id="83d71-123">Starting with Windows 8.1, the [Windows Imaging Component (WIC)](-wic-about-windows-imaging-codec.md) JPEG codec supports reading and writing image data in its native YC<sub>b</sub>C<sub>r</sub> form.</span></span> <br/> |
| [<span data-ttu-id="83d71-124">Gestion des couleurs</span><span class="sxs-lookup"><span data-stu-id="83d71-124">Color Management</span></span>](-wic-colormanagement.md)<br/>                               | <span data-ttu-id="83d71-125">WIC simplifie la gestion des couleurs en fournissant l’interface [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) et l’interface [**IWICColorTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform) .</span><span class="sxs-lookup"><span data-stu-id="83d71-125">WIC simplifies color management by providing the [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) interface and the [**IWICColorTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform) interface.</span></span><br/>          |
| [<span data-ttu-id="83d71-126">Développement de composants</span><span class="sxs-lookup"><span data-stu-id="83d71-126">Component Development</span></span>](-wic-component-development.md)<br/>                    | <span data-ttu-id="83d71-127">Le WIC est une plateforme extensible qui fournit une API de bas niveau pour les images numériques.</span><span class="sxs-lookup"><span data-stu-id="83d71-127">The WIC is an extensible platform that provides low-level API for digital images.</span></span><br/>                                                                                                                          |



 

## <a name="see-also"></a><span data-ttu-id="83d71-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="83d71-128">See Also</span></span>

[<span data-ttu-id="83d71-129">Référence WIC</span><span class="sxs-lookup"><span data-stu-id="83d71-129">WIC Reference</span></span>](-wic-codec-reference.md)


[<span data-ttu-id="83d71-130">Exemples WIC</span><span class="sxs-lookup"><span data-stu-id="83d71-130">WIC Samples</span></span>](-wic-samples.md)


 

 




