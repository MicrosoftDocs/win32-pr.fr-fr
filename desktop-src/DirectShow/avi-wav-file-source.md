---
description: Source de fichier AVI/WAV
ms.assetid: b8abf5d8-ba7f-441d-beef-9f85859318d5
title: Source de fichier AVI/WAV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef659d880ef570176f94ac91875291ea9d200cf5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106517387"
---
# <a name="aviwav-file-source"></a><span data-ttu-id="3aefe-103">Source de fichier AVI/WAV</span><span class="sxs-lookup"><span data-stu-id="3aefe-103">AVI/WAV File Source</span></span>

<span data-ttu-id="3aefe-104">(Déconseillé.</span><span class="sxs-lookup"><span data-stu-id="3aefe-104">(Deprecated.</span></span> <span data-ttu-id="3aefe-105">Pour les fichiers AVI et WAV, utilisez la [source de fichier (Async)](file-source--async--filter.md) et le [séparateur AVI](avi-splitter-filter.md) ou l' [analyseur Wave](wave-parser-filter.md).)</span><span class="sxs-lookup"><span data-stu-id="3aefe-105">For AVI and WAV files, use the [File Source (Async)](file-source--async--filter.md) and the [AVI Splitter](avi-splitter-filter.md) or [WAVE Parser](wave-parser-filter.md).)</span></span>

<span data-ttu-id="3aefe-106">Le filtre de source de fichier AVI/WAV lit les fichiers sources AVI et WAV et génère les broches de sortie appropriées pour le type de fichier.</span><span class="sxs-lookup"><span data-stu-id="3aefe-106">The AVI/WAV File Source filter reads AVI and WAV source files and generates the appropriate output pins for the file type.</span></span>

<span data-ttu-id="3aefe-107">Pour les fichiers WAV, le filtre crée une broche de sortie audio qui produit un flux audio qui peut être connecté à un filtre de rendu audio ou un filtre de transformation audio intermédiaire.</span><span class="sxs-lookup"><span data-stu-id="3aefe-107">For WAV files, the filter creates an audio output pin, which produces an audio stream that can be connected to an audio rendering filter or intervening audio transform filter.</span></span>

<span data-ttu-id="3aefe-108">Pour les fichiers AVI, le filtre crée une broche de sortie vidéo qui produit un flux AVI compressé adapté au filtre de codec AVI, et une broche de sortie audio qui produit un flux audio adapté à un filtre de rendu audio ou à un filtre de transformation audio intermédiaire.</span><span class="sxs-lookup"><span data-stu-id="3aefe-108">For AVI files, the filter creates a video output pin, which produces a compressed AVI stream suitable for the AVI codec filter, and an audio output pin, which produces an audio stream suitable for an audio rendering filter or an intervening audio transform filter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3aefe-109">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3aefe-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3aefe-110">Filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="3aefe-110">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



