---
description: Recherche de types de sortie d’encodeur audio
ms.assetid: cd47d45b-ea47-4dec-867e-d51145d7f084
title: Recherche de types de sortie d’encodeur audio (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5389274cca1178ebc0ae03e21f7a804f73a5db48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106541179"
---
# <a name="finding-audio-encoder-output-types-microsoft-media-foundation"></a><span data-ttu-id="2d0c3-103">Recherche de types de sortie d’encodeur audio (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="2d0c3-103">Finding Audio Encoder Output Types (Microsoft Media Foundation)</span></span>

<span data-ttu-id="2d0c3-104">Étant donné que vous devez utiliser un format de sortie d’encodeur audio qui est énuméré par l’encodeur audio, vous devez disposer d’un moyen de rechercher le format le plus adapté à vos besoins.</span><span class="sxs-lookup"><span data-stu-id="2d0c3-104">Because you must use an audio encoder output format that is enumerated by the audio encoder, you need to have a way of finding the format that is most suited to your needs.</span></span> <span data-ttu-id="2d0c3-105">Le nombre de canaux, le nombre de bits par échantillon et le taux d’échantillonnage de la sortie que vous choisissez doivent correspondre aux valeurs du contenu que vous compressez.</span><span class="sxs-lookup"><span data-stu-id="2d0c3-105">The number of channels, bits per sample, and sample rate of the output that you choose must match the values for the content that you compress.</span></span> <span data-ttu-id="2d0c3-106">Toutefois, l’encodeur peut prendre en charge plusieurs types au sein de ces contraintes.</span><span class="sxs-lookup"><span data-stu-id="2d0c3-106">However, the encoder may support several types within these constraints.</span></span>

<span data-ttu-id="2d0c3-107">Le facteur de décision pour le choix d’un type est la vitesse de transmission du flux encodé. vous souhaitez trouver un type de média qui correspond à votre entrée et a une vitesse de transmission aussi proche que possible d’une valeur cible.</span><span class="sxs-lookup"><span data-stu-id="2d0c3-107">The deciding factor for choosing a type is the bit rate of the encoded stream; you want to find a media type that matches your input and has a bit rate that is as close as possible to a target value.</span></span> <span data-ttu-id="2d0c3-108">Si vous énumérez des types de sortie VBR à un passage, il s’agit de la valeur de qualité qui détermine le type que vous utilisez.</span><span class="sxs-lookup"><span data-stu-id="2d0c3-108">If you are enumerating one-pass VBR output types, it is the quality value that will decide the type you use.</span></span> <span data-ttu-id="2d0c3-109">Pour plus d’informations sur les valeurs de qualité dans les types de sortie énumérés, consultez [énumération des types audio pour des modes d’encodage spécifiques](enumeratingaudiotypesforspecificencodingmodes.md).</span><span class="sxs-lookup"><span data-stu-id="2d0c3-109">For more information about quality values in enumerated output types, see [Enumerating Audio Types for Specific Encoding Modes](enumeratingaudiotypesforspecificencodingmodes.md).</span></span>

> [!Note]  
>    <span data-ttu-id="2d0c3-110">L’encodeur audio énumère certains types qui sont des doublons d’autres types de presque toutes les façons.</span><span class="sxs-lookup"><span data-stu-id="2d0c3-110">The audio encoder enumerates some types that are duplicates of other types in almost all ways.</span></span> <span data-ttu-id="2d0c3-111">Ces doublons existent pour les formats dans lesquels le nombre de paquets par seconde ne correspond pas à la configuration requise pour le stockage dans les fichiers ASF lors de la synchronisation avec la vidéo.</span><span class="sxs-lookup"><span data-stu-id="2d0c3-111">These duplicates exist for formats where the number of packets per second does not meet the requirements for storage in ASF files when synchronized with video.</span></span> <span data-ttu-id="2d0c3-112">L’audio synchronisé avec la vidéo dans un fichier ASF doit avoir au moins 3 paquets par seconde pour les vitesses de transmission inférieures à 32000, et 5 paquets ou plus par seconde pour les vitesses de bits supérieures ou égales à 32000.</span><span class="sxs-lookup"><span data-stu-id="2d0c3-112">Audio synchronized with video in an ASF file must have 3 or more packets per second for bit rates less than 32000, and 5 or more packets per second for bit rates greater than or equal to 32000.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="2d0c3-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2d0c3-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2d0c3-114">Configuration de l’encodage audio</span><span class="sxs-lookup"><span data-stu-id="2d0c3-114">Configuring Audio Encoding</span></span>](configuringaudioencoding.md)
</dt> <dt>

[<span data-ttu-id="2d0c3-115">Énumération des types audio pour des modes d’encodage spécifiques</span><span class="sxs-lookup"><span data-stu-id="2d0c3-115">Enumerating Audio Types for Specific Encoding Modes</span></span>](enumeratingaudiotypesforspecificencodingmodes.md)
</dt> </dl>

 

 



