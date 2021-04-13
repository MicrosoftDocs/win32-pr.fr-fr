---
title: À propos de la discontinuité
description: À propos de la discontinuité
ms.assetid: 29210758-a1e6-47f2-9428-38f79623fbca
keywords:
- Plug-ins du lecteur Windows Media, DSP audio
- plug-ins, DSP audio
- plug-ins de traitement de signal numérique, discontinuité audio
- Plug-ins DSP, discontinuité audio
- plug-ins DSP audio, discontinuité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0448220d4616122b3c99670357bbbd78de11c392
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379658"
---
# <a name="about-discontinuity"></a><span data-ttu-id="0b1b3-108">À propos de la discontinuité</span><span class="sxs-lookup"><span data-stu-id="0b1b3-108">About Discontinuity</span></span>

<span data-ttu-id="0b1b3-109">À tout moment, le lecteur Windows Media peut signaler une interruption dans le flux d’entrée en appelant la méthode **IMediaObject ::D iscontinuity** .</span><span class="sxs-lookup"><span data-stu-id="0b1b3-109">At any time, Windows Media Player can signal a break in the input stream by calling the **IMediaObject::Discontinuity** method.</span></span> <span data-ttu-id="0b1b3-110">Cela se produit régulièrement au début et à la fin d’un flux, ainsi qu’avant chaque opération de recherche ou lorsque le contenu de diffusion en continu est interrompu pour une raison quelconque.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-110">This occurs routinely at the start and end of a stream, and also prior to each seek operation or when streaming content is interrupted for any reason.</span></span> <span data-ttu-id="0b1b3-111">L’exemple de plug-in DSP généré par l’Assistant de plug-in du lecteur Windows Media n’a pas besoin de traiter les discontinuités pour les raisons suivantes :</span><span class="sxs-lookup"><span data-stu-id="0b1b3-111">The sample DSP plug-in that the Windows Media Player Plug-in wizard generates does not need to deal with discontinuities for the following reasons:</span></span>

-   <span data-ttu-id="0b1b3-112">Les exemples PCM sont atomiques, ce qui signifie qu’ils peuvent être traités sans tenir compte des autres exemples dans le flux.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-112">PCM samples are atomic, meaning they can be processed without regard to the other samples in the stream.</span></span> <span data-ttu-id="0b1b3-113">Certains formats vidéo contiennent des données qui dépendent d’images clés et d’exemples compressés.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-113">Some video formats contain data that depends on key frames and compressed samples.</span></span>
-   <span data-ttu-id="0b1b3-114">L’exemple de code est écrit pour toujours forcer le client à traiter toute la sortie avant que le plug-in n’accepte davantage d’entrées.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-114">The sample code is written to always force the client to process all output before the plug-in will accept more input.</span></span>

<span data-ttu-id="0b1b3-115">L’implémentation par défaut de **IMediaObject ::D iscontinuity** retourne simplement S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-115">The default implementation of **IMediaObject::Discontinuity** simply returns S\_OK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0b1b3-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0b1b3-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0b1b3-117">**Implémentation d’un plug-in DSP audio**</span><span class="sxs-lookup"><span data-stu-id="0b1b3-117">**Implementing an Audio DSP Plug-in**</span></span>](implementing-an-audio-dsp-plug-in.md)
</dt> </dl>

 

 




