---
title: Ouverture de Waveform-Audio périphériques d’entrée
description: Ouverture de Waveform-Audio périphériques d’entrée
ms.assetid: 46cdbce6-2433-433a-abd2-39e4146aa2e9
keywords:
- sons Waveform, ouverture des périphériques d’entrée
- Waveform-interface audio, ouverture des périphériques d’entrée
- enregistrement de la forme d’onde audio, ouverture des appareils d’entrée
- ouverture de périphériques d’entrée Waveform-Audio
- waveInOpen fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c92b7f49b9d170ceb8ebce287025ce0e0c1c5530
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "106512308"
---
# <a name="opening-waveform-audio-input-devices"></a><span data-ttu-id="88694-108">Ouverture de Waveform-Audio périphériques d’entrée</span><span class="sxs-lookup"><span data-stu-id="88694-108">Opening Waveform-Audio Input Devices</span></span>

<span data-ttu-id="88694-109">Utilisez la fonction [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) pour ouvrir un appareil d’entrée Waveform-Audio pour l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="88694-109">Use the [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) function to open a waveform-audio input device for recording.</span></span> <span data-ttu-id="88694-110">Cette fonction ouvre l’appareil associé à l’identificateur de périphérique spécifié et retourne un handle de l’appareil ouvert en écrivant le handle d’un emplacement de mémoire spécifié.</span><span class="sxs-lookup"><span data-stu-id="88694-110">This function opens the device associated with the specified device identifier and returns a handle of the open device by writing the handle of a specified memory location.</span></span>

<span data-ttu-id="88694-111">Certains ordinateurs multimédias possèdent plusieurs périphériques d’entrée Waveform-Audio.</span><span class="sxs-lookup"><span data-stu-id="88694-111">Some multimedia computers have multiple waveform-audio input devices.</span></span> <span data-ttu-id="88694-112">À moins que vous ne sachiez que vous souhaitez ouvrir un périphérique d’entrée Wave-Audio spécifique dans un système, vous devez utiliser la \_ constante du mappeur Wave pour l’identificateur de l’appareil lorsque vous ouvrez un appareil.</span><span class="sxs-lookup"><span data-stu-id="88694-112">Unless you know you want to open a specific waveform-audio input device in a system, you should use the WAVE\_MAPPER constant for the device identifier when you open a device.</span></span> <span data-ttu-id="88694-113">La fonction [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) choisit l’appareil dans le système le plus approprié pour enregistrer le format de données spécifié.</span><span class="sxs-lookup"><span data-stu-id="88694-113">The [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) function will choose the device in the system best able to record in the specified data format.</span></span>

## <a name="related-topics"></a><span data-ttu-id="88694-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="88694-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="88694-115">Enregistrement de la forme d’onde</span><span class="sxs-lookup"><span data-stu-id="88694-115">Recording Waveform Audio</span></span>](recording-waveform-audio.md)
</dt> </dl>

 

 