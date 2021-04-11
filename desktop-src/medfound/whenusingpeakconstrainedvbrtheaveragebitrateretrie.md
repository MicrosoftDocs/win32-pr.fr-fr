---
description: Lorsque j’utilise le VBR avec un pic restreint, le taux de bits moyen récupéré à partir de l’objet codec est plus grand que le taux binaire de pointe.
ms.assetid: 5fc344f8-4492-4878-802a-94606c5f33e0
title: Lorsque j’utilise le VBR avec un pic restreint, le taux de bits moyen récupéré à partir de l’objet codec est plus grand que le taux binaire de pointe. Comment est-ce possible ?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa2bb2e09f5210baf8817553377fc832b9826b4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318913"
---
# <a name="when-i-use-peak-constrained-vbr-the-average-bit-rate-retrieved-from-the-codec-object-is-larger-than-the-peak-bit-rate-how-is-that-possible"></a><span data-ttu-id="dce3f-104">Lorsque j’utilise le VBR avec un pic restreint, le taux de bits moyen récupéré à partir de l’objet codec est plus grand que le taux binaire de pointe.</span><span class="sxs-lookup"><span data-stu-id="dce3f-104">When I use peak-constrained VBR, the average bit rate retrieved from the codec object is larger than the peak bit rate.</span></span> <span data-ttu-id="dce3f-105">Comment est-ce possible ?</span><span class="sxs-lookup"><span data-stu-id="dce3f-105">How is that possible?</span></span>

<span data-ttu-id="dce3f-106">La relation entre la vitesse de transmission moyenne et la vitesse de transmission maximale est souvent mal comprise.</span><span class="sxs-lookup"><span data-stu-id="dce3f-106">The relationship between the average bit rate and the peak bit rate is often misunderstood.</span></span> <span data-ttu-id="dce3f-107">Le taux de bits de pointe décrit une contrainte de mémoire tampon sur une période spécifiée par la fenêtre de mémoire tampon de pointe.</span><span class="sxs-lookup"><span data-stu-id="dce3f-107">The peak bit rate describes a buffer constraint over a period of time specified by the peak buffer window.</span></span> <span data-ttu-id="dce3f-108">La vitesse de transmission moyenne pour le VBR à deux passes (sans contrainte ou PIC) est le nombre moyen de bits par seconde sur la durée du fichier.</span><span class="sxs-lookup"><span data-stu-id="dce3f-108">The average bit rate for two-pass VBR (unconstrained or peak-constrained) is the average bits per second over the duration of the file.</span></span>

<span data-ttu-id="dce3f-109">Comme décrit dans [le modèle de mémoire tampon de compartiment avec fuite](the-leaky-bucket-buffer-model.md), le taux de bits réel utilisé sur une période de temps égale à la fenêtre de mémoire tampon peut s’approcher de deux fois la vitesse de transmission.</span><span class="sxs-lookup"><span data-stu-id="dce3f-109">As described in [The Leaky Bucket Buffer Model](the-leaky-bucket-buffer-model.md), the actual bit rate used over a period of time equal to the buffer window can approach twice the bit rate.</span></span> <span data-ttu-id="dce3f-110">Cela est dû au fait que la mémoire tampon, définie sous la forme d’un nombre de bits égal à la vitesse de transmission de la mémoire tampon (en secondes), est vidée à une fréquence constante.</span><span class="sxs-lookup"><span data-stu-id="dce3f-110">This is because the buffer, defined as a number of bits equal to the bit rate times the buffer window (in seconds), is being emptied at a constant rate.</span></span>

<span data-ttu-id="dce3f-111">Par exemple, dans une seconde d’un flux de 56 Kbits/s, l’encodeur crée des exemples totalisant 59 Ko.</span><span class="sxs-lookup"><span data-stu-id="dce3f-111">For example, in one second of a 56 Kbps stream, the encoder creates samples totaling 59 Kb.</span></span> <span data-ttu-id="dce3f-112">Ainsi, 56 Ko de données sont supprimés de la mémoire tampon dans cette seconde, ce qui laisse 3 Ko dans la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="dce3f-112">So, 56 Kb of data is removed from the buffer in that second, leaving 3 Kb in the buffer.</span></span> <span data-ttu-id="dce3f-113">Si le flux a une fenêtre de mémoire tampon de trois secondes, et donc une taille de mémoire tampon totale de 168 Ko, il faut presque 40 secondes pour remplir la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="dce3f-113">If the stream has a buffer window of three seconds, and thus a total buffer size of 168 Kb, it would take almost 40 seconds to fill the buffer.</span></span> <span data-ttu-id="dce3f-114">La vitesse de transmission moyenne du flux (si sa durée est inférieure au temps nécessaire pour remplir la mémoire tampon) est de 59 Kbits/s, même si la vitesse de transmission est définie à 56 Kbps.</span><span class="sxs-lookup"><span data-stu-id="dce3f-114">The average bit rate for the stream (if its duration is less than the time it takes to fill the buffer) is 59 Kbps, even though the bit rate is set to 56 Kbps.</span></span>

<span data-ttu-id="dce3f-115">Le même phénomène s’applique aux contraintes de taux de bits de pointe.</span><span class="sxs-lookup"><span data-stu-id="dce3f-115">The same phenomenon applies to peak bit rate constraints.</span></span> <span data-ttu-id="dce3f-116">Pour du contenu de petite taille, le taux de bits moyen calculé par l’objet codec après l’encodage est supérieur au taux de bits de pointe.</span><span class="sxs-lookup"><span data-stu-id="dce3f-116">For short content, the average bit rate computed by the codec object after encoding is completed can be greater than the peak bit rate.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dce3f-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="dce3f-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dce3f-118">Questions fréquentes (FAQ)</span><span class="sxs-lookup"><span data-stu-id="dce3f-118">Frequently Asked Questions</span></span>](frequentlyaskedquestions.md)
</dt> </dl>

 

 



