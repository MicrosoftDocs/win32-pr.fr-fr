---
title: Suppression du code pour traiter une valeur supérieure à 16 bits
description: Suppression du code pour traiter une valeur supérieure à 16 bits
ms.assetid: 90c165e1-bc77-42a5-878d-056762c62991
keywords:
- Plug-ins du lecteur Windows Media, méthode DoProcessOutput d’exemple Echo
- plug-ins, ECHO, exemple DoProcessOutput, méthode
- plug-ins de traitement de signal numérique, méthode DoProcessOutput d’exemple Echo
- DSP plug-ins, ECHO, exemple DoProcessOutput, méthode
- Echo DSP, exemple de plug-in, méthode DoProcessOutput
- Echo DSP, exemple de plug-in, traitement supérieur à 16 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec33332ee332d0ca7b615844ba8ad5cd7b00eb2f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840066"
---
# <a name="removing-the-code-to-process-greater-than-16-bits"></a><span data-ttu-id="ad734-109">Suppression du code pour traiter une valeur supérieure à 16 bits</span><span class="sxs-lookup"><span data-stu-id="ad734-109">Removing the Code to Process Greater than 16 Bits</span></span>

<span data-ttu-id="ad734-110">Dans la mesure où cet exemple traite uniquement des données audio 8 bits ou 16 bits, vous devez modifier le code dans **CEcho :: ValidateMediaType** pour retourner le \_ type DMO E \_ \_ non \_ accepté pour les types de média supérieurs à 16 bits.</span><span class="sxs-lookup"><span data-stu-id="ad734-110">Because this sample only processes 8-bit or 16-bit audio, you need to modify the code in **CEcho::ValidateMediaType** to return DMO\_E\_TYPE\_NOT\_ACCEPTED for media types greater than 16 bits.</span></span> <span data-ttu-id="ad734-111">Pour ce faire, vous devez modifier le code dans le bloc switch qui teste les formats de type WAVE \_ \_ extensible.</span><span class="sxs-lookup"><span data-stu-id="ad734-111">To accomplish this, you must change the code in the switch block that tests formats of type WAVE\_FORMAT\_EXTENSIBLE.</span></span> <span data-ttu-id="ad734-112">Remplacez le code de l’Assistant par l’exemple de code suivant :</span><span class="sxs-lookup"><span data-stu-id="ad734-112">Replace the wizard code with the following example code:</span></span>


```C++
case WAVE_FORMAT_EXTENSIBLE:
    {
         // Sample size is greater than 16-bit or is multichannel.
        WAVEFORMATEXTENSIBLE *pWaveXT = (WAVEFORMATEXTENSIBLE *) pWave;

        if (KSDATAFORMAT_SUBTYPE_PCM != pWaveXT->SubFormat)
        {
            return DMO_E_TYPE_NOT_ACCEPTED;
        }
    }
    break;

```



<span data-ttu-id="ad734-113">Ensuite, supprimez ou commentez les sections de code dans **DoProcessOutput** qui gèrent le son haute résolution.</span><span class="sxs-lookup"><span data-stu-id="ad734-113">Next, delete or comment out the sections of code in **DoProcessOutput** that handle high bit resolution audio.</span></span> <span data-ttu-id="ad734-114">Voici les sections qui commencent par le cas 24 et le cas 32.</span><span class="sxs-lookup"><span data-stu-id="ad734-114">These are the sections that begin with case 24 and case 32.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ad734-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ad734-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ad734-116">**Implémentation de CEcho ::D oProcessOutput**</span><span class="sxs-lookup"><span data-stu-id="ad734-116">**Implementing CEcho::DoProcessOutput**</span></span>](implementing-cecho--doprocessoutput.md)
</dt> </dl>

 

 




