---
title: Calcul de la vitesse de transmission et des valeurs de fenêtre de mémoire tampon pour les flux arbitraires
description: Calcul de la vitesse de transmission et des valeurs de fenêtre de mémoire tampon pour les flux arbitraires
ms.assetid: 28ba863b-9c3e-4b0e-875d-6b696600888c
keywords:
- flux, vitesses de transmission
- codecs, calcul des vitesses de transmission pour les flux arbitraires
- vitesses de transmission, calcul pour les flux arbitraires
- flux, calcul des vitesses de transmission pour les flux arbitraires
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45d704352d414b1fe5079fb068593c2d0d8b2f8c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028636"
---
# <a name="calculating-bit-rate-and-buffer-window-values-for-arbitrary-streams"></a><span data-ttu-id="cfc4d-107">Calcul de la vitesse de transmission et des valeurs de fenêtre de mémoire tampon pour les flux arbitraires</span><span class="sxs-lookup"><span data-stu-id="cfc4d-107">Calculating Bit Rate and Buffer Window Values for Arbitrary Streams</span></span>

<span data-ttu-id="cfc4d-108">Le calcul de la vitesse de transmission et de la fenêtre de mémoire tampon appropriées pour un type de flux arbitraire n’est pas une science exacte.</span><span class="sxs-lookup"><span data-stu-id="cfc4d-108">Calculating the proper bit rate and buffer window for an arbitrary stream type is not an exact science.</span></span> <span data-ttu-id="cfc4d-109">Une approche simple consiste à définir la vitesse de transmission pour qu’elle corresponde à la taille du flux divisé par sa longueur, en secondes.</span><span class="sxs-lookup"><span data-stu-id="cfc4d-109">One simple approach is to set the bit rate to match the size of the stream divided by its length, in seconds.</span></span> <span data-ttu-id="cfc4d-110">Par exemple, un flux contenant un total de 68000 bits durables 20 secondes peut avoir un débit binaire de 3400 bits par seconde (68000 bits/20 secondes = 3400 bits par seconde).</span><span class="sxs-lookup"><span data-stu-id="cfc4d-110">For example, a stream containing a total of 68000 bits lasting 20 seconds might have a bit rate of 3400 bits per second (68000 bits / 20 seconds = 3400 bits per second).</span></span>

<span data-ttu-id="cfc4d-111">Le problème avec cette technique simple consistant à affecter la vitesse de transmission est qu’elle ne prend pas en compte la distribution des données dans le flux.</span><span class="sxs-lookup"><span data-stu-id="cfc4d-111">The problem with this simple technique of assigning bit rate is that it does not take into account the distribution of data within the stream.</span></span> <span data-ttu-id="cfc4d-112">De nombreux flux arbitraires contiennent de plus grandes quantités de données à des intervalles le long de la chronologie du fichier.</span><span class="sxs-lookup"><span data-stu-id="cfc4d-112">Many arbitrary streams contain larger amounts of data at intervals along the timeline of the file.</span></span> <span data-ttu-id="cfc4d-113">Les flux d’images, par exemple, ont des exemples qui sont plutôt importants, mais qui sont généralement espacés de plusieurs secondes.</span><span class="sxs-lookup"><span data-stu-id="cfc4d-113">Image streams, for example, have samples that are rather large, but are usually spaced several seconds apart.</span></span> <span data-ttu-id="cfc4d-114">La fenêtre de mémoire tampon doit être définie pour garantir que la mémoire tampon ne peut pas déborder.</span><span class="sxs-lookup"><span data-stu-id="cfc4d-114">The buffer window must be set to ensure that the buffer will not overflow.</span></span>

<span data-ttu-id="cfc4d-115">Pour vérifier la fenêtre de mémoire tampon, multipliez la vitesse de transmission (bits par seconde) par la fenêtre de mémoire tampon (en secondes) et divisez par 1000 pour obtenir la taille, en bits, de la mémoire tampon pour le flux.</span><span class="sxs-lookup"><span data-stu-id="cfc4d-115">To check the buffer window, multiply the bit rate (bits per second) by the buffer window (in seconds) and divide by 1000 to get the size, in bits, of the buffer for the stream.</span></span> <span data-ttu-id="cfc4d-116">Ensuite, assurez-vous que la taille de la mémoire tampon est suffisamment grande pour contenir toute combinaison d’échantillons dans le flux qui sont inférieurs à la fenêtre de la mémoire tampon en dehors de l’heure de présentation.</span><span class="sxs-lookup"><span data-stu-id="cfc4d-116">Then make sure that the buffer size is large enough to hold any combination of samples in the stream that are less than the buffer window apart in presentation time.</span></span> <span data-ttu-id="cfc4d-117">En cas de doute, définissez les deux valeurs un peu plus haut que vous ne le jugez nécessaire.</span><span class="sxs-lookup"><span data-stu-id="cfc4d-117">When in doubt, set both values a little higher than you think you need them.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cfc4d-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="cfc4d-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cfc4d-119">**Mise en mémoire tampon du contenu**</span><span class="sxs-lookup"><span data-stu-id="cfc4d-119">**Buffering Content**</span></span>](buffering-content.md)
</dt> <dt>

[<span data-ttu-id="cfc4d-120">**Configuration de types de flux arbitraires**</span><span class="sxs-lookup"><span data-stu-id="cfc4d-120">**Configuring Arbitrary Stream Types**</span></span>](configuring-arbitrary-stream-types.md)
</dt> </dl>

 

 




