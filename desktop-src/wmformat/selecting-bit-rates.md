---
title: Sélection des vitesses de transmission
description: Sélection des vitesses de transmission
ms.assetid: 466524a6-2473-4768-8ae3-0ac18807f88c
keywords:
- profils, choix des vitesses de transmission
- profils, vitesses de transmission
- codecs, choix des vitesses de transmission
- codecs, vitesses de transmission
- profils, sélection de vitesses de transmission
- codecs, sélection de vitesses de transmission
- vitesses de transmission, sélection
- vitesses de transmission, profils
- vitesses de transmission, codecs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cd8c125aacc5add255962ca37e6060af20d66f8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309161"
---
# <a name="selecting-bit-rates"></a><span data-ttu-id="71a44-112">Sélection des vitesses de transmission</span><span class="sxs-lookup"><span data-stu-id="71a44-112">Selecting Bit Rates</span></span>

<span data-ttu-id="71a44-113">Pour les fichiers qui seront diffusés en continu sur un réseau, vous devez prendre en compte soigneusement les vitesses de transmission que vous devez utiliser.</span><span class="sxs-lookup"><span data-stu-id="71a44-113">For files that will be streamed over a network, you must consider carefully what bit rates you should use.</span></span> <span data-ttu-id="71a44-114">Dans la plupart des cas, vous pouvez ajouter les vitesses de transmission de tous les flux d’un fichier pour obtenir une idée générale de la bande passante disponible nécessaire pour diffuser le fichier.</span><span class="sxs-lookup"><span data-stu-id="71a44-114">Under most circumstances you can add the bit rates of all of the streams in a file together to get a general idea of the available bandwidth required to stream the file.</span></span> <span data-ttu-id="71a44-115">Toutefois, une certaine surcharge est également requise pour chaque flux.</span><span class="sxs-lookup"><span data-stu-id="71a44-115">However, a certain amount of overhead is also required for each stream.</span></span> <span data-ttu-id="71a44-116">Cette surcharge est résumée dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="71a44-116">This overhead is summarized in the following table.</span></span>



| <span data-ttu-id="71a44-117">Plage du taux de bits (Kbits/s)</span><span class="sxs-lookup"><span data-stu-id="71a44-117">Bit-rate range (Kbps)</span></span> | <span data-ttu-id="71a44-118">Bande passante supplémentaire requise pour la surcharge (Kbits/s)</span><span class="sxs-lookup"><span data-stu-id="71a44-118">Additional bandwidth required for overhead (Kbps)</span></span> |
|-----------------------|---------------------------------------------------|
| <span data-ttu-id="71a44-119">10 – 16</span><span class="sxs-lookup"><span data-stu-id="71a44-119">10 – 16</span></span>               | <span data-ttu-id="71a44-120">3</span><span class="sxs-lookup"><span data-stu-id="71a44-120">3</span></span>                                                 |
| <span data-ttu-id="71a44-121">17 – 30</span><span class="sxs-lookup"><span data-stu-id="71a44-121">17 – 30</span></span>               | <span data-ttu-id="71a44-122">4</span><span class="sxs-lookup"><span data-stu-id="71a44-122">4</span></span>                                                 |
| <span data-ttu-id="71a44-123">31 – 45</span><span class="sxs-lookup"><span data-stu-id="71a44-123">31 – 45</span></span>               | <span data-ttu-id="71a44-124">5</span><span class="sxs-lookup"><span data-stu-id="71a44-124">5</span></span>                                                 |
| <span data-ttu-id="71a44-125">46 – 70</span><span class="sxs-lookup"><span data-stu-id="71a44-125">46 – 70</span></span>               | <span data-ttu-id="71a44-126">6</span><span class="sxs-lookup"><span data-stu-id="71a44-126">6</span></span>                                                 |
| <span data-ttu-id="71a44-127">71 – 225</span><span class="sxs-lookup"><span data-stu-id="71a44-127">71 – 225</span></span>              | <span data-ttu-id="71a44-128">7</span><span class="sxs-lookup"><span data-stu-id="71a44-128">7</span></span>                                                 |
| <span data-ttu-id="71a44-129">>225</span><span class="sxs-lookup"><span data-stu-id="71a44-129">>225</span></span>               | <span data-ttu-id="71a44-130">9</span><span class="sxs-lookup"><span data-stu-id="71a44-130">9</span></span>                                                 |



 

<span data-ttu-id="71a44-131">La surcharge normale requise pour un flux ne prend pas en compte les extensions d’unité de données.</span><span class="sxs-lookup"><span data-stu-id="71a44-131">The normal overhead required for a stream does not take data unit extensions into account.</span></span> <span data-ttu-id="71a44-132">Chaque extension d’unité de données ajoute à la taille de l’échantillon auquel elle est attachée.</span><span class="sxs-lookup"><span data-stu-id="71a44-132">Every data unit extension adds to the size of the sample to which it is attached.</span></span> <span data-ttu-id="71a44-133">Selon le type d’extension d’unité de données, cela peut augmenter de façon considérable la vitesse de transmission du flux.</span><span class="sxs-lookup"><span data-stu-id="71a44-133">Depending upon the type of data unit extension, this can greatly increase the bit rate for the stream.</span></span>

<span data-ttu-id="71a44-134">Vous devez également tenir compte du fait que la bande passante maximale théorique disponible sur une connexion réseau n’est pas une vitesse de transmission cible pratique.</span><span class="sxs-lookup"><span data-stu-id="71a44-134">You must also consider that the theoretical maximum bandwidth available over a network connection is not a practical target bit rate.</span></span> <span data-ttu-id="71a44-135">La bande passante disponible moyenne pour une connexion donnée se situe bien au-dessus de la capacité de bande passante de la connexion, en raison du trafic réseau et de nombreux autres facteurs.</span><span class="sxs-lookup"><span data-stu-id="71a44-135">The average available bandwidth for any given connection falls well short of the bandwidth capacity of the connection, because of network traffic and many other factors.</span></span>

## <a name="related-topics"></a><span data-ttu-id="71a44-136">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="71a44-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="71a44-137">**Conception de profils**</span><span class="sxs-lookup"><span data-stu-id="71a44-137">**Designing Profiles**</span></span>](designing-profiles.md)
</dt> </dl>

 

 




