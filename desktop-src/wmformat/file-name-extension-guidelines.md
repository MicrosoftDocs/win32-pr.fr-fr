---
title: Instructions relatives à l’extension de nom de fichier
description: Instructions relatives à l’extension de nom de fichier
ms.assetid: 71189ed8-4140-446f-a765-d72f35dd3d88
keywords:
- Windows Media Format SDK, extensions de nom de fichier
- ASF (Advanced Systems Format), extensions de noms de fichiers
- ASF (format de systèmes avancés), extensions de nom de fichier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bed1fb59379644711a3954dc5eb82707e0e42f8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939918"
---
# <a name="file-name-extension-guidelines"></a><span data-ttu-id="5896b-106">Instructions relatives à l’extension de nom de fichier</span><span class="sxs-lookup"><span data-stu-id="5896b-106">File Name Extension Guidelines</span></span>

<span data-ttu-id="5896b-107">Une extension de nom de fichier fournit à un éditeur de logiciels indépendant des informations sur les exigences de rendu d’une application qui utilise cette extension particulière.</span><span class="sxs-lookup"><span data-stu-id="5896b-107">A file name extension provides an independent software vendor with information about the rendering requirements of an application that uses that particular extension.</span></span>

<span data-ttu-id="5896b-108">L’extension de nom de fichier que vous devez utiliser pour un fichier créé par une application basée sur le kit de développement logiciel (SDK) Windows Media format est déterminée par le type de contenu du fichier.</span><span class="sxs-lookup"><span data-stu-id="5896b-108">The file name extension you must use for a file created by an application based on the Windows Media Format SDK is determined by the type of content in the file.</span></span> <span data-ttu-id="5896b-109">Utilisez la logique suivante pour déterminer l’extension de nom de fichier que vous devez utiliser.</span><span class="sxs-lookup"><span data-stu-id="5896b-109">Use the following logic to determine the file name extension you must use.</span></span>

<span data-ttu-id="5896b-110">Si le fichier contient des flux encodés avec des codecs tiers ou des données non compressées non prises en charge (y compris des données arbitraires), le fichier doit utiliser l’extension. ASF.</span><span class="sxs-lookup"><span data-stu-id="5896b-110">If the file contains any streams encoded with third-party codecs or any unsupported uncompressed data (including arbitrary data), the file must use the .asf extension.</span></span>

<span data-ttu-id="5896b-111">Si le fichier ne contient pas de flux non pris en charge et contient un ou plusieurs flux vidéo décompressés ou encodés avec n’importe quel codec vidéo Windows Media, le fichier doit utiliser l’extension. wmv.</span><span class="sxs-lookup"><span data-stu-id="5896b-111">If the file contains no unsupported streams and contains one or more video streams either uncompressed or encoded with any Windows Media video codec, the file must use the .wmv extension.</span></span> <span data-ttu-id="5896b-112">Ces fichiers peuvent également inclure des flux audio PCM, des flux audio encodés avec n’importe quel codec audio Windows Media, flux de script et flux Web.</span><span class="sxs-lookup"><span data-stu-id="5896b-112">These files may also include PCM audio streams, audio streams encoded with any Windows Media audio codec, script streams, and Web streams.</span></span>

<span data-ttu-id="5896b-113">Si le fichier ne contient pas de flux non pris en charge et qu’aucun flux vidéo n’est pris en charge, et contient un ou plusieurs flux audio non compressés PCM ou encodés avec n’importe quel codec audio Windows Media, le fichier doit utiliser l’extension. WMA.</span><span class="sxs-lookup"><span data-stu-id="5896b-113">If the file contains no unsupported streams and no supported video streams, and contains one or more audio streams either uncompressed PCM or encoded with any Windows Media audio codec, the file must use the .wma extension.</span></span> <span data-ttu-id="5896b-114">Ces fichiers peuvent également contenir des flux de script et des flux Web.</span><span class="sxs-lookup"><span data-stu-id="5896b-114">These files may also contain script streams, and Web streams.</span></span>

<span data-ttu-id="5896b-115">Si le fichier contient uniquement des flux qui ne sont ni des données audio ni des vidéos, il doit utiliser l’extension. ASF.</span><span class="sxs-lookup"><span data-stu-id="5896b-115">If the file contains only streams that are neither audio nor video, it must use the .asf extension.</span></span>

<span data-ttu-id="5896b-116">Les types de vidéo non compressés pris en charge sont RGB8, RGB565, RGB555, RGB24, RGB32, I420, IYUV, YV12, YUY2, UYVY, YVYU et YVU9.</span><span class="sxs-lookup"><span data-stu-id="5896b-116">Supported uncompressed video types include RGB8, RGB565, RGB555, RGB24, RGB32, I420, IYUV, YV12, YUY2, UYVY, YVYU, and YVU9.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5896b-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5896b-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5896b-118">**Considérations relatives aux projets**</span><span class="sxs-lookup"><span data-stu-id="5896b-118">**Project Considerations**</span></span>](project-considerations.md)
</dt> </dl>

 

 




