---
description: Capture audio
ms.assetid: 2b7fbdcb-7b59-407e-8e82-e66bd5606507
title: Capture audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e91c9063d96a5e56d078651c338b0ffd80f5aa79
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104317782"
---
# <a name="audio-capture"></a><span data-ttu-id="4577f-103">Capture audio</span><span class="sxs-lookup"><span data-stu-id="4577f-103">Audio Capture</span></span>

<span data-ttu-id="4577f-104">Une application peut utiliser DirectShow pour capturer des données audio à partir de micros, de lecteurs de bandes et d’autres périphériques, par le biais des entrées de la carte son.</span><span class="sxs-lookup"><span data-stu-id="4577f-104">An application can use DirectShow to capture audio data from microphones, tape players, and other devices, through the inputs on the sound card.</span></span> <span data-ttu-id="4577f-105">Voici quelques exemples de scénarios courants :</span><span class="sxs-lookup"><span data-stu-id="4577f-105">Typical scenarios include:</span></span>

-   <span data-ttu-id="4577f-106">Enregistrement d’une narration VoiceOver pour une copie ultérieure sur un flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="4577f-106">Recording a voiceover narration for later dubbing over a video stream.</span></span>
-   <span data-ttu-id="4577f-107">Conversion de contenu audio analogue hérité en format numérique.</span><span class="sxs-lookup"><span data-stu-id="4577f-107">Converting legacy analog audio content to digital format.</span></span>
-   <span data-ttu-id="4577f-108">Capture de la voix ou de la musique pour la transmission sur un réseau.</span><span class="sxs-lookup"><span data-stu-id="4577f-108">Capturing voice or music for transmission over a network.</span></span>

<span data-ttu-id="4577f-109">Les utilisateurs finaux disposent de plusieurs options pour capturer l’audio de la carte son sur le disque dur.</span><span class="sxs-lookup"><span data-stu-id="4577f-109">End users have several options for capturing audio from the sound card to the hard disk.</span></span> <span data-ttu-id="4577f-110">La plupart des cartes fournissent des applications pour le mixage et l’enregistrement à partir de leurs entrées audio.</span><span class="sxs-lookup"><span data-stu-id="4577f-110">Most cards provide applications for mixing and recording from their audio inputs.</span></span> <span data-ttu-id="4577f-111">Windows fournit un magnétophone, une application utilitaire simple pour l’enregistrement à partir d’un microphone.</span><span class="sxs-lookup"><span data-stu-id="4577f-111">Windows provides Sound Recorder, a simple utility application for recording from a microphone.</span></span> <span data-ttu-id="4577f-112">L’encodeur Windows Media peut être intégré à une application DirectShow sous la forme d’un [objet de média DirectX](directx-media-objects.md) (DMO).</span><span class="sxs-lookup"><span data-stu-id="4577f-112">The Windows Media Encoder can be incorporated into a DirectShow application as a [DirectX Media Object](directx-media-objects.md) (DMO).</span></span> <span data-ttu-id="4577f-113">Cette section décrit comment intégrer la fonctionnalité de capture audio dans votre propre application à l’aide de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="4577f-113">This section describes how to integrate audio capture functionality within your own application using DirectShow.</span></span>

<span data-ttu-id="4577f-114">Cette section contient les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="4577f-114">This section contains the following topics:</span></span>

-   [<span data-ttu-id="4577f-115">À propos du filtre de capture audio</span><span class="sxs-lookup"><span data-stu-id="4577f-115">About the Audio Capture Filter</span></span>](about-the-audio-capture-filter.md)
-   [<span data-ttu-id="4577f-116">Sélection d’un périphérique de capture</span><span class="sxs-lookup"><span data-stu-id="4577f-116">Selecting a Capture Device</span></span>](selecting-a-capture-device.md)
-   [<span data-ttu-id="4577f-117">Création d’un graphique de capture audio</span><span class="sxs-lookup"><span data-stu-id="4577f-117">Creating an Audio Capture Graph</span></span>](creating-an-audio-capture-graph.md)
-   [<span data-ttu-id="4577f-118">Création d’un graphique de capture audio avec aperçu</span><span class="sxs-lookup"><span data-stu-id="4577f-118">Creating an Audio Capture Graph with Preview</span></span>](creating-an-audio-capture-graph-with-preview.md)
-   [<span data-ttu-id="4577f-119">Définition des propriétés de capture audio</span><span class="sxs-lookup"><span data-stu-id="4577f-119">Setting Audio Capture Properties</span></span>](setting-audio-capture-properties.md)

## <a name="related-topics"></a><span data-ttu-id="4577f-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4577f-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4577f-121">Utilisation de DirectShow</span><span class="sxs-lookup"><span data-stu-id="4577f-121">Using DirectShow</span></span>](using-directshow.md)
</dt> </dl>

 

 



