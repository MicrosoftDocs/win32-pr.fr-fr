---
title: Mise en mémoire tampon du contenu
description: Mise en mémoire tampon du contenu
ms.assetid: e14e0130-aefd-4e46-b288-4302d2333de2
keywords:
- Windows Media Format SDK, mise en mémoire tampon du contenu
- mise en mémoire tampon du contenu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a06b378431653f21be742c12b4e4a5ae2a994318
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106511202"
---
# <a name="buffering-content"></a><span data-ttu-id="e2b30-105">Mise en mémoire tampon du contenu</span><span class="sxs-lookup"><span data-stu-id="e2b30-105">Buffering Content</span></span>

<span data-ttu-id="e2b30-106">Lorsque l’objet lecteur ouvre un fichier de diffusion en continu, il détermine la taille de la mémoire tampon en fonction des paramètres de l’en-tête du fichier.</span><span class="sxs-lookup"><span data-stu-id="e2b30-106">When the reader object opens a streaming file, it determines the size of the buffer based upon settings in the header of the file.</span></span> <span data-ttu-id="e2b30-107">Vous pouvez considérer la mémoire tampon comme un compartiment avec un trou dans le bas, ce qui entraîne une fuite à une vitesse constante.</span><span class="sxs-lookup"><span data-stu-id="e2b30-107">You can think of the buffer as a bucket with a hole in the bottom that leaks at a constant rate.</span></span> <span data-ttu-id="e2b30-108">Tant que la vitesse à laquelle le compartiment est rempli n’est pas, en moyenne, supérieure à la vitesse à laquelle elle subit des fuites, le compartiment ne risque jamais de déborder.</span><span class="sxs-lookup"><span data-stu-id="e2b30-108">As long as the rate at which the bucket is filled is not, on average, greater than the rate at which it is leaking, the bucket will never overflow.</span></span>

<span data-ttu-id="e2b30-109">La vitesse à laquelle le compartiment imaginaire perd est la vitesse de transmission du flux.</span><span class="sxs-lookup"><span data-stu-id="e2b30-109">The rate at which the imaginary bucket leaks is the bit rate of the stream.</span></span> <span data-ttu-id="e2b30-110">La vitesse de remplissage du compartiment correspond à la vitesse de transmission en continu réelle.</span><span class="sxs-lookup"><span data-stu-id="e2b30-110">The rate at which the bucket fills is the actual streaming bit rate.</span></span> <span data-ttu-id="e2b30-111">Les données d’un flux compressé varient en fonction de la taille de l’échantillon à échantillonner en fonction du volume de compression atteint.</span><span class="sxs-lookup"><span data-stu-id="e2b30-111">The data in a compressed stream varies in size from sample to sample depending on the amount of compression that was achieved.</span></span> <span data-ttu-id="e2b30-112">Ainsi, même si la vitesse de transmission du flux est définie dans le profil, elle représente la vitesse de transmission moyenne, et non une constante.</span><span class="sxs-lookup"><span data-stu-id="e2b30-112">Thus, even though the bit rate of the stream is set in the profile, it represents the average bit rate, not a constant.</span></span>

<span data-ttu-id="e2b30-113">L’autre paramètre de flux important pour le processus de mise en mémoire tampon est la fenêtre de mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="e2b30-113">The other stream setting important to the buffering process is the buffer window.</span></span> <span data-ttu-id="e2b30-114">La fenêtre de mémoire tampon est mesurée dans le temps et spécifie la quantité de contenu qui peut être mise en mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="e2b30-114">The buffer window is measured in time and specifies how much content can be buffered.</span></span> <span data-ttu-id="e2b30-115">La capacité du compartiment imaginaire peut être trouvée à l’aide de la fenêtre de mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="e2b30-115">The capacity of the imaginary bucket can be found using the buffer window.</span></span> <span data-ttu-id="e2b30-116">Par exemple, si vous avez un flux avec une vitesse de transmission de 32 kbit/s et une fenêtre de mémoire tampon de 3 secondes, la mémoire tampon est dimensionnée de façon à contenir 3 secondes de contenu de 32 kbps, soit 12 000 octets (32 000 bits par seconde x 3 secondes/8 bits par octet).</span><span class="sxs-lookup"><span data-stu-id="e2b30-116">For example, if you have a stream with a bit rate of 32 Kbps and a buffer window of 3 seconds, the buffer is sized to hold 3 seconds of 32 Kbps content, or 12,000 bytes (32,000 bits per second x 3 seconds / 8 bits per byte).</span></span> <span data-ttu-id="e2b30-117">Le codec limite la variation entre la vitesse de transmission en continu réelle des échantillons encodés afin qu’au cours d’une période égale à la fenêtre de la mémoire tampon, la vitesse de transmission moyenne ne soit pas supérieure à la vitesse de transmission du flux.</span><span class="sxs-lookup"><span data-stu-id="e2b30-117">The codec limits the variation between the actual streaming bit rate of encoded samples so that over a period of time equal to the buffer window, the average bit rate is no greater than the bit rate of the stream.</span></span>

<span data-ttu-id="e2b30-118">Normalement, vous définissez la vitesse de transmission et la fenêtre de mémoire tampon d’un flux dans un profil, et l’enregistreur gère le reste.</span><span class="sxs-lookup"><span data-stu-id="e2b30-118">Normally, you set the bit rate and buffer window for a stream in a profile, and the writer handles the rest.</span></span> <span data-ttu-id="e2b30-119">Toutefois, lorsque vous passez des échantillons compressés au lecteur, vous devez vous assurer que les valeurs correctes sont transférées vers le nouveau fichier en définissant la vitesse de transmission et la fenêtre de mémoire tampon pour le flux du profil de destination sur les valeurs du flux compressé.</span><span class="sxs-lookup"><span data-stu-id="e2b30-119">When passing compressed samples to the reader, however, you must ensure that the correct values are transferred to the new file by setting the bit rate and buffer window for the stream in the destination profile to the values from the compressed stream.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e2b30-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e2b30-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e2b30-121">**Concepts**</span><span class="sxs-lookup"><span data-stu-id="e2b30-121">**Concepts**</span></span>](concepts.md)
</dt> <dt>

[<span data-ttu-id="e2b30-122">**Exemples de supports**</span><span class="sxs-lookup"><span data-stu-id="e2b30-122">**Media Samples**</span></span>](media-samples.md)
</dt> <dt>

[<span data-ttu-id="e2b30-123">**Entrées, flux et sorties**</span><span class="sxs-lookup"><span data-stu-id="e2b30-123">**Inputs, Streams and Outputs**</span></span>](inputs-streams-and-outputs.md)
</dt> </dl>

 

 




