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
# <a name="removing-the-code-to-process-greater-than-16-bits"></a>Suppression du code pour traiter une valeur supérieure à 16 bits

Dans la mesure où cet exemple traite uniquement des données audio 8 bits ou 16 bits, vous devez modifier le code dans **CEcho :: ValidateMediaType** pour retourner le \_ type DMO E \_ \_ non \_ accepté pour les types de média supérieurs à 16 bits. Pour ce faire, vous devez modifier le code dans le bloc switch qui teste les formats de type WAVE \_ \_ extensible. Remplacez le code de l’Assistant par l’exemple de code suivant :


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



Ensuite, supprimez ou commentez les sections de code dans **DoProcessOutput** qui gèrent le son haute résolution. Voici les sections qui commencent par le cas 24 et le cas 32.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Implémentation de CEcho ::D oProcessOutput**](implementing-cecho--doprocessoutput.md)
</dt> </dl>

 

 




