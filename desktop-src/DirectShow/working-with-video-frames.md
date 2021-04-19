---
description: Utilisation des images vidéo
ms.assetid: a5ad74dd-abfd-4810-a512-42e4b98a6c59
title: Utilisation des images vidéo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ead597fac5a28befc9c9868485840d03b46e5185
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106525091"
---
# <a name="working-with-video-frames"></a><span data-ttu-id="98913-103">Utilisation des images vidéo</span><span class="sxs-lookup"><span data-stu-id="98913-103">Working with Video Frames</span></span>

<span data-ttu-id="98913-104">Une vidéo non compressée est une séquence de bitmaps jouée rapidement, en général à un débit d’environ 30 images par seconde.</span><span class="sxs-lookup"><span data-stu-id="98913-104">Uncompressed video is a sequence of bitmaps played in rapid succession, typically at a rate of about 30 frames per second.</span></span> <span data-ttu-id="98913-105">Étant donné que la plupart des vidéos entrent dans un graphique de filtre DirectShow dans un format compressé, le flux vidéo passe généralement par un décodeur pour la décompression.</span><span class="sxs-lookup"><span data-stu-id="98913-105">Because most video enters a DirectShow filter graph in a compressed format, the video stream generally goes through a decoder for decompression.</span></span> <span data-ttu-id="98913-106">De nombreux décodeurs génèrent des données dans un format YUV et laissent la conversion finale en RVB pour le matériel vidéo juste avant le rendu.</span><span class="sxs-lookup"><span data-stu-id="98913-106">Many decoders output data in a YUV format and leave the final conversion to RGB for the video hardware just prior to rendering.</span></span> <span data-ttu-id="98913-107">Si un décodeur utilise l’accélération vidéo DirectX, le matériel vidéo effectue un travail supplémentaire pour décoder l’image.</span><span class="sxs-lookup"><span data-stu-id="98913-107">If a decoder uses DirectX Video Acceleration, the video hardware performs additional work to decode the image.</span></span> <span data-ttu-id="98913-108">Ainsi, la décompression finale des bitmaps peut ne pas être effectuée tant que les données n’ont pas atteint le matériel vidéo.</span><span class="sxs-lookup"><span data-stu-id="98913-108">Thus, final decompression of the bitmaps may not be performed until the data reaches the video hardware.</span></span>

<span data-ttu-id="98913-109">Mais pour effectuer de nombreux types d’analyses vidéo, de traitement ou de modification, il est souvent nécessaire de travailler sur des bitmaps non compressées dans un certain type de format RGB ou YUV avant leur rendu ou leur écriture dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="98913-109">But to perform many types of video analysis, processing, or editing, it is often necessary to work on uncompressed bitmaps in some type of RGB or YUV format before they are rendered or written to file.</span></span> <span data-ttu-id="98913-110">Ce travail est généralement effectué dans un filtre de transformation basé sur la classe de base [**CTransformFilter**](ctransformfilter.md) , en particulier dans la méthode **Transform** .</span><span class="sxs-lookup"><span data-stu-id="98913-110">This work is typically done within a transform filter based on the [**CTransformFilter**](ctransformfilter.md) base class, specifically in the **Transform** method.</span></span> <span data-ttu-id="98913-111">Cette méthode reçoit un pointeur vers un objet [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) qui encapsule les données vidéo.</span><span class="sxs-lookup"><span data-stu-id="98913-111">This method receives a pointer to an [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) object that encapsulates the video data.</span></span> <span data-ttu-id="98913-112">La méthode **IMediaSample :: GetPointer** retourne un pointeur vers le premier octet des données brutes.</span><span class="sxs-lookup"><span data-stu-id="98913-112">The **IMediaSample::GetPointer** method returns a pointer to the first byte of the raw data.</span></span> <span data-ttu-id="98913-113">Pour les cadres non compressés, ces données se composent de pixels qui sont accessibles ou modifiés directement par le filtre.</span><span class="sxs-lookup"><span data-stu-id="98913-113">For uncompressed frames, this data consists of pixels that can be accessed or modified directly by the filter.</span></span> <span data-ttu-id="98913-114">Les sections suivantes fournissent des informations générales qui vous aideront à travailler efficacement avec les données DIB de cette manière.</span><span class="sxs-lookup"><span data-stu-id="98913-114">The following sections provide background information that will help you work effectively with DIB data in this manner.</span></span>

> [!Note]  
> <span data-ttu-id="98913-115">Vous pouvez également modifier les bits à l’aide des fonctions GDI, GDI+, DirectDraw ou Direct3D, mais ces techniques n’entrent pas dans le cadre de cet article.</span><span class="sxs-lookup"><span data-stu-id="98913-115">You can also modify the bits by using GDI, GDI+, DirectDraw or Direct3D functions, but these techniques are beyond the scope of this article.</span></span>

 

<span data-ttu-id="98913-116">Cette section contient les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="98913-116">This section contains the following topics:</span></span>

-   [<span data-ttu-id="98913-117">Bottom-Up de haut en haut et DIB</span><span class="sxs-lookup"><span data-stu-id="98913-117">Top-Down vs. Bottom-Up DIBs</span></span>](top-down-vs--bottom-up-dibs.md)
-   [<span data-ttu-id="98913-118">Utilisation d’une couleur RVB 16 bits</span><span class="sxs-lookup"><span data-stu-id="98913-118">Working with 16-bit RGB</span></span>](working-with-16-bit-rgb.md)

 

 



