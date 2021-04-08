---
title: Écriture de flux d’images
description: Écriture de flux d’images
ms.assetid: 3a017bdd-9723-4b7f-b5e1-22838c0ba4ff
keywords:
- ASF (Advanced Systems Format), écriture de flux d’images
- ASF (format de systèmes avancés), écrire des flux d’images
- ASF (Advanced Systems Format), flux d’images
- ASF (format des systèmes avancés), flux d’images
- flux d’images, écriture
- flux, écrire des flux d’images
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60daa9b62701c172d127c4cff1fb6c301edf7d86
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103940686"
---
# <a name="writing-image-streams"></a><span data-ttu-id="7fecf-109">Écriture de flux d’images</span><span class="sxs-lookup"><span data-stu-id="7fecf-109">Writing Image Streams</span></span>

<span data-ttu-id="7fecf-110">Les entrées d’un flux d’image doivent être des images bitmap au format RVB.</span><span class="sxs-lookup"><span data-stu-id="7fecf-110">The inputs for an image stream must be RGB-formatted bitmap images.</span></span> <span data-ttu-id="7fecf-111">L’enregistreur coordonne la compression des exemples d’images d’entrée à l’aide du format JPEG.</span><span class="sxs-lookup"><span data-stu-id="7fecf-111">The writer coordinates the compression of input image samples using the JPEG format.</span></span> <span data-ttu-id="7fecf-112">Avant de commencer à écrire un fichier contenant un flux d’image, vous devez définir une qualité d’image pour l’entrée, à l’aide du \_ paramètre g wszJPEGCompressionQuality.</span><span class="sxs-lookup"><span data-stu-id="7fecf-112">Before you begin writing a file containing an image stream, you must set an image quality for the input, using the g\_wszJPEGCompressionQuality setting.</span></span> <span data-ttu-id="7fecf-113">Utilisez [**IWMWriterAdvanced2 :: SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) pour définir la qualité sur une valeur **DWORD** comprise entre 1 et 100.</span><span class="sxs-lookup"><span data-stu-id="7fecf-113">Use [**IWMWriterAdvanced2::SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) to set the quality to a **DWORD** value ranging from 1 to 100.</span></span> <span data-ttu-id="7fecf-114">Les valeurs basses représentent un taux de compression élevé au détriment de la qualité, tandis que les valeurs élevées produisent des images de haute qualité qui nécessitent davantage d’espace.</span><span class="sxs-lookup"><span data-stu-id="7fecf-114">Low values represent a high compression ratio at the expense of quality, while high values produce high quality images that require more space.</span></span>

<span data-ttu-id="7fecf-115">Les flux d’image requièrent souvent des mémoires tampons plus volumineuses que les flux vidéo ordinaires.</span><span class="sxs-lookup"><span data-stu-id="7fecf-115">Image streams often require larger buffer windows than ordinary video streams.</span></span> <span data-ttu-id="7fecf-116">La taille exacte requise dépend du type d’image et de la qualité de l’image, entre autres facteurs.</span><span class="sxs-lookup"><span data-stu-id="7fecf-116">The exact size required depends on the type of image and the image quality, among other factors.</span></span> <span data-ttu-id="7fecf-117">Utilisez la version d’évaluation et l’erreur pour déterminer la taille appropriée pour les images que vous souhaitez traiter.</span><span class="sxs-lookup"><span data-stu-id="7fecf-117">Use trial and error to determine the appropriate size for the images you intend to process.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7fecf-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7fecf-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7fecf-119">**Flux d’images**</span><span class="sxs-lookup"><span data-stu-id="7fecf-119">**Image Streams**</span></span>](image-streams.md)
</dt> <dt>

[<span data-ttu-id="7fecf-120">**Pour définir les paramètres d’entrée**</span><span class="sxs-lookup"><span data-stu-id="7fecf-120">**To Set Input Settings**</span></span>](to-set-input-settings.md)
</dt> <dt>

[<span data-ttu-id="7fecf-121">**Écriture de fichiers ASF**</span><span class="sxs-lookup"><span data-stu-id="7fecf-121">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




