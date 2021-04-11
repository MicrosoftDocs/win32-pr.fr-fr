---
title: Rééchantillonnage audio
description: Rééchantillonnage audio
ms.assetid: ec6ad6b2-1d35-4ac4-9a1e-3fc9c053000c
keywords:
- Windows Media Format SDK, rééchantillonnage audio
- Windows Media Format SDK, rééchantillonnage de l’audio
- ASF (Advanced Systems Format), rééchantillonnage audio
- ASF (format des systèmes avancés), rééchantillonnage audio
- ASF (Advanced Systems Format), rééchantillonnage de l’audio
- ASF (format des systèmes avancés), rééchantillonnage de l’audio
- rééchantillonnage audio
- rééchantillonnage de l’audio, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 608272a7e531d7380991a705d391e6226a6758d1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309986"
---
# <a name="audio-resampling"></a><span data-ttu-id="6fb20-111">Rééchantillonnage audio</span><span class="sxs-lookup"><span data-stu-id="6fb20-111">Audio Resampling</span></span>

<span data-ttu-id="6fb20-112">Chaque format compressé d’un codec audio a un taux d’échantillonnage et une taille d’échantillon spécifiques.</span><span class="sxs-lookup"><span data-stu-id="6fb20-112">Every compressed format of an audio codec has a specific sample rate and sample size.</span></span> <span data-ttu-id="6fb20-113">Ils n’ont pas besoin de correspondre aux paramètres du format d’entrée ou du format de sortie.</span><span class="sxs-lookup"><span data-stu-id="6fb20-113">These do not need to match the settings of the input format or output format.</span></span> <span data-ttu-id="6fb20-114">Si un format d’entrée a des paramètres différents de ceux du format compressé décrit dans le profil, le writer rééchantillonnera l’audio, pendant le processus d’encodage, pour qu’il corresponde au format compressé.</span><span class="sxs-lookup"><span data-stu-id="6fb20-114">If an input format has different settings than the compressed format described in the profile, the writer will resample the audio, during the encoding process, to match the compressed format.</span></span> <span data-ttu-id="6fb20-115">Seuls certains formats sont acceptés par le writer comme entrée.</span><span class="sxs-lookup"><span data-stu-id="6fb20-115">Only certain formats are accepted by the writer as input.</span></span> <span data-ttu-id="6fb20-116">Lorsque vous énumérez les formats d’entrée pour un flux audio compressé, tous les formats récupérés peuvent être rééchantillonnés pour correspondre au format du profil.</span><span class="sxs-lookup"><span data-stu-id="6fb20-116">When you enumerate the input formats for a compressed audio stream, all of the formats retrieved can be resampled to match the format in the profile.</span></span>

<span data-ttu-id="6fb20-117">Lors de la lecture de l’audio compressé, le lecteur rééchantillonnera le contenu pour qu’il corresponde au format de sortie.</span><span class="sxs-lookup"><span data-stu-id="6fb20-117">When reading compressed audio, the reader will resample the content to match the output format.</span></span> <span data-ttu-id="6fb20-118">Vous devez utiliser l’un des formats de sortie énumérés par le lecteur, afin de garantir que l’audio peut être rééchantillonné aux paramètres de format de sortie.</span><span class="sxs-lookup"><span data-stu-id="6fb20-118">You must use one of the output formats enumerated by the reader, so you are guaranteed that the audio can be resampled to the output format settings.</span></span>

<span data-ttu-id="6fb20-119">Chaque rééchantillonnage peut affecter la qualité du son.</span><span class="sxs-lookup"><span data-stu-id="6fb20-119">Each resampling potentially affects the quality of the audio.</span></span> <span data-ttu-id="6fb20-120">Lorsque cela est possible, vous devez utiliser des formats d’entrée et de sortie avec des paramètres qui correspondent au format compressé.</span><span class="sxs-lookup"><span data-stu-id="6fb20-120">When possible, you should use input and output formats with settings that match the compressed format.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6fb20-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6fb20-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6fb20-122">**Fonctionnalités d’écriture de fichier**</span><span class="sxs-lookup"><span data-stu-id="6fb20-122">**File Writing Features**</span></span>](file-writing-features.md)
</dt> <dt>

[<span data-ttu-id="6fb20-123">**Utilisation des entrées**</span><span class="sxs-lookup"><span data-stu-id="6fb20-123">**Working with Inputs**</span></span>](working-with-inputs.md)
</dt> <dt>

[<span data-ttu-id="6fb20-124">**Utilisation des sorties**</span><span class="sxs-lookup"><span data-stu-id="6fb20-124">**Working with Outputs**</span></span>](working-with-outputs.md)
</dt> </dl>

 

 




