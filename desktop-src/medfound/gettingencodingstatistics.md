---
description: Décrit les statistiques que vous pouvez récupérer à partir d’un codec Windows Media.
ms.assetid: 86c029af-e0fb-436a-b758-3f7d10c8bdeb
title: Obtention des statistiques d’encodage (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92fb298b35e9cd4114d1a5ba2f5badfad36c09c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749220"
---
# <a name="getting-encoding-statistics-microsoft-media-foundation"></a><span data-ttu-id="75ca3-103">Obtention des statistiques d’encodage (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="75ca3-103">Getting Encoding Statistics (Microsoft Media Foundation)</span></span>

<span data-ttu-id="75ca3-104">Les informations relatives à ce qui se passe dans une session d’encodage sont généralement immédiatement disponibles sous la forme de codes d’erreur retournés lors du traitement des exemples.</span><span class="sxs-lookup"><span data-stu-id="75ca3-104">Information about what is happening in an encoding session is generally immediately available in the form of error codes returned when processing samples.</span></span> <span data-ttu-id="75ca3-105">Toutefois, il existe des statistiques que vous pouvez récupérer à partir du codec sur différents aspects d’encodage.</span><span class="sxs-lookup"><span data-stu-id="75ca3-105">However, there are some statistics that you can retrieve from the codec about various encoding aspects.</span></span>

## <a name="video-frame-information"></a><span data-ttu-id="75ca3-106">Informations sur les trames vidéo</span><span class="sxs-lookup"><span data-stu-id="75ca3-106">Video Frame Information</span></span>

<span data-ttu-id="75ca3-107">Certaines statistiques vidéo que vous pouvez récupérer avec le nombre de trames traitées par l’encodeur.</span><span class="sxs-lookup"><span data-stu-id="75ca3-107">Some video statistics that you can retrieve deal with the number of frames processed by the encoder.</span></span> <span data-ttu-id="75ca3-108">Il existe trois propriétés de nombre d’images que vous pouvez lire à partir de l’encodeur vidéo :</span><span class="sxs-lookup"><span data-stu-id="75ca3-108">There are three frame number properties that you can read from the video encoder:</span></span>

-   <span data-ttu-id="75ca3-109">[MFPKEY \_ TOTALFRAMES](mfpkey-totalframesproperty.md) est le nombre de trames traitées par le biais du flux d’entrée de la DMO.</span><span class="sxs-lookup"><span data-stu-id="75ca3-109">[MFPKEY\_TOTALFRAMES](mfpkey-totalframesproperty.md) is the number of frames processed through the input stream of the DMO.</span></span>
-   <span data-ttu-id="75ca3-110">[MFPKEY \_ CODEDFRAMES](mfpkey-codedframesproperty.md) est le nombre de trames encodées.</span><span class="sxs-lookup"><span data-stu-id="75ca3-110">[MFPKEY\_CODEDFRAMES](mfpkey-codedframesproperty.md) is the number of frames encoded.</span></span> <span data-ttu-id="75ca3-111">En soustrayant cette valeur du nombre total de frames passés, vous pouvez déterminer le nombre de frames qui ont été supprimés.</span><span class="sxs-lookup"><span data-stu-id="75ca3-111">By subtracting this value from the total number of frames passed, you can determine how many frames were dropped.</span></span>
-   <span data-ttu-id="75ca3-112">[MFPKEY \_ ZEROBYTEFRAMES](mfpkey-zerobyteframesproperty.md) est le nombre de trames qui ne sont pas encodées, car il s’agit déjà d’un contenu dupliqué.</span><span class="sxs-lookup"><span data-stu-id="75ca3-112">[MFPKEY\_ZEROBYTEFRAMES](mfpkey-zerobyteframesproperty.md) is the number of frames not encoded because they duplicated content already included.</span></span> <span data-ttu-id="75ca3-113">Cette valeur n’est pas soustraite du nombre d’images codées signalées par DMO.</span><span class="sxs-lookup"><span data-stu-id="75ca3-113">This value is not subtracted from the number of coded frames reported by the DMO.</span></span>

<span data-ttu-id="75ca3-114">Vous pouvez lire les propriétés de l’image vidéo à tout moment pendant l’encodage.</span><span class="sxs-lookup"><span data-stu-id="75ca3-114">You can read video frame properties at any time during encoding.</span></span> <span data-ttu-id="75ca3-115">Cela peut être utile pour déterminer si les paramètres d’encodage sont adaptés à votre contenu. s’il existe une grande différence entre les trames totales et les trames codées, le contenu compressé peut ne pas répondre à vos besoins en matière de qualité.</span><span class="sxs-lookup"><span data-stu-id="75ca3-115">This can be useful in determining if the encoding settings are appropriate for your content; if there is a large difference between total frames and coded frames, the compressed content might not meet your quality requirements.</span></span> <span data-ttu-id="75ca3-116">Vous pouvez lire les valeurs finales une fois l’encodage terminé.</span><span class="sxs-lookup"><span data-stu-id="75ca3-116">You can read the final values after you finish encoding.</span></span>

## <a name="vbr-buffer-statistics"></a><span data-ttu-id="75ca3-117">Statistiques du tampon VBR</span><span class="sxs-lookup"><span data-stu-id="75ca3-117">VBR Buffer Statistics</span></span>

<span data-ttu-id="75ca3-118">En fonction du mode d’encodage utilisé, une partie ou la totalité des paramètres de la mémoire tampon peut être déterminée lors de l’encodage (par exemple, la vitesse de transmission du VBR basé sur la qualité n’est pas connue tant que le contenu n’est pas encodé).</span><span class="sxs-lookup"><span data-stu-id="75ca3-118">Depending upon the encoding mode used, some or all of the buffer settings may be determined during encoding (for example, the bit rate of quality based VBR is not known until the content is encoded).</span></span> <span data-ttu-id="75ca3-119">Il existe quatre propriétés de mémoire tampon VBR que vous pouvez obtenir à l’aide de la méthode **IPropertyBag :: Read** :</span><span class="sxs-lookup"><span data-stu-id="75ca3-119">There are four VBR buffer properties that you can get using the **IPropertyBag::Read** method:</span></span>

-   <span data-ttu-id="75ca3-120">[MFPKEY \_ RAVG](mfpkey-ravgproperty.md) est la vitesse de transmission moyenne du contenu VBR.</span><span class="sxs-lookup"><span data-stu-id="75ca3-120">[MFPKEY\_RAVG](mfpkey-ravgproperty.md) is the average bit rate of the VBR content.</span></span>
-   <span data-ttu-id="75ca3-121">[MFPKEY \_ BAVG](mfpkey-bavgproperty.md) est la fenêtre de mémoire tampon pour la vitesse de transmission moyenne.</span><span class="sxs-lookup"><span data-stu-id="75ca3-121">[MFPKEY\_BAVG](mfpkey-bavgproperty.md) is the buffer window for the average bit rate.</span></span>
-   <span data-ttu-id="75ca3-122">[MFPKEY \_ RMAX](mfpkey-rmaxproperty.md) est le taux binaire de pointe du contenu VBR.</span><span class="sxs-lookup"><span data-stu-id="75ca3-122">[MFPKEY\_RMAX](mfpkey-rmaxproperty.md) is the peak bit rate of the VBR content.</span></span>
-   <span data-ttu-id="75ca3-123">[MFPKEY \_ BMAX](mfpkey-bmaxproperty.md) est la fenêtre de mémoire tampon de pointe.</span><span class="sxs-lookup"><span data-stu-id="75ca3-123">[MFPKEY\_BMAX](mfpkey-bmaxproperty.md) is the peak buffer window.</span></span>

<span data-ttu-id="75ca3-124">Une fois que vous avez commencé le traitement des exemples, vous ne devez pas lire les propriétés VBR tant que vous n’avez pas terminé d’encoder le flux.</span><span class="sxs-lookup"><span data-stu-id="75ca3-124">After you begin processing samples, you should not read any of the VBR properties until you are finished encoding the stream.</span></span> <span data-ttu-id="75ca3-125">Si vous le faites, l’encodeur interprète votre demande comme un signal indiquant que l’encodage est terminé.</span><span class="sxs-lookup"><span data-stu-id="75ca3-125">If you do, the encoder interprets your request as a signal that the encoding is complete.</span></span> <span data-ttu-id="75ca3-126">L’exemple suivant que vous traitez est traité comme une nouvelle session d’encodage.</span><span class="sxs-lookup"><span data-stu-id="75ca3-126">The next sample that you process is treated as a new encoding session.</span></span>

## <a name="related-topics"></a><span data-ttu-id="75ca3-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="75ca3-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="75ca3-128">Codecs Windows Media</span><span class="sxs-lookup"><span data-stu-id="75ca3-128">Windows Media Codecs</span></span>](windows-media-codecs.md)
</dt> </dl>

 

 



