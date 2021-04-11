---
description: Création d’un graphique de capture audio avec aperçu
ms.assetid: 73c0b799-060b-4b20-b072-6a0c5c30de20
title: Création d’un graphique de capture audio avec aperçu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2962dc0ffa08e19618d81a03515e970dcb439913
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103950352"
---
# <a name="creating-an-audio-capture-graph-with-preview"></a><span data-ttu-id="34df0-103">Création d’un graphique de capture audio avec aperçu</span><span class="sxs-lookup"><span data-stu-id="34df0-103">Creating an Audio Capture Graph with Preview</span></span>

<span data-ttu-id="34df0-104">Le graphique de filtre décrit dans [création d’un graphique de capture audio effectue une](creating-an-audio-capture-graph.md) capture uniquement, sans aperçu.</span><span class="sxs-lookup"><span data-stu-id="34df0-104">The filter graph described in [Creating an Audio Capture Graph](creating-an-audio-capture-graph.md) performs capture only, with no preview.</span></span> <span data-ttu-id="34df0-105">Pour obtenir un aperçu et une capture en même temps, le graphique de filtre doit utiliser le [filtre tee de code confidentiel infini](infinite-pin-tee-filter.md).</span><span class="sxs-lookup"><span data-stu-id="34df0-105">To preview and capture at the same time, the filter graph needs to use the [Infinite Pin Tee Filter](infinite-pin-tee-filter.md).</span></span> <span data-ttu-id="34df0-106">Ce filtre a une broche d’entrée et crée autant de broches de sortie que nécessaire.</span><span class="sxs-lookup"><span data-stu-id="34df0-106">This filter has one input pin and creates as many output pins as needed.</span></span> <span data-ttu-id="34df0-107">(Il commence par une broche de sortie.</span><span class="sxs-lookup"><span data-stu-id="34df0-107">(It starts with one output pin.</span></span> <span data-ttu-id="34df0-108">Chaque fois que vous connectez une broche de sortie, elle en crée une autre.) Le filtre tee de pin infini remet chaque échantillon qu’il reçoit, sans modification, à travers toutes ses broches de sortie.</span><span class="sxs-lookup"><span data-stu-id="34df0-108">Each time you connect an output pin, it creates another one.) The Infinite Pin Tee filter delivers every sample that it receives, unchanged, through all of its output pins.</span></span>

<span data-ttu-id="34df0-109">Connectez le filtre de capture audio au code confidentiel infini et connectez l’Infinite pin tee au multiplexeur et au [filtre de convertisseur DirectSound](directsound-renderer-filter.md).</span><span class="sxs-lookup"><span data-stu-id="34df0-109">Connect the Audio Capture Filter to the Infinite Pin Tee, and connect the Infinite Pin Tee to the multiplexer and the [DirectSound Renderer Filter](directsound-renderer-filter.md).</span></span> <span data-ttu-id="34df0-110">Connectez le multiplexeur au writer de fichier, comme précédemment.</span><span class="sxs-lookup"><span data-stu-id="34df0-110">Connect the multiplexer to the file writer, as before.</span></span> <span data-ttu-id="34df0-111">Le diagramme suivant illustre le graphique de filtre résultant pour un fichier AVI.</span><span class="sxs-lookup"><span data-stu-id="34df0-111">The following diagram illustrates the resulting filter graph for an AVI file.</span></span>

![graphique de capture audio avec aperçu](images/audio-capture-graph.png)

<span data-ttu-id="34df0-113">Étant donné que le convertisseur DirectSound est le convertisseur audio par défaut, il vous suffit d’appeler la méthode [**IGraphBuilder :: Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) sur la broche de sortie d’un tee pin infini.</span><span class="sxs-lookup"><span data-stu-id="34df0-113">Because the DirectSound Renderer is the default audio renderer, you can simply call the [**IGraphBuilder::Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) method on the Infinite Pin Tee's output pin.</span></span> <span data-ttu-id="34df0-114">Le gestionnaire de graphique de filtre utilise la [connexion intelligente](intelligent-connect.md) pour créer le convertisseur, l’ajouter au graphique de filtre et connecter les broches.</span><span class="sxs-lookup"><span data-stu-id="34df0-114">The Filter Graph Manager uses [Intelligent Connect](intelligent-connect.md) to create the renderer, add it to the filter graph, and connect the pins.</span></span>

> [!Note]  
> <span data-ttu-id="34df0-115">Si vous capturez de l’audio à partir d’un microphone et que vous l’affichez à partir d’un haut-parleur sur le même ordinateur, vous pouvez créer des commentaires audio.</span><span class="sxs-lookup"><span data-stu-id="34df0-115">If you capture audio from a microphone and preview it from a speaker on the same computer, you might create audio feedback.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="34df0-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="34df0-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="34df0-117">Capture audio</span><span class="sxs-lookup"><span data-stu-id="34df0-117">Audio Capture</span></span>](audio-capture.md)
</dt> </dl>

 

 



