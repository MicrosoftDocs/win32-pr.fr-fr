---
description: Pourquoi l’encodeur vidéo rejette-t-il un format de sortie que j’essaie de définir, lorsque j’ai récupéré le format du même objet ?
ms.assetid: f0747450-d224-423a-a9f1-04580df8a17e
title: Pourquoi l’encodeur vidéo rejette-t-il un format de sortie que j’essaie de définir, lorsque j’ai récupéré le format du même objet ?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 680908ec814fe322585c1ac97d3bb79deddaf034
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034289"
---
# <a name="why-does-the-video-encoder-reject-an-output-format-that-i-try-to-set-when-i-retrieved-the-format-from-the-same-object"></a><span data-ttu-id="6413c-103">Pourquoi l’encodeur vidéo rejette-t-il un format de sortie que j’essaie de définir, lorsque j’ai récupéré le format du même objet ?</span><span class="sxs-lookup"><span data-stu-id="6413c-103">Why does the video encoder reject an output format that I try to set, when I retrieved the format from the same object?</span></span>

<span data-ttu-id="6413c-104">Contrairement aux types de sortie de l’encodeur audio, les sorties prises en charge énumérées par les encodeurs vidéo ne sont pas complètes comme remises.</span><span class="sxs-lookup"><span data-stu-id="6413c-104">Unlike audio encoder output types, the supported outputs enumerated by the video encoders are not complete as delivered.</span></span> <span data-ttu-id="6413c-105">Vous devez définir la vitesse de transmission du flux dans le membre **dwBitrate** de la structure **VIDEOINFOHEADER** pour qu’elle corresponde à la valeur définie pour la propriété [ \_ RAVG MFPKEY](mfpkey-ravgproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="6413c-105">You must set the bit rate of the stream in the **dwBitrate** member of the **VIDEOINFOHEADER** structure to match the value set for the [MFPKEY\_RAVG](mfpkey-ravgproperty.md) property.</span></span>

<span data-ttu-id="6413c-106">Une fois toutes les options définies comme vous le souhaitez, vous devez récupérer les données privées du codec et les ajouter à la structure **VIDEOINFOHEADER** .</span><span class="sxs-lookup"><span data-stu-id="6413c-106">After all of the options are set the way that you want them, you must retrieve the codec private data and append it to the **VIDEOINFOHEADER** structure.</span></span> <span data-ttu-id="6413c-107">Pour plus d’informations, consultez [utilisation de données privées de codec vidéo](usingvideocodecprivatedata.md).</span><span class="sxs-lookup"><span data-stu-id="6413c-107">For more information, see [Using Video Codec Private Data](usingvideocodecprivatedata.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6413c-108">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6413c-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6413c-109">Questions fréquentes (FAQ)</span><span class="sxs-lookup"><span data-stu-id="6413c-109">Frequently Asked Questions</span></span>](frequentlyaskedquestions.md)
</dt> </dl>

 

 



