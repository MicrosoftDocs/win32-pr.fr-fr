---
description: À propos du filtre de capture audio
ms.assetid: ff345670-5a75-40d3-a228-8bc22aa76708
title: À propos du filtre de capture audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf5e28bef37ca52f0a33fc95b6d2a387cbbe2fb3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109687"
---
# <a name="about-the-audio-capture-filter"></a><span data-ttu-id="b6a1a-103">À propos du filtre de capture audio</span><span class="sxs-lookup"><span data-stu-id="b6a1a-103">About the Audio Capture Filter</span></span>

<span data-ttu-id="b6a1a-104">DirectShow permet la capture à partir des entrées analogiques sur une carte son par le biais du [filtre de capture audio](audio-capture-filter.md).</span><span class="sxs-lookup"><span data-stu-id="b6a1a-104">DirectShow enables capture from the analog inputs on a sound card through the [Audio Capture Filter](audio-capture-filter.md).</span></span> <span data-ttu-id="b6a1a-105">Ce filtre utilise les API Wave *xxx* pour contrôler tout appareil dont le pilote prend en charge ces API.</span><span class="sxs-lookup"><span data-stu-id="b6a1a-105">This filter uses the waveIn *XXX* APIs to control any device whose driver supports these APIs.</span></span> <span data-ttu-id="b6a1a-106">Chaque carte sur le système est représentée par une instance distincte du filtre.</span><span class="sxs-lookup"><span data-stu-id="b6a1a-106">Each card on the system is represented by a separate instance of the filter.</span></span>

<span data-ttu-id="b6a1a-107">Le filtre de capture audio expose chaque entrée sur la carte, telle que le microphone ou l’entrée MIDI, en tant que broche d’entrée.</span><span class="sxs-lookup"><span data-stu-id="b6a1a-107">The Audio Capture filter exposes each input on the card, such as the microphone or the MIDI input, as an input pin.</span></span> <span data-ttu-id="b6a1a-108">Les broches d’entrée représentent ce que le pilote expose en tant que lignes de la source audio.</span><span class="sxs-lookup"><span data-stu-id="b6a1a-108">The input pins represent what the driver exposes as audio source lines.</span></span> <span data-ttu-id="b6a1a-109">Aucune donnée ne transite par ces broches d’entrée, mais elles ne se connectent pas à d’autres filtres DirectShow.</span><span class="sxs-lookup"><span data-stu-id="b6a1a-109">No data travels through these input pins, however, and they do not connect to other DirectShow filters.</span></span> <span data-ttu-id="b6a1a-110">Elles fournissent simplement un moyen pour une application de contrôler les entrées.</span><span class="sxs-lookup"><span data-stu-id="b6a1a-110">They simply provide a way for an application to control the inputs.</span></span> <span data-ttu-id="b6a1a-111">L’application peut utiliser une broche d’entrée pour activer ou désactiver l’entrée, ou pour définir des propriétés de combinaison telles que l’égalisation des basses, l’égalisation des aigus, le panoramique, etc.</span><span class="sxs-lookup"><span data-stu-id="b6a1a-111">The application can use an input pin to enable or disable the input, or to set mixing properties such as bass equalization, treble equalization, pan, and so forth.</span></span> <span data-ttu-id="b6a1a-112">La quantité de contrôle disponible dépend du pilote.</span><span class="sxs-lookup"><span data-stu-id="b6a1a-112">The amount of control that is available depends on the driver.</span></span> <span data-ttu-id="b6a1a-113">Pour bien comprendre et exploiter les fonctionnalités d’une carte audio particulière, vous aurez besoin de la documentation du fabricant de la carte.</span><span class="sxs-lookup"><span data-stu-id="b6a1a-113">To fully understand and exploit the capabilities of a particular sound card, you will need the documentation from the card's manufacturer.</span></span>

> [!Note]  
> <span data-ttu-id="b6a1a-114">Vous pouvez capturer à partir de l’entrée de CD-Audio, mais ce flux audio est déjà passé par le convertisseur numérique-analogique, de sorte qu’il y aura une perte de qualité du son sur le CD d’origine.</span><span class="sxs-lookup"><span data-stu-id="b6a1a-114">You can capture from the CD-Audio input, but this audio stream has already gone through the digital-to-analog converter, so there will be a loss of sound quality from the original CD.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="b6a1a-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b6a1a-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b6a1a-116">Capture audio</span><span class="sxs-lookup"><span data-stu-id="b6a1a-116">Audio Capture</span></span>](audio-capture.md)
</dt> </dl>

 

 



