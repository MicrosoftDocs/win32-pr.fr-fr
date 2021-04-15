---
title: À propos du gestionnaire de compression vidéo
description: À propos du gestionnaire de compression vidéo
ms.assetid: 2a5ebc95-3ee8-4145-b2c5-512d82e49c6d
keywords:
- Multimédia Windows, gestionnaire de compression vidéo (VCM)
- multimédia, gestionnaire de compression vidéo (VCM)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6841446a5a0f22b8c05c2419448e65b035f90703
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104463059"
---
# <a name="about-the-video-compression-manager"></a><span data-ttu-id="026b3-105">À propos du gestionnaire de compression vidéo</span><span class="sxs-lookup"><span data-stu-id="026b3-105">About the Video Compression Manager</span></span>

<span data-ttu-id="026b3-106">En règle générale, les compresseurs installables utilisent des données d’image vidéo stockées dans des fichiers AVI (Audio-Video entrelacés).</span><span class="sxs-lookup"><span data-stu-id="026b3-106">Typically, installable compressors operate with video-image data stored in audio-video interleaved (AVI) files.</span></span> <span data-ttu-id="026b3-107">Cette vue d’ensemble explique les techniques de programmation utilisées pour accéder aux compresseurs installables par le biais de VCM et aborde les sujets suivants :</span><span class="sxs-lookup"><span data-stu-id="026b3-107">This overview explains the programming techniques used to access installable compressors through VCM and covers the following topics:</span></span>

-   <span data-ttu-id="026b3-108">VCM et vidéo pour l’architecture Windows</span><span class="sxs-lookup"><span data-stu-id="026b3-108">VCM and the Video for Windows architecture</span></span>
-   <span data-ttu-id="026b3-109">Compression et décompression des données d’image de votre application</span><span class="sxs-lookup"><span data-stu-id="026b3-109">Compressing and decompressing image data from your application</span></span>
-   <span data-ttu-id="026b3-110">Utilisation de convertisseurs VCM pour dessiner des données à partir de votre application</span><span class="sxs-lookup"><span data-stu-id="026b3-110">Using VCM renderers to draw data from your application</span></span>
-   <span data-ttu-id="026b3-111">Structures et fonctions VCM</span><span class="sxs-lookup"><span data-stu-id="026b3-111">VCM functions and structures</span></span>

<span data-ttu-id="026b3-112">Avant de lire cette vue d’ensemble, vous devez être familiarisé avec les services graphiques Microsoft Win32.</span><span class="sxs-lookup"><span data-stu-id="026b3-112">Before you read this overview, you should be familiar with the Microsoft Win32 graphic services.</span></span> <span data-ttu-id="026b3-113">En particulier, les bitmaps et les structures associées à la bitmap, telles que [**BITMAPINFO,**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) et [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader), sont largement utilisées par VCM.</span><span class="sxs-lookup"><span data-stu-id="026b3-113">In particular, bitmaps and bitmap-related structures, such as [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) and [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader), are used extensively by VCM.</span></span> <span data-ttu-id="026b3-114">Pour plus d’informations sur les structures **BITMAPINFO,** et **BITMAPINFOHEADER** , consultez [bitmaps](/previous-versions//ms532349(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="026b3-114">For additional information about the **BITMAPINFO** and **BITMAPINFOHEADER** structures, see [Bitmaps](/previous-versions//ms532349(v=vs.85)).</span></span>

> [!Note]  
> <span data-ttu-id="026b3-115">Le gestionnaire de compression audio (ACM) fournit une prise en charge au niveau du système pour les pilotes de compression et de décompression audio.</span><span class="sxs-lookup"><span data-stu-id="026b3-115">The audio compression manager (ACM) provides system-level support for audio compression and decompression drivers.</span></span> <span data-ttu-id="026b3-116">Pour obtenir une description des services de compression audio, consultez [Gestionnaire de compression audio](audio-compression-manager.md).</span><span class="sxs-lookup"><span data-stu-id="026b3-116">For a description of the audio compression services, see [Audio Compression Manager](audio-compression-manager.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="026b3-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="026b3-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="026b3-118">Gestionnaire de compression vidéo</span><span class="sxs-lookup"><span data-stu-id="026b3-118">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> </dl>

 

 