---
description: Encodage vidéo avec compression temporelle
ms.assetid: df363017-97c5-45b0-b8a5-44ac73b7a0e7
title: Encodage vidéo avec compression temporelle (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ee107d8bf6b1ef6b1700abff105b0bdb79f72f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518408"
---
# <a name="video-encoding-with-temporal-compression-microsoft-media-foundation"></a><span data-ttu-id="440f6-103">Encodage vidéo avec compression temporelle (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="440f6-103">Video Encoding with Temporal Compression (Microsoft Media Foundation)</span></span>

<span data-ttu-id="440f6-104">Pour obtenir les taux de compression les plus élevés possibles, les codecs Windows Media Video utilisent la *compression temporelle*.</span><span class="sxs-lookup"><span data-stu-id="440f6-104">To achieve the highest compression ratios possible, the Windows Media Video codecs use *temporal compression*.</span></span> <span data-ttu-id="440f6-105">La compression temporelle est une technique qui consiste à réduire la taille de la vidéo compressée en n’codant pas chaque frame en tant qu’image complète.</span><span class="sxs-lookup"><span data-stu-id="440f6-105">Temporal compression is a technique of reducing compressed video size by not encoding each frame as a complete image.</span></span> <span data-ttu-id="440f6-106">Les frames encodés complètement (comme une image statique) sont appelés *images clés*.</span><span class="sxs-lookup"><span data-stu-id="440f6-106">The frames that are encoded completely (like a static image) are called *key frames*.</span></span> <span data-ttu-id="440f6-107">Toutes les autres images de la vidéo sont représentées par des données qui spécifient la modification depuis la dernière image.</span><span class="sxs-lookup"><span data-stu-id="440f6-107">All other frames in the video are represented by data specifying the change since the last frame.</span></span> <span data-ttu-id="440f6-108">Ces frames sont appelés des *frames Delta*.</span><span class="sxs-lookup"><span data-stu-id="440f6-108">These frames are called *delta frames*.</span></span>

<span data-ttu-id="440f6-109">La quantité de compression qui peut être obtenue à l’aide de la compression temporelle dépend du contenu.</span><span class="sxs-lookup"><span data-stu-id="440f6-109">The amount of compression that can be achieved using temporal compression depends upon the content.</span></span> <span data-ttu-id="440f6-110">Si la vidéo est statique, sans mouvement important ou autre modification dans l’image, de nombreuses images Delta peuvent être créées pour chaque image clé.</span><span class="sxs-lookup"><span data-stu-id="440f6-110">If the video is static, without a lot of motion or other changes in image, many delta frames can be created for each key frame.</span></span> <span data-ttu-id="440f6-111">Plus le nombre d’images Delta utilisées est élevé, plus le flux vidéo encodé est petit.</span><span class="sxs-lookup"><span data-stu-id="440f6-111">The more delta frames that are used, the smaller the encoded video stream.</span></span> <span data-ttu-id="440f6-112">Toutefois, si la vidéo est dynamique, avec un grand nombre de couleurs animées ou changeantes, l’avantage de l’utilisation de la compression temporelle est plus petit.</span><span class="sxs-lookup"><span data-stu-id="440f6-112">However, if the video is dynamic, with lots of motion or changing colors, the benefit of using temporal compression is smaller.</span></span>

## <a name="related-topics"></a><span data-ttu-id="440f6-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="440f6-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="440f6-114">Utilisation de la vidéo</span><span class="sxs-lookup"><span data-stu-id="440f6-114">Working with Video</span></span>](workingwithvideo.md)
</dt> </dl>

 

 



