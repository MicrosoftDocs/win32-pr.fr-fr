---
title: Encodage à débit binaire constant (CBR)
description: Encodage à débit binaire constant (CBR)
ms.assetid: f87277a5-55f1-46c7-a6a4-5824f3904d60
keywords:
- Windows Media Format SDK, encodage CBR
- Windows Media Format SDK, débit binaire constant (CBR)
- codecs, encodage CBR
- codecs, débit binaire constant (CBR)
- débit binaire constant (CBR)
- CBR (vitesse binaire constante)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d3ded3709e2e7a3e5b567b91a127ad3486a0b66
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380291"
---
# <a name="constant-bit-rate-cbr-encoding"></a><span data-ttu-id="deb53-109">Encodage à débit binaire constant (CBR)</span><span class="sxs-lookup"><span data-stu-id="deb53-109">Constant Bit Rate (CBR) Encoding</span></span>

<span data-ttu-id="deb53-110">L’encodage à débit binaire constant (CBR) est la méthode par défaut d’encodage avec le kit de développement logiciel (SDK) de format Windows Media.</span><span class="sxs-lookup"><span data-stu-id="deb53-110">Constant bit rate (CBR) encoding is the default method of encoding with the Windows Media Format SDK.</span></span> <span data-ttu-id="deb53-111">Lorsque vous utilisez l’encodage CBR, vous spécifiez la vitesse de transmission cible d’un flux et le codec utilise la quantité de compression nécessaire pour l’obtenir.</span><span class="sxs-lookup"><span data-stu-id="deb53-111">When using CBR encoding, you specify the target bit rate for a stream, and the codec uses whatever amount of compression is necessary to achieve it.</span></span>

<span data-ttu-id="deb53-112">Avec l’encodage CBR, la vitesse de transmission et la taille du flux encodé sont connues avant l’encodage.</span><span class="sxs-lookup"><span data-stu-id="deb53-112">With CBR encoding the bit rate and size of the encoded stream are known prior to encoding.</span></span> <span data-ttu-id="deb53-113">Par exemple, si vous encodez une chanson de trois minutes à 32 000 bits par seconde, vous savez que la taille du fichier est d’environ 704 kilo-octets (32 000 BPS x 180 secondes/8 bits par octet/1 024).</span><span class="sxs-lookup"><span data-stu-id="deb53-113">For example, if you are encoding a three minute song at 32,000 bits per second, you know that the file size will be about 704 kilobytes (32,000 bps x 180 seconds / 8 bits per byte / 1,024).</span></span> <span data-ttu-id="deb53-114">Vous savez également que la bande passante requise pour diffuser le contenu encodé est environ 32 000 bits par seconde.</span><span class="sxs-lookup"><span data-stu-id="deb53-114">You also know that the bandwidth required to stream the encoded content is about 32,000 bits per second.</span></span>

<span data-ttu-id="deb53-115">L’encodage à vitesse de transmission variable avec restriction (décrite dans la section suivante) vous permet également de connaître la vitesse de transmission avant l’encodage, mais étant donné que le taux est variable, le fichier résultant ne peut pas être diffusé en continu aussi efficacement qu’un fichier encodé en mode CBR.</span><span class="sxs-lookup"><span data-stu-id="deb53-115">Constrained variable bit rate encoding (described in the following section) also enables you to know the bit rate prior to encoding, but since the rate is variable, the resulting file cannot be streamed as efficiently as a file encoded in CBR mode.</span></span> <span data-ttu-id="deb53-116">Avec CBR, le taux de bits dans le temps reste toujours proche de la vitesse de transmission moyenne ou cible, et la quantité de variation peut être spécifiée.</span><span class="sxs-lookup"><span data-stu-id="deb53-116">With CBR, the bit rate over time always remains close to the average or target bit rate, and the amount of variation can be specified.</span></span>

<span data-ttu-id="deb53-117">L’inconvénient de l’encodage CBR est que la qualité du contenu encodé n’est pas constante.</span><span class="sxs-lookup"><span data-stu-id="deb53-117">The disadvantage of CBR encoding is that the quality of the encoded content will not be constant.</span></span> <span data-ttu-id="deb53-118">Étant donné que le contenu est plus difficile à compresser, les parties d’un flux CBR auront une qualité inférieure à celle des autres.</span><span class="sxs-lookup"><span data-stu-id="deb53-118">Because some content is more difficult to compress, parts of a CBR stream will be of lower quality than others.</span></span> <span data-ttu-id="deb53-119">Par exemple, un film classique présente des scènes relativement statiques et des scènes qui sont pleines d’actions.</span><span class="sxs-lookup"><span data-stu-id="deb53-119">For example, a typical movie has some scenes that are fairly static and some scenes that are full of action.</span></span> <span data-ttu-id="deb53-120">Si vous encodez un film à l’aide de CBR, les scènes qui sont statiques et, par conséquent, faciles à coder efficacement, présentent une qualité supérieure à celle des scènes d’action, qui sont bien plus difficiles à coder efficacement.</span><span class="sxs-lookup"><span data-stu-id="deb53-120">If you encode a movie using CBR, the scenes that are static, and therefore easy to encode efficiently, will be of higher quality than the action scenes, which are much more difficult to encode efficiently.</span></span>

<span data-ttu-id="deb53-121">L’encodage CBR peut également aboutir à une qualité incohérente d’un fichier à un autre.</span><span class="sxs-lookup"><span data-stu-id="deb53-121">CBR encoding can also result in inconsistent quality from one file to another.</span></span> <span data-ttu-id="deb53-122">Si vous utilisez CBR pour encoder plusieurs chansons de différents genres à la même vitesse de transmission, vous pouvez remarquer une différence de qualité entre eux.</span><span class="sxs-lookup"><span data-stu-id="deb53-122">If you use CBR to encode several songs of different genres at the same bit rate, you may notice some difference in quality between them.</span></span>

<span data-ttu-id="deb53-123">En général, les variations de la qualité d’un fichier CBR sont plus prononcées à des vitesses de transmission inférieures.</span><span class="sxs-lookup"><span data-stu-id="deb53-123">In general, variations in the quality of a CBR file are more pronounced at lower bit rates.</span></span> <span data-ttu-id="deb53-124">À des vitesses de transmission supérieures, la qualité d’un fichier encodé CBR continuera à varier, mais les problèmes de qualité seront moins perceptibles pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="deb53-124">At higher bit rates, the quality of a CBR-encoded file will still vary, but the quality issues will be less noticeable to the user.</span></span> <span data-ttu-id="deb53-125">Lorsque vous utilisez l’encodage CBR, vous devez définir la bande passante aussi élevée que possible.</span><span class="sxs-lookup"><span data-stu-id="deb53-125">When using CBR encoding, you should set the bandwidth as high as your delivery scenario allows.</span></span>

## <a name="related-topics"></a><span data-ttu-id="deb53-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="deb53-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="deb53-127">**Choix d’une méthode d’encodage**</span><span class="sxs-lookup"><span data-stu-id="deb53-127">**Choosing an Encoding Method**</span></span>](choosing-an-encoding-method.md)
</dt> <dt>

[<span data-ttu-id="deb53-128">**Fonctionnalités du codec**</span><span class="sxs-lookup"><span data-stu-id="deb53-128">**Codec Features**</span></span>](codec-features.md)
</dt> <dt>

[<span data-ttu-id="deb53-129">**Encodage à vitesse de transmission variable (VBR)**</span><span class="sxs-lookup"><span data-stu-id="deb53-129">**Variable Bit Rate (VBR) Encoding**</span></span>](variable-bit-rate--vbr--encoding.md)
</dt> </dl>

 

 




