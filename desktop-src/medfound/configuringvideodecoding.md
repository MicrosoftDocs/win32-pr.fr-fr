---
description: Configuration du décodage vidéo
ms.assetid: 897b8e2d-9827-428d-91ae-632038c4c8c0
title: Configuration du décodage vidéo (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f386e3dbb39d6296756f2fe8eec1b94c5533bff0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106530826"
---
# <a name="configuring-video-decoding-microsoft-media-foundation"></a><span data-ttu-id="ee21e-103">Configuration du décodage vidéo (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="ee21e-103">Configuring Video Decoding (Microsoft Media Foundation)</span></span>

<span data-ttu-id="ee21e-104">Le décodage est essentiellement l’opposé de l’encodage en termes de configuration.</span><span class="sxs-lookup"><span data-stu-id="ee21e-104">Decoding is essentially the opposite of encoding in terms of configuration.</span></span> <span data-ttu-id="ee21e-105">Le décodeur prend en charge très peu de propriétés et aucun d’entre eux n’est requis.</span><span class="sxs-lookup"><span data-stu-id="ee21e-105">The decoder supports very few properties, and none of them is required.</span></span> <span data-ttu-id="ee21e-106">Définissez le type d’entrée sur le type utilisé pour la sortie du décodeur (y compris les données privées du codec).</span><span class="sxs-lookup"><span data-stu-id="ee21e-106">Set the input type to the type used for the decoder output (including the codec private data).</span></span> <span data-ttu-id="ee21e-107">Ensuite, définissez la sortie au format non compressé souhaité, définissez la structure [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) pour qu’elle reflète la taille d’image appropriée et commencez le traitement des exemples.</span><span class="sxs-lookup"><span data-stu-id="ee21e-107">Then set the output to the desired uncompressed format, set the [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure to reflect the proper frame size, and start processing samples.</span></span>

<span data-ttu-id="ee21e-108">Vous devez fournir au décodeur un type de média qui comprend les données privées de codec positionnées immédiatement après la structure [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) .</span><span class="sxs-lookup"><span data-stu-id="ee21e-108">You must supply the decoder with a media type that includes the codec private data positioned immediately after the [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure.</span></span> <span data-ttu-id="ee21e-109">Le décodeur ne peut pas décoder le contenu sans ces données.</span><span class="sxs-lookup"><span data-stu-id="ee21e-109">The decoder cannot decode the content without this data.</span></span> <span data-ttu-id="ee21e-110">La validation de format effectuée par le décodeur ne valide pas les données privées.</span><span class="sxs-lookup"><span data-stu-id="ee21e-110">The format validation performed by the decoder does not validate the private data.</span></span> <span data-ttu-id="ee21e-111">Si les données privées du codec sont manquantes ou incorrectes, le décodeur répond comme si le flux de bits était endommagé.</span><span class="sxs-lookup"><span data-stu-id="ee21e-111">If the codec private data is missing or incorrect, the decoder responds as if the bit stream is corrupted.</span></span> <span data-ttu-id="ee21e-112">Pour plus d’informations, consultez [utilisation de données privées de codec vidéo](usingvideocodecprivatedata.md).</span><span class="sxs-lookup"><span data-stu-id="ee21e-112">For more information, see [Using Video Codec Private Data](usingvideocodecprivatedata.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ee21e-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ee21e-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ee21e-114">Utilisation de données privées de codec vidéo</span><span class="sxs-lookup"><span data-stu-id="ee21e-114">Using Video Codec Private Data</span></span>](usingvideocodecprivatedata.md)
</dt> <dt>

[<span data-ttu-id="ee21e-115">Utilisation de la vidéo</span><span class="sxs-lookup"><span data-stu-id="ee21e-115">Working with Video</span></span>](workingwithvideo.md)
</dt> </dl>

 

 
