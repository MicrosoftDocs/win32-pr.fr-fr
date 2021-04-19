---
description: Utilisation du codec d’écran Windows Media Video 9
ms.assetid: d88d5f5e-0935-4bbe-8abf-72cc536f9b40
title: Utilisation du codec d’écran Windows Media Video 9 (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b825e053c4c732481c8d1ca5d4dc972f804f262a
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106538038"
---
# <a name="using-the-windows-media-video-9-screen-codec-microsoft-media-foundation"></a><span data-ttu-id="939ec-103">Utilisation du codec d’écran Windows Media Video 9 (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="939ec-103">Using the Windows Media Video 9 Screen Codec (Microsoft Media Foundation)</span></span>

<span data-ttu-id="939ec-104">Le codec d’écran Windows Media Video 9 est optimisé pour la compression de la vidéo de l' *application*, qui se compose de captures d’écran consécutives pour un affichage d’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="939ec-104">The Windows Media Video 9 Screen codec is optimized for compressing *application video*, which consists of consecutive screen shots for a computer display.</span></span> <span data-ttu-id="939ec-105">Le codec tire parti de la simplicité d’image classique (relativement peu de couleurs, beaucoup de lignes droites, etc.) et du manque de mouvement relatif pour obtenir un taux de compression très élevé.</span><span class="sxs-lookup"><span data-stu-id="939ec-105">The codec takes advantage of the typical image simplicity (relatively few colors, lots of straight lines, and so on) and relative lack of motion to achieve a very high compression ratio.</span></span> <span data-ttu-id="939ec-106">L’inconvénient de cette optimisation est que la vidéo qui n’est pas conforme aux caractéristiques attendues de la vidéo d’application peut être difficile à compresser avec un niveau de qualité acceptable.</span><span class="sxs-lookup"><span data-stu-id="939ec-106">The disadvantage of this optimization is that video that doesn't conform to the expected characteristics of application video can be difficult to compress with an acceptable level of quality.</span></span>

<span data-ttu-id="939ec-107">L’encodeur d’écran Windows Media Video 9 est identifié par l’identificateur de classe CLSID \_ CMSSEncMediaObject2 et le décodeur est identifié par l’identificateur de classe CLSID \_ CMSSDecMediaObject.</span><span class="sxs-lookup"><span data-stu-id="939ec-107">The Windows Media Video 9 Screen encoder is identified by the class identifier CLSID\_CMSSEncMediaObject2, and the decoder is identified the class identifier CLSID\_CMSSDecMediaObject.</span></span> <span data-ttu-id="939ec-108">La valeur FOURCC pour les types de média utilisant ce codec est « MSS2 ».</span><span class="sxs-lookup"><span data-stu-id="939ec-108">The FOURCC value for media types using this codec is "MSS2".</span></span>

## <a name="configuring-the-encoder"></a><span data-ttu-id="939ec-109">Configuration de l’encodeur</span><span class="sxs-lookup"><span data-stu-id="939ec-109">Configuring the Encoder</span></span>

<span data-ttu-id="939ec-110">L’encodeur du codec d’écran Windows Media Video 9 est configuré de la même façon que le décodeur vidéo standard.</span><span class="sxs-lookup"><span data-stu-id="939ec-110">The encoder of the Windows Media Video 9 Screen codec is configured in the same way as the standard video decoder.</span></span>

> [!Note]  
> <span data-ttu-id="939ec-111">L’encodeur d’écran ne prend en charge qu’un seul encodage à passage.</span><span class="sxs-lookup"><span data-stu-id="939ec-111">The screen encoder supports only one-pass encoding.</span></span> <span data-ttu-id="939ec-112">Vous pouvez définir la propriété [MFPKEY \_ PASSESUSED](mfpkey-passesusedproperty.md) sur 2 et traiter les entrées deux fois sans erreur, mais il n’y a aucun avantage à le faire.</span><span class="sxs-lookup"><span data-stu-id="939ec-112">You can set the [MFPKEY\_PASSESUSED](mfpkey-passesusedproperty.md) property to 2 and process the inputs twice without error, but there is no benefit to doing so.</span></span> <span data-ttu-id="939ec-113">Il s’agit d’un problème connu qui peut être corrigé dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="939ec-113">This is a known issue and may be corrected in future releases.</span></span>

 

## <a name="getting-the-best-results"></a><span data-ttu-id="939ec-114">Obtention des meilleurs résultats</span><span class="sxs-lookup"><span data-stu-id="939ec-114">Getting the Best Results</span></span>

<span data-ttu-id="939ec-115">Si vous découvrez que la qualité souhaitée dans le contenu de la capture d’écran nécessite une vitesse de transmission supérieure à celle que vous pouvez utiliser pour votre scénario de distribution, vous pouvez essayer les techniques suivantes pour obtenir plus d’efficacité à partir du codec :</span><span class="sxs-lookup"><span data-stu-id="939ec-115">If you discover that the quality you want in your screen capture content requires a higher bit rate than you can use for your delivery scenario, you can try the following techniques to get more efficiency from the codec:</span></span>

-   <span data-ttu-id="939ec-116">Utilisez une résolution plus petite pour la capture d’écran.</span><span class="sxs-lookup"><span data-stu-id="939ec-116">Use a smaller resolution for the screen capture.</span></span> <span data-ttu-id="939ec-117">La capture d’une résolution d’écran plus grande que nécessaire peut confondre la visionneuse en présentant des informations inutiles.</span><span class="sxs-lookup"><span data-stu-id="939ec-117">Capturing a larger screen resolution than needed can confuse the viewer by presenting unnecessary information.</span></span>
-   <span data-ttu-id="939ec-118">Utilisez une fréquence d’images plus lente.</span><span class="sxs-lookup"><span data-stu-id="939ec-118">Use a slower frame rate.</span></span> <span data-ttu-id="939ec-119">Les captures d’écran peuvent souvent être efficaces à des fréquences d’images très basses (parfois jusqu’à 4 ou 5 images par seconde).</span><span class="sxs-lookup"><span data-stu-id="939ec-119">Screen captures can often be effective at very low frame rates (sometimes as low as 4 or 5 frames per second).</span></span>
-   <span data-ttu-id="939ec-120">Utilisez moins de graphiques dans la capture d’écran.</span><span class="sxs-lookup"><span data-stu-id="939ec-120">Use fewer graphics in the screen capture.</span></span> <span data-ttu-id="939ec-121">Le codec d’écran Windows Media Video 9 est optimisé pour encoder des primitives Windows et du texte de haute qualité.</span><span class="sxs-lookup"><span data-stu-id="939ec-121">The Windows Media Video 9 Screen codec is optimized to encode Windows primitives and text with high quality.</span></span> <span data-ttu-id="939ec-122">En général, des problèmes se produisent en raison des graphiques bitmap, qui contiennent souvent des milliers de couleurs individuelles.</span><span class="sxs-lookup"><span data-stu-id="939ec-122">Usually problems occur because of bitmapped graphics, which often contain thousands of individual colors.</span></span> <span data-ttu-id="939ec-123">Moins il y a d’images bitmap à l’écran lors de la capture, plus vos résultats seront nombreux.</span><span class="sxs-lookup"><span data-stu-id="939ec-123">The fewer bitmaps that are on the screen when you capture, the better your results will be.</span></span> <span data-ttu-id="939ec-124">Si vous ne pouvez pas éliminer les graphiques de la capture d’écran, il existe plusieurs façons de réduire l’impact d’une image bitmap sur la qualité de l’image :</span><span class="sxs-lookup"><span data-stu-id="939ec-124">If you cannot eliminate graphics from your screen capture, there are several ways to minimize the impact that a bitmap has on image quality:</span></span>
    -   <span data-ttu-id="939ec-125">Réduisez la taille du graphique.</span><span class="sxs-lookup"><span data-stu-id="939ec-125">Reduce the size of the graphic.</span></span>
    -   <span data-ttu-id="939ec-126">Réduisez le nombre de graphiques individuels qui s’affichent à l’écran en même temps.</span><span class="sxs-lookup"><span data-stu-id="939ec-126">Reduce the number of individual graphics that appear on the screen at the same time.</span></span>
    -   <span data-ttu-id="939ec-127">Réduisez la quantité de mouvement du graphique.</span><span class="sxs-lookup"><span data-stu-id="939ec-127">Reduce the amount of movement of the graphic.</span></span> <span data-ttu-id="939ec-128">Par exemple, si le graphique est dans une fenêtre, laissez la fenêtre aussi stationnaire que possible.</span><span class="sxs-lookup"><span data-stu-id="939ec-128">For example, if the graphic is in a window, keep the window as stationary as possible.</span></span>
    -   <span data-ttu-id="939ec-129">Évitez de déplacer le pointeur de la souris sur le graphique, ou de faire glisser des fenêtres ou d’autres éléments sur le graphique.</span><span class="sxs-lookup"><span data-stu-id="939ec-129">Avoid moving the mouse pointer over the graphic, or dragging windows or other elements over the graphic.</span></span>

## <a name="decoding"></a><span data-ttu-id="939ec-130">Décodage</span><span class="sxs-lookup"><span data-stu-id="939ec-130">Decoding</span></span>

<span data-ttu-id="939ec-131">Il n’existe aucune exigence particulière pour décoder la vidéo de capture d’écran.</span><span class="sxs-lookup"><span data-stu-id="939ec-131">There are no special requirements for decoding screen capture video.</span></span> <span data-ttu-id="939ec-132">Toutefois, comme pour tous les codecs Windows Media Video 9, le décodeur de capture d’écran ne peut pas décompresser correctement le contenu encodé sans les données privées du codec.</span><span class="sxs-lookup"><span data-stu-id="939ec-132">However, as with all Windows Media Video 9 codecs, the screen capture decoder cannot properly decompress the encoded content without the codec private data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="939ec-133">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="939ec-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="939ec-134">Configuration de l’encodage vidéo</span><span class="sxs-lookup"><span data-stu-id="939ec-134">Configuring Video Encoding</span></span>](configuringvideoencoding.md)
</dt> <dt>

[<span data-ttu-id="939ec-135">Utilisation de données privées de codec vidéo</span><span class="sxs-lookup"><span data-stu-id="939ec-135">Using Video Codec Private Data</span></span>](usingvideocodecprivatedata.md)
</dt> <dt>

[<span data-ttu-id="939ec-136">Encodeur d’écran Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="939ec-136">Windows Media Video 9 Screen Encoder</span></span>](windowsmediavideo9screenencoder.md)
</dt> <dt>

[<span data-ttu-id="939ec-137">Utilisation de la vidéo</span><span class="sxs-lookup"><span data-stu-id="939ec-137">Working with Video</span></span>](workingwithvideo.md)
</dt> </dl>

 

 



