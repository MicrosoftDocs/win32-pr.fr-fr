---
title: Interrogation Waveform-Audio périphériques d’entrée
description: Interrogation Waveform-Audio périphériques d’entrée
ms.assetid: 573b33bc-f445-496e-a0e6-0194d30bb668
keywords:
- audio Wave, interrogation des périphériques d’entrée
- Waveform-interface audio, interrogation des périphériques d’entrée
- enregistrement de la forme d’onde audio, interrogation des périphériques d’entrée
- interrogation des périphériques d’entrée Waveform-Audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91b915b3f39ad417a3d92396d887e5fb66092119
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103940929"
---
# <a name="querying-waveform-audio-input-devices"></a><span data-ttu-id="6a045-107">Interrogation Waveform-Audio périphériques d’entrée</span><span class="sxs-lookup"><span data-stu-id="6a045-107">Querying Waveform-Audio Input Devices</span></span>

<span data-ttu-id="6a045-108">Avant d’enregistrer l’audio de la forme d’onde, vous devez appeler la fonction [**waveInGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetdevcaps) pour déterminer les fonctionnalités d’entrée Waveform-Audio du système.</span><span class="sxs-lookup"><span data-stu-id="6a045-108">Before recording waveform audio, you should call the [**waveInGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetdevcaps) function to determine the waveform-audio input capabilities of the system.</span></span> <span data-ttu-id="6a045-109">Cette fonction remplit une structure [**WAVEINCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-waveincaps) avec des informations sur les fonctionnalités d’un appareil spécifié.</span><span class="sxs-lookup"><span data-stu-id="6a045-109">This function fills a [**WAVEINCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-waveincaps) structure with information about the capabilities of a specified device.</span></span> <span data-ttu-id="6a045-110">Ces informations incluent les identificateurs de fabricant et de produit, un nom de produit pour l’appareil et le numéro de version du pilote de périphérique.</span><span class="sxs-lookup"><span data-stu-id="6a045-110">This information includes the manufacturer and product identifiers, a product name for the device, and the version number of the device driver.</span></span> <span data-ttu-id="6a045-111">En outre, la structure **WAVEINCAPS** fournit des informations sur les formats audio Waveform standard pris en charge par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="6a045-111">In addition, the **WAVEINCAPS** structure provides information about the standard waveform-audio formats that the device supports.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6a045-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6a045-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6a045-113">Enregistrement de la forme d’onde</span><span class="sxs-lookup"><span data-stu-id="6a045-113">Recording Waveform Audio</span></span>](recording-waveform-audio.md)
</dt> </dl>

 

 