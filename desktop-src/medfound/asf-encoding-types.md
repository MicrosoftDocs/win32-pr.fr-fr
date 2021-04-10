---
description: Types d’encodage ASF
ms.assetid: ffa99c6b-3b62-4068-96d5-ad57c340d088
title: Types d’encodage ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c6187f4bbf49eafaf50a46a8af92b71b4e72885
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111891"
---
# <a name="asf-encoding-types"></a><span data-ttu-id="addca-103">Types d’encodage ASF</span><span class="sxs-lookup"><span data-stu-id="addca-103">ASF Encoding Types</span></span>

<span data-ttu-id="addca-104">Les méthodes d’encodage se concentrent sur la mémoire tampon utilisée par l’encodeur pour gérer les données d’entrée non compressées.</span><span class="sxs-lookup"><span data-stu-id="addca-104">The encoding methods all focus on the buffer used by the encoder to manage uncompressed input data.</span></span> <span data-ttu-id="addca-105">Cette mémoire tampon est définie par la vitesse de transmission du flux, en bits par seconde, et la fenêtre de mémoire tampon, en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="addca-105">This buffer is defined by the bit rate of the stream, in bits per second, and the buffer window, in milliseconds.</span></span> <span data-ttu-id="addca-106">Lors de l’encodage de fichiers ASF, les encodeurs Windows Media respectent les contraintes de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="addca-106">When encoding to ASF files, the Windows Media encoders abide by the constraints of the buffer.</span></span> <span data-ttu-id="addca-107">Pour plus d’informations sur la fenêtre de mémoire tampon, consultez [le modèle de tampon de compartiment](the-leaky-bucket-buffer-model.md)perdu.</span><span class="sxs-lookup"><span data-stu-id="addca-107">For more information about the buffer window, see [The Leaky Bucket Buffer Model](the-leaky-bucket-buffer-model.md).</span></span> <span data-ttu-id="addca-108">Savoir quand et comment utiliser chaque méthode peut vous aider à créer du contenu compressé de haute qualité.</span><span class="sxs-lookup"><span data-stu-id="addca-108">Knowing how and when to use each method can help you create high-quality compressed content.</span></span> <span data-ttu-id="addca-109">Le tableau suivant contient des liens vers des rubriques relatives à chacune des méthodes d’encodage disponibles qu’une application peut utiliser pour encoder les données multimédias en ASF.</span><span class="sxs-lookup"><span data-stu-id="addca-109">The following table contains links to topics about each of the available encoding methods that an application can use to encode media data to ASF.</span></span>



| <span data-ttu-id="addca-110">Méthode de codage</span><span class="sxs-lookup"><span data-stu-id="addca-110">Encoding method</span></span>                                                                                      | <span data-ttu-id="addca-111">Description</span><span class="sxs-lookup"><span data-stu-id="addca-111">Description</span></span>                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="addca-112">Encodage à vitesse binaire constante</span><span class="sxs-lookup"><span data-stu-id="addca-112">Constant Bit Rate Encoding</span></span>](constant-bit-rate-encoding.md)                                         | <span data-ttu-id="addca-113">L’encodeur compresse les données à une vitesse de transmission spécifiée.</span><span class="sxs-lookup"><span data-stu-id="addca-113">The encoder compresses data to a specified bit rate.</span></span>                                                                                                                                                     |
| [<span data-ttu-id="addca-114">Encodage de la vitesse de transmission variable basée sur la qualité</span><span class="sxs-lookup"><span data-stu-id="addca-114">Quality-Based Variable Bit Rate Encoding</span></span>](quality-based-variable-bit-rate--vbr--encoding.md)       | <span data-ttu-id="addca-115">L’encodeur compresse les données à une valeur de qualité particulière afin que la qualité du média encodé soit cohérente tout au long de sa durée, indépendamment des exigences de mémoire tampon du flux résultant.</span><span class="sxs-lookup"><span data-stu-id="addca-115">The encoder compresses data to a particular quality value so that the quality of the encoded media is consistent throughout its duration, regardless of the buffer requirements of the resulting stream.</span></span> |
| [<span data-ttu-id="addca-116">Encodage de la vitesse de transmission variable sans contrainte</span><span class="sxs-lookup"><span data-stu-id="addca-116">Unconstrained Variable Bit Rate Encoding</span></span>](unconstrained-variable-bit-rate--vbr--encoding.md)       | <span data-ttu-id="addca-117">L’encodeur compresse les données à la meilleure qualité possible tout en conservant une vitesse de transmission spécifiée.</span><span class="sxs-lookup"><span data-stu-id="addca-117">The encoder compresses data to the highest possible quality while maintaining a specified bit rate.</span></span> <span data-ttu-id="addca-118">Ce mode est également appelé encodage VBR (variable bit rate) à 2 passes.</span><span class="sxs-lookup"><span data-stu-id="addca-118">This mode is also called 2-pass variable bit rate (VBR) encoding.</span></span>                                    |
| [<span data-ttu-id="addca-119">Chiffrement à vitesse de transmission variable à forte limite</span><span class="sxs-lookup"><span data-stu-id="addca-119">Peak-Constrained Variable Bit Rate Encoding</span></span>](peak-constrained-variable-bit-rate--vbr--encoding.md) | <span data-ttu-id="addca-120">L’encodeur compresse les données à une vitesse de transmission spécifiée tout en conservant les valeurs de mémoire tampon dans la fenêtre de mémoire tampon maximale et la vitesse de transmission spécifiées.</span><span class="sxs-lookup"><span data-stu-id="addca-120">The encoder compresses data to a specified bit rate while keeping the buffer values under the specified maximum buffer window and bit rate.</span></span> <span data-ttu-id="addca-121">Ce mode est également appelé 2-passe pic VBR.</span><span class="sxs-lookup"><span data-stu-id="addca-121">This mode is also called 2-pass peak VBR.</span></span>                    |



 

## <a name="related-topics"></a><span data-ttu-id="addca-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="addca-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="addca-123">Prise en charge ASF dans Media Foundation</span><span class="sxs-lookup"><span data-stu-id="addca-123">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="addca-124">Encodeurs Windows Media</span><span class="sxs-lookup"><span data-stu-id="addca-124">Windows Media Encoders</span></span>](windows-media-encoders.md)
</dt> </dl>

 

 



